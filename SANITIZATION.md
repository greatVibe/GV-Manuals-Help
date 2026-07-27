# Sanitization Checklist

This checklist is used before adding or changing any file in GV-Manuals-Help. Its job is to keep the repository safe for public readers while preserving useful help content.

## 1. Blocked Content

A document must not be published if it contains any of the following:

- Credentials, tokens, keys, secrets, or private configuration
- Internal infrastructure, deployment details, routing details, or service internals
- Private URLs, private repositories, local machine paths, hostnames, or ports
- Customer names, private customer data, or unreleased customer work
- Pricing strategy, revenue plans, COGS, or internal commercial planning
- Staff-only workflows, internal approvals, or private operating notes
- Implementation contracts that are not intended as public API documentation
- Migration plans, roadmap promises, or unreleased feature commitments

If any blocked content is present, remove it or rewrite the document before publishing.

## 2. Source Review

Before drafting from a source document, record:

- Source path
- Intended public target path
- Source risk level
- Specific red flags found
- Sections allowed for reuse
- Sections excluded from reuse
- Whether the public document must be written fresh or can be lightly edited

Any source with internal workings is rewrite-only.

## 3. Rewrite Rules

Rewrite for a public reader.

- Replace internal product, infrastructure, workflow, and operator examples with neutral examples.
- Keep the document focused on what a reader can safely do, understand, or troubleshoot.
- Remove source-system names when the public reader does not need them.
- Avoid implementation mechanisms unless they are already public and useful.
- Prefer plain language over internal terms.
- Do not preserve internal headings just because they appeared in the source.

## 4. Safe Examples

Examples should use fake names, neutral folders, generic services, placeholder domains, and dummy values.

Good placeholder patterns include:

- `example.com`
- `sample-report.xlsx`
- `quarterly-summary.csv`
- `docs/demo/`
- `DEMO_API_KEY`, only when clearly marked as fake

Do not use real local paths, real credentials, real customer names, real service names, live account identifiers, or private URLs.

## 5. Public Claims

Only include claims that are already safe for public use.

Avoid:

- Launch promises
- Roadmap dates
- Unreleased feature claims
- Customer commitments
- Pricing statements
- Security guarantees beyond documented practice
- Claims that require legal or commercial review

## 6. Final Review Checklist

Before publishing, confirm:

- The document has a public audience.
- All blocked content is removed.
- Examples are neutral and fake.
- Source-specific internal language is rewritten.
- Links are public-safe.
- No private customer or staff context remains.
- No implementation contract is exposed.
- No roadmap or pricing claim slipped in.
- The exact final text has been reviewed and approved.

## 7. Review Record

For each published document, keep a short review note with:

- Target file
- Source material used
- Sanitization summary
- Reviewer decision
- Remaining concerns

Do not store private source excerpts in the public repository.
