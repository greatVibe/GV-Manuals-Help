# Watch The Guest Tour

The guest tour shows how to write a prompt, follow Agent IQ, use Sealed Secrets
and review the work that comes back. Johnathon presents it in a compact video
beside the demo, leaving room to see the controls he explains.

**Video:** greatVibe Guest Tour: Prompts, Agent IQ and Turn Cards  
**Catalogue slug:** `greatvibe-welcome`  
**Length:** 12:14 (734 seconds)  
**Format:** square presenter video, 1440 × 1440  
**Read instead:** [timestamped transcript](../videos/transcripts/greatvibe-welcome.md)

## Start, Pause And Stop

Choose **Start demo** in the guest welcome experience. Use the floating space
selector to pause, resume or stop. The tour is a demonstration: its work,
responses and examples are simulated.

While the guest demo is active, **Send** adds a labelled synthetic reaction to
the demo. It does not start an agent request or spend one of your free turns.
This also applies while the demo is paused. To ask a real question, choose
**Stop demo**, then enter your request and press **Send**. A prompt used in the
demo is not silently sent again when you stop.

The turns-left bar hides during the active or paused demo and returns when
the demo stops or ends. For guest limits and sign-up, read
[Ask Mochi for help](../getting-started/ask-mochi-for-help.md#as-a-guest).

## Follow The Six Chapters

### 00:00 — Welcome and guest console

Find the prompt area, Agent IQ and the guest controls. The welcome story and
the demo are separate: **greatVibe story** returns to the story, while
**Start demo** runs the walkthrough. You can stop the demo whenever you are
ready to try a request.

### 01:08 — Prompts and Agent IQ

Write the outcome you want and include the context needed to do it. Agent IQ
shows the current focus and supporting spaces. Interactions carries the
conversation. During a real request, ask for evidence and review the result
before deciding what comes next.

See [prompt controls](use-console-main-row-and-prompt-controls.md) and
[Turn Card actions](use-gvturn-actions.md).

### 02:47 — Mochi nodes and live work

A node is where work runs. Select **Mochi** in Quick Access to request a
temporary workspace. Wait for readiness before sending work. Mochi is for
questions, public help and light assistance; use a development node for
sustained builds or files you need to keep.

Mochi has a 30-minute idle lease and a one-hour maximum. Its files are
disposable. Selecting a managed or bring-your-own node is a separate step.
Read [what a node is](../concepts/what-is-a-node.md) and
[manage organisations, meshes and nodes](manage-organizations-meshes-and-nodes.md).

### 05:42 — Sealed Secrets

Use **Attach (+) → Sealed Secret** for a token, password or another supported
secret. Describe what the agent should do with the attachment in your prompt.
Never paste the secret itself into the prompt or the conversation.

The advanced form lets you choose the supported use and retention. Choose
these deliberately: a temporary attachment does not become a permanent
credential because a task continues. An agent works through the permitted
capability rather than reading the secret's plaintext. See
[secrets and credentials](../manuals/development/security-and-secrets.md).

### 07:39 — Interactions and steering

Interactions explains what is happening and carries follow-up information.
For supported member turns, a focused steer can add context or change scope
while the work continues. It is delivered at a supported checkpoint, so a
long-running operation may finish its current step first.

Guest real turns do not support mid-turn steering. Wait for the result and
send your follow-up afterward. Read [steer a running turn](steer-a-running-turn.md)
for the current capability limits.

### 09:20 — Credentials history and next steps

After the demo, try a concrete request and inspect the Turn Card, evidence,
checks and next actions. For your own development node, use the protected
credential setup flow and only the access the task needs. See
[add an AI agent credential](add-ai-agent-credential.md),
[review AI work](review-ai-work.md) and
[turn history](manage-turns-with-gv-menu-eventlog-gvturns.md).

## Read The Recording In Context

The presenter calls this a five-minute demo, but the published recording is
12:14. Its references to a free trial, included servers, retention and
security are spoken explanations, not a replacement for current policy.

- Read [plans and pricing](../reference/plans-and-pricing.md) for current
  subscription, card and billing terms. Use the live Add Node quote for
  eligible node allowances and costs.
- Temporary Mochi files are not promised to survive expiry. Do not treat a
  recorded account's history or node count as your own current state.
- Use the protected Sealed Secret workflow and its stated retention. Do not
  infer blanket deletion, no-storage or access guarantees from the recording.

## Ask A Useful Follow-Up

Try: “I stopped the demo. Show me how to ask my first real question.”
Or: “Explain the difference between Agent IQ and Interactions.”

For a longer example of reviewing and steering work on a folding phone, watch
[Complex Turns on Mobile](work-with-complex-turns-on-mobile.md). It is an
optional tutorial, separate from this guest demo.

## Notes For Agents

Use `greatvibe-welcome` to select this tour from `videos/index.json`. Read the
timestamped transcript for what was said; use the linked task guide for
current instructions. Keep the presenter compact beside the demonstration.
Do not switch a guest to a real request merely because they type during the
demo, and do not replay their demo prompt after stopping.
