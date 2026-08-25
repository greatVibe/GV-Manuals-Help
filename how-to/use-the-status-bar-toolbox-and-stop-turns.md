# Use The Status Bar Toolbox And Stop Turns

Ask: **“Open the status-bar toolbox.”** The agent calls:

```text
konui_console_open_surface({username: "<dashboard-user>", surface: "settings", action: "all", requestId: "<current-request-id>"})
```

The toolbox exposes the Settings cards. Use `gv.eventlog` to confirm which turn is active and `gv.gvturns` to review its saved card. Before pressing **Stop Turn**, confirm both the selected node and the active turn ID so you do not stop unrelated work.

Stopping is a deliberate user control. Wait for the UI to show a terminal state, then check Eventlog before starting replacement work. If the turn remains active, ask the agent to inspect it rather than repeatedly clicking Stop.

Related: `understand-the-status-bar.md` and `manage-turns-with-gv-menu-eventlog-gvturns.md`.
