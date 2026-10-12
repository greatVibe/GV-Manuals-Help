# Security And Secrets In The Development Loop

## Never Paste A Secret

Never put passwords, tokens, keys or connection strings in a prompt. Attach
them with **Sealed Secret 🔒** and describe what to do with the attachment.
Agents never ask you to paste a secret.

If a secret was pasted by mistake: rotate it, revoke the old one, check Git
history for it, and attach the replacement with Sealed Secret.

## How Sealed Secrets Work

A sealed secret becomes a short-lived, node-local **capability**. The agent
sees only a fingerprint, never the value.

| Use | What happens |
| --- | --- |
| Call an API through a connector | The connector request is made on the node with the secret injected. The agent gets the response, not the secret |
| Type a password into a program | The secret is written once to the standard input of an exact running command in an IDE terminal, then wiped. Terminal output is redacted |

Limits:

- A capability expires within 15 minutes and is bound to your user and
  session.
- Connector capabilities allow at most 100 uses; terminal ones exactly one.
- A terminal capability only works for the command it was sealed for. If the
  terminal changes, seal again.

Example: for `sudo`, start a form that reads standard input, such as
`sudo -S -p '' <command>`, then deliver the sealed password.

## Credentials

- Saved credentials are encrypted and shown only as metadata.
- Each agent session uses its own isolated home folder for its credential.
  Agents never edit credential files or read another session's.
- Add credentials through the dashboard. See `../../how-to/add-ai-agent-credential.md`,
  `../../how-to/add-github-credential.md` and `../../how-to/add-aws-credential.md`.

## Keep Secrets Out Of Code

| Rule | Why |
| --- | --- |
| No hardcoded secrets | Read them from the environment or a sealed capability |
| Environment files stay ignored | Never commit `.env` files |
| Never log secrets | Logs and turn records are kept |
| Redact before storing | Tokens and personal data never reach storage |
| Validate all input | Type, range and format, at the boundary |
| Deny by default | Allow explicitly |

## Actions That Need Your Confirmation

| Action | Why |
| --- | --- |
| Force push | Rewrites shared history |
| Hard reset | Discards uncommitted work |
| Deleting large directories or bulk records | Wide blast radius |
| Destructive migrations | May drop data |
| Cloud write tools | Confirmation-gated by design |
| Credential or secret changes | Not covered by general authorisation |

Agents never skip Git hooks or rewrite pushed history unless you ask.

## Security Findings In Agent IQ

When a turn reviews or changes security-relevant code, the agent declares
findings in the Security space:

| Field | Values |
| --- | --- |
| Kind | vuln, secret, authz, crypto, dependency, compliance, config |
| Severity | info, low, medium, high, critical |
| State | open, mitigated, accepted, verified |

Findings cite exact file and line evidence and may name a standard such as
OWASP A01. They are shown as agent analysis, not scanner output. `verified`
means the turn has evidence of the fix.

To report a security problem in greatVibe itself, use a support request with
request type `security`.

## Related

- `git-and-repositories.md`
- `devops-cicd-and-iac.md`
- `../../reference/public-safety-rules.md`
