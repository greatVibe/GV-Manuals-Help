# View Turns Across Nodes

Ask: **“List every node I can access, then open gvturns for the node I choose.”** The agent must start with:

```text
node_list({scope: "global"})
```

`global` means the protected inventory readable by your authenticated account. Do not substitute local/self-only mesh state. Choose the exact node from the returned inventory, switch the dashboard to it, then open the visible turn history:

```text
konui_console_open_surface({username: "<dashboard-user>", surface: "settings", action: "gv.gvturns", requestId: "<current-request-id>"})
```

Check the node label before reviewing, stopping, or continuing a turn. Access boundaries still apply: nodes you cannot read should not appear or be inferred.
