# Agile Work Management

greatVibe tracks work at three levels: the **turn** (minutes), the **plan or
flow** (hours to days), and the **issue** (a bug or request with a lifecycle).
This chapter shows how to run an agile cadence with them.

## Levels Of Work

| Level | greatVibe object | Agile equivalent |
| --- | --- | --- |
| Turn | gvturn card | A commit-sized task |
| Plan | `plan` gvturn with steps | A story broken into tasks |
| Investigation | `investigation` gvturn with findings | A spike |
| Flow | A thread of related turns | A feature in progress |
| Issue | Support issue | A backlog item, bug or request |

## Plans

Ask for a plan before a multi-step change:

> "Plan adding SSO to `my-service`. List steps with acceptance criteria. Don't
> change code."

The result is a `plan` gvturn. Each step has a status: pending, in progress,
completed or skipped. Progress is completed steps over total steps. Then run
one step per turn ("Do step 3 of the SSO plan"). The agent marks the step and
links the turn that did it.

## Investigations (Spikes)

For a bug hunt or a design question:

> "Investigate why `GET /items` is slow. Start with the hypothesis that the
> index is missing."

An investigation records findings in order, typed as hypothesis, evidence,
question, note or conclusion, each with a confidence and sources. It ends
**concluded**, **blocked** or **abandoned**, with a written conclusion.

## Flows

Related turns group into **flows** automatically: a flow starts with the
first prompt on a topic, later turns join it, and related flows can merge.
A flow completes when the work ships. Agents link each card to the right flow,
so the dashboard shows one thread per feature instead of loose cards.

## Issues As Backlog Items

Use support issues to record work that must not be lost.

| Kind | Use for | Required |
| --- | --- | --- |
| `customer_project` | A bug or request in **your own** application, repository, deployment or configuration | The repository or project reference |
| `greatvibe` | A problem in greatVibe itself | — |

Fields you set when you create an issue:

| Field | Values |
| --- | --- |
| Request type | bug, feature, documentation, performance, security, access, billing, other |
| Severity | low, medium, high, critical |
| Summary | 8 to 500 characters, no secrets |
| Evidence | Up to 5 references: turn IDs, commits, file paths |
| GitHub | Organisation, repository, issue and up to 20 commit references |
| Turns | Turns where you saw the problem, and turns that fixed it |

Repeats of the same problem are recognised and counted on one issue instead of
creating duplicates.

On issues you own you can recategorise, attach evidence, set labels, add
notes, link related issues and link more turns.

**Procedure: log a bug found during a turn.**

> "Raise a customer project issue for `my-service`: pagination returns
> duplicates on page 2. Severity medium, request type bug. Link this turn."

**Procedure: close the loop.** After the fix lands: "Link the fixing turn and
commit to that issue."

### Lifecycle And Planning

Issues move through a lifecycle (new, triaged, acknowledged, in progress,
waiting, resolved, closed, or dismissed/duplicate). Lifecycle changes and
delivery planning fields (work item type, sprint, release, estimate, delivery
state) are managed by support. You see them on the request. See
`../../how-to/report-and-follow-support-requests.md`.

## A Working Cadence

| Ceremony | How to run it in greatVibe |
| --- | --- |
| Backlog refinement | "List my open customer project issues for `my-service`, highest severity first." |
| Sprint planning | Pick items; ask for a `plan` per item |
| Daily work | One plan step per turn; audit risky turns |
| Stand-up | "Summarise yesterday's turns across my nodes." |
| Review | Walk the cards and the CI/CD space for what shipped |
| Retro | "Which turns needed audit fixes this week, and why?" |

## Working Together

- **Tandem Turns:** several people on the same node co-write one prompt live,
  then send it as a single turn. See `../../how-to/use-tandem-turns.md`.
- **Turns across nodes:** see your team's work in one place. See
  `../../how-to/view-turns-across-nodes.md`.
- **Steering:** redirect a running turn. See
  `../../how-to/steer-a-running-turn.md`.

## Related

- `turn-lifecycle-and-sdlc.md`
- `../../how-to/report-and-follow-support-requests.md`
- `../../how-to/manage-turns-with-gv-menu-eventlog-gvturns.md`
