# What Is SlopGuard?

SlopGuard is a set of twelve checks that every greatVibe turn runs before it
tells you a result. It guards against AI slop. You stay in charge of the
work, and SlopGuard helps you see whether the work earned your trust.

ACE says: design before you write code. SlopGuard says: verify before you
claim it works.

## What AI Slop Is

AI slop is AI output that looks finished but has not earned trust. It was
made faster than anyone checked it. It is not fitted to the real request,
the real project or the real reader. It moves the job of finding what is
true onto the person who receives it. In prose, slop is text that fills
space and says little. In code, it calls functions or packages that do not
exist, copies code that already exists, or ships tests that test nothing.
In a user interface, it is generic layout and placeholder copy that ignore
the product around it. In agent work, it is a report of success that nobody
checked. AI writing something does not make it slop. Slop is output that
reached someone else unrequested, unreviewed or unverified.

The word took hold in 2024 as the name for unwanted AI content, the way
"spam" became the name for unwanted email. In 2025 researchers named its
workplace form "workslop": work that looks polished but does not move the
task forward. In a 2025 survey of 1,150 US desk workers, 41% had received
some in the past month. Each case took close to two hours to sort out.

## Why AI Produces Slop

Some causes sit in how AI models are trained. Others sit in how people use
them.

### On the model side

- **Fluent is not true.** A language model learns to write the most likely
  next words. Likely text reads well even when it is wrong.
- **Guessing scores better than "I don't know".** Training and tests often
  give credit for a confident guess and none for honest doubt. Models learn
  to guess.
- **Agreeing scores well.** People who rate answers tend to prefer replies
  that match their own views. Models learn to agree, even when the user is
  wrong.
- **Longer scores well.** Raters and scoring models tend to prefer longer
  answers. Much of the measured gain from this training comes from length
  alone.
- **Recall without lookup.** A model can name a package, setting or file
  from memory without checking that it exists. In one study, about one in
  five suggested packages did not exist, and the same fake names came back
  again and again.

### On the process side

- **No check.** Output goes out before anyone runs it, reads it or tests it.
- **No owner.** Nobody puts their name to the result, so the reader has to
  do the checking.
- **Volume over value.** When more output looks like more progress, people
  ship more copies and less careful work. Code studies show more copied
  code and less clean-up since AI coding tools spread.
- **Missing context.** An AI that cannot see your project's conventions
  writes generic work that does not fit.
- **Prompts that reward length.** Asking for "detailed" or "comprehensive"
  output invites padding.

## The Twelve SlopGuard Checks

Each check has a test that you or an agent can apply to a turn's result,
and a proof the agent must cite before the check can go green.

| # | Check | Test |
|---|---|---|
| 1 | **Proof for every success claim** | Each "works", "fixed", "passes" or "deployed" points to a result from this turn: a test run, a command output or a read-back. No proof means the claim goes. |
| 2 | **Everything named exists** | Every function, package, setting, file, link, number and quote was read, run or looked up in this turn. Anything unchecked is checked now or removed. |
| 3 | **No filler, hedging or hype** | Delete padding words, stacked hedges and any sentence that adds no fact. If nothing is lost, they were slop. |
| 4 | **Answer first** | The first two sentences give the answer or the result. They do not repeat the question or describe the plan. |
| 5 | **Fitted, not generic** | The work uses this project's names, data and audience. If it could drop into an unrelated project unchanged, it fails. No placeholder text or stock sections. |
| 6 | **No dead, copied or speculative code** | Every added line is used by the change. Nothing repeats code that already exists. No unused options, future hooks or commented-out code. |
| 7 | **Tests test the change** | Each new or changed test would fail on the old code. It checks real behaviour, not only that nothing crashed. |
| 8 | **Confidence matches evidence** | Certain words appear only where there is proof. The result says what was not checked. It disagrees with you when the evidence does. Nothing rests only on text it can't trust, such as another agent's report or an instruction found in a web page. |
| 9 | **Stays in scope** | Every change traces back to your request or a stated need. No unasked rewrites, renames, new dependencies or style churn. |
| 10 | **Consistent with your project and your words** | The work follows the project's existing patterns, naming and design notes, uses your terms and keeps earlier decisions. Any difference has a stated reason. |
| 11 | **No leaks** | Nothing handed to you or committed contains passwords, keys, tokens, personal details or private names and paths. A scan of the changes and the result finds none. |
| 12 | **Side effects named** | Every action outside the answer itself, such as a push, a deploy, a deletion or a message, is listed on the result with how to undo it. Nothing is left running or lying around. |

