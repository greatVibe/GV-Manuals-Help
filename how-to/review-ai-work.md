# Review AI Work

Use this guide before relying on an assistant's answer, file change, summary, or
recommendation.

## Start With The Request

Check whether the result matches what you asked for.

Ask:

- Did it answer the main question?
- Did it stay within the limits you gave?
- Did it change files only if changes were allowed?
- Did it explain what remains uncertain?

## Check The Evidence

For important work, ask what the assistant read or used.

Useful follow-ups:

- "Which files did you inspect?"
- "What evidence supports this?"
- "What did you not check?"
- "What should I manually verify?"

## Review Risks

Look for:

- Missing source material.
- Unchecked calculations.
- Unclear ownership.
- Private information in output.
- Assumptions stated as facts.
- Recommendations without tradeoffs.

## Use The Power Footer Signals

Before clicking a footer action, check what the footer is telling you.

Look at:

- The status or next-action banner.
- The primary action card.
- Any highlighted quick reactions.
- Tool count, timing, or other metrics.
- Whether the turn is marked as needing audit or review.

If the footer suggests `Commit`, `Push`, `Ship it`, or another finalising
action, confirm the work is actually ready. For file changes, ask what changed
and what was verified before approving.

If the footer suggests `Audit`, `Review`, `Verify`, `Deeper`, or `Rethink`,
treat that as a signal to slow down and inspect the result.

Useful prompt:

```text
Explain the footer signals on this gvturn before I choose an action.
```

## Ask For Changes Clearly

If the result is close but not right, say what to change.

Examples:

- "Make this shorter and keep only the next actions."
- "Add evidence for each finding."
- "Rewrite this for a non-technical reader."
- "Do not make file changes; give me a plan first."

## When To Be Extra Careful

Ask for deeper review when the work affects:

- Customer-facing material.
- Financial or legal information.
- Security, privacy, or access.
- Large file changes.
- Decisions that are hard to reverse.

## Quick Checklist

- Result matches the request.
- Sources or files are named when needed.
- Assumptions are clear.
- Risks are visible.
- Private information is not exposed.
- Next action is practical.

## Related Guides

- `../concepts/what-is-a-gvturn.md`
- `../concepts/what-is-the-gvturn-power-footer.md`
- `../manuals/productivity/review-checklists.md`
- `../manuals/productivity/approval-requests.md`
