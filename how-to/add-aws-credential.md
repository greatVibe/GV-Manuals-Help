# Add An AWS Credential

Ask: **“Open the Add Credential wizard for AWS.”** The agent calls:

```text
konui_console_open_surface({username: "<dashboard-user>", surface: "settings", action: "credential-add", requestId: "<current-request-id>"})
```

Choose the AWS template. Prefer temporary, role-based, or narrowly scoped access where available. Supply the account label, region, and secret material only in the secure wizard.

Then ask the agent to use the native AWS identity/status tools to verify the intended account and region before any resource-changing action. Never put access keys in prompts, repositories, screenshots, or gvturns. Rotate them immediately if exposed.

Related: `builtin-credential-and-connector-templates.md` and `../reference/public-safety-rules.md`.
