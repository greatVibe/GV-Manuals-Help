# Read Architecture In Agent IQ

Architecture shows the components the agent is working with and how they depend
on one another. Ask: **“Show the architecture for this change, highlight the
focus, and explain any concerns.”** Then open **Architecture** in Agent IQ.

## Read The Colours

**Green means focus.** Brighter green marks the main subject of the turn.
Lighter attention uses a quieter green; related components stay neutral.
Green does not mean a test passed or a service is healthy.

**Red means a stated concern.** The agent can distinguish a concern, a problem
or a critical concern. Each needs a note explaining what needs attention. A
component may be important to the task and also have a concern.

The map is the agent's analysis. Check the cited evidence before treating a
concern as a confirmed defect. Tests and other observed results remain in their
own Agent IQ spaces.

## Follow A Connection

An arrow points from a component to something it depends on. For example, a
project view may depend on a service, which depends on a data store.

Each card has a symbol for its kind, such as an interface window, a data store
or a group of machines. Named parts appear inside the card when the agent has
declared them. **Depends on** counts its direct dependencies; **Used by** counts
the other components that directly use it. Wider cards name those connections.

Tap or click a component to open its details. You can also focus it with Tab and
press Enter or Space. Details can show:

- Why the component matters and any concern.
- The parts inside it that the agent is considering.
- Its dependencies and the other components that depend on it.
- Evidence references the agent supplied.

**Dependency reach** includes indirect dependants in the declared map. It does
not prove that all those components are affected by a runtime fault.

The details panel opens within the Architecture view and scrolls when needed.
Use **Close** or Escape to return to the diagram. Evidence references are text
for inspection, not automatically opened pages.
Updates within the same turn keep your reading position and focused control.

## Choose A View

Use the layout menu to arrange the same declared components:

| View | Use it for |
| --- | --- |
| Focus map | See the current focus and the components around it |
| Dependency flow | Trace dependencies through the system |
| Component layers | Group interface, service, data, machine, agent and test components |

Changing the view keeps your selected component. Your mode and selection belong
to the current turn. A new turn starts with its own map.

On a phone or a short pane, scroll inside the diagram to reach the remaining
components. You can use the normal Agent IQ fullscreen gesture for more reading
room. Reduced-motion settings keep the diagram static.

## Know What Is Missing

The agent declares a bounded map of up to 12 components. It may show only the
part of a system relevant to the task. Missing components and connections are
not evidence that they do not exist.

If the space says no components were declared, ask the agent to add a map. If a
label or concern is unclear, ask for a note and evidence. A map can remain
unchanged while work continues; it does not animate to imply activity.

## Related

- [Review AI work](review-ai-work.md)
- [Build Agent IQ layouts](build-agent-iq-metal-layouts.md)
- [Steer a running turn](steer-a-running-turn.md)
