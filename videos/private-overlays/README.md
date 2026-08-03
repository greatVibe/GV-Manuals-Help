# Private Video Overlays

This folder documents the overlay pattern for video metadata that should not be
committed to the public help repository.

## Why This Exists

Vimeo unlisted videos may require an embed hash. That hash is access-control
data. Public docs and public catalogue entries should not expose it.

The public `videos/index.json` file therefore stores `embed_hash_ref` values.
A node-local private overlay can map those refs to real hashes at runtime.

## Example Overlay Shape

Do not commit real hashes in this repository.

```json
{
  "version": "1.0.0",
  "videos": {
    "greatvibe-welcome": {
      "provider": "vimeo",
      "embed_hash": "placeholderhash"
    }
  }
}
```

## Runtime Behavior

A renderer or helper tool can:

1. Load `videos/index.json`.
2. Select a matching public video entry.
3. Resolve `embed_hash_ref` from a private node-local overlay.
4. Build the iframe from structured fields.
5. Avoid showing the hash in visible UI or analytics.

If no overlay exists, the agent can still recommend the written guide and show a
safe external video link when available.
