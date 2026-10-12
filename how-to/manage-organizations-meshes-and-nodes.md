# Manage Organizations, Meshes, And Nodes

Account Admin is the human control plane for organisations and meshes. Ask: **“Open Account Admin so I can manage my organisations and meshes.”**

```text
konui_console_open_surface({username: "<dashboard-user>", surface: "account-admin", action: "default", requestId: "<current-request-id>"})
```

In Account Admin, choose the organisation first, then create or select its mesh. Review names, ownership, region, and access before saving.

For a new node, ask: **“Open Add Node.”**

```text
konui_console_open_surface({username: "<dashboard-user>", surface: "node-create", action: "hosted", requestId: "<current-request-id>"})
```

The Add Node sheet starts with the active organisation and mesh. You can deploy a GreatVibe-hosted development node or follow the BYO path for an on-premises/cloud node. Signup sets up your personal organisation and mesh. Mochi is a temporary workspace for help and general questions. Select Mochi in Quick Access to request an assignment and switch when it is ready. Guest and signed-in Mochi workspaces follow the same disposable design. They end after 15 idle minutes and have a one-hour maximum. Keep work you need on a development node.
