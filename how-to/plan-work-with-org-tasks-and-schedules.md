# Plan work with org tasks, to-dos and schedules

Your organisation has one shared task list that people and agents on any of
your nodes can see and act on. Use it for work that outlives a single turn:
follow-ups, checks someone must do, and recurring jobs.

- **Task:** a piece of work for a person, an agent or both.
- **To-do:** a private task only you can see.
- **Schedule:** a rule that creates a task on a repeating date, such as
  "every weekday at 09:30".

You can manage all three by asking your agent, and see them in the
[Agenda](use-the-agenda.md).

## Where a task lives

| Scope | Who can see it | Good for |
| --- | --- | --- |
| Organisation | Everyone in the organisation | Company-wide work |
| Mesh | People with a role on that mesh | A team's work |
| Node | People with a role on that node's mesh | Work tied to one machine |
| Private | Only you, and an assignee you name | Your own reminders |

A task's scope cannot change after it is created.

## Who does the work

| Performer | Meaning |
| --- | --- |
| Human | A person does it. |
| AI | An agent does it and attaches its result card. |
| AI then human | An agent prepares the work; a person reviews and approves it. |
| Script | A registered script on one node would do it, without an AI turn. |

**AI and script tasks do not start by themselves yet.** A due time on an AI
task is a reminder, not a promise that it will run. To have an agent do it
now, open the task in the Agenda and choose **Run now with AI**, or ask your
agent: "Do task <id> and report the result." Script tasks are recorded and
shown but are not run automatically.

## A task's life

| Status | How it gets there |
| --- | --- |
| Open | Created, or reopened with a reason |
| In progress | Someone started or claimed it |
| Blocked | Stopped, with a reason; unblock to continue |
| Draft ready | AI-prepared work submitted for review |
| Done | Submitted, or a draft approved |
| Skipped | A scheduled occurrence passed over, with a reason |
| Cancelled | No longer needed |

Rules worth knowing:

- **Evidence first.** A checklist item marked "evidence required" must be
  ticked with a link or reference before the task can be submitted. AI and
  script work needs its result card attached.
- **People approve.** Only a signed-in person can approve AI-prepared work.
  An agent can submit a draft but cannot approve it.
- **Proposals.** A task created as a proposal is visible only to the people
  who can accept it. They accept it or turn it down.
- **Private to-dos** can be marked done in one step.

## Due times, reminders and snoozing

Give a task a due time and time zone. You can also ask for a reminder before
it is due and an escalation after it is overdue. Reminders reach the
assignee (or the queue, or the creator when nobody is assigned); later
escalations also reach the people who manage the scope.

Snooze a task to hide it from reminders for a while (up to 90 days). It stays
on the list and shows as snoozed.

## Who can do what

| Action | Organisation task | Mesh task | Private |
| --- | --- | --- | --- |
| See it | Every member | Mesh members | Creator and assignee |
| Work on it (start, tick, comment, submit) | Admins, or the member it is assigned to | Mesh admins, or the assigned mesh member | Creator and assignee |
| Create, assign, edit, cancel, approve | Organisation owners and admins | Organisation or mesh owners and admins | Creator |

Node tasks follow the mesh column, and a node's owners and admins can also
manage them. Where your organisation allows it, mesh members can create mesh
tasks too. Anyone can create private to-dos.

An unassigned open task can be claimed by any member who could work on it.
Elevated greatVibe support staff can read organisation, mesh and node tasks,
never private ones, and cannot change them.

## Schedules

A schedule creates one task per occurrence. Set:

- **Repeat:** daily, weekly on chosen days, or monthly on chosen dates, with
  an optional interval such as "every 2 weeks".
- **Time and time zone:** for example 09:30 in your city. Daylight-saving
  changes are handled.
- **Start date** and an optional **end date**.
- **Lead time:** how early the task appears before it is due (15 minutes to
  7 days; 12 hours by default).
- **Due after:** an optional gap between the scheduled time and the due time.
- **Missed occurrences:** after an outage, create only the latest one (the
  default), all of them (up to 7), or none.

Each occurrence is created once, even if something retries. You can pause,
resume or delete a schedule; the Agenda shows its next runs.

## Try these prompts

- "Create an org task for Sam to renew the example.com certificate, due
  Friday 17:00, high priority, with a checklist."
- "Add a private to-do: call the accountant tomorrow at 10:00."
- "Every weekday at 09:30, create a task to check the overnight build."
- "List my open tasks that are overdue."
- "Propose a task for the team admins: tidy the old staging buckets."
- "Snooze task <id> until Monday 9:00."

## For agents

| Tool | Use |
| --- | --- |
| `org_task_create` / `org_task_update` | Create; edit fields or move status with `op` (start, submit, approve, reject, block, unblock, skip, cancel, reopen, accept) |
| `org_task_list` / `org_task_get` | Filter by mine, status, scope, label, sprint, project or due date |
| `org_task_claim`, `org_task_tick`, `org_task_comment`, `org_task_report` | Claim, tick a checklist item with evidence, comment, attach a result card or link |
| `org_todo_add` / `org_todo_list` / `org_todo_done` | Private to-dos |
| `org_schedule_create` / `_list` / `_pause` / `_delete` | Schedules (`pause` with `resume: true` resumes) |

Writes need the task's current version. Check the list before creating, so
you update or comment instead of duplicating. Never put secrets, tokens or
personal data in task text.

## Related

- [Use the Agenda](use-the-agenda.md)
- [Run sprints and projects](run-sprints-and-projects.md)
- [What is the org brain?](../concepts/what-is-the-org-brain.md)
