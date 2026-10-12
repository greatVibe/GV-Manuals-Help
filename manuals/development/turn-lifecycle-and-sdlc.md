# The Turn Loop And Your SDLC

In greatVibe every unit of work is a **turn**: you send a prompt, an agent works
on a node, and the turn ends with one recorded outcome. This chapter maps the
software development lifecycle onto that loop.

## The Loop

```
prompt ─► understand ─► design (ACE) ─► change ─► test ─► commit ─► gvturn card ─► review / audit ─► next prompt
                ▲                                                                        │
                └──────────────────────── steering while it runs ◄───────────────────────┘
```

| SDLC phase | What happens in greatVibe | Evidence you can check |
| --- | --- | --- |
| Requirements | Your prompt, attachments and repository context | The prompt in turn history |
| Plan | A `plan` gvturn with numbered steps, or a short plan in the card | Plan steps and their status |
| Design | The agent reads and updates ACE files before code | ACE diffs in the commit |
| Build | Edits and builds on the node that holds the repository | Files space, Builds space |
| Test | Tests for the changed code run in the same turn | Tests space receipts |
| Review | The gvturn card, then an audit turn for risky changes | Card status, audit card |
| Release | Commit, push, and your CI/CD pipeline | Git space, CI/CD space |
| Operate | Pipeline and cloud state read through connectors | CI/CD and IaC spaces |

## How A Turn Ends

A visible turn ends with exactly one terminal outcome. For development work
that is almost always a **gvturn** card created as the turn's last action.
Nothing runs after it.

A gvturn records the result as structured HTML, a type, a status and 2 to 5
next-step choices with one primary choice. See `../../concepts/what-is-a-gvturn.md`.

### Status Tells You What To Do Next

| Status | Meaning | Your action |
| --- | --- | --- |
| `completed` | Read-only or informational work, finished | Nothing required |
| `audit_required` | The turn changed 3 or more files, or touched security or an API contract | Run the audit (see below) |
| `pending` | The agent needs a human decision | Choose an option |
| `in_progress` | Work continues next turn | Continue |

greatVibe also raises a turn to `audit_required` automatically when it made a
large number of tool calls, even if the agent marked it complete.

### Types Used In Development

| Type | Use it for |
| --- | --- |
| `general` | Most implementation results |
| `plan` | A multi-step implementation plan with trackable steps |
| `investigation` | Hypotheses, findings and a conclusion for a bug hunt |
| `support_request` | Creating or following a support issue |
| `manual_action` | Steps only a human can do, such as approving in a provider console |
| `comparison` | Option A against option B |

Card titles must stay within 100 characters.

## The Commit-Per-Turn Rule

Every turn that changes files commits before it creates its card. Code and its
ACE files are committed together. The message format is:

```
Turn: <what changed, 50 characters or less>

<optional detail: why, tests run, follow-ups>

GVTurn: <the gvturn title>
```

Read-only turns, output-only turns and turns where you said "don't commit" are
the only exceptions. Pushing is a separate step: ask for it, or use the **Push**
reaction on the card.

## Audit Turns

An `audit_required` card replaces its normal choices with **Audit Now** and
**Override Audit**.

**Audit Now** sends a prompt that names the source card. The auditing agent:

1. Re-reads the change, its ACE notes and its tests.
2. Looks for bugs, scope creep, edge cases and missing tests.
3. Fixes real problems in a new commit, with a regression test that fails
   before the fix.
4. Marks the source card complete and creates its own card with the findings.

Use audits for anything that ships to production. Tests passing in one runtime
do not prove behaviour in another; an audit is where a reviewer asks that
question.

## Steering A Running Turn

You can send a message while a turn runs. The agent receives it at its next
step, replies with a one-line acknowledgement and changes course. Use steering
to narrow scope, add a requirement or stop a wrong direction early. See
`../../how-to/steer-a-running-turn.md`.

## Long Or Repeating Work

- **Chained turns.** A card can carry an auto-continue setting: after a short
  delay greatVibe sends the next prompt itself, until a maximum number of
  iterations or a maximum duration is reached. You can cancel at any time.
  Use it for batches, such as "migrate the next ten files".
- **Background waits.** Long builds and deliberate waits are tracked as
  operations so the dashboard shows real progress instead of a frozen turn.
  See `nodes-builds-and-tests.md`.

## Procedure: A Feature In One Turn

1. Prompt with the outcome, the repository and the acceptance test. Example:
   "In `my-service`, add pagination to `GET /items`. Keep the response shape.
   Add tests. Commit, don't push."
2. Watch Agent IQ. Files shows reads and writes, Tests shows test receipts.
3. Steer if it drifts.
4. Read the card. If it is `audit_required`, choose **Audit Now**.
5. When the audit card is clean, choose **Push**, then check the CI/CD space.

## Procedure: A Bigger Change Across Turns

1. Ask for a plan first: "Plan the move from REST polling to webhooks in
   `my-service`. Don't change code yet." You get a `plan` card.
2. Approve the plan or edit it with steering.
3. Ask for one step per turn: "Do step 2 of the plan." The plan's step status
   updates as each step lands.
4. Audit each step that changes three or more files.

## Related

- `overview.md`
- `ace-and-context.md`
- `../../how-to/review-ai-work.md`
- `../../how-to/use-gvturn-actions.md`
- `../../concepts/what-is-the-gvturn-power-footer.md`
