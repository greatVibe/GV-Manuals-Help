# Ask An Agent To Open The Right UI

An agent can open supported Konui surfaces, or point to controls with guidance
bubbles when you only need orientation.

## Open A Surface

| Ask for | Surface | Action |
| --- | --- | --- |
| Main action row only | `main-row` | `default` |
| A main-row card without opening its destination | `main-row` | `attach`, `sealed-secret`, `history`, `files`, `ide`, `chitchat`, or `settings` |
| Toolbox | `toolbox` | `default` |
| Toolbox focused on Stop turn | `toolbox` | `stop-turn` |
| Add a credential | `settings` | `credential-add` |
| Eventlog | `settings` | `gv.eventlog` |
| Turn history | `settings` | `gv.gvturns` |
| Files | `files` | `default` |
| Prompt history | `history` | `default` |
| Attach choices | `attach` | `default` |
| ChitChat | `chitchat` | `default` |
| IDE | `ide` | `default` |
| Sealed Secret | `secrets` | `default` or `advanced` |
| Add Node | `node-create` | `hosted` |
| Account Admin | `account-admin` | `default` |
| Personalisation | `account-admin` | `personalisation` |

The dashboard must be connected. The agent checks delivery count and the
browser receipt before saying a surface is visible. Camera, gallery, file, and
clipboard pickers still require your click.

## Ask For Guidance Instead

Guidance bubbles attach to a closed set of safe, human-facing targets:

<!-- gv-guidance: {"id":"profile-picker","target":"profile-picker","message":"Choose the AI profile for this console here."} -->
- Status bar: `connection-health`, `node-picker`, `profile-picker`,
  `model-picker`, `turn-status`, `git-status`, `jump-latest`, `toolbox`,
  `stop-turn`, and `turn-timer`.
<!-- gv-guidance: {"id":"main-row-files","target":"files","message":"Open the Files workspace from this main action.","surface":"main-row","action":"files"} -->
- Main row: `main-row-toggle`, `attach`, `sealed-secret`, `history`, `files`,
  `ide`, `chitchat`, and `settings`.
<!-- gv-guidance: {"id":"prompt-input","target":"prompt-input","message":"Write or refine the next request in this prompt box."} -->
- Prompt controls: `prompt-input`, `composer`, and `send-prompt`.

An agent uses the single guidance tool for one bubble and the dedicated
guidance-group tool for two to eight bubbles in one fast command. Concurrent
guidance appears together. Sequenced guidance shows one step at a time with a
Next control. Bubbles stay for about 30 seconds unless you dismiss them.

The presentation includes one centered “Click to dismiss guidance” control.
You can also click any ordinary console element: the guidance closes and that
click continues normally. When guidance is all you requested, the verified
bubble presentation ends the agent turn without adding a general gvturn card.

Hidden controls must be revealed first. The guidance tools can combine one
closed surface reveal with the bubble presentation in the same command. For
example, an agent reveals `main-row` before pointing at Files, or reveals
`toolbox` before pointing at Stop turn. This prevents a tool from claiming
success when the requested anchor is not actually visible.

<!-- gv-guidance: {"id":"toolbox-stop-1","target":"toolbox","message":"Open the turn toolbox here.","surface":"toolbox","action":"stop-turn","group":"stop-turn-tour","order":1,"mode":"sequence"} -->
<!-- gv-guidance: {"id":"toolbox-stop-2","target":"stop-turn","message":"Stop the active turn with this control.","surface":"toolbox","action":"stop-turn","group":"stop-turn-tour","order":2,"mode":"sequence"} -->

## Useful Requests

- “Show the main row, then point to Files without opening Files.”
- “Point out the node picker, profile picker, and prompt box.”
- “Open the toolbox and show me the Stop turn button.”
- “Show me Attach, the full composer button, and Send.”

Related: `use-console-main-row-and-prompt-controls.md` and
`use-the-status-bar-toolbox-and-stop-turns.md`. Agents and documentation
maintainers can read the marker schema in `../reference/guidance-markers.md`.
