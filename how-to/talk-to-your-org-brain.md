# Talk to your org brain

Brain Talk lets you ask your organisation's brain directly. Use it to find
team decisions, understand current work or ask a general question without
starting a work turn.

The [org brain](../concepts/what-is-the-org-brain.md) supplies the answer.
Brain Talk does not change files, run commands or assign work for you.

## Open Brain Talk

1. Select a node in the organisation you want to ask about.
2. Open **Brain Talk** from Quick Access.
3. Choose **Organisation** for questions about your team's records, or
   **Open questions** for broader questions. Open questions is selected initially.
4. Write your question and select **Send**.

The selected node determines which organisation's brain answers. Switching
nodes closes this view; reopen Brain Talk on the new node. A brain must be
available for that organisation, and your access is checked when you ask.

## Write and correct a question

The message box holds your draft until you send it. You can select text,
replace a word, use backspace or paste several lines before submitting.
Your draft edits are not sent as separate questions.

- **Enter** sends the question. **Shift+Enter** adds a new line.
- While your keyboard is composing a character or word, Enter finishes that
  composition. It does not also send the question.
- Only one question waits for an answer at a time. Empty questions are not
  sent. Keep each question within 1,000 characters; the message box reports
  when a question is too long.
- **Stop waiting** stops this view waiting for a reply. The brain may still
  finish the request. It is not automatically sent again.

If sending fails, read the message before trying again. A timed-out request
may have reached the brain; retrying is a new question.

## Read earlier answers

Scroll the conversation with your finger, mouse wheel or keyboard. If you
are reading an earlier answer, a new reply leaves your reading position in
place. Select **Jump to latest** when you want to return to the newest reply.

The view keeps a bounded amount of recent text. Older text can fall out of
the view during a long session. It is not an archive of your organisation's
work; use [global search](use-global-search.md) for result cards.

**Questions are independent.** Earlier questions and answers remain visible
for you to read, but are not silently attached to the next question. Include
the necessary subject in each question: "What did we decide about the import
job?" is clearer than "What about that?"

## Clear or close the view

**Clear** removes the displayed questions, answers and draft. A reply that
arrives after that clear does not restore the old conversation.

**Close** discards this view's conversation and stops waiting for any reply.
The conversation is kept only while the view is open. Reopening starts an
empty view; it does not restore a previous browser or terminal conversation.

Clearing this view does not delete a saved org-brain note, task or result
card. Those are separate records.

## Understand the answer and its sources

**Organisation** asks concern your organisation's records. **Open questions** also
allows general knowledge and, when available, web search. The answer should
identify the sources it used. A web answer is not evidence of what your team
has done.

Check the cited source before acting on an answer. In particular:

- A note records what someone wrote. Read its date and the current task
  outcome before treating an old finding as an unresolved problem.
- A live-work view shows the work it can currently observe. An empty view
  does not establish that nobody worked during the last six hours.
- A document describes the version it covers. A repository name alone does
  not mean the brain has read its files or verified the current code.
- Missing access or an unavailable source means the evidence is incomplete.
  Ask your agent for a scoped investigation when you need code or deployment
  proof.

Expand **Sources** to read returned records that match the answer's citations.
**Unverified citations** have no matching returned source record, so do not
treat them as evidence. **Retrieved notes** were returned without citations;
their presence does not show that the answer used them. Read the source itself
before relying on the answer's claim.

**Coverage** reports whether a source is available, partial, unavailable or
unknown. **Coverage not reported** means no usable coverage details were
returned. It does not mean the brain searched all your organisation's records.

The reply shows the answering model and effort when that information is returned.
Your organisation controls its configured default and backup. Model answers
can be off for a newly started brain; then it matches words in the available
notes. See [Deploy and run your org brain](deploy-and-run-your-org-brain.md).

## Use the terminal version

Select **Open terminal** to switch to the terminal version on a node with the
Brain Talk utility installed. This clears the browser conversation first.
The terminal's input and history controls belong to the terminal app, so
they differ from the browser view above. Type **/help** for its controls.

| Command or key | What it does |
| --- | --- |
| `/notes` | Browse org-brain notes; use Up/Down to choose, Enter to open and Esc to return |
| `/today` | Read the organisation's Today headline |
| `/note` | Prepare a shared note; review the exact text and confirm before saving |
| `/model` | List available models; `/model auto` returns to the configured default |
| `/clear` | Clear the chat and request that the node's terminal copy is cleared |
| Esc | Cancel waiting for the current request |
| `/quit` | Leave the terminal app |

The terminal lists only models configured for the organisation. Choose one
with `/model` followed by its displayed number or name. A choice affects
later questions in that terminal session.

Use Up/Down to move through history a line at a time, Page Up/Page Down for
a page, and Home/End for the top or latest text. On a phone, terminal swipes
may be translated into app keys; the browser conversation uses native
scrolling.

Cancelling a note save does not prove the note was not saved. Check `/notes`
before saving it again.

## Keep private chat and shared notes distinct

Asking a question does not automatically save it as an org-brain note.
Explicitly saved notes are visible to your organisation. Only the author can
replace or delete their note.

Do not include passwords, keys or tokens in a question or note. The temporary
browser history is not a promise about every system's retention: the question
still goes to the brain and, for model answers, its configured provider.

## Related

- [What is the org brain?](../concepts/what-is-the-org-brain.md)
- [Use Terminal with your agent](use-terminal-with-your-agent.md)
- [Find past work across nodes](use-global-search.md)
- [Org work tools for agents](../reference/org-work-tools.md)
