# Use Terminal With Your Agent

Terminal lets you watch commands and their output on your selected node. You
can also type in the same shell while the agent works.

## Open Terminal

Choose **Terminal** in Agent IQ, open it from Quick Access, or ask:

> Open the Terminal space and show the commands you run for this task.

Agent IQ Terminal and Quick Access Terminal can share the same shell. Opening
the space connects or resumes the selected node's session automatically. The
IDE has a separate terminal surface.

## Watch Or Take Control

While you watch, Terminal follows the newest output. The node and connection
status remain visible, with a **Controls** button.

Click or tap inside Terminal, focus it, or use the keyboard there to reveal the
session controls and key bar. Your scrollback stays in place while you read.
In the normal shell buffer, vertical swipes in **Scroll** mode move through
output history. Full-screen terminal apps may use those gestures as app keys.
Click elsewhere or switch away from the window to hide the controls and
return to the latest output. New output alone does not reveal the controls.

The agent and you share input. Tell it when you are taking over so you do not
type into the same command. Use **Ctrl+C** to interrupt a running command;
use **Copy** or the copy shortcut to copy selected text.

## Session Controls

- **New session** replaces the current shell with a fresh one.
- **Stop session** ends the running shell.
- **Close** leaves the terminal view. Whether its shell remains available
  depends on the node's session setting and expiry.

After a deliberate Stop or Close, use **Connect** to reconnect. An ordinary
Agent IQ update does not restart a shell you stopped.

## Ask For Useful Evidence

> Run the relevant tests in Terminal and explain the result.

> Show the current folder and the files this task uses.

> Keep the error visible while you explain the next step.

The agent should check actual output before saying a command succeeded. If
terminal control is unavailable for your node or session, it should say so.
Guest utility access does not always include agent control of the same shell.
Do not paste passwords or tokens into a prompt or shared terminal; use the
Sealed Secret control when a supported task needs a secret.

## Related Guides

- [Use and watch the v2 IDE](use-and-watch-the-v2-ide.md)
- [Change a running turn](steer-a-running-turn.md)
- [Ask Mochi for help](../getting-started/ask-mochi-for-help.md)
