# Deploy and run your org brain

Each organisation has its own [org brain](../concepts/what-is-the-org-brain.md):
its own notes, its own view of running work and its own Today headline. You
start it, watch its health and reset it from the **Org brain** tab of your
organisation in Account Admin.

## Who can use the tab

Organisation owners and admins see the **Org brain** tab on their
organisation's card. Members, viewers and guests do not. Starting or resetting
a brain asks you to verify your access with your passkey first.

## Open it

1. Ask your agent: "Open Account Admin so I can manage my organisations."
2. Find your organisation's card and select **+** to expand it.
3. Select the **Org brain** tab (beside Overview, Access and Settings).

## Start a brain for your organisation

**New organisations:** when you create an organisation, **Deploy an org brain
(recommended)** is checked. Leave it checked and the brain starts within a
minute of creating the organisation, with no extra step.

**Existing organisations without one:** the tab says "The org brain is not
hosted for this org yet." and shows a **Deploy** group.

1. Select **Deploy org brain**.
2. Verify your access with your passkey when asked.
3. The line under the button follows the request:

| Line | Meaning |
| --- | --- |
| Waiting for the ring to start the brain. | The request is queued |
| Starting the brain. | The brain is starting |
| Brain deployed. It shows here as soon as the ring reports in, within a minute. | Done; the tab switches to the brain's status by itself |

You can leave the tab open; it switches over without a reload. If something
goes wrong you see one plain line, such as "Org brains are not available in
this org's region yet." or "The brain took too long to start. Try again.",
and the button works again.

## Read its status

Once the brain runs, the tab shows four groups and refreshes every minute
while it is open.

| Group | What it tells you |
| --- | --- |
| Provisioning | Whether the brain is hosted, whether the task list is available, and whether AI runs are on |
| Running state | Brain and task list state (running, degraded, unreachable), their releases, how long they have been up, and when the last status arrived |
| Health | How quickly each answers, their CPU and memory, the size of the brain's store, and whether model answers (Deep ask) are on |
| Usage | Notes, live turns on the board, and task counts: open, overdue, blocked, in progress, awaiting approval, schedules, sprints and projects |

An amber note says when the status is more than three minutes old. A
**History** section draws the last 24 hours or 7 days: CPU, memory, brain
store, response time, and running turns with open tasks.

Readings that are normal for a new brain:

- **Live turns on the board: 0** until someone in the organisation runs a
  turn.
- **"Brain: no samples"** on the CPU chart for its first minute; CPU needs
  two readings a minute apart.
- **Deep ask: Off.** A new brain answers from notes and the live board; model
  answers are switched on separately.

## Reset it

The **Restart** group appears once the brain runs.

- **Reset this org's brain** empties the live board. Running turns reappear
  as they report their next step. Notes are kept, and other organisations
  are not affected. Use it when the board looks wrong.
- The list under it shows recent requests (deploys, resets) with who asked,
  when, and the result.

## Who can reach your brain

Only your organisation. Every question, note and task call goes to the brain
of the organisation that owns the node it comes from. A node in another
organisation, even one your meshes trust, reaches its own organisation's
brain, never yours. People who belong to two organisations reach the second
brain only from a node in it.

## Related

- [What is the org brain?](../concepts/what-is-the-org-brain.md)
- [Manage organisations, meshes and nodes](manage-organizations-meshes-and-nodes.md)
- [Plan work with org tasks and schedules](plan-work-with-org-tasks-and-schedules.md)
- [Org work tools for agents](../reference/org-work-tools.md)
