# GV-Manuals-Help

Public help and reference material for GreatVibe users, partners, and developers.

This repository contains customer-facing manuals, authoring guides, and public engineering standards. It is designed to be safe to share publicly and easy to seed onto GreatVibe nodes as a local help reference.

## What Belongs Here

GV-Manuals-Help is for documentation that helps people use, understand, or work with GreatVibe-facing tools without exposing private implementation details.

Good fits include:

- User manuals and workflow guides
- Public troubleshooting notes
- Authoring guides for diagrams and documentation
- Public engineering standards
- Public explanations of documentation methods such as ACE
- Sanitized examples that do not reveal private systems or customer data

## What Does Not Belong Here

Do not add private or internal material to this repository.

Excluded content includes:

- Credentials, tokens, keys, secrets, or private configuration
- Internal infrastructure, deployment, routing, or service details
- Private URLs, private repositories, local machine paths, or hostnames
- Customer names, private customer data, or unreleased customer work
- Pricing strategy, revenue plans, COGS, or internal commercial planning
- Staff-only workflows, internal operating notes, or approval records
- Implementation contracts that are not intended as public API documentation
- Roadmap promises or unreleased product commitments

If a source document contains any of the above, rewrite it into a public-safe guide before adding it here.

## Repository Map

Current structure:

```text
GV-Manuals-Help/
|-- README.md
|-- SANITIZATION.md
|-- CATALOGUE.md
|-- getting-started/
|   |-- welcome-to-greatvibe.md
|   |-- first-10-minutes.md
|   `-- ask-mochi-for-help.md
|-- concepts/
|   |-- what-is-a-node.md
|   |-- what-is-a-gvturn.md
|   |-- what-is-the-gvturn-power-footer.md
|   |-- what-is-gvcontext.md
|   `-- what-is-ace.md
|-- how-to/
|   |-- review-ai-work.md
|   |-- work-with-files.md
|   |-- recover-a-failed-turn.md
|   |-- add-ai-agent-credential.md
|   |-- add-github-credential.md
|   |-- builtin-credential-and-connector-templates.md
|   |-- understand-the-status-bar.md
|   |-- use-gvturn-actions.md
|   `-- manage-turns-with-gv-menu-eventlog-gvturns.md
|-- manuals/
|   |-- productivity/
|   |   |-- approval-requests.md
|   |   |-- calendar-planning.md
|   |   |-- change-logs.md
|   |   |-- csv-files.md
|   |   |-- data-cleanup.md
|   |   |-- data-validation.md
|   |   |-- decision-records.md
|   |   |-- document-review.md
|   |   |-- email-writing.md
|   |   |-- excel-formulas.md
|   |   |-- exporting-files.md
|   |   |-- feedback-tracking.md
|   |   |-- file-naming.md
|   |   |-- follow-up-actions.md
|   |   |-- issue-reporting.md
|   |   |-- meeting-notes.md
|   |   |-- overview.md
|   |   |-- pdf-review.md
|   |   |-- presentation-prep.md
|   |   |-- prioritising-work.md
|   |   |-- project-summaries.md
|   |   |-- recover-failed-dashboard-turn.md
|   |   |-- recurring-reviews.md
|   |   |-- review-checklists.md
|   |   |-- sharing-files.md
|   |   |-- spreadsheet-formatting.md
|   |   |-- status-updates.md
|   |   |-- task-tracking.md
|   |   |-- troubleshooting.md
|   |   `-- work-handoffs.md
|-- reference/
|   |-- glossary.md
|   `-- public-safety-rules.md
`-- videos/
    |-- README.md
    |-- index.json
    |-- index.schema.json
    |-- mochi-experience-map.json
    |-- mochi-experience-map.schema.json
    |-- private-overlays/
    |   `-- README.md
    `-- transcripts/
        |-- greatvibe-first-screen-recording.md
        `-- greatvibe-welcome.md
```

## Using These Manuals

Start with `CATALOGUE.md`, then choose the topic closest to your task:

- For first-session help, see `getting-started/`.
- For GreatVibe vocabulary, see `concepts/`.
- For practical task workflows, see `how-to/`.
- For document workflows, see `manuals/productivity/`.
- For safety rules and definitions, see `reference/`.
- For training videos, see `videos/index.json`.

Each document should be written for a public reader. Prefer plain explanations, safe examples, and clear troubleshooting steps.

## Publishing Rules

Before adding or changing a document:

1. Confirm the document is intended for public use.
2. Remove private names, links, paths, tokens, credentials, and operational details.
3. Replace internal examples with neutral examples.
4. Avoid claims about unreleased features or future roadmap dates.
5. Keep the document focused on what a user can safely do or understand.
6. Ask for review when in doubt.

Use `SANITIZATION.md` as the checklist before publishing.

## Contributing

Contributions should improve clarity, safety, or usefulness for public readers.

When proposing a change, include:

- What changed
- Why it helps the reader
- Whether any source material was sanitized
- Any remaining review concerns

## Status

This repository is being prepared as the public, sanitized help companion for GreatVibe documentation. Content should be added gradually, with review before publishing.
