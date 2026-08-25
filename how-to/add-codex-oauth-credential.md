# Add A Codex OAuth Credential

Ask: **“Open the Add Credential wizard for my Codex credential.”** The agent uses:

```text
konui_console_open_surface({username: "<dashboard-user>", surface: "settings", action: "credential-add", requestId: "<current-request-id>"})
```

Choose the Codex/OpenAI OAuth template, add a clear label, and finish the authorised sign-in flow. Keep OAuth codes and tokens inside the secure wizard. Do not paste them into chat.

After saving, run one small Codex request. A provider, expiry, or quota error means the credential needs attention; it does not mean the secret should be revealed to the agent.

Related: `add-ai-agent-credential.md`.
