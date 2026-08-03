# Public Safety Rules

Use these rules before adding docs, examples, video metadata, or transcripts to
this repository.

## Good Public Content

Good public content helps a reader safely understand or use GreatVibe without
revealing private operations.

Good fits include:

- User manuals.
- Workflow guides.
- Public troubleshooting notes.
- Public concept explanations.
- Safe examples using fake data.
- Public training video metadata.

## Do Not Publish

Do not publish:

- Credentials, tokens, keys, or secrets.
- Private URLs, hostnames, ports, or local paths.
- Customer names or private customer data.
- Staff-only workflows or approval records.
- Internal infrastructure and deployment details.
- Pricing strategy, revenue plans, or commercial planning.
- Roadmap promises or unreleased commitments.
- Raw iframe or script snippets copied from video providers.

## Video Metadata

Use structured video metadata. Do not paste provider iframe HTML into docs.

For Vimeo, treat privacy hashes as access-control data. Public catalogue entries
should use an overlay reference instead of storing the real hash directly.

## Final Check

Before publishing, confirm:

- The audience is public.
- Examples are fake or generic.
- Links are safe.
- Private details are removed.
- The guide says what users can do, not how internal systems work.

For the full checklist, use `../SANITIZATION.md`.
