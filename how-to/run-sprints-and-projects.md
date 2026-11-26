# Run sprints and projects

Sprints and projects group your [org tasks](plan-work-with-org-tasks-and-schedules.md).
A **sprint** is a short time box with one goal. A **project** groups work for a
customer or an internal effort, over any length of time. A task can belong to
one sprint and one project at the same time.

## Sprints

A sprint covers organisation or mesh work. Private to-dos never join one.

| Setting | Rule |
| --- | --- |
| Name and goal | The goal is what the team commits to finish |
| Start and end dates | At most 42 days apart |
| Time zone | Days are counted in this zone ("day 3 of 10") |
| Scope | Organisation or one mesh |

Only one sprint can be active per scope at a time. A sprint goes from
**planned** to **active** when someone starts it, and to **closed** when it
ends. When you close a sprint, the unfinished tasks you can manage move to
another open sprint you choose, or back to the backlog. A closed sprint does
not change; if some work was left behind, ask your agent to carry it over
again.

A person's task in a sprint needs a short summary of what was done when it
finishes. **Complete** in the [Agenda](use-the-agenda.md) asks for it, and
the summary becomes the task's outcome. An agent that finishes such a task
writes the summary itself when it submits.

Each sprint shows simple counts over the tasks you can see: total, done,
open, in progress, blocked and overdue.

### Ceremonies

When you create a sprint you can ask for ceremonies. greatVibe then creates
three repeating tasks in the sprint's time zone:

| Ceremony | When |
| --- | --- |
| Stand-up | Every weekday, 09:30 by default (you can pick the time) |
| Review | Last day, 14:00 |
| Retro | Last day, 15:00 |

They are "AI then human" tasks: an agent can prepare each one and people run
it. The preparation starts only from **Run now with AI**, an accepted
schedule's run authority or a covering brain mandate; a due time alone
starts nothing. Open the task and choose **Run now with AI**, or ask your
agent. A person
approves the prepared stand-up, review or retro with a short summary.

### Sprints in the Agenda

The [Agenda](use-the-agenda.md) shows the active sprint with its day and
goal. **Plan with AI** and **Stand-up with AI** put a ready-made prompt in
your prompt box. Nothing is sent until you send it.

## Projects

A project covers organisation or mesh work. Private tasks can join a project
too.

| Field | Rule |
| --- | --- |
| Name | Up to 80 characters |
| Code | A short unique handle shown on task chips, such as `ACME-WEB`: 2 to 16 capital letters, digits or hyphens, starting with a letter or digit |
| Customer | Optional, up to 120 characters |
| Billable | A yes or no label for the work |
| Repositories | Up to 8 git repositories, such as `example-org/website` |

Codes are unique among your organisation's active projects. If a code is
taken, pick another. Archive a project when the work ends: it keeps its tasks
and takes no new ones. Restore it to use it again, as long as its code is
still free.

Projects do not record time. The billable label marks which work is for a
customer; it does not track hours or create invoices.

### Projects in the Agenda

Tasks show their project code as a chip. The Projects pills above the task
lists filter them to one project.

## Who can manage them

Organisation owners and admins manage organisation sprints and projects.
Mesh owners and admins (and organisation owners and admins) manage a mesh's.
Anyone who can edit a task can put it into a sprint or project they can see.

## Try these prompts

- "Create a two-week sprint for the website team starting Monday, goal:
  launch the new pricing page, with ceremonies at 09:15."
- "Put tasks <id> and <id> into the current sprint."
- "Close the sprint and move unfinished work to the next one."
- "Create a billable project ACME-WEB for customer Acme Ltd, linked to
  example-org/website."
- "List open tasks in project ACME-WEB that are overdue."

## For agents

| Tool | Use |
| --- | --- |
| `org_sprint_create` | `{scope, name, goal?, startOn, endOn, tz?, ceremonies?{standupAt?}}` |
| `org_sprint_update` | Edit name, goal or end date, or `op` start, close (with `carryTo`) or carry; needs the current version |
| `org_sprint_list` / `org_sprint_get` | Sprints with day N of M and counts |
| `org_project_create` / `org_project_update` | Create; edit fields or `op` archive / restore; needs the current version |
| `org_project_list` / `org_project_get` | Projects with counts |
| `org_task_create` / `org_task_update` with `sprint` or `project` | Put a task in (an empty value takes it out) |

Sprint tools need a recent node version, and project tools a newer one. If a
tool is missing, the node's owner can update it with **Update to …** on the
`gv.system` card in Settings. Inputs, limits and errors:
[Org work tools for agents](../reference/org-work-tools.md).

## Related

- [Plan work with org tasks and schedules](plan-work-with-org-tasks-and-schedules.md)
- [Use the Agenda](use-the-agenda.md)
- [Plans, investigations, flows and backlog issues](../manuals/development/agile-work-management.md)
