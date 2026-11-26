# Talk to your org brain

Brain Talk helps you find team decisions, understand current work and ask a
general question. It can also propose work, link to an existing task and
start permitted work through your organisation's run controls.

## Open Brain Talk

1. Select a node in the organisation you want to ask about.
2. Open **Brain Talk** from Quick Access.
3. Write your question and select **Send**.

The selected node determines which organisation's brain answers. Switching
nodes closes the view. Reopen it on the new node. Your access is checked when
you ask. **Pop out**, where offered, opens a separate view without sending a
question or copying your current conversation into it.

## Write a question

Your draft stays in the message box until you send it. Select text, replace a
word or paste several lines before submitting.

- **Enter** sends. **Shift+Enter** adds a new line. While your keyboard is
  composing a character, Enter finishes that composition first.
- The composer accepts up to 50,000 characters. A serving brain or older
  node may enforce a smaller request limit and reports a refusal.
- Up to two questions can wait for answers. Each answer stays beside its
  own question, even when the second finishes first. Network commands are
  unavailable while ordinary questions are pending.
- **Stop waiting** stops this view waiting. The brain may still finish.
  It does not automatically resend the question.

Daily question allowances are unlimited by default. An organisation can still
set an explicit daily limit for the organisation or each person. Model
availability, the size of one request, concurrent questions and delayed-check
limits are separate.

Elapsed time means how long you have waited. It is not a completion estimate.
Progress labels such as **Gathering context for your question**, **Reading
sources for your question** and **Writing your answer** describe returned
stages only. If a progress read fails temporarily, Brain Talk keeps waiting
and checks again while your question is pending. **Checking for another
update** does not mean the answer failed or that a new stage was observed.
A timed-out question may have reached the brain; sending it again creates
a new question.

Scroll to read earlier replies. New replies preserve your reading position.
Select **Jump to latest** to return to the newest reply.

## Attach an image

Use **Attach images** beside the composer, or paste an image into it. You can
attach up to four JPEG, PNG or WebP images. Brain Talk prepares smaller copies;
their combined size must fit within 2 MiB. Review the previews and remove any
image you do not want to send before selecting **Send**.

Images are used for that question only. Their bytes are not kept in
conversation memory or restored history. The text of the question and answer
can still be remembered. A later question that needs the picture must attach
it again. The question and images go to the configured model provider.

Use **Org + general** or **Organisation only** for private image questions.
Images are not sent to public web research. Legacy public-web image requests
are refused. An image question cannot be saved as a delayed check or authorise
a task or other action; send a separate text request for that work. If an image
is refused, correct or remove it before sending again.

## Conversation memory and scopes

The brain remembers your answered private conversations for follow-up
questions and later recall. This memory belongs to you within the organisation.
Other members do not see it. Reopening can restore recent exchanges. The
visible transcript and remembered material are bounded; use
[global search](use-global-search.md) for saved result cards.

Use the scope controls beside the composer:

| Scope | What the answer can use |
| --- | --- |
| **Org + general** | Accessible organisation records, remembered conversation and general model knowledge. Web research stays off. |
| **Org + web** | Organisation context and conversation for the answer, with only the current question sent to web research. The exchange can join your remembered conversation. |
| **Organisation only** | Organisation records and conversation. Web research stays off. |

Check your question before using Org + web: its text goes to web research.
Selecting it does not prove a search ran. Read the returned web status and
sources. Restored older **Public web** answers describe a separate scope that
excluded organisation context and prior messages.

**Clear** removes the visible conversation and draft. It keeps your chosen
scope, and does not erase remembered conversations, saved notes, tasks or
result cards. **Close** stops this view waiting and discards its displayed
text. **Forget remembered conversations** erases your remembered exchanges;
it does not delete shared org notes or tasks.

## Read sources before acting

Answers can show numbered citation chips and expandable evidence. A cited task
can open from its chip or **Open task**. Sources report returned records,
with their dates and relevant details. A repository name alone does not prove
the brain read current files or verified a deployment.

