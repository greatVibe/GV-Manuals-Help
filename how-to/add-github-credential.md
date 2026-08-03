# Add A GitHub Credential

Use this guide when GreatVibe needs permission to inspect or work with GitHub
repositories.

## What The Credential Is For

A GitHub credential can let GreatVibe perform allowed repository work such as:

- Listing repositories.
- Reading files.
- Inspecting branches.
- Preparing changes.
- Creating or updating pull requests, when permitted.

The exact actions depend on the credential permissions and the connected tools.

## Choose The Narrowest Access

Before creating or adding a credential, decide what access is needed.

Prefer:

- Repository-specific access over all-repository access.
- Read-only access when changes are not required.
- Short-lived or revocable credentials when available.
- Organisation-approved credential types and policies.

Avoid giving write or admin access unless the workflow genuinely needs it.

## Add The Credential

Use the approved credential workflow in GreatVibe.

Store safe metadata such as:

- Provider: GitHub.
- Label: a clear name for the token or app connection.
- Intended repository or organisation.
- Read or write purpose.
- Expiry or review date.

Do not paste the token into a normal prompt or commit it into a repository.

## Verify It Works

After adding the credential:

1. Confirm the credential is listed and masked.
2. Ask for a small read-only check, such as listing accessible repositories.
3. Confirm the expected repository appears.
4. If write access is needed, test with a low-risk workflow such as preparing a branch or draft pull request.
5. Review any permission errors before widening access.

## Troubleshooting

If access fails, check:

- The token or app installation has access to the repository.
- Organisation policy allows the credential type.
- Required scopes or permissions are present.
- The credential has not expired or been revoked.
- GreatVibe is using the intended credential, not an older one.

## Safety Rules

- Treat GitHub tokens as secrets.
- Rotate the token if it was pasted into chat, docs, logs, or code.
- Remove unused credentials.
- Review write access regularly.

## Related Guides

- `work-with-files.md`
- `review-ai-work.md`
- `../reference/public-safety-rules.md`
