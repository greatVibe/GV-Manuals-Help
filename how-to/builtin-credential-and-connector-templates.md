# Built-In Credential And Connector Templates

GreatVibe may provide built-in templates to make common setup work easier.

A template is a safe starting shape. It does not remove the need to review the
provider, permissions, and intended use.

## Credential Templates

A credential template helps describe a secret or access token.

It may suggest:

- Provider name.
- Credential type.
- Label pattern.
- Safe usage notes.
- Expiry or rotation fields.
- Where the credential can be used.

The secret value should still be entered through an approved secure input and
masked afterward.

## Connector Templates

A connector template helps describe an external service or tool endpoint.

It may suggest:

- Service category.
- Display name.
- Health check type.
- Required credential reference.
- Safe usage hint for agents.
- Allowed actions or paths.

Connectors should reference credentials by ID. They should not store secret
values directly.

## When To Use A Built-In Template

Use a built-in template when:

- The provider is common.
- You want the standard fields and labels.
- You are not sure which metadata matters.
- You want the assistant to understand how the connection should be used later.

Create a custom setup only when the built-in template does not match the
service or workflow.

## Review Before Saving

Before saving a credential or connector from a template, check:

- The provider is correct.
- The label is clear.
- The access level is the narrowest practical option.
- The connector points to the intended credential.
- Health or test checks are safe to run.
- No secret appears in visible notes, labels, or docs.

## Related Guides

- `add-ai-agent-credential.md`
- `add-github-credential.md`
- `../reference/public-safety-rules.md`
