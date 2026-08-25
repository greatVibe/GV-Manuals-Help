# Ask An Agent To Open The Right UI

GreatVibe agents should act first when a supported Konui surface can help. Useful requests and exact actions are:

| Ask for | `konui_console_open_surface` surface/action |
| --- | --- |
| Add a credential | `settings` / `credential-add` |
| Eventlog | `settings` / `gv.eventlog` |
| Turn history | `settings` / `gv.gvturns` |
| Toolbox | `settings` / `all` |
| Add Node | `node-create` / `hosted` |
| Account Admin | `account-admin` / `default` |
| Personalisation | `account-admin` / `personalisation` |
| Files, IDE, or Secrets | the corresponding documented surface/action |

The agent includes your dashboard username and current request ID, checks `sentToSocketCount` and the browser receipt, and only then explains what opened. The dashboard must be connected; there is no offline UI queue. Camera, gallery, file, and clipboard pickers still require your click.

For node-wide discovery, agents use `node_list({scope: "global"})`. For repository work, they use native Git MCP tools so stored GitHub credentials and private-repository connectors work correctly.
