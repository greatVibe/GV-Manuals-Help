# What Is GvContext?

GvContext is the guidance that helps an assistant understand how to work in a
GreatVibe workspace.

It can include rules, documentation pointers, repository notes, and safety
instructions. The goal is to help the assistant choose the right tools, read the
right docs, and produce work in the expected format.

## Why It Matters

Without context, an assistant may need to rediscover basic information every
time. Good context helps it:

- Follow local rules.
- Find the right manual.
- Avoid unsafe assumptions.
- Keep output consistent.
- Use the right vocabulary.

## How This Help Repo Fits

This repository is a local help source. An assistant can read the catalogue,
manuals, and video index before answering user questions.

The help repo should hold durable public guidance. Long transcripts and manuals
should stay as normal files, not be copied wholesale into every assistant
prompt.

## What Users Should Do

You can ask:

- "Read the local help catalogue and suggest the right guide."
- "Use the video index to find a relevant training video."
- "Explain this concept using the public manuals only."

## Related Guides

- `what-is-ace.md`
- `../CATALOGUE.md`
- `../videos/README.md`
