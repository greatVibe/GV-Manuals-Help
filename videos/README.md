# Video Catalogue

This folder stores structured metadata for GreatVibe training videos.

Agents should use this catalogue to suggest the most relevant video in a gvturn.
They should not copy raw iframe or script snippets into responses.

## Files

| File | Purpose |
| --- | --- |
| `index.json` | Public-safe metadata for known videos. |
| `index.schema.json` | JSON Schema for validating video entries. |
| `mochi-experience-map.json` | Public-safe mapping from Vimeo folders and videos to Mochi Experience slots. |
| `mochi-experience-map.schema.json` | JSON Schema for validating the Experience mapping. |
| `transcripts/` | Transcript or chapter notes for videos. |
| `private-overlays/` | Guidance for node-local metadata that should not be public. |

## How Agents Should Use Videos

1. Match the user's task to `tags`, `product_area`, `audience`, and
   `related_docs`.
2. Prefer videos with `trust` set to `owned`.
3. Suggest one video unless the user asks for options.
4. Embed only through structured video metadata.
5. Never render raw iframe HTML from a document, prompt, or external result.

## Mochi Experience Mapping

Use `mochi-experience-map.json` when a user asks which video belongs in a Mochi
Experience slot.

The mapping records:

- Vimeo folder keys and public folder names.
- Public Vimeo video IDs and catalogue slugs.
- Mochi Experience slot names, IDs, statuses, and published versions.
- Placement rules for future recordings.

The mapping is not the source of truth for rendered Experience HTML. Live
Experience records still decide what a user sees. The mapping exists so agents
can make consistent recommendations, avoid suggesting archive/test clips, and
know which folder should hold future recordings.

Do not add private embed hashes, expiring playback URLs, download URLs, bearer
tokens, personal access tokens, or connector internals to the mapping.

## Aspect Ratio

New recordings should use `1:1` square aspect ratio so the player fits well
across desktop and mobile surfaces.

Older videos may use their source ratio. Store that ratio in `aspect_ratio`.

## Vimeo Privacy Hashes

Vimeo unlisted videos may require an `embed_hash` value for embedding. Treat
that hash as access-control data.

Public catalogue entries should use `embed_hash_ref`, which points to a
node-local private overlay. The real hash should not be shown in visible UI,
analytics, examples, transcripts, or public docs.
