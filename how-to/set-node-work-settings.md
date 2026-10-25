# Set Node Work Settings

Agents can spread work across your nodes. Before they start a build, a test
suite or another heavy job, they check each node's **work settings** to decide
where it may run. You set these in **Account Admin**, so they stay with the
node even after you reinstall or rebuild it.

Ask: **"Open Account Admin so I can set work settings for my nodes."**

```text
konui_console_open_surface({username: "<dashboard-user>", surface: "account-admin", action: "default", requestId: "<current-request-id>"})
```

## The four settings

| Setting | Choices | What agents do with it |
|---|---|---|
| Heavy work | Always, Night, Never | When heavy jobs may run on the node. Night uses the node's own time zone. |
| Max heavy jobs | 1 to 64 | How many heavy jobs agents may run there at once. |
| Note | Up to 160 characters | A short hint for agents, for example "Home internet, prefer for CPU work". |
| Bandwidth check | On, Off | Whether the node measures its internet speed (a small download and upload every six hours) so agents can tell fast links from slow ones. |

## Set once, override where needed

Each setting can be set at three levels. A lower level wins:

1. **Node** — the node's Settings tab.
2. **Mesh** — the mesh's Settings tab. Applies to every node in that mesh.
3. **Organisation** — the organisation's Settings tab. Applies to every mesh.

Leave a field on **Inherit** to use the level above. Each field shows what it
currently inherits and where that comes from. If nothing is set, the node's
default applies:

| Node type | Heavy work | Max heavy jobs | Note | Bandwidth check |
|---|---|---|---|---|
| Your own machine (BYO) | Always | 3 | Home internet, prefer for CPU work | On |
| greatVibe hosted node | Always | 2 | greatVibe hosted node | Off |
| Guest workspace | Never | 0 | Guest container node with restrictions | Off |

Guest workspaces are always locked to their row. Nothing can change them.

The node's Settings tab also lists what is sent to the node and where each
value comes from. A note can be up to 160 characters, with no hidden or
control characters.

Saving needs the same passkey check as other organisation changes. Today
only organisation owners and admins can save; everyone else sees the section
read-only. Changes reach a connected node within two minutes.

## Optional: settings on the machine itself

On your own machine you can also set these as environment variables for the
node service. They apply only where Account Admin leaves the field on
Inherit all the way up, so Account Admin always wins:

```text
GVMESH_NODE_HEAVY_WORK=always|night|never
GVMESH_NODE_MAX_HEAVY_JOBS=3
GVMESH_NODE_NOTE=Home internet, prefer for CPU work
GVMESH_BANDWIDTH_PROBE=on|off
```

Prefer Account Admin: environment variables are easy to lose when a machine
is rebuilt.

## Good to know

- The note is shown to agents as information, never as instructions.
- Agents see these settings only for nodes you can already reach, in your
  mesh and in meshes it trusts.
- Updating a node to the latest version lets it pick up Account Admin
  settings and report its time zone.