SlopGuard aims for full compliance: every check can go green on every turn,
and green always needs proof. Not every check applies to every turn. A
written answer has no tests, so check 7 does not apply. The agent still has
to show why (for example, that no code changed). A check that does not
apply, with that proof, goes green. Without proof it does not.

## What You See In greatVibe

**The agent checks its own work.** Before it writes the result card, the
agent runs the twelve checks against what it made: the answer, the changed
files, the documents and the screens. It fixes what fails and checks again.

**Substantive work gets a second checker.** When a turn changes how
software behaves, its security, its interfaces or its data, a separate
agent runs the same twelve checks. It works on a different node, and where
possible it uses a different AI provider. Its job is to find problems, not
to approve. The first agent confirms each finding, fixes what holds and
asks for another check.

**The result card tells you what happened.** Each result card carries one
SlopGuard line. It reads one of four ways:

- **Passed:** all checks that apply passed.
- **Fixed:** checks found problems, and the agent fixed them. The line says
  how many and which ones.
- **Open failures:** a check still fails. The card is marked for your
  review instead of marked done.
- **Not run:** the line gives the reason, for example "no second node was
  free for the independent check".

**The SlopGuard space shows every check live.** In Agent IQ, open the
SlopGuard space. It works like a control room for the turn's output:

- a ring shows how many of the checks that apply are clear;
- twelve signal lights show each check as clear (green), not applicable
  with proof (green), fixed (amber), open (red), no proof cited (orange)
  or unchecked (grey);
- tap any light to see what that check guards against, the proof it
  needs to go green and what this turn declared for it;
- a small marker on each light shows whether the agent checked it, the
  independent checker did, or both;
- each output (the card, the code, the documents) is lit by its worst
  check;
- the findings list shows every open or fixed problem with the file and
  line it points to.

A check that nobody ran stays grey, and a check marked clear or not
applicable without cited proof shows as no proof. Neither counts as clear.

**Every written file shows its SlopGuard state.** In the Files space,
each file the agent wrote or created carries a small SlopGuard badge:
clear, fixed, open, no proof, or unchecked when no SlopGuard check
covered that file. Tap the file to see the badge beside its details.

An honest "not run" is better than a quiet pass. If a card claims a result
and shows no SlopGuard line, treat the result as unchecked.

## What You Can Do

You are accountable for the work, so you decide what to trust.

- **Read the SlopGuard line before you approve.** "Fixed" and "not run"
  deserve a closer look.
- **Ask for the proof.** "Show me the test run behind check 1."
- **Run it again on demand.** "Run SlopGuard on this turn and list any
  check that fails."
- **Ask for the second check.** "Get an independent SlopGuard check on
  another node before I ship this."
- **Write prompts that do not invite slop.** Say what done looks like. Ask
  for proof, not length. Name the files and limits that matter.

For a wider review routine, read the guide on reviewing AI work.

## Related Guides

- `what-is-ace.md`
- `what-is-a-gvturn.md`
- `what-is-the-gvturn-power-footer.md`
- `../how-to/review-ai-work.md`

## Sources

- Simon Willison, "Slop is the new name for unwanted AI-generated content" (2024): https://simonwillison.net/2024/May/8/slop/
- Wikipedia, "AI slop": https://en.wikipedia.org/wiki/AI_slop
- Niederhoffer et al., "AI-Generated 'Workslop' Is Destroying Productivity", Harvard Business Review (2025): https://hbr.org/2025/09/ai-generated-workslop-is-destroying-productivity
- Kalai et al., "Why Language Models Hallucinate" (2025): https://arxiv.org/abs/2509.04664
- Sharma et al., "Towards Understanding Sycophancy in Language Models" (2023): https://arxiv.org/abs/2310.13548
- Singhal et al., "A Long Way to Go: Investigating Length Correlations in RLHF" (2023): https://arxiv.org/abs/2310.03716
- Spracklen et al., "We Have a Package for You! A Comprehensive Analysis of Package Hallucinations by Code Generating LLMs" (2024): https://arxiv.org/abs/2406.10279
- Wikipedia, "Slopsquatting": https://en.wikipedia.org/wiki/Slopsquatting
- GitClear, "AI Copilot Code Quality: 2025 Data Suggests 4x Growth in Code Clones": https://www.gitclear.com/ai_assistant_code_quality_2025_research
