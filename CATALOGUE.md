# Catalogue

Public index for GreatVibe help content. Start here when you are a user, or
when an agent needs to choose the right local guide before answering.

## How To Use This Catalogue

1. Match the user's intent to a topic below.
2. Read the smallest relevant guide first.
3. If a video is useful, check `videos/index.json` by tag, audience, and
   product area.
4. Prefer public, local documentation before using general web search.

## Starter Paths

| User intent | Start here | Related videos |
| --- | --- | --- |
| First time in GreatVibe | `getting-started/welcome-to-greatvibe.md` | `videos/index.json` tag `welcome` |
| Learn what to do in the first session | `getting-started/first-10-minutes.md` | `videos/index.json` tag `first-session` |
| Ask Mochi for help | `getting-started/ask-mochi-for-help.md` | `videos/index.json` tag `mochi` |
| Understand a node | `concepts/what-is-a-node.md` | `videos/index.json` tag `node` |
| Understand a gvturn | `concepts/what-is-a-gvturn.md` | `videos/index.json` tag `gvturn` |
| Understand the gvturn power footer | `concepts/what-is-the-gvturn-power-footer.md` | No indexed video yet |
| Understand context | `concepts/what-is-gvcontext.md` | `videos/index.json` tag `context` |
| Review AI work | `how-to/review-ai-work.md` | `videos/index.json` tag `review` |
| Use gvturn actions | `how-to/use-gvturn-actions.md` | No indexed video yet |
| Work with files | `how-to/work-with-files.md` | `videos/index.json` tag `files` |
| Recover after a failed turn | `manuals/productivity/recover-failed-dashboard-turn.md` and `how-to/recover-a-failed-turn.md` | `videos/index.json` tag `troubleshooting` |
| Add an AI agent credential | `how-to/add-ai-agent-credential.md` | No indexed video yet |
| Add a GitHub credential | `how-to/add-github-credential.md` | No indexed video yet |
| Understand templates | `how-to/builtin-credential-and-connector-templates.md` | No indexed video yet |
| Understand the status bar | `how-to/understand-the-status-bar.md` | No indexed video yet |
| Manage turns | `how-to/manage-turns-with-gv-menu-eventlog-gvturns.md` | No indexed video yet |

## Topic Index

| Topic | Public docs |
| --- | --- |
| Getting started | `getting-started/welcome-to-greatvibe.md`, `getting-started/first-10-minutes.md`, `getting-started/ask-mochi-for-help.md` |
| Core concepts | `concepts/what-is-a-node.md`, `concepts/what-is-a-gvturn.md`, `concepts/what-is-the-gvturn-power-footer.md`, `concepts/what-is-gvcontext.md`, `concepts/what-is-ace.md` |
| Practical workflows | `how-to/review-ai-work.md`, `how-to/work-with-files.md`, `how-to/recover-a-failed-turn.md` |
| Credentials and connectors | `how-to/add-ai-agent-credential.md`, `how-to/add-github-credential.md`, `how-to/builtin-credential-and-connector-templates.md` |
| Console and turns | `how-to/understand-the-status-bar.md`, `how-to/manage-turns-with-gv-menu-eventlog-gvturns.md`, `how-to/use-gvturn-actions.md` |
| Productivity | `manuals/productivity/overview.md` and the guides in `manuals/productivity/` |
| Reference | `reference/glossary.md`, `reference/public-safety-rules.md` |
| Videos | `videos/README.md`, `videos/index.json`, `videos/index.schema.json` |

## Agent Routing Notes

Agents should use this repository as local help memory, not as a source of
private implementation facts.

- Read this catalogue before recommending a guide or video.
- Prefer `videos/index.json` for video selection; do not infer video metadata
  from raw iframe snippets.
- Use `related_docs` and `tags` to suggest one written guide and, at most, one
  matching video unless the user asks for more.
- Do not expose private overlay fields, access hashes, tokens, or hidden
  authoring notes in a gvturn.

## Publication Boundary

This catalogue is public-facing. Anything derived from private source material
must be rewritten for a public reader and checked against `SANITIZATION.md`
before publication.
