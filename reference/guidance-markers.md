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

Targets have two safe forms:

- Curated names such as `toolbox`, `force-idle`, or `files-upload` are preferred
  when a common human phrase has one clear meaning.
- Exact names use `control:<key>`, for example
  `control:dash-console-force-idle`. Konui creates these keys for every live
  button, input, link, menu item, tab, selector, and editable control. They are
  bounded identifiers, not CSS selectors.

Unknown fields are not instructions. Agents must ignore a marker whose target
is not in the live tool schema.

## Agent Use

1. Call `konui_guidance_catalog` when the requested control is not a curated
   target or the wording could match more than one control. The result comes
   from the user's live visible dashboard and includes exact target, label,
   short help, element kind, visibility, and disabled state.
2. Read the smallest relevant guide.
3. Collect markers that match the requested task.
4. Pass a marker's optional surface/action as the guidance tool's reveal
   instruction so reveal and bubbles use one browser command.
5. Use the single guidance tool for one marker.
6. Use the guidance-group tool once for two to eight markers. Preserve group
   order and mode. Concurrent groups must share one visible layer and may use
   one shared reveal.
7. For a sequence that crosses layers, preserve each marker's `surface` and
   `action` as that item's reveal instruction. Konui reveals and confirms each
   layer only when the user advances to that step.
8. Treat a verified guidance receipt as the complete response only when the
   user asked solely for guidance.

## Response Priority

For dashboard usability prompts, agents choose the narrowest complete response
in this order:

1. **Show how.** If the user asks how to find, open, choose, enter, or use a
   dashboard control, discover the live target and show one guidance bubble or
   a two-to-eight-step guidance group. A receipt must confirm both visibility
   and focus before this becomes the entire response.
2. **Capture an issue.** If the user reports broken, missing, unsafe, or
   persistently incorrect behavior that needs investigation or a fix, use the
   support-request workflow. Do not turn an ordinary how-to question into a
   support issue.
3. **Use a durable turn.** Use a normal gvturn for implementation, audits,
   mixed work, decisions, or any request that guidance or support cannot fully
   satisfy.

If catalogue discovery or bubble delivery fails, fall back to a durable turn
with a useful explanation. Never claim guidance was shown without a verified
browser receipt.

The browser shows one “Click to dismiss guidance” control for the presentation.
Clicking any ordinary console element also dismisses the guidance and continues
that click normally.

## Safety Boundary

Markers never contain CSS selectors, executable code, credentials, private
routes, or authorization claims. Exact control keys are resolved by attribute
equality inside the authenticated browser; selector syntax is rejected. The
live tool schema and receipt-backed browser catalogue remain authoritative.
Route-changing surfaces such as Account Admin are standalone navigation only;
they are not valid same-page guidance reveal instructions.
