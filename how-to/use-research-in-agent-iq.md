# Use Research in Agent IQ

Research shows the sources your agent consulted during the current turn, why it
read them, and what it found. Ask the agent to open Research while it compares
options, checks documentation, reviews a paper or investigates a question.

For example: **“Compare these options and show the sources you read in Research.”**

## Read a finding

Choose a source to see its research method, source type, topic, optional genre,
purpose and finding. An exact reference identifies the document, code location
or tool result consulted. A public source may also have an **Open source** link.
Links open only when you activate them.

With more than five sources, use the filter to search titles, topics, purposes,
references and findings. Your selected source stays selected when its finding
updates. The view adapts to a phone, foldable, tablet or desktop. Short spaces
scroll within their own area.

Research carries an **Agent analysis · consulted source** label. It records the
agent's account of its research. It does not turn that account into a verified
tool receipt, prove that a source is correct, or fetch a remote page on your behalf.
You can inspect the sources and ask the agent to check a claim further.

## What belongs here

The agent should add a source only after reading it in this turn. A planned
search, an unread search result, a familiar source from memory, or a suggestion
for later reading does not belong in the consulted-source list.

A finding can include uncertainty or conflicting evidence. Ask the agent to
state what the source supports, what it does not settle, and why that matters
to your task. Research starts empty for each new turn.

## Author a Research declaration

Agents propose `research` through the usual Agent IQ spaces arrangement and
include a hidden declaration in their scene. This illustrative example is a
format reference, not a claim that the sample source was read:

```html
<div data-gv-iq-research="v1" data-gv-iq-role="detail" style="display:none">
  <div data-research-id="source-guide"
    data-research-title="Sample source guide"
    data-research-type="docs"
    data-research-method="comparison"
    data-research-topic="Choosing an approach"
    data-research-genre="Technical reference"
    data-research-purpose="Compare the documented behavior of two approaches."
    data-research-ref="docs/sample-guide.md:20"
    data-research-url="https://example.com/guide">State the finding supported by the source here, after reading it.</div>
</div>
```

Each declaration allows up to twelve unique sources. Use a stable ID beginning
with a letter, with at most 48 letters, digits, underscores or hyphens. Required
fields are title (120 characters), type, method, topic (100), purpose (240), and
a finding in the row's text (600). Genre is optional (60).

Source types are `web`, `docs`, `code`, `paper`, `dataset`, `tool` or `other`.
Research methods are `source-review`, `comparison`, `literature`,
`investigation`, `fact-check` or `other`. These are separate: a comparison can
consult both documentation and code.

Supply at least one exact source reference (300 characters) or public HTTPS
URL (512). References allow letters, digits, spaces and `_ . / : # @ ( ) -`.
Public URLs cannot contain credentials, queries, private hostnames, IP addresses
or nonstandard ports. Do not include secrets or private information that the
people viewing the turn should not see. The renderer displays plain text;
scripts, images, remote HTML and embedded pages are not part of this format.

A later declaration replaces the list. Keep source IDs stable across revisions.
Omitting the block preserves this turn's sources; an empty block clears them.
Native readback reports the current turn's source model even while Research is
closed, without opening the space or changing the reader's selection.

See [Agent IQ layouts](build-agent-iq-metal-layouts.md) for arrangement and
[gvContext](../concepts/what-is-gvcontext.md) for how turn context and spaces fit
together.
