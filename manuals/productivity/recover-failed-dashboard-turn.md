# Recover a Failed Dashboard Turn

Use this guide when a dashboard request ends unexpectedly, the console shows a failed turn, or the expected result card does not appear.

The goal is to preserve enough public-safe context to continue the work without guessing. Do not include passwords, access tokens, private customer details, or unrelated message history in a recovery note.

## When to use this guide

Use this guide when:

- The console shows `Turn Failed: Turn ended unexpectedly`.
- A request id is visible, but no result card appears.
- A workflow stopped before the user received clear next steps.
- A retry is being considered, but the previous state should be recorded first.
- A support or operations handoff needs a short, factual summary.

## What to keep

Record only the information needed to recover the work:

- The request id shown in the dashboard.
- The dashboard session or conversation where the failure happened.
- The visible error title or status.
- The original user request, if it is safe to repeat.
- The last successful result card, if one exists.
- The next action the user needs.

Avoid copying private files, secrets, internal logs, or unrelated conversation history into a public manual, issue, or status update.

## Recovery steps for users

1. Copy the request id exactly as shown in the dashboard.
2. Check whether a result card appeared after the failure.
3. Check the recent cards in the same workflow for the last completed step.
4. Write a short recovery note with the visible request id, visible failure title, and the task that was interrupted.
5. State whether the missing result was recovered, partially recovered, or not recovered.
6. Decide whether to retry the original request or continue from the last completed step.

Keep the note factual. If the result cannot be recovered, say that clearly instead of reconstructing content from memory.

## When to ask for operator help

Ask for operator help when:

- The request id is visible, but no card or recent result can be found.
- The same request fails more than once.
- The failed work involved publishing, credentials, customer data, billing, or production systems.
- The recovery requires access to logs or systems not visible in the dashboard.
- You are not sure whether retrying the request would duplicate work.

A public handoff should describe the visible problem and the needed outcome. Internal log checks should stay in the appropriate private operations channel.

## What recovery can and cannot do

Recovery can preserve the visible failure state, request id, session context, timestamps, and next action.

Recovery cannot recreate model output that was never saved. It also should not mark unrelated pending work complete unless the failed request is clearly matched to that work.

## Public-safe recovery note template

Use this template when recording a failed dashboard turn:

```text
Title:
[Short description of the failed request]

Visible status:
[Failure title or missing-card status]

Request id:
[Dashboard request id]

Interrupted task:
[What the user was trying to do]

Last completed step:
[Last visible completed card or result]

Recovery result:
[Recovered, partially recovered, or not recovered]

Next action:
[Retry, continue from a step, ask for operator help, or no action needed]
```

## Recommended wording

Use direct status language:

`The request id was inspected, but no saved result card was found. Retry the original request if the missing work product is still needed.`

If the result was recovered, use:

`The failed request was matched to a saved result card. Continue from that card instead of retrying the original request.`

## Quick checklist

Before closing a failed-turn recovery item, confirm that:

- The request id is recorded exactly.
- The last visible completed card is noted.
- The recovery result is stated plainly.
- The next action is clear.
- No secrets, private customer data, internal logs, or unrelated messages were copied into the public note.
- Related pending work is closed only when it is clearly matched to the recovered request.

## Key takeaway

A failed dashboard turn should leave a clear, public-safe trail: what failed, what was checked, what was recovered, and what should happen next.
