# Connect A Private GitHub Repository

First ask the agent to open the credential wizard:

```text
konui_console_open_surface({username: "<dashboard-user>", surface: "settings", action: "credential-add", requestId: "<current-request-id>"})
```

Choose GitHub, authorise only the repositories and permissions you need, and save a clear label. Then give the agent the repository URL—not the token—and ask it to use GreatVibe's native Git MCP tools.

Agents should use `git_clone`, `git_pull`, `git_push`, `git_repo_status`, and related Git tools first. Those tools resolve the stored GitHub credential/connector and can reach authorised private repositories; shell Git is a fallback only when the native capability is genuinely absent.

Related: `add-github-credential.md`.
