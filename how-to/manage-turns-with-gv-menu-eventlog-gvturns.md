# Manage Turns With The Gv Menu, Event Log, And Gvturns

Use this guide when you need to start a turn, check whether work is still
running, stop or pause work, or understand what happened in a previous turn.

## Start A Turn

A turn starts when you send a request to GreatVibe.

Before starting, make the request clear:

- Name the outcome.
- Name the file, folder, or topic.
- Say whether file changes are allowed.
- Say whether you want a plan first.

Example:

```text
Review the local help catalogue and suggest missing onboarding guides.
Do not change files yet.
```

## Check Turn Status

Use the visible gv menu, status bar, or turn history to check whether work is:

- Running.
- Waiting for input.
- Completed.
- Failed.
- Needing review.

You can also ask:

```text
Check the latest turn status and summarise what is running, completed, or waiting for review.
```

## Use The Event Log

The event log is useful when you need to understand what happened during a turn.
It may show the sequence of text, tool use, tool results, errors, and final
gvturn cards.

Ask:

```text
Use the event log for the latest turn and explain the important events in order.
```

For a failed or confusing turn, ask for the last successful step and the first
visible error.

## Use Gvturn History

Gvturn history is useful after the turn finishes. It records the card, status,
choices, and review state.

Ask:

```text
List the latest gvturns and tell me which ones need review.
```

or:

```text
Open the gvturn for the failed work and summarise what remains.
```

## Stop Or Pause Work

If the UI offers a stop, cancel, or pause action, use the visible label. If you
are unsure whether work stopped, ask for a status check before starting another
turn.

Use a prompt like:

```text
Check whether the previous turn is still running. Do not start new work until the status is clear.
```

## Recover After Problems

If a turn fails, ends unexpectedly, or creates partial work:

1. Preserve the original request.
2. Check the event log.
3. Check changed files, if edits were allowed.
4. Ask for a recovery summary.
5. Continue with a smaller next action.

## Related Guides

- `recover-a-failed-turn.md`
- `understand-the-status-bar.md`
- `../concepts/what-is-a-gvturn.md`
