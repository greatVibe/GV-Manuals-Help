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

Elapsed time means how long you have waited. It is not a completion estimate.
Progress labels describe returned stages only. An unavailable update does not
prove the answer failed. A timed-out request may have reached the brain;
retrying sends a new question.

Scroll to read earlier replies. New replies preserve your reading position.
Select **Jump to latest** to return to the newest reply.

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

The answer shows its model and effort when supplied. Model access depends on
your organisation's current configuration and availability. A configured
choice does not guarantee it can answer at that moment.

## Ask for work

Ask plainly, for example: "Run the report review task" or "Close this sprint
and start the next one." The brain can return an action card. Check its
summary and current instructions before confirming a change.

A run can start without another confirmation only when an owner or admin has
given the brain a current mandate that covers that work. Permissions, allowed
kinds, node eligibility, expiry and limits still apply. A mandate never
approves an AI-prepared draft on a person's behalf. Requests requiring review
show that reason instead of claiming they started.

Read the result: **Started**, **Scheduled**, **Not started automatically** and
a proposal awaiting confirmation mean different things. Open the linked task
for its current run and outcome. An answer saying it intends to work is not a
run receipt. See [org tasks](plan-work-with-org-tasks-and-schedules.md) and
[the Agenda](use-the-agenda.md).

## Short delayed checks

A short request such as "Check the review progress again in 3
minutes" uses a lightweight read-only check where the serving brain
supports it. It does not need a repeating Agenda schedule.

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
- **/mandate** shows what the brain may start and when that permission ends.
  Owners and admins can set or revoke it through the command's instructions.
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