**Unverified citations** have no matching returned record. **Retrieved notes**
were returned without being cited. Neither proves the answer used that source.
Coverage can be available, partial, unavailable, unknown or **not checked**.
A quick question may skip evidence it did not need. **Coverage not reported**
means no usable coverage details arrived. Missing access and empty results do
not prove that no work happened.

The answer shows its model and effort when supplied.

## Choose a model

Use **/model** to open the choices. Models reported as unavailable are disabled,
with a reason and a resume time when one is supplied. A suspended model is
not selectable. **Availability could not be checked** also leaves a choice
disabled; being listed does not grant access. Use **Filter models** when it
appears to narrow a longer list.

**Auto preference ranking** shows the configured preference among currently
available models. It is not the order every question will try. Phase priority
and temporary cooldown can change which model runs. Use **/model auto** to
return to automatic choice. Read the model on the returned answer to see
which one answered. A displayed resume time is not proof the model has resumed.

## Ask for work

Ask plainly, for example: "Create a task to review the import job and run
it now", "Raise the priority of the release checklist" or "Close this sprint
and start the next one." Changes you confirm run as you, with your
permissions.

**When you asked for it, it goes through.** If the change matches what you
asked for in your own words, Brain Talk confirms it for you from your
signed-in session. Its details fold away under the result.

- A delete, a schedule delete, a sprint rollover, or any change marked as
  permanent waits 5 seconds with a **Stop** button first. **Stop** leaves everything unchanged and shows the
  normal **Confirm** button.
- You still check and confirm a card when the brain drafted something you
  did not ask for, when the instructions mention secrets or sending data
  out, and when the card was restored after you reopened Brain Talk.
- Running an existing task shows a **Run a task** card. **Run now** opens
  the task in the Agenda in front of Brain Talk, ready for you to confirm
  once.
- On a confirm card, cancelling a task, pausing a schedule and raising a
  priority take one tap. Creating a task, a sprint rollover and a permanent
  delete take two.

**Under the org policy.** If you set the brain's org policy, or you are
an organisation owner or admin, a run it covers can start without your
confirmation. It runs as the person who set the policy. Other members
get **Not started automatically** with the reason. Allowed kinds and limits
still apply, and the policy never approves an AI-prepared draft on a
person's behalf. Requests requiring review show that reason instead of
claiming they started.

Read the result: **Started**, **Scheduled**, **Not started automatically** and
a proposal awaiting confirmation mean different things. An answer saying it
intends to work is not a run receipt. See
[org tasks](plan-work-with-org-tasks-and-schedules.md) and
[the Agenda](use-the-agenda.md).

### Follow a run

When a task you asked for is created and queued, or a run starts under a
org policy, a line under the result follows it: waiting for a node, starting,
running, then finished, waiting for approval, blocked, failed or cancelled.
It checks about every 8 seconds while Brain Talk is open, for up to 45
minutes. A run scheduled for later is not followed; open the task instead.
If the line cannot read the run, it says so: open the task to check.

When a run that ran as you finishes, including one the brain started under
your policy, the brain can also tell you in Brain Talk. Another member who
only asked for the work is not told; open the task instead.

## Short delayed checks

A short request such as "Check the review progress again in three minutes"
uses a lightweight read-only check where the serving brain supports it.
Other supported forms include "Check the review progress in 3mins from now
and report back to me" and "Recheck in 2 minutes if the review has finished".
Name one read-only goal and one delay. It does not need a repeating Agenda
schedule. This path does not perform general timed jobs, edits or deployments.

Treat it as scheduled only after Brain Talk shows a saved receipt with a due
time. Use **Cancel** on that receipt to withdraw a pending check. A refusal,
clarification or sentence promising to come back is not a saved receipt.
Checking status later does not grant permission to change files, start a job
or deploy something.

The server handles an accepted check independently of the open view. Brain
Talk retrieves the result while open and can restore it later in the same
conversation. Clear starts a different conversation and stops showing those
checks; it does not promise server cancellation. Older nodes can report that
delayed results are unavailable. A successful scheduling receipt proves the
request was saved, not that due-time delivery has succeeded. If no result
arrives, ask for a scoped investigation of that receipt. Browser notifications
and delivery to a closed phone are not guaranteed.

