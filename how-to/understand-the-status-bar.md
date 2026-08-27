# Understand The Status Bar

The status bar sits directly above the prompt. It shows which node and AI
profile will receive your next prompt, what the current turn is doing, and the
controls used to inspect or recover the console.

## Controls From Left To Right

| Control | What it shows | What happens when you use it |
| --- | --- | --- |
| GreatVibe logo | Browser and console connection state | Click it to open Browser Connection Health and inspect reconnect or timing details. |
| Node picker | The selected node's human-readable name | Click for Quick Access to another node; hold for the fuller topology view. |
| Profile picker | The selected AI profile, such as Codex or Claude | Click to choose the profile that receives the next prompt. |
| Model controls | Model, thinking effort, and tone when available | Click the relevant pill to change that part of the active profile. |
| Turn status | Short live text such as starting, working, waiting, replaying, or ready | Read this before repeating a prompt or using recovery controls. |
| Git status | Repository state for the selected node | Click to open repository details and available Git actions. |
| Jump to latest | A downward arrow | Click to scroll the console to its newest output. |
| Toolbox | Session, turn, connection, history, and recovery tools | Click to open Stop turn, Force idle, Browser Health, Reconnect, Reset console history, Access Tree, New session, and Reload. |
| Turn timer | Elapsed time while a turn is active | Use it with the status text to judge whether work is still progressing. |

Some controls appear only when relevant. The timer is normally empty while no
turn is running, and compact layouts may hide optional model controls to make
room for higher-priority status.

## Status Bar Versus The Power Footer

The status bar describes the selected console and active turn. A gvturn power
footer belongs to one saved result and offers follow-up actions such as Verify,
Audit, Commit, or Continue.

Use the status bar to change the destination of your next prompt, inspect live
work, scroll, or recover the console. Use the power footer to respond to a
specific completed or reviewable gvturn.

## Ask For Point-Of-Use Help

You can ask an agent to point at one or several controls without taking you to
another page. Examples:

- “Show me the node picker and profile picker.”
- “Point out the Git status and jump-to-latest controls.”
- “Show me where turn status and elapsed time appear.”
- “Show me how to stop this turn.”

Guidance bubbles remain visible for about 30 seconds, can be dismissed
individually, and can appear together for a multi-step explanation.

## When Something Looks Wrong

1. Read the live turn status and timer.
2. Click the logo to inspect Browser Connection Health.
3. Confirm the selected node and profile.
4. Use Jump to latest in case the newest result is below the visible console.
5. Open the toolbox only if you need a recovery action.

Do not repeatedly send the same prompt or press Stop several times while the
status is still changing.

## Related Guides

- `use-the-status-bar-toolbox-and-stop-turns.md`
- `use-console-main-row-and-prompt-controls.md`
- `manage-turns-with-gv-menu-eventlog-gvturns.md`
- `../concepts/what-is-a-node.md`
- `../concepts/what-is-a-gvturn.md`
