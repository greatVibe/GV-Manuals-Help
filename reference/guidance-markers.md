# Guidance Markers

Guidance markers give an AI agent a public, machine-readable bridge from a help
paragraph to a safe Konui bubble target. They are HTML comments, so they do not
interrupt the reader.

## Marker Shape

```html
&lt;!-- gv-guidance: {"id":"stop-turn","target":"stop-turn","message":"Stop the active turn here.","surface":"toolbox","action":"stop-turn","group":"stop-turn-tour","order":2,"mode":"sequence"} --&gt;
```

| Field | Required | Meaning |
| --- | --- | --- |
| `id` | Yes | Stable marker name within the repository. |
| `target` | Yes | One closed semantic Konui guidance target. |
| `message` | Yes | Plain bubble copy, from 1 to 180 characters. |
| `surface` | No | Surface the agent should reveal before showing the bubble. |
| `action` | No | Closed surface action used during reveal. |
| `group` | No | Stable name shared by related bubbles. |
| `order` | With `group` | One-based unique order inside the group. |
| `mode` | With `group` | `concurrent` or `sequence`. |

Unknown fields are not instructions. Agents must ignore a marker whose target
is not in the live tool schema.

## Agent Use

1. Read the smallest relevant guide.
2. Collect markers that match the requested task.
3. Pass a marker's optional surface/action as the guidance tool's reveal
   instruction so reveal and bubbles use one browser command.
4. Use the single guidance tool for one marker.
5. Use the guidance-group tool once for two to eight markers. Preserve group
   order and mode, and use one shared reveal when the markers agree.
6. Treat a verified guidance receipt as the complete response only when the
   user asked solely for guidance.

The browser shows one “Click to dismiss guidance” control for the presentation.
Clicking any ordinary console element also dismisses the guidance and continues
that click normally.

## Safety Boundary

Markers never contain CSS selectors, executable code, credentials, private
routes, or authorization claims. They provide context; the live tool schema,
authenticated browser, and closed target vocabulary remain authoritative.
