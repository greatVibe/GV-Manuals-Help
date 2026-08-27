# Use The Status Bar Toolbox And Stop Turns

The toolbox button sits near the right side of the status bar, between Jump to
latest and the elapsed-turn timer. It opens a menu of turn, recovery, and
session controls.

## Open It Yourself

1. Confirm the human-readable node name in the node picker.
2. Click the toolbox button.
3. Choose the action you need.

The most important actions are:

- **Stop turn** interrupts the active turn on the selected node.
- **Force idle** clears stuck local running indicators; it does not replace
  Stop turn when work is genuinely still running.
- **Browser Health** opens connection and timing details.
- **Reconnect** rebuilds the live console and admin connections.
- **Reset console history** clears browser-side history caches and fetches the
  authoritative history again.
- **Access Tree** opens the organisation, mesh, and node access map.
- **New session** starts fresh context for the selected profile.
- **Reload** reloads the dashboard tab.

## Ask An Agent To Open It

Ask: **“Open the status-bar toolbox.”** The agent uses the toolbox surface and
checks the browser receipt before claiming it opened:

```text
konui_console_open_surface({username: "<dashboard-user>", surface: "toolbox", action: "default", requestId: "<current-request-id>"})
```

To open the menu and focus the interrupt control, ask: **“Show me how to stop
this turn.”** The reliable two-step flow is:

1. Open `toolbox` with action `stop-turn`.
2. Show guidance bubbles on `toolbox` and `stop-turn`, explaining the menu and
   the actual interrupt button.

The second step may display both bubbles together. Each remains for about 30
seconds and can be dismissed separately.

## Stop The Correct Turn

Before choosing **Stop turn**, verify the selected node. Stop affects the active
turn on that node. After stopping, wait for the status text and timer to return
to an idle or terminal state before starting replacement work.

If the browser looks stuck after the stop has completed, inspect Browser Health
or ask the agent to diagnose the turn. Use Force idle only for stale local
chrome, not as a substitute for interruption.

Related: `understand-the-status-bar.md` and
`manage-turns-with-gv-menu-eventlog-gvturns.md`.
