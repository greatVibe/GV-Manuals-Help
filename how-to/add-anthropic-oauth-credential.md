# Add An Anthropic OAuth Credential

Ask your agent: **“Open the Add Credential wizard for my Anthropic OAuth credential.”**

The agent should act first:

```text
konui_console_open_surface({username: "<dashboard-user>", surface: "settings", action: "credential-add", requestId: "<current-request-id>"})
```

After the browser acknowledges the action, choose the Anthropic or Claude OAuth template, give it a recognisable label, and complete the provider sign-in flow. Enter tokens only in the secure wizard—never in a prompt, file, screenshot, or gvturn.

Verify with a small Claude request and check the credential status. If the tool reports zero connected dashboards or a failed receipt, keep the dashboard open and ask the agent to retry.

Related: `add-ai-agent-credential.md` and `builtin-credential-and-connector-templates.md`.
