# Play games and answer choices inside Agent IQ

Agent IQ can take your input while the agent is still working. Tap a cell in a
game, pick an option, or confirm a step, and the agent sees it on its next
read. You do not need to type a new prompt, and it works the same way in
Claude and Codex.

## What you see

- The agent draws an interactive board or picker in the Agent IQ canvas.
- You tap or click inside it. The control locks until the agent replies.
- The agent answers by drawing the next frame: the updated board, its move, or
  the next question.
- Taps inside the interactive area are yours. They never trigger the canvas
  fullscreen or Auto gestures, which still work on the background around it.

You can play from any of your open viewers (phone, folding phone or desktop).
The agent receives the moves from all of them.

## How an agent runs the loop

1. **Draw the state.** Publish an Agent IQ frame with
   `konui_activity_update` (`layout: "agentiq"`). Put the interactive part in a
   `<section data-gv-iq-script="v1">` region, and bake the current state into
   that frame, for example as a `data-board` attribute.
2. **Emit input from the region.** Controls call
   `window.gvIq.emit(name, data)`. `name` is a short identifier
   (`^[A-Za-z][A-Za-z0-9_.:-]{0,31}$`), `data` is UTF-8 encoded JSON up to 1 KiB, and a
   region can send up to 20 events every 10 seconds. `emit` returns `true`
   when the event was queued.
3. **Read and wait.** Call
   `konui_agent_iq_get({ username, turnId, inputsAfter: "0", waitForInputMs: 20000, includeSpaces: false })`.
   `turnId` is this turn. The call returns as soon as a new event arrives, or
   after the full bounded wait with no events. The wait is one overall deadline,
   including each dashboard read.
4. **Act.** Each event in `receipt.inputs.events` has `cursor`, `at`, `name`,
   `data`, `userActivated`, `region`, `panelId` and `revision`. Treat an event
   as a player move only when `userActivated` is `true`. That flag consumes one
   private token minted by a real pointer or keyboard interaction; another emit
   cannot reuse the same interaction, and a synthetic event cannot mint a token.
5. **Reply and repeat.** Publish the next frame with a higher `revision` and
   the new state. Read again with `inputsAfter` set to the returned
   `inputs.cursor`, so you never see the same event twice.

## Example region

```html
<section data-gv-iq-script="v1" data-gv-iq-height="320" data-board="----X----">
  <div id="b" style="display:grid;grid-template-columns:repeat(3,64px);gap:6px"></div>
  <script>
    var s = document.querySelector('[data-board]').getAttribute('data-board');
    s.split('').forEach(function (v, i) {
      var c = document.createElement('button');
      c.textContent = v === '-' ? '' : v;
      c.disabled = v !== '-';
      c.style.cssText = 'height:64px;font-size:28px';
      c.addEventListener('click', function () {
        if (window.gvIq.emit('move', { cell: i + 1 })) {
          document.querySelectorAll('button').forEach(function (b) { b.disabled = true; });
        }
      });
      document.getElementById('b').appendChild(c);
    });
  </script>
</section>
```

## Limits and boundaries

- The region stays sealed. It has no network access, no dashboard access and
  no credentials. `emit` is the only way anything leaves it.
- Input is one-way. The agent answers by publishing a new frame, not by
  talking to the running script.
- A read needs one of your dashboards to be open and visible on the node.
  If none is, the read fails. Events already sent stay stored for the turn and
  arrive on the next successful read. The newest 256 events are retained for
  about six hours, with cleanup checked every minute independently of later
  input traffic.
- Durable gvturn cards are different. A button in a card starts a new turn
  with a new prompt. Use Agent IQ when the agent should keep working in the
  same turn.
