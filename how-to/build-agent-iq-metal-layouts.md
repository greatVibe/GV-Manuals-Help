# Agent IQ Metal Design System

Agent IQ Metal is a visual language for showing what an agent is doing, what it
has learned, and what useful result is coming next. Deep navy surfaces,
illuminated glass and metal edges, cyan connections and a compact greatVibe
symbol make the work easy to follow. The design adapts to the available space
and to the current task.

This guide is for people requesting an Agent IQ view and for AI agents or other
authors building one. Start with the [layout catalogue](#layout-catalogue), then
open the [self-contained starter](../reference/agent-iq-metal-starter.html).
Download or save that HTML file and open it in a browser if your documentation
viewer shows its source. It uses no external libraries, fonts or network calls.
Every scenario in the starter is labelled **illustrative**; it reports no real
work or production measurements.

## Ask for the design

You can ask an agent:

> Use the Agent IQ Metal Design System for this task. Fill the space I have
> allocated, put the current action and next step first, and reflow for phone,
> Fold and desktop. Keep a compact greatVibe symbol with an honest stage label.
> Make the important work larger as priorities change. Show verified evidence
> and a usable result. Preserve my reading position and chosen layout.

The request does not require a particular panel count or a three-step process.
A comparison, annotated preview, map, decision tree or timeline may explain your
task better than a work sequence. Ask for the form that helps you understand the
answer. Agent IQ is the live explanation; a saved result or downloadable artifact
still belongs in the final delivery.

## Visual vocabulary

| Element | Design rule | Meaning |
| --- | --- | --- |
| Canvas | Deep navy, starting at `#10151f` | Quiet background for the work |
| Metal cells | Fine edge highlights, restrained bevels, precise shadows | Separate related pieces without a wall of identical cards |
| Glass | Subtle translucent layers over dark surfaces | Depth while keeping text legible |
| Cyan | Luminous `#56d9ec` structure and connections | Relationships, direction and supporting information |
| Amber | `#f5b34d` active accent | Work currently happening or a decision still needed |
| Green | `#98c379`, only beside verified results | Evidence that the stated check or result is complete |
| Pending information | Muted, readable blue-grey | Not yet known or not yet checked |
| Type | Inter first, with system fallbacks | Short, clear labels and a consistent reading rhythm |

Use the canonical greatVibe symbol: three white curved paths flowing from one
amber origin dot. Keep its proportions, orientation and colours. The starter
contains the exact vector primitives for reuse. Put a short stage beside or
below the symbol; do not add a second greatVibe wordmark, rotate the symbol,
replace it with an invented mark, or turn the mark into a progress gauge.

The status core should be compact enough to leave room for the actual work.
Glass and metal are a finish, not a reason to add empty machinery, decorative
numbers, gauges or extra panels. Connectors should explain a relationship such
as request → approach, evidence → confidence, or work → useful output.

Use plain language in the visible copy: “Starting”, “Checking the example”,
“What we found”, “Next”, “Ready for review”. Technical authoring terms such as
frame, turn, internal worker or telemetry belong in implementation discussion,
not in labels that users must decode.

## Space and reading order

Use the full width and height allocated to Agent IQ. On a large display, extend
the composition with useful context, previews or evidence instead of leaving a
small diagram surrounded by empty space. Filling the canvas does not mean
stretching every cell equally or making the logo huge.

Keep the current action and its next step in the top third. Give the important
visual enough room to explain the task. Remaining work is concise; completed
evidence is available but visually secondary. Reuse the same cells as priorities
change so a reader can see what moved and why.

The available **panel dimensions** determine the composition. A desktop browser
may contain a short, narrow panel; a Fold may have a wide panel with very little
height. Reflow within each viewer's allocation. Do not resize the application,
force fullscreen or Follow, change the person's reading position, or clear a
manual layout choice to make your composition fit.

## Layout catalogue

These are named examples of the design system. The native opening layout is a
starting point while useful information is still arriving; authored views
should adapt to the actual task.

### Wide opening

The original wide arrangement has a compact centre status core between two
useful panes, with a result pane across the bottom:

```text
Current action and next step
┌───────────────────┬─────────────┬─────────────────────┐
│ The approach      │ Symbol      │ Useful discoveries  │
│                   │ Starting    │                     │
├───────────────────┴─────────────┴─────────────────────┤
│ The result                                           │
└─────────────────────────────────────────────────────┘
```

“Starting” is an honest unknown state. These panes describe what will become
useful; they do not assert that an approach, discovery or result already exists.
The native introductory path, Understand → Work → Deliver, explains a typical
journey. It does not prescribe a workflow for every task.

### Phone portrait

Keep the current action and next step first. Stack a readable, roughly square
core graphic and the useful cells below it; do not shrink desktop labels into
a tiny diagram. The native opening puts the core before the approach and
discoveries, with the result following them. An authored view can put the most
important work immediately after the focus instead.

Allow supporting detail to scroll locally when necessary. The core, headline,
next step and basic controls must remain legible without requiring fullscreen.
Text should wrap naturally, with no sideways page scrolling or overlapping
application controls.

### Compact Fold

For a wide but short allocation, keep a **small status core on the left** and
the three useful panes alongside it. Condense supporting text before sacrificing
the current action or next step:

```text
Current action · Next step
┌────────┬────────────────┬─────────────────┬──────────────┐
│ Symbol │ The approach   │ Discoveries     │ The result   │
│ Stage  │                │                 │              │
└────────┴────────────────┴─────────────────┴──────────────┘
```

The native opening uses this compact treatment when its allocation is at least
640 CSS pixels wide and no more than 360 CSS pixels high. That is an allocation
rule, not device detection. Authored layouts may use a different breakpoint if
their content needs it. Avoid large empty sides, oversized branding, or making
the user scroll past a tall status graphic before reaching useful work.

### Adaptive focus layouts

An authored scene can keep the same useful cells while changing their size and
position. The starter demonstrates three examples:

| Example | Dominant content | Supporting content |
| --- | --- | --- |
| Work focus | Current action, draft or implementation preview | Checks still needed and intended output |
| Verify focus | Evidence, comparison, review or test results | What was changed and what can be delivered |
| Deliver focus | The useful answer, artifact or handoff | Relevant evidence, limits and next action |

These names are examples, not required stages or tool values. On a large panel,
the dominant cell grows. On a phone, it moves earlier in the reading order. In
Compact Fold, the status stays small and the most useful cell moves next to it.
The design should follow the work rather than locking every scene to three
panes, three stages or six equal cards.

## Spaces beside the frame

Alongside the authored frame, the Agent IQ canvas offers nine dockable
**spaces** the reader can open with the chip toolbar in the corner of the
canvas: **Topology** (how the work is organised right now), **Evidence**
(observed results collected during the turn), **Files** (the live file and node
activity map), **Tests** (test plans, live output and verified results), **Git**
(repository state, dirty files and bounded patches), **Patterns**
(evidence-linked conceptual and algorithmic structure), **CI/CD** (delivery
runs, stages and observed progress), **Before · After** (a side-by-side of the
change) and **Architecture** (the system as the agent declared it, with a
this-turn focus heatmap). The **Main view** chip hides or
restores the agent's main frame while keeping the open spaces. Close an
individual space with its own chip or close control.

The reader stays in control:

- A chip **toggles** its space open or closed; up to three spaces can be open
  at once, and each pane has its own close control.
- Spaces can **split apart**: long-press a pane's header and drag it to any
  edge — right, left, bottom or top — and only that pane moves there, so
  different spaces can sit on different edges at the same time. Dropping on
  another pane's header reorders the two panes. Alt+arrows on a header do
  the same move from the keyboard, and a reset control returns everything to
  one dock on the default edge.
- Any space can become the **hero**: drop a pane on the centre zone while
  dragging, tap the ⛶ button in its header, or press H on the header. The
  hero space takes the primary zone and the frame swaps into the hero's dock
  slot. The frame is always the default primary — hero is an explicit,
  reversible choice (toggle ⛶ again to swap back).
- Sizing preferences (the share of the canvas, preferred edges) are
  remembered on the device. **Every turn starts clean**, though: when a new
  turn begins the canvas returns to the full main view with the spaces
  closed, on "autopilot" — the agent's opening frame (or your own taps)
  decides what this turn shows. Nothing lingers from the previous turn.

### Fullscreen and Auto, by touch or mouse

Use an empty background in the main view or a space, not a file or button:

| Gesture | What it does |
|---------|--------------|
| Single click/tap | Show only that view fullscreen; repeat the single gesture to return |
| Double click/tap | Show the whole canvas fullscreen; repeat the double gesture to return |
| Long-press | Toggle agent auto-layout, just like the Auto pill |

Turn end releases either fullscreen mode. AI messages, the Interactions drawer,
blur, resizing and Escape do not close it. Interactive files, buttons, links and
inputs keep their normal actions: touching a file inspects its evidence, and
does not also fullscreen the canvas. Header drag handles remain layout controls.

**Auto off** stops the agent rearranging your spaces; it does not stop live
activity or file evidence. **Auto on** applies the latest arrangement the agent
proposed. Manually changing chips, positions, hero or reset pauses Auto until you
explicitly turn it on again. The agent cannot resume arranging from silence.

### The agent can propose the arrangement

The authoring agent may suggest which spaces open and where, using three
optional attributes on the scene root of a normal frame — no new tool is
involved; they travel inside the same published frame:

```html
<section data-gv-iq-scene="v1"
  data-gv-iq-spaces="architecture,files@right,evidence@bottom"
  data-gv-iq-hero="architecture"
  data-gv-iq-layout="right"
  data-gv-iq-share="0.34"> … </section>
```

- `data-gv-iq-spaces` — up to three of `topology`, `evidence`, `files`,
  `tests`, `git`, `patterns`, `cicd`, `beforeafter`, `architecture`
  (comma-separated); an empty value closes all spaces. Each
  entry may carry its own edge with `@top`/`@right`/`@bottom`/`@left`
  (`evidence@bottom`) to split that space onto its own dock; a bare name uses
  the default edge.
- `data-gv-iq-hero` — one of the listed space names: that space takes the
  primary zone for this frame and the frame swaps into its dock slot. Omit
  the attribute (the normal case) and the frame stays primary.
- `data-gv-iq-layout` — the default edge for spaces without an `@edge`:
  `top`, `right`, `bottom` or `left`.
- `data-gv-iq-share` — the fraction of the canvas the docks take (a decimal
  such as `0.34`; the canvas clamps it to a readable range).
- `data-gv-iq-spaces-compact` / `data-gv-iq-hero-compact` — a **second
  arrangement for small screens**, same grammar as the base pair and read only
  when the base `data-gv-iq-spaces` is also present. A canvas that *measures*
  compact (a short or narrow band — phones, or a folding phone's main screen
  with the Interactions drawer open) applies the compact pair instead of the
  base pair; desktop and roomy canvases read the base pair unchanged. Put your
  full arrangement in the base tags and the ONE most important space in the
  compact tags. If a frame has no compact tags, a compact canvas keeps things
  readable on its own: a multi-space proposal opens only the hero (else the
  first space) and the remaining chips glow so one tap opens them.
- `data-gv-iq-mainview` — `off` hides the main view so the open space(s) fill
  the whole canvas (an explicit hero, else the first open space, takes the
  primary zone); `on` restores it. It needs at least one open space and obeys
  the same follow-and-veto rules. Use it when a space *is* the story.

Two automatic behaviours support this on phones — no attributes needed: the
space chips move into their own reserved lane at the foot of a compact canvas
(they never sit on pane content), and an ultra-short canvas (for example while
the on-screen keyboard is open) temporarily hides the main view so the hero
space fits — the frame returns by itself as soon as the canvas grows back.

This is **display-only and advisory**. It is honoured only while the reader is
following the agent with Auto enabled. Manual layout changes pause Auto until
the reader explicitly re-enables it; the latest proposal is retained meanwhile,
and the native live data keeps updating. A new turn also starts with Auto enabled.

The proposal is read from **every published frame**, so the agent can also
**move the spaces while the turn runs**: open the Evidence dock on the right
during the working phase, publish the next update with
`data-gv-iq-layout="bottom"` to slide the whole dock under the frame for a
comparison, swap the open set with a new `data-gv-iq-spaces` list, widen it
with a larger `data-gv-iq-share`, and finish with `data-gv-iq-spaces=""` to
hand the full canvas back to the closing frame. Each frame's attributes
replace the previous proposal; a frame that omits them leaves the current
arrangement alone. One rule to remember: `data-gv-iq-layout` and
`data-gv-iq-share` are only read when `data-gv-iq-spaces` is present on the
same frame — so when repositioning, restate the space list even if it is
unchanged.

### Choose the space that matches the work

All nine spaces have equal priority. No space, including Tests, is shown just
because a turn started. The agent should choose the opening arrangement and
single compact hero from the current goal and evidence:

| Space | Best fit |
|-------|----------|
| Topology | Workers and relationships across components |
| Evidence | Receipts, claims and verification artifacts |
| Files | Live file/node activity and confirmed write evidence |
| Tests | The active test/check path |
| Git | Branch, dirty files, ahead/behind and patch review |
| Patterns | Recognized code patterns and algorithms with evidence, fit and trade-offs |
| CI/CD | Delivery runs, pipeline stages and observed progress |
| Before · After | A concrete comparison |
| Architecture | The declared system and dependency map |

Keep the chosen space open while it is the critical path, then switch only at a
real phase boundary. Your manual layout and Auto setting still take priority.

### Follow test runs in Tests

Tests fills itself from observed test and check commands. A run can appear as
queued or running after an observed start; live output is added only from
bounded progress receipts, and passed, failed or blocked results and counts are
shown only after terminal evidence arrives. The agent does not type results into
the frame or infer a pass from silence.

When a test run is the most important current evidence, the agent should put
`tests` in the next arrangement and keep it open until the terminal result.
On a phone or short Fold allocation, Tests can be the one compact space and hero
when that makes the critical path clearest. The pane updates as recognized
receipts arrive. Your manual arrangement and Auto setting still take priority.

Observed output recognizes common source and configuration formats for syntax
highlighting, shows additions and removals distinctly, and formats Markdown/ACE
headings, lists, emphasis, inline code and quotes. JSON is highlighted too.
Unknown and unsupported formats stay readable as literal text. Output is
bounded, links are not activated and receipt content is never executed.

### Keep the Files space current

Files fills itself from operations observed during the running turn. Reads are
green, writes are red, cache reads are orange only when cache provenance is
explicit, and node references use the same human name and colour as Quick
Access. Local filesystem work has its own `node name — this node` pill, so you
can immediately tell local paths from activity on another node.

Files uses a connected activity map instead of a deep folder tree. The newest
filename is prominent even in a short pane. Recent activity is newest-first;
touch, click or use the keyboard to select a file and inspect its path and
available evidence. Fullscreen gives the map and details more room on phone and
desktop. The connections show which node the file belongs to, not guessed
dependencies between files. The map shows a small recent sample; **Activity**
provides the remaining retained files in newest-first order. This is a bounded
view of the turn, not a complete filesystem browser. Shortened labels do not change a file's identity,
and the same filename on another node remains a separate object.

Brief pulses mark newly observed activity; they do not claim that old work is
still running. Reduced-motion settings keep the same information without the
animation. New activity should not steal a file selection you are reading.

A quick diff appears only for a confirmed successful write with matching edit
evidence. Native write completion can include a bounded, redacted patch or
content excerpt for this purpose. The preview is a bounded excerpt of that operation, not a new read of
the filesystem or a complete repository diff. Pending or failed attempts are not presented as completed
changes. If success or edit evidence is unavailable, Files does not invent a
diff. Names, paths and preview content are displayed as text, never executed.

Do not type file rows into the frame and do not guess cache hits from speed or
repetition. If files or nodes are central to the request, include `files` in the
opening proposal and keep it open through work and verification; its native
eventlog feed updates while the turn runs. A later frame can omit the arrangement
attributes to leave it where it is. Move or close it only when the task reaches
a real phase boundary. On a compact code-review, build or audit turn, Files is a
strong single hero.

### Review dirty repositories in Git

Git is read-only: the space shows sampled repository truth and never runs a Git
command. Select a repository to see its branch, clean/dirty state, observed
ahead/behind values and changed-file count. Dirty repositories can expose a
bounded list of files. The changed-file count reflects the full deduplicated
bounded sample even when the interactive list is capped. Staged, unstaged,
untracked and conflicted states remain distinct even when one path appears in
more than one source list.

Select a file to read its bounded observed diff, patch or preview. If no patch
was supplied by the sample, Git says it is unavailable instead of reading the
working tree or inventing one. New samples preserve the selected repository and
file when they still exist. Unknown remote values remain unknown rather than
looking like zero.

### Explain structure in Patterns

Patterns should call out a recognizable software pattern, computer-science
concept or algorithm that is actually present in the code. It is agent analysis
tied to exact evidence, not measured telemetry or an automatic static-analysis
verdict. Name the pattern in the row text, then supply:

- exact code references in `data-pattern-evidence`;
- a short “why it fits” explanation in `data-pattern-fit`;
- the functions, types or modules playing the roles in
  `data-pattern-participants`;
- honest costs or limitations in `data-pattern-tradeoffs`;
- useful time, space or operational constraints in `data-pattern-complexity`.

Use `data-pattern-shape`, `data-pattern-signal` and
`data-pattern-concepts` to select the right representation. Tree-like
algorithms become branches; state machines and event loops become cycles;
dynamic programming becomes a matrix; map/reduce and producer/consumer become
fans; graph and observer structures become networks; layered and hexagonal
architecture keep those forms; other patterns use an ordered flow.

```html
<div data-gv-iq-patterns="v1">
  <div data-pattern-id="memoized-search" data-pattern-kind="algorithm"
    data-pattern-state="recognized" data-pattern-repo="catalog-service"
    data-pattern-shape="dynamic-programming" data-pattern-signal="invariant"
    data-pattern-evidence="src/search.ts:lookup;tests/search.test.ts:memoizes"
    data-pattern-fit="Overlapping subproblems reuse results by normalized key."
    data-pattern-participants="lookup;cache;key normalizer"
    data-pattern-tradeoffs="Extra memory;cache invalidation"
    data-pattern-complexity="time O(states);space O(states)"
    data-pattern-concepts="state;transition;memo">Memoized search</div>
</div>
```

The selected showcase keeps the diagram dominant and groups fit, participants,
evidence, trade-offs and complexity around it. When concept labels are missing,
safe algorithmic defaults supply useful vocabulary. The visible label remains
**Agent analysis · evidence linked**. History is keyed by node, repository,
stable id and exact evidence so unrelated code is never merged.

### Follow delivery in CI/CD

CI/CD combines correlated receipts from AWS, Azure, Google, GitHub, GitLab,
Jenkins and on-prem tools. Select a run to see a graphical pipeline: named stage
nodes connected in order, each coloured from its observed state. A progress bar
appears only when the stage total is known, and counts only terminal stages; no
missing stage or duration is guessed.

The normalizer understands provider-native nesting, including AWS stage names
outside `latestExecution`, Azure terminal `result` fields and GitHub job
`conclusion` fields. Not-started stays queued, and deployment scripts with
suffixes such as `deploy-prod.sh` count as on-prem delivery. If a receipt is
terminal but has no stage detail, the pane says so and keeps the missing stages
unknown.

### Populate the Architecture space

The Architecture space draws the system **as the agent knows it**: components
laid out by dependency (foundations left, consumers right), a kind glyph per
component, and a four-step heat ramp showing where the agent expects this
turn's work to land. Populate it with a flat declaration block anywhere in the
authored frame — the block is treated as data and never shown as frame text:

```html
<div data-gv-iq-arch="v1">
  <div data-arch-node="konui" data-arch-kind="ui" data-arch-heat="3"
       data-arch-deps="gvmesh">Konui dashboard</div>
  <div data-arch-node="gvmesh" data-arch-kind="service"
       data-arch-heat="1">gvmesh</div>
</div>
```

- `data-arch-node` — a short id (letter first, up to 32 characters). Up to 12
  components are drawn per declaration.
- `data-arch-kind` — one of `ui`, `service`, `data`, `infra`, `agent`, `test`.
- `data-arch-heat` — `0` to `3`, the **declared** focus for this turn. Hot
  components (`3`) pulse gently. Say where the work will go; the space itself
  labels heat as the agent's declaration, never as measured telemetry.
- `data-arch-deps` — up to six comma-separated ids of other declared
  components. Unknown or self references are dropped.
- `data-arch-parts` (optional) — up to six comma-separated names (24
  characters each) for the pieces **inside** that component this turn
  touches, e.g. `data-arch-parts="renderer,sanitizer,storage"`. Readers see
  them when they tap the box — a second layer of depth that works for both
  developers and business readers. Declare parts on the hot components
  especially; that is where people tap.

A frame **without** a new declaration keeps the previous model, so you can
re-declare heat as work moves and the map cools and warms across the turn.
Before any declaration the space shows a plain-English explanation of what
will appear there — readers are never shown primitives or code.

### Use the spaces well during a turn

A short playbook that turns the mechanics above into good turns:

- **Declare architecture every visible turn.** The space only draws what a
  frame declares — a turn that declares nothing leaves the reader looking at
  the cheat-sheet. Build the model from facts collected in the same turn and
  put live detail (a version, a state, a vital) in each row's label. Six to
  eight components with dependencies converging on the real hub read best.
- **Let heat tell the story.** Heat is the declared focus, not a measurement:
  mark what this turn is about hot, its neighbours warm, and re-declare so the
  map warms while you work and cools on the closing frame. Observed results
  belong in the Evidence space.
- **Choose the hero by subject.** Make the space the turn is *about* the hero.
  For architecture and system investigations,
  `data-gv-iq-spaces="architecture,evidence@bottom"` with
  `data-gv-iq-hero="architecture"` is a strong default: the model gets the big
  canvas, evidence stays glanceable, and the frame reads fine as a strip.
- **Treat all nine spaces as peers.** Use the current goal and observed evidence,
  not a fixed Tests-first order. Git, Patterns, CI/CD or any other space can be
  the compact hero when it best explains the current critical path.
- **Keep Files live for file and node work.** It refreshes from observed
  running-turn activity without authored rows. It keeps newest work at the top
  and offers bounded quick diffs for confirmed writes with edit evidence. Leave it open through
  verification and move or close it only at a real phase boundary.
- **Split to monitor, hero to read.** A three-way split is great when each
  pane only needs a glance; a dense model or comparison deserves the hero
  zone. Don't leave an 8-component map squeezed into a side strip.
- **Move at phase changes, not every frame.** Each rearrangement should mean
  something: split when a comparison phase starts, hero for the reveal, and
  close with the arrangement that best presents the outcome — or hand the
  whole canvas back with an empty spaces list. Remember to restate the spaces
  list on any frame that repositions.
- **The reader always wins.** Any chip tap, drag, ⛶ or reset overrides your
  proposals until the reader explicitly enables Auto again — treat that as
  steering, not failure, and keep declaring the model so their layout stays fed.

## Honest state, progress and evidence

Start with a stage such as “Starting” or “Waiting for an update” when no measured
work is available. Show a percentage only for an observed, finite amount of
work with a known positive denominator. For example, a check list of four known
items with two actually completed items supports “2 of 4 checked”. An imagined
three-stage process does not support “33% complete”.

This small helper validates the numeric shape of an **already observed** measure.
It cannot establish whether the inputs are true; the caller must do that.

```js
function progressLabel(stage, observed) {
  if (!observed || !Number.isInteger(observed.completed) ||
      !Number.isInteger(observed.total) || observed.total <= 0 ||
      observed.completed < 0 || observed.completed > observed.total) {
    return stage;
  }
  const percentage = Math.floor(100 * observed.completed / observed.total);
  return `${observed.completed} of ${observed.total} checked (${percentage}%)`;
}
```

Keep the denominator and the measured activity visible. A percentage for checked
items describes those items, not overall project completion. Do not invent
elapsed time, counters, throughput, remaining time or successful checks to make
a display appear active. A green result needs actual supporting evidence. A
running command, an accepted update and a visible result are different facts.

Refresh at meaningful milestones and approximately every 30 seconds during
sustained active work when the runtime permits. If nothing has changed, update
only truthful freshness or the current stage. Stop empty updates after the work
has finished. Pair any final claimed outcome with the useful artifact or saved
answer that the reader can inspect.

## Copyable starting code

The [Metal starter HTML](../reference/agent-iq-metal-starter.html) is a complete
local example. It includes the canonical symbol, metal cells, responsive
allocation rules, reduced-motion support and keyboard-accessible controls.
Choose Wide opening, Work focus, Verify focus or Deliver focus to see the same
cells move. Resize the browser to compare desktop, phone and Compact Fold.

Most frames need no script region: the native SVG example below, and the
animated-SVG patterns after it, are the standard starting point. For the
optional, advanced script-region form, on a runtime that supports it, copy the
`<section data-gv-iq-script="v1" …>` region, including its style and script. Do
not send the outer `doctype`, `html`, `head` or `body` preview wrapper as an
activity update. Replace the illustrative text with observed information and
remove the demonstration controls when they do not help the actual task.
The example's local functions are ordinary JavaScript, not GreatVibe APIs.
Keep the region's `html, body` size and padding reset with its styles. It gives
the local size container a definite height inside the isolated renderer; relying
on the standalone preview wrapper alone can collapse the copied composition.

The starter requests Inter but makes no font download. It uses a readable system
fallback when Inter is unavailable. It has no timers that manufacture progress,
no external dependencies and no host application calls.

### Native inert HTML

For a simple graphical update, native HTML and basic SVG need no script region.
The optional priority-scene structure tells a supporting runtime what is
essential and what can be condensed. This example has no claimed results:

```html
<section data-gv-iq-scene="v1"
  style="min-height:100%;width:100%;box-sizing:border-box;padding:16px;background:#10151f;color:#edf5ff;font-family:Inter,-apple-system,BlinkMacSystemFont,'Segoe UI',sans-serif;">
  <div data-gv-iq-role="focus" style="margin-bottom:14px;">
    <div style="color:#f5b34d;font-size:12px;">Starting</div>
    <h2 style="margin:6px 0;font-size:22px;">Understand the request</h2>
    <p style="margin:0;font-size:14px;line-height:1.5;">Next: identify the answer that will help.</p>
  </div>
  <div data-gv-iq-role="graphic"
    style="display:flex;flex-wrap:wrap;gap:12px;align-items:stretch;">
    <svg viewBox="0 0 360 110" role="img" aria-label="The request informs the approach, which produces a useful outcome"
      style="width:100%;max-height:180px;">
      <rect x="5" y="20" width="100" height="70" rx="12" fill="#1b3040" stroke="#56d9ec"/>
      <rect x="130" y="20" width="100" height="70" rx="12" fill="#1b3040" stroke="#f5b34d"/>
      <rect x="255" y="20" width="100" height="70" rx="12" fill="#1b3040" stroke="#56d9ec"/>
      <path d="M105 55 H127 M120 48 L127 55 L120 62 M230 55 H252 M245 48 L252 55 L245 62"
        fill="none" stroke="#56d9ec" stroke-width="2"/>
      <text x="55" y="60" text-anchor="middle" fill="#edf5ff" font-size="14">Request</text>
      <text x="180" y="60" text-anchor="middle" fill="#edf5ff" font-size="14">Approach</text>
      <text x="305" y="60" text-anchor="middle" fill="#edf5ff" font-size="14">Outcome</text>
    </svg>
    <div style="flex:1 1 180px;padding:18px;border:1px solid #56d9ec;border-radius:12px;background:linear-gradient(145deg,#253d4d,#13202f);">
      <div style="color:#56d9ec;font-size:12px;">Request → approach</div>
      <h3 style="font-size:18px;margin:8px 0;">Find the useful path</h3>
      <p style="font-size:14px;line-height:1.5;">Choose a method that matches the question.</p>
    </div>
    <div style="flex:1 1 180px;padding:18px;border:1px solid #416777;border-radius:12px;background:linear-gradient(145deg,#253d4d,#13202f);">
      <div style="color:#56d9ec;font-size:12px;">Work → useful outcome</div>
      <h3 style="font-size:18px;margin:8px 0;">Make the answer usable</h3>
      <p style="font-size:14px;line-height:1.5;">Bring back the result with evidence and any limits.</p>
    </div>
  </div>
  <div data-gv-iq-role="detail" style="margin-top:12px;color:#a2b1c6;font-size:12px;">
    Layout example only. No results have been reported.
  </div>
</section>
```

Use one `DIV` or `SECTION` scene root. Its direct `DIV` or `SECTION` children
have one role each: `focus`, `graphic` or `detail`. Use exactly one concise focus,
at least one meaningful graphic, and at most 24 role blocks. Essential content
must never depend on optional `detail`. A supporting runtime can put the focus
first, place the graphic below it and hide only optional detail when space is
limited. This structure is optional and does not prescribe the graphic itself.

Native content is sanitized and inert: no script, event handler, form, embedded
page or remote asset. Use bounded SVG or supported CSS motion only where it helps
explain active work. Provide a readable static equivalent for reduced motion.

### Advanced graphics with motion

Animated SVG is the standard way to show live movement in an Agent IQ view. It is
admitted by the host, needs no script region, degrades safely for reduced motion,
and renders reliably. Use it to show a result arriving, a check in progress or
data moving between cells — always to explain real work, never as decoration.
Keep every animated element inside a role block, and author the still first frame
to read correctly, because a reduced-motion viewer sees exactly that frame with
the motion stopped.

Reveal a result as it settles into place:

```html
<g>
  <animateTransform attributeName="transform" type="translate" from="0 24" to="0 0" dur="0.8s" fill="freeze"/>
  <!-- the row or card that just became true -->
</g>
```

Show honest, unmeasured progress with a turning ring — no invented percentage:

```html
<g transform="translate(40,40)">
  <circle r="26" fill="none" stroke="#1d3646" stroke-width="6"/>
  <circle r="26" fill="none" stroke="#56d9ec" stroke-width="6" stroke-linecap="round" stroke-dasharray="90 200">
    <animateTransform attributeName="transform" type="rotate" from="0" to="360" dur="1.1s" repeatCount="indefinite"/>
  </circle>
</g>
```

Mark state with a blinking caret or a pulsing dot — amber for active, green for a
verified result, muted for pending:

```html
<circle cx="0" cy="0" r="6" fill="#f5b34d">
  <animate attributeName="opacity" values="1;0.3;1" dur="1.1s" repeatCount="indefinite"/>
</circle>
```

Show a relationship, or data moving between cells, with a flowing connector.
Define the gradient it references so the snippet works on its own:

```html
<defs>
  <linearGradient id="flow" x1="0" y1="0" x2="1" y2="0">
    <stop offset="0" stop-color="#56d9ec" stop-opacity="0"/>
    <stop offset="0.5" stop-color="#56d9ec" stop-opacity="0.9"/>
    <stop offset="1" stop-color="#56d9ec" stop-opacity="0"/>
  </linearGradient>
</defs>
<path d="M0 40 C 120 10,240 70,360 40" fill="none" stroke="url(#flow)" stroke-width="2.4" stroke-dasharray="60 320">
  <animate attributeName="stroke-dashoffset" values="380;0" dur="5.5s" repeatCount="indefinite"/>
</path>
```

Compose these into the shape of the task — a before-and-after comparison, a step
or file list with a status dot on each row, a timeline or a topology. Keep motion
gentle and purposeful, and remember that green belongs only beside a checked
result.

### Optional isolated script region

Interactive examples, local canvas drawings or richer responsive compositions
can use an explicit `DIV` or `SECTION` with `data-gv-iq-script="v1"` where the
runtime supports it. The starter demonstrates this form:

```html
<section data-gv-iq-script="v1" data-gv-iq-height="fill">
  <!-- Local HTML and CSS, followed by classic inline JavaScript. -->
</section>
```

`fill` uses the available bounded allocation. A numeric height can be between
120 and 800 CSS pixels; the default is 360. Keep the composition responsive to
its actual region, including short allocations. Up to four regions, each with
one to eight inline scripts, are supported, subject to the overall activity
body size limit. Do not nest script regions, use script `src` or modules, or
paste TypeScript without compiling it to browser JavaScript first.

This region runs separately from the surrounding application. Its scripts can
update its own content; they cannot access the dashboard DOM, credentials,
parent APIs, network resources, prompts or gvturn functions. A script region is
therefore suitable for a local illustrative control or renderer, not for fetching
live application data or issuing commands. An agent must supply authorized,
observed information through the supported activity update path.

A script region is advanced and optional, not the default. On some runtimes a
region can be accepted by the browser yet still not become visible, so treat the
animated SVG above as the first choice and rely on a script region only when the
update receipt confirms the scripts ran and the view is visible.

## Find layouts and inspect the current view

Start with this guide and the public [catalogue](../CATALOGUE.md) for the design
language and reusable examples. If the current tool manifest exposes
`konui_agent_iq_get`, an agent can also request a read-only description of the
available layouts/templates and the current viewer's Agent IQ state. Check
availability first; older runtimes may not expose this capability yet.

The tool accepts the authenticated `username` and optional `nodeId`, `turnId`
and command `requestId`. Use the authorized current context rather than
inventing identifiers. The tool can infer the current node when it is omitted;
an optional turn selects an expected exact owner. Read the live tool schema
before calling it. A query does not switch layouts, focus, Follow or the sidebar.

The bounded version-1 result contains:

| Field | Use |
| --- | --- |
| `catalog.layouts`, `catalog.templates` | Discover supported layout IDs, descriptions and template guide references |
| `viewer`, `owner`, `panel` | Understand the current viewing mode, manual choice, owner and panel revision |
| `canvas` | Read mounted/visible/deferred state and the current width and height |
| `evidence.script`, `evidence.raster` | Inspect the current mounted update's execution/decode state and proof |
| `freshness`, `observedAt` | Distinguish authored/telemetry timestamps from the time of this observation |

An absent owner, panel, revision or timestamp is an unknown state, not zero
progress. The query does not expose raw authored HTML, prompts or credentials.
Catalog entries describe what is available; they do not prove that a particular
layout is visible. Current proof applies to the matching mounted content only.

Trusted native integrations have a corresponding, feature-detected
`window.gvAgentActivity.inspect({nodeId, turnId?})` method. It requires a node;
the turn is optional. For example, a native integration that already has the
authorized context can use this wrapper:

```js
function inspectCurrentAgentIq(context) {
  const activity = window.gvAgentActivity;
  if (!activity || typeof activity.inspect !== "function") return null;
  const request = { nodeId: context.nodeId };
  if (typeof context.turnId === "string" && context.turnId.trim()) {
    request.turnId = context.turnId;
  }
  return activity.inspect(request);
}
```

This native method is **not available inside an isolated Agent IQ script or
widget**. Such renderers use snapshots supplied by their authorized caller.
They must not create a network or parent-DOM bridge to inspect the dashboard.
If neither read capability is exposed, use the available public documentation
and state what remains unverified.

## Publish and verify an update

If `konui_activity_update` is available, read its current schema and use the
current authorized activity context. Select `layout: "agentiq"` and
`view: "agentiq"` when supported, reuse the same panel ID, and increase its
revision for meaningful updates. Do not invent identifiers or call unavailable
tools. Preserve a person's manual layout choice, reader hold and dismissal.

If the activity tool is absent and the runtime supports the assistant-output
fallback, emit a standalone commentary message with this outer structure:

```html
<section data-gv-activity-panel="v1" data-panel-id="work-phase" data-layout="agentiq" data-view="agentiq" data-title="Current work">
  <!-- Insert the native inert scene here. -->
</section>
```

The section must be the entire delivered message, without prose or Markdown
fences around it. Keep the whole message within 32 KiB and the body within
24 KiB. Reuse the panel ID. Ordinary fallback HTML remains inert. An explicit
script region runs only when the receiving runtime supports that capability;
the fallback envelope alone is not proof. Prefer the native inert scene when
that capability is unknown. This live panel does not replace the durable final
answer.

Read the returned receipt before claiming delivery:

| Receipt | What it establishes |
| --- | --- |
| `activityAccepted: true` | The matching update was accepted |
| `activityVisible: true` | The update was displayed |
| `activityDeferred` or a reader/manual hold | The viewer's choice should remain in control |
| `activityScript` with `version: 1`, `executed: true` and the expected count | Script regions completed their synchronous bootstrap; it does not prove later async work or visual quality |

A missing or failed receipt leaves delivery unverified. Do not turn acceptance
into a claim of visibility. Inspect the rendered, sanitized layout at narrow
and wide sizes before claiming that it fits: a visible receipt does not prove
readable labels, unclipped content or usable controls.

## Reuse and review

When adapting the starter, keep these checks close to the work:

1. The focus and next action are readable in the top third at the viewer's size.
2. The full allocation contains useful content; the core stays compact.
3. Phone, short Fold and desktop preserve reading order and usable controls.
4. Status and percentages describe observed facts, with an actual denominator.
5. Green means verified; unknowns and limitations remain clear.
6. Motion has a static reduced-motion version, and the example needs no network.
7. Manual layout, reader hold and panel allocation remain under the viewer's control.
8. The final delivery includes a usable result, not only an attractive live view.

For general review and saved results, see [Review AI work](review-ai-work.md)
and [Use gvturn actions](use-gvturn-actions.md). For console controls, see
[Use the main row and prompt controls](use-console-main-row-and-prompt-controls.md).
Return to the [public catalogue](../CATALOGUE.md) to find related guidance.
