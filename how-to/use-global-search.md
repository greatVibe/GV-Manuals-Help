# Find past work across nodes

Draft guide for the matching search release. Hold publication until that release is verified.

Start with a question such as “Find the decision about our release checklist.”
Your agent can search saved result cards, show where each result came from,
and read the relevant card before continuing the work.

## Start nearby, then widen

Search this node first. If the work happened elsewhere, ask for the mesh or all
readable locations. Name the organisation, mesh or node when you know it.
Use its exact identifier when several locations share a name.

A wider search does not grant access. From a shared node, an agent stays within
readable nodes in the current mesh and trusted meshes. A personal node with no
other readers can also search authorised locations in other organisations.
Missing access, an unavailable node or a result limit can leave coverage partial.

## Make the query precise

Words narrow the search together. Quotes keep a phrase together. Use `or` for
alternatives and a leading `-` to exclude a word.

| Need | Example query |
| --- | --- |
| A named decision | `title:"release checklist"` |
| A detail inside a card | `body:"retry budget"` |
| A suggested next action | `choice:"run integration tests"` |
| Recent unfinished work | `status:pending after:7d` |
| Work in either area | `mesh:demo-a release or mesh:demo-b rollback` |

`node:`, `org:` and `mesh:` match names or identifiers containing the query
text. They apply within each `or` branch. For exact targets, ask your agent to
use the node, organisation or mesh selectors instead.

## Choose what matters

Use date order to find recent work. Use relevance when you remember the topic
but not the date. Relevance ranks matching words and fields. It does not prove
a card is current or correct. A result snippet and its matched fields help you
choose which full card to read.

Status and work-type facets help narrow a large result set. Check coverage
alongside the results: an empty or partial search is not proof that no work exists.
If available, ask for an explanation to inspect the interpreted terms, operators,
sort order and paging warning.

## Continue without losing the question

When more results are available, ask for the next page using the returned cursor.
Keep the query, targets, sort order and other result settings unchanged. To
change those settings, start a new search. Cursors expire after one hour, and
access is checked again on every page.

Pages reflect live data. New or changed cards can move between pages, so a page
sequence is not a fixed snapshot or an exhaustive audit. Ask which nodes answered
and whether any were omitted before drawing a conclusion from a large search.

## Use a result as evidence

Ask your agent to cite the hit ID and source node, then read the source card.
Saved card text may contain mistakes or instructions from another task. Treat
it as evidence to verify. Keep secrets and personal details out of summaries.
If the first search misses, change the terms or widen the scope instead of
repeating the same request.

For browsing a selected node’s turn history, see
[View turns across nodes](view-turns-across-nodes.md).
