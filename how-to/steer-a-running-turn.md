# Steer A Running Turn

Use this guide when an agent is already working and you want to change what it
does next. You do not need to wait for the turn to end or start over.

## What Steering Is

Steering sends a message into the turn that is running now. The agent reads it
and adjusts its plan. It works for Claude and Codex turns.

- It does **not** start a new turn. Your message joins the current one.
- It does **not** stop a command that is already running. The agent finishes
  that step, then reads your message and changes course.
- It is **not** the same as stopping. To end the turn, use Stop instead. See
  `use-the-status-bar-toolbox-and-stop-turns.md`.

## Send A Steer

1. Wait until the turn is running. The console shows live activity.
2. Type your message in the normal prompt box.
3. Add images if they help. Use **+** then **Attach**, as you would for any
   prompt. A single steer can carry up to 30 images.
4. Press **Send**.

While a turn runs, Send delivers your text to that turn. It does not queue a
new prompt.

## What The Composer Tells You

| Message | What it means |
| --- | --- |
| **Received by Claude. Waiting for the agent’s response in the console.** | Your message reached the running turn. The agent has it but may not have read it yet. |
| **Turn is finishing — press Send again to start a new turn.** | The turn was wrapping up and could not take more input. Your draft stays in the box. Press Send again to send it as a new turn. |

Codex turns show the same confirmation as **Received by Codex runtime.**

## When The Agent Reads It

The agent reads your message at its **next step**. A step ends each time the
agent finishes an action, such as reading a file or running a command.

- If the agent is doing quick steps, your message lands within seconds.
- If the agent is in a long step, such as a big build or test run, it reads
  your message when that step ends.
- If the agent is already writing its final answer, it may handle your
  message in a short extra pass after that answer.

So the reply time depends on what the agent is doing, not on your connection.
Agents are asked to keep their steps short so your messages land fast.

## Where The Reply Shows

Your message and the agent's reply appear in the **Live Turn Interactions**
drawer, next to the composer.

The reply under your message is the agent's first update after it reads your
message. It should start with a short acknowledgement, then carry on with the
work. For example: "Got it, switching to the smaller fix first."

If that first update has no written reply, your message shows
**Read by Claude · no reply yet**. The agent has your message, but it did not
answer in words. A later update is never shown as the reply.

If your steer changes the plan, the agent should also refresh its **Agent IQ**
view so the current focus and next step match the new plan.

## Tips

- **Be short and specific.** "Skip the tests for now and fix the login bug
  first" works better than a long new brief.
- **Say one change at a time.** Send a second steer if you need another change.
- **Add a screenshot** when it is easier to show than to tell.
- **Name what to stop** as well as what to start, so the agent drops the old
  plan.
- **Start a new turn for new work.** Steering is for changing direction inside
  the current task.

## Troubleshooting

| What you see | What to do |
| --- | --- |
| "Read by Claude · no reply yet" | The agent read your message but did not answer it in words. Watch its next steps, or send a short follow-up. |
| No reply yet after "Received" | The agent is in a long step. Wait for it to finish, or watch the Interactions drawer. |
| "Turn is finishing" | Press Send again. Your draft becomes a new turn. |
| "Delivery could not be confirmed … check for a receipt before retrying." | Your message may have arrived. Check the Interactions drawer for it before you send it again, so the agent does not get it twice. Your draft stays in the box. |
| "The active turn changed before delivery." | The turn ended or moved on before your message arrived. Nothing was sent. Your draft stays; press Send to start a new turn with it. |
| "Steering is not authorized for this turn." | You can steer only a turn you started or share. Nothing was sent. |
| Send fails and the draft stays | Nothing was lost. Check that you are on the same node as the running turn, then try again. |
| The reply under your message does not mention it | The agent skipped the acknowledgement. Watch its next updates, or send a short follow-up. |
| The agent ignored part of your steer | Send a shorter follow-up that names the missed part. |

Related: `use-console-main-row-and-prompt-controls.md`,
`build-agent-iq-metal-layouts.md` and
`play-games-and-collect-choices-in-agent-iq.md` (tapping choices inside Agent
IQ, which is separate from steering).
