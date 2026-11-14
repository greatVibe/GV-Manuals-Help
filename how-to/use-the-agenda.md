# Use the Agenda

The Agenda is your day in one panel: your tasks, the organisation's open work,
schedules, projects and the current sprint. It is for signed-in members; guest
workspaces do not show it.

## Open it

Select the **☰** button at the left of the top bar, beside the greatVibe
logo. The Agenda slides out from the left. **Expand agenda to full screen**
grows it over the page (select it again to shrink it back), and the Agenda
can also open in its own pop-out window. On wider screens you can switch to
a week or month calendar.

The Agenda shows one organisation at a time. It opens on the organisation of
the node selected in the console, so a node in your company shows your
company's work and a node in a customer's organisation shows theirs. If you
belong to more than one organisation with an org brain, the **Org** buttons at
the top switch between them.

The Org buttons sit on one row, named by organisation. The selected node's
organisation is first on the left, followed by the organisations you opened
most recently. If the row is wider than the panel, scroll it sideways.
Organisations without an org brain have no task list, so they do not get a
button; a node in one of them opens the Agenda on your leftmost organisation.

The Agenda refreshes about once a minute while it is open.

## What you see, top to bottom

| Section | What it shows |
| --- | --- |
| Org | One named button per organisation with an org brain, shown when there is more than one; the selected one is highlighted. |
| Today headline | One line about the selected organisation's day, from the [org brain](../concepts/what-is-the-org-brain.md). Select **Why?** for the reasoning. |
| Plan your day | Your late, started, urgent and due-today tasks with rough time estimates against the time left before 18:00. |
| Sprint | The active sprint's name, day and goal, with **Plan with AI** and **Stand-up with AI**. |
| Projects | Pills that filter the task lists to one project. |
| My tasks | Open tasks assigned to you. |
| Org tasks | Other open work you can see in the selected organisation (titled "Your org"). |
| Done today | What was finished today, with each task's outcome. |
| Snoozed | Tasks you snoozed, with their wake time. |
| Schedules | Repeating work and its next runs. |

If part of the Agenda cannot load, it says that part is unavailable instead
of showing an empty list.

## Plan your day

Plan your day ranks what needs you today. Its estimates follow a simple,
labelled rule: about 30 minutes per task plus 10 per extra open checklist
item, 10 minutes to review AI-prepared work, and nothing for work an AI or
script does. A bar compares the planned time with the time left before 18:00
your time. Select **Plan my day with AI** to put a planning prompt in your
prompt box; it is not sent until you send it.

## Work a task

Select a task to see its details, checklist, evidence, history and comments.
The details show its status, priority, due time, scope, owner, performer and
creator. A finished task also shows when it was **Completed**, its
**Outcome** and who **Completed by**. Open tasks show an **AI fit** hint: who
does the work (you, AI, AI then a person, or a script) and why.

Depending on your permissions:

| Action | What it does |
| --- | --- |
| **Claim** | Assigns an unassigned task to you and starts it |
| **Start** | Marks it in progress (it does not run anything) |
| **Complete** | Opens **What was done**: write a short summary, then **Complete**. See below |
| **Defer** | Moves its due time |
| **Snooze** | Hides it from reminders: 1 h, 3 h, **Tomorrow 9:00**, or **Clear** |
| **Change assignment** | Picks the owner (people the organisation's tasks already name, or **Unassigned**) and the performer: Human, AI, or AI then a human |
| **Run on node** | Picks the node an AI task should use (**Default** restores it) |
| **Run now with AI** | For AI tasks: sends a prompt to your dashboard console so an agent does the task now and records the result |
| **Run in console** | Puts the task into your prompt box so you can edit and send it yourself |
| **Open full task** | Opens the complete task view |

**Run now with AI** starts a normal turn in your own console. Nothing else
starts AI tasks automatically yet; see
[org tasks](plan-work-with-org-tasks-and-schedules.md#who-does-the-work).

### Complete and the completion record

**Complete** always asks **What was done** (up to 500 characters). The label
says "required" when the task needs a summary: a person's task in a sprint,
an AI-prepared draft that has no summary yet, and an AI or script task you
finish yourself without the agent's result card. Otherwise it says
"optional". A draft waiting for approval shows
**Approve and complete** instead.

Complete takes the task through every step it needs (it starts an open task
first) and always shows the result. If the task list refuses, you see why,
for example a checklist item that still needs evidence; the task never just
stays where it was. The summary then shows as the task's **Outcome** and in
**Done today**. The performer cannot change while a draft waits for approval
or an AI run is active.

## Calendar

Switch to the calendar for a week or month grid. Select a task or a scheduled
run to open a full-width day view with a countdown, an hour timeline with a
"now" line, and actions grouped as Do and Move. Back or Escape returns to the
calendar.

- Drag a task to another day to move it. On touch screens, hold first.
- With the keyboard, Alt + Left or Right Arrow moves a selected task by a day.
- The side panel lists Next up, Overdue, No due date, Done today and Snoozed.
- Opening the Agenda always returns the calendar to today; a cue jumps to
  overdue work from earlier weeks.

## Reminders

Due and overdue reminders appear as small notices in any open dashboard tab,
even with the Agenda closed. In the Agenda you can turn on a chime and allow
browser notifications.

## Watching agents work with tasks

When an agent creates or changes tasks and schedules during a turn, the
**Agenda** space in Agent IQ shows those changes beside a live view of what
is due now. Tap any card to see more: a task opens its details and
actions, a schedule shows its rule and next runs, and an agent's call shows
what it asked for and, if it failed, the reason. The **Org brain** space
shows the agent's questions to the org brain.

## Related

- [Plan work with org tasks and schedules](plan-work-with-org-tasks-and-schedules.md)
- [Run sprints and projects](run-sprints-and-projects.md)
- [Understand the status bar](understand-the-status-bar.md)