## Useful commands

Use **/help** for the commands supported by your current view.

- **/model** lists model choices. **/model auto** restores automatic selection.
- **/deep <question>** asks with the full available notes and activity.
- **/web <question>** selects Org + web and asks the question.
- **/charter** reads the owner's priorities. **/guide** shows guidance help.
- **/policy** shows what the brain may start, the ceiling and the brain's
  last change. Owners and admins can set it (**/policy set**), stop the brain
  changing it (**/policy brain off**), undo the brain's last change
  (**/policy undo**) or revoke it (**/policy revoke**). **/mandate** still
  works.
- **/checkins off** stops quiet-time follow-ups. **/checkins on** allows a
  relevant check-in after 20 quiet minutes while the view is open, up to three
  until you interact. These are separate from saved delayed checks.

Reply chips are suggested next questions. Tapping one sends that text.
Shared notes are separate from private conversation memory; save only material
you intend the organisation to read.

## Use the terminal version

Select **Open terminal** to switch to the terminal version on a node with the
Brain Talk utility installed. This clears the visible browser conversation first.
The terminal's input and history controls belong to the terminal app, so
they differ from the browser view above. Type **/help** for its controls.

| Command or key | What it does |
| --- | --- |
| `/notes` | Browse org-brain notes; use Up/Down to choose, Enter to open and Esc to return |
| `/today` | Read the organisation's Today headline |
| `/note` | Prepare a shared note; review the exact text and confirm before saving |
| `/model` | List available models; `/model auto` returns to the configured default |
| `/web <question>` | Request public web research for this question only, without attaching organisation context |
| `/clear` | Clear the chat and request that the node's terminal copy is cleared |
| Esc | After the paste recovery notice, recover the draft; outside paste, cancel waiting for the current request |
| `/quit` | Leave the terminal app |

The terminal lists only models configured for the organisation. Choose one
with `/model` followed by its displayed number or name. A choice affects
later questions in that terminal session.

After `/web`, the next ordinary question returns to the default org-and-general
mode. If the terminal or brain cannot support web research, it reports that
limit rather than silently sending the question in another mode.

Use Up/Down to move through history a line at a time and Page Up/Page Down
for a page. With an empty draft, Home/End moves to the top or latest text.
While editing a draft, Home/End moves to its start or end. On a phone,
terminal swipes may be translated into app keys; the browser conversation
uses native scrolling.

If a paste is interrupted and no more input arrives for five seconds, the
terminal shows **Esc: recover paste**. Wait for this notice, then press
**Esc once** to recover your draft. Review it and press **Enter** when you
are ready to send. During a paste, Escape only recovers after the notice
appears. Recovering the paste does not send the draft or cancel an answer
already in progress. Pasted line breaks stay in the draft instead of sending
a question while a recognised paste remains active, both before and during
the recovery notice. Pause after pressing Esc before continuing to type.

The terminal must recognise where a paste starts. A severely delayed or
damaged paste boundary may be treated as typed text, so a pasted line break
can send a question. If a broken terminal control sequence makes a character
disappear, press **Esc once** and pause before typing again. Outside paste,
Esc cancels a waiting request or clears an idle draft. Check the remaining
draft before pressing Enter.

Cancelling a note save does not prove the note was not saved. Check `/notes`
before saving it again.

## Privacy and shared notes

An explicitly saved note is visible to your organisation. Private conversation
memory is separate. Do not include passwords, keys or tokens in a question or
note. Questions go to the brain and, for model answers, its configured provider.
Turning web research off does not keep the question inside your browser.

## Related

- [What is the org brain?](../concepts/what-is-the-org-brain.md)
- [Deploy and run your org brain](deploy-and-run-your-org-brain.md)
- [Plan work with org tasks and schedules](plan-work-with-org-tasks-and-schedules.md)
- [Use the Agenda](use-the-agenda.md)
