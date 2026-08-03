# Add An AI Agent Credential

Use this guide when you need to connect an AI provider credential for Claude,
Codex, or another supported assistant runtime.

## What This Credential Does

An AI agent credential lets GreatVibe call the selected provider for allowed
assistant work. The credential should be stored in the credential manager, not
in a document, chat message, screenshot, or code file.

## Before You Add It

Confirm:

- Which provider the credential is for.
- Which agent or model family should use it.
- Whether the credential is personal, team-owned, or organisation-managed.
- What spending or usage limits apply.
- Whether a built-in credential template already exists.

Do not paste the secret into a normal prompt. Use the product's credential
entry flow or an approved secure input.

## Add The Credential

Use the credential area in GreatVibe or ask Mochi to open the relevant
credential workflow.

Record safe metadata only:

- Provider, such as Claude or Codex.
- Label, such as "Team Claude credential".
- Intended use, such as console agent work.
- Owner or review contact, if needed.
- Expiry or rotation reminder, if known.

The secret value should be masked after entry. A normal list or status view
should not reveal it.

## Verify It Works

After adding the credential:

1. Check that the credential appears with the expected provider and label.
2. Confirm it is not expired.
3. Run a small test request.
4. Check the result for provider or quota errors.
5. Record any setup notes without recording the secret.

## Troubleshooting

If the credential does not work, check:

- The provider was selected correctly.
- The key or token was copied without extra spaces.
- The credential has permission for the requested model or API.
- The credential has not expired or hit a quota limit.
- The connector or agent is pointing to the intended credential.

## Safety Rules

- Never paste a real credential into a document or chat.
- Never commit credentials to a repository.
- Rotate the credential if it may have been exposed.
- Use the narrowest credential that can do the job.
- Remove credentials that are no longer needed.

## Related Guides

- `builtin-credential-and-connector-templates.md`
- `../reference/public-safety-rules.md`
- `review-ai-work.md`
