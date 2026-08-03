# Recover A Failed Turn

Use this guide when a turn ends unexpectedly, a gvturn is missing, or the answer
does not clearly finish the request.

## First, Preserve Context

Before starting over, note:

- What you asked for.
- Whether files may have been changed.
- Any visible error message.
- The last useful output.
- What outcome you still need.

## Ask For A Recovery Summary

Use a prompt like:

```text
The previous turn failed or ended unexpectedly.
Please inspect the current workspace state, summarise what appears complete,
what remains uncertain, and what safe next step you recommend.
Do not make file changes yet.
```

## Check For File Changes

If the previous request allowed edits, ask:

- "What files changed?"
- "Were the changes complete?"
- "Are there partial files I should review?"
- "Can you verify the result before continuing?"

## Continue With A Smaller Request

If the task was broad, restart with one narrow next action.

Examples:

- "Only inspect the changed files."
- "Only finish the catalogue file."
- "Only validate the JSON schema."
- "Only explain the failure and do not edit files."

## When To Ask For Review

Ask for review when:

- Files were changed before the failure.
- The task involved customer-facing content.
- The assistant reports uncertainty.
- The same failure happens more than once.
- The result will be shared outside the workspace.

## Related Guides

- `../manuals/productivity/recover-failed-dashboard-turn.md`
- `review-ai-work.md`
- `../concepts/what-is-a-gvturn.md`
