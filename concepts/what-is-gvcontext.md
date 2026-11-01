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

## Turn Context

Turn context is the small, current layer supplied at the start of a turn. It
can identify the selected node, request, theme, outstanding work and the rules
that matter most for the task. It reinforces the durable gvContext contract;
it does not create a tool, permission or capability that is not actually
available.

Good agents keep the distinction clear:

- gvContext holds durable behavior and safety rules.
- Turn context holds current facts and reminders.
- Repository ACE files explain the design intent of the files being changed.

## Your Active Persona

Choose General, Developer, Creative, Executive, Analyst or Tester in the profile
picker. General is the default. Each turn receives the selected persona so the
agent can adjust its approach: creative options and finished writing, for
example, or evidence and calculations for an analysis.

Persona is guidance, not a limit on what you can ask. Your request comes first.
Shared privacy, permission, safety and evidence rules still apply. Engineering
workflows such as reading ACE files, running tests and reviewing code apply
when the task involves that work, whichever persona you chose.

## How Agent IQ Fits

Agent IQ is the visible work explanation. Its main view tells the current
story, while optional spaces show supporting views such as Topology,
Evidence, Files, Tests, Git, Patterns, CI/CD, Before · After and Architecture.
The agent chooses spaces from the current task and evidence; there is no fixed
Tests-first layout, and your manual layout or Auto-off choice always wins.

Persona helps the agent choose a useful starting view. Creative work may use
Web to show concepts, while analysis may use Research and Evidence. Actual work
and available evidence determine which spaces belong on screen. Choosing a
persona does not create new spaces or fill them with invented activity.

Some spaces fill from observed activity. Files, Tests and Git must never be
typed into existence. CI/CD progress comes from correlated delivery receipts
and is shown only when the stage total is known. Topology keeps observed worker
facts separate from the agent's declared explanation.

Patterns is deliberately explicit. When an agent reads or writes non-trivial
code, reviews a change or investigates a root cause, it should open Patterns
and declare two to six useful observations with exact file-and-line or
file-and-symbol evidence from that turn. These are labelled as agent analysis,
not as automatic telemetry or measured truth.

## What Users Should Do

You can ask:

- "Read the local help catalogue and suggest the right guide."
- "Use the video index to find a relevant training video."
- "Explain this concept using the public manuals only."

## Related Guides

- `what-is-ace.md`
- `../how-to/build-agent-iq-metal-layouts.md`
- `../CATALOGUE.md`
- `../videos/README.md`
