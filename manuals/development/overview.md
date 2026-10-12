# Develop Software With greatVibe

A technical, procedural manual for developers and technical founders. It
describes how greatVibe works today, so you and your agents can plan, build,
test, ship and run software with it.

**Agents:** read this page, then the one chapter that matches the question.

## The Model In One Minute

| Concept | What it is | Read |
| --- | --- | --- |
| Turn | One prompt and the agent's work on it, ending in one recorded outcome | `turn-lifecycle-and-sdlc.md` |
| gvturn | The card a turn ends with: result, status and next steps | `../../concepts/what-is-a-gvturn.md` |
| Node | The machine where the agent works, with your repos and tools | `nodes-builds-and-tests.md` |
| Mesh | Your nodes connected as one workgroup | `../../how-to/manage-organizations-meshes-and-nodes.md` |
| ACE | A small design note beside every code file and folder | `ace-and-context.md` |
| gvContext | The compiled rules and repo knowledge every agent starts with | `ace-and-context.md` |
| Connector | A saved, governed connection to GitHub, CI/CD, cloud or an API | `devops-cicd-and-iac.md` |
| Agent IQ | The live view of a running turn: files, tests, builds, Git, CI/CD | `../../concepts/what-is-gvcontext.md` |

## The Development Loop

1. **Ask** for an outcome, naming the repository and how to verify it.
2. The agent **reads** the folder and file ACE notes, then the code.
3. It **updates the ACE** design note, then the code.
4. It **runs the tests** for what it changed, on the node that has the repo.
5. It **commits** code and ACE together with a `Turn:` message.
6. It ends with a **gvturn** card. Changes to 3 or more files are marked
   `audit_required`.
7. You **audit**, then **push**, then watch **CI/CD**.

## Quick Reference

| I want to… | Ask or do | Chapter |
| --- | --- | --- |
| Start a feature | "In `my-service`, add X. Add tests. Commit, don't push." | `turn-lifecycle-and-sdlc.md` |
| Plan before coding | "Plan X in `my-service`. Don't change code yet." | `agile-work-management.md` |
| Review risky work | Choose **Audit Now** on an `audit_required` card | `turn-lifecycle-and-sdlc.md` |
| See repo state | "Show the status and diff of `my-service`." | `git-and-repositories.md` |
| Push everything | "Push all repos." | `git-and-repositories.md` |
| Run a long build | The agent tracks it as an operation; watch Builds | `nodes-builds-and-tests.md` |
| Build on another node | "Run the tests for `my-service` on `node_example`." | `nodes-builds-and-tests.md` |
| Check a pipeline | "What state is the `my-service` pipeline in?" | `devops-cicd-and-iac.md` |
| Change infrastructure | "Create a CloudFormation change set for this template; don't execute." | `devops-cicd-and-iac.md` |
| Track a bug | "Raise a customer project issue for this bug in `my-service`." | `agile-work-management.md` |
| Use a secret | Attach it with **Sealed Secret 🔒**, never paste it | `security-and-secrets.md` |

## Chapters

1. `turn-lifecycle-and-sdlc.md` — SDLC phases mapped to turns, statuses,
   commits, audits, steering, chained turns.
2. `ace-and-context.md` — design-led coding with ACE files and repository
   context.
3. `git-and-repositories.md` — repositories, branches, commits, pushes and
   merges through agent tools.
4. `nodes-builds-and-tests.md` — where code runs, runtimes, test discovery,
   long builds, other nodes, the IDE.
5. `devops-cicd-and-iac.md` — CI/CD connectors, cloud reads and gated
   changes, infrastructure as code, delivery evidence.
6. `agile-work-management.md` — plans, flows, investigations, support issues
   as work items, team prompts.
7. `security-and-secrets.md` — secrets, credentials and actions that need
   your confirmation.

## Where To Do Development

| Place | Use it for |
| --- | --- |
| Mochi | Questions, onboarding, reading these manuals. Temporary and disposable, not for builds |
| Hosted node | Your day-to-day development node. Add it from **Add node** |
| Your own machine | Connect a machine you already run, with your own runtimes and access |

Pricing for nodes is in `../../reference/plans-and-pricing.md`.

## Ground Rules For Agents Using This Manual

- Describe only what the tools and product do today. If a capability is not
  in this manual or visible in your tool list, say it is not available.
- Use agent tools (Git, files, connectors, cloud) before shell fallbacks.
- Never ask for secrets in a prompt. Use Sealed Secret.
- Confirm before destructive actions: force pushes, hard resets, deleting
  stacks or large directories.
