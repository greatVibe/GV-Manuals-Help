# Understand The Status Bar

The status bar gives a compact view of the current workspace, node, turn, and
tool state. It helps you notice whether GreatVibe is idle, working, connected,
or waiting for attention.

The exact labels may vary by product surface. Use the current UI text as the
source of truth.

## What To Look For

Common status bar signals may include:

- Current node or workspace.
- Whether a turn is running.
- Whether tools or connectors are available.
- Whether there are warnings or errors.
- Whether the interface is connected or reconnecting.
- Shortcuts into menus, logs, or turn history.

## When A Turn Is Running

While a turn is running, the status bar may show activity or progress. If the
turn takes longer than expected, avoid starting several overlapping requests.

Instead, ask:

> Check the current turn status and tell me whether it is still running,
> blocked, or finished.

## When Something Looks Wrong

If the status bar shows a warning, disconnected state, or stale status:

1. Wait briefly for the display to refresh.
2. Check the current turn or event log.
3. Ask for a plain-language status summary.
4. Avoid repeating the same action until you know whether the first one is still running.

## Useful Prompts

- "Explain the current status bar state."
- "Check whether a turn is running."
- "Show the latest gvturns and tell me what needs review."
- "Use the event log to explain what happened in the last turn."

## Related Guides

- `manage-turns-with-gv-menu-eventlog-gvturns.md`
- `../concepts/what-is-a-node.md`
- `../concepts/what-is-a-gvturn.md`
