# Work With Complex Turns On Mobile

Use a folding phone to prepare a clear request, follow the evidence while it
runs, and review the result. This recording shows Johnathon using the
greatVibe PWA on the main screen of a Samsung Galaxy Z Fold7, with his camera
in a small inset.

**Video:** Complex Turns on Mobile: greatVibe on Galaxy Z Fold7  
**Catalogue slug:** `greatvibe-mobile-tips`  
**Length:** 24:22 (1462 seconds)  
**Format:** 1080 × 1200, 9:10 screen recording  
**Read instead:** [timestamped transcript](../videos/transcripts/greatvibe-mobile-tips.md)

This is an optional tutorial alongside the guest story. Playing it does not
start or replace the guest demo. It shows one recorded account and piece of
work; the nodes, permissions and counts on screen are examples.

## Prepare The Next Request

### 00:00 — Turn Cards and recommended actions

Read the result before choosing a footer action. Check what changed, what was
tested and what remains unverified. An audit is useful when a change affects
several files, important behavior or a boundary that needs another review.

### 02:05 — Hold to edit and the prompt composer

A quick tap sends an action's suggested prompt. Hold the action for about
half a second to put its text into the prompt box without submitting it.
Add your constraints and desired outcome before sending. Use the larger
composer when a request needs more room.

See [Turn Card actions](use-gvturn-actions.md) and
[the prompt controls](use-console-main-row-and-prompt-controls.md).

### 03:13 — Inline images and clear instructions

Place images next to the instructions they explain. Say what each image
shows, what should change and what must stay. Give the agent the relevant
content rather than assuming it can see another app on your phone.

For sensitive information, use the appropriate protected attachment flow.
Never put tokens or passwords in a screenshot or ordinary prompt.

### 04:16 — Co-write with Tandem Turns

Use the **TT** button, the two-head icon, when another person should help
write one prompt. Participants must be on the same node. The controller
approves other users joining; sending confirms one shared request and ends
the editing session. The larger prompt composer is a separate control.

See [Tandem Turns](use-tandem-turns.md) for joining, approval and reconnect
behavior.

## Follow The Work On A Small Screen

### 05:17 — Send the prompt and read Agent IQ

After sending, use **Main view** for the current focus and the next check.
Use **Interactions** for the agent's explanation and your follow-up context.
The other Agent IQ spaces expose supporting evidence as it becomes available.

### 06:40 — Fullscreen and choosing spaces

Tap a space's empty background to fullscreen that space. Repeat to return.
Double-tap the background to fullscreen the entire Agent IQ canvas; repeat
to release it. Taps on files and controls keep their own actions.

Use the floating space selector to choose the evidence you want to inspect.
On a folding phone, inspect one dense space fullscreen instead of making
every label smaller. Your manual layout choice takes precedence over the
agent's proposed arrangement. Auto can arrange spaces again when you enable it.

### 08:21 — Read Architecture and Patterns

**Architecture** connects components and dependencies. Its focus styling
shows where the agent is looking, not a service-health measurement. Inspect
the evidence and any explicitly stated concerns before drawing conclusions.

**Patterns** explains engineering observations and tradeoffs with source
references. It is the agent's analysis of the code, not proof that tests
passed. Read the cited code and check results for that evidence.

See [Architecture](use-architecture-in-agent-iq.md) and
[Agent IQ spaces](build-agent-iq-metal-layouts.md).

### 11:13 — Handle support while work continues

**Support** keeps issues connected to the work. Distinguish a problem in
greatVibe from a defect in your own project. Inspect the issue, give the
agent relevant context, and keep the original task clear if you add a repair
to the current work.

An issue should be marked resolved only after evidence supports the fix.
Your authorization controls which issues you can see and manage. Do not
assume another viewer can access the same issue list. See
[report and follow support requests](report-and-follow-support-requests.md).

### 15:27 — Follow builds pipelines and file changes

**Builds** follows tracked operations. **CI/CD** shows observed pipeline
state. A request to publish is not proof that publication succeeded; look for
the terminal result and any deployment checks.

**Files** shows observed file activity and the node where it happened.
Inspect source or an available diff when you need to understand a change.
Missing evidence stays unknown. See
[nodes, builds and tests](../manuals/development/nodes-builds-and-tests.md) and
[CI/CD](../manuals/development/devops-cicd-and-iac.md).

### 17:26 — Inspect Topology and workers

**Topology** shows the work's components and available worker activity.
It helps explain who is doing what and how work relates across nodes.
Worker availability depends on the current runtime, account and permissions.
The recording's number of workers is not a guaranteed limit or allocation.

## Steer And Review

### 19:24 — Steer work across authorized nodes

For a supported member turn, send one focused update that says how the
remaining work should change. For example: “Use another available development
node for the independent test run, and keep the original task in scope.”

The agent must check which nodes and capabilities are available and use only
authorized access. A recorded node name does not make that node available to
you. A steer is delivered at a supported checkpoint; it does not interrupt
every tool immediately. Guest real turns cannot be steered mid-turn.

See [steer a running turn](steer-a-running-turn.md).

### 22:27 — Deploy and verify the work

Keep the intended target and scope clear. Follow the build or deployment
receipt, then the checks that prove the result works. If the agent cannot
verify the deployed result, it should say what is missing rather than report
success from elapsed time or an accepted request.

### 23:34 — Review changes and wrap up

Read the final Turn Card and remaining checks. Compare its changes with the
repository state: a dirty-file count can include earlier work, so it is not
automatically the number of files changed by this request. Use an audit or
focused follow-up when the evidence leaves an unresolved concern.

## Quick Reference While Watching

Hold a suggested action to edit its prompt before sending. Add images beside
the instructions they explain. Use Agent IQ to inspect Architecture,
Patterns, Files, Support and Topology while work runs. Send a focused steer
when scope changes. Review evidence and remaining checks before approving
the result.

For an agent, a useful request is: “Explain the mobile video at 06:40 and
show me how to inspect one Agent IQ space.” Read the matching transcript
chapter before quoting the recording, then use the current task guide for
the steps that apply to this account.

## Related Guides

- [Watch the shorter guest tour](watch-the-guest-tour.md).
- [Review AI work](review-ai-work.md).
- [Turn lifecycle and audits](../manuals/development/turn-lifecycle-and-sdlc.md).
- [Work with files](work-with-files.md).
- [Plans, trial and billing](../reference/plans-and-pricing.md).
