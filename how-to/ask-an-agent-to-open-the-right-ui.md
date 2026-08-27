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

- Status bar: `connection-health`, `node-picker`, `profile-picker`,
  `model-picker`, `turn-status`, `git-status`, `jump-latest`, `toolbox`,
  `stop-turn`, and `turn-timer`.
- Main row: `main-row-toggle`, `attach`, `sealed-secret`, `history`, `files`,
  `ide`, `chitchat`, and `settings`.
- Prompt controls: `prompt-input`, `composer`, and `send-prompt`.

An agent can show up to eight bubbles in one explanation. Concurrent guidance
appears together. Sequenced guidance preserves the requested order while
leaving earlier steps visible. Bubbles stay for about 30 seconds unless you
dismiss them.

Hidden controls must be revealed first. For example, an agent opens
`main-row` before pointing at Files, or opens `toolbox` before pointing at Stop
turn. This prevents a tool from claiming success when the requested anchor is
not actually visible.

## Useful Requests

- “Show the main row, then point to Files without opening Files.”
- “Point out the node picker, profile picker, and prompt box.”
- “Open the toolbox and show me the Stop turn button.”
- “Show me Attach, the full composer button, and Send.”

Related: `use-console-main-row-and-prompt-controls.md` and
`use-the-status-bar-toolbox-and-stop-turns.md`.
