# Check Eventlog In Dashboard Console

Ask: **“Open Eventlog and explain the latest turn.”** The agent should open the real card before explaining it:

```text
konui_console_open_surface({username: "<dashboard-user>", surface: "settings", action: "gv.eventlog", requestId: "<current-request-id>"})
```

Use Eventlog to inspect tool calls, progress, errors, and the boundary between the last successful event and the first failure. Agents can use `eventlog_running_describe` for the current turn or `eventlog_list` followed by `eventlog_get` for older turns, then relate that evidence to the visible card.

If the UI receipt fails, the agent must say it did not open; keep the dashboard connected and retry.

Related: `manage-turns-with-gv-menu-eventlog-gvturns.md`.
