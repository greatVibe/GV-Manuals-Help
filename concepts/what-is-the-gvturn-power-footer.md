# What Is The Gvturn Power Footer?

The gvturn power footer is the action area below a gvturn card. It helps you
respond to the work, choose the next step, change the tone of a follow-up, and
inspect useful turn information.

You can think of it as the control panel for a gvturn.

## Why It Matters

A gvturn is not only an answer. It is a work record with suggested next actions.
The power footer keeps those actions visible so you do not have to guess what to
do next.

The footer may show:

- Quick reactions.
- A next-action or review banner.
- Action cards.
- Tone controls and utility actions.
- Turn metrics and status details.

## Zone 1: Quick Reactions

Quick reactions are short response chips. They let you answer with one tap.

Common reactions include:

| Reaction | Meaning |
| --- | --- |
| Good | Acknowledge that the result is fine. |
| Ship it | Continue toward finalising, pushing, or publishing when appropriate. |
| Deeper | Ask for more detail or investigation. |
| Continue | Keep going with the same direction. |
| Rethink | Ask the assistant to reconsider the approach. |
| Commit | Commit file changes when that is the right next step. |
| Push | Push committed work to the remote repository. |
| Audit | Review a larger or riskier change. |
| Backlog | Record follow-up work. |
| Verify | Run or explain checks. |
| Clean up | Remove or tidy leftover work. |
| Review | Ask for a focused review. |

Some suggested reactions may be highlighted. A highlight is a recommendation,
not an automatic action. You still choose whether to use it.

## Zone 2: Next Action Or Review Banner

This area tells you what kind of attention the gvturn needs.

It may show:

- The recommended next action.
- A decision-needed banner.
- An audit or review-needed banner.
- A short legend for click, hold, and keyboard shortcuts.

If the banner says review is needed, read the card before continuing.

## Zone 3: Action Cards

Action cards are the main next-step choices. The primary recommendation is
usually the largest or most prominent card.

Click behavior:

- Click an action card to send that prompt immediately.
- Hold an action card to put the prompt into the input box so you can edit it
  before sending.

Use hold-to-edit when the suggested action is close but not exactly what you
want.

## Zone 4: Tone And Utility Controls

Tone controls change how the next response should feel.

Common tone choices:

- Concise.
- Detailed.
- Urgent.
- Casual.

Utility controls may include actions such as comment, bookmark, copy, share, or
more options. The available utilities can vary by product surface.

## Zone 5: Metrics And Badges

Metrics and badges help you understand the turn.

They may include:

- Token or usage information.
- Tool count.
- Timing.
- Model or agent information.
- Work type.
- Status.
- Submitter or source.

Treat metrics as context. A high tool count, long runtime, or audit status may
mean the work deserves closer review.

## Keyboard Shortcuts

When supported:

- `1` to `5` can trigger action cards.
- `Shift+1` to `Shift+5` can place an action into the input for editing.
- `Escape` can cancel a hold or edit action.

If shortcuts do not work in your current surface, use the visible buttons.

## Common Status Signals

| Signal | What it means |
| --- | --- |
| Completed | The turn finished its requested work. Review before relying on it. |
| Pending | A decision or next action is waiting. |
| In progress | Work is still active or continuing. |
| Audit required | A larger or riskier change needs review before it is treated as done. |

## What To Ask If You Are Unsure

Useful prompts:

```text
Explain the power footer on this gvturn and recommend which action I should use.
```

```text
Tell me what the status, metrics, and primary action mean before I click anything.
```

```text
Rewrite the primary action so I can edit it before sending.
```

## Related Guides

- `what-is-a-gvturn.md`
- `../how-to/review-ai-work.md`
- `../how-to/manage-turns-with-gv-menu-eventlog-gvturns.md`
