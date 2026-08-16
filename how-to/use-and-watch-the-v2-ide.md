# Use And Watch The V2 IDE

Use the v2 IDE when you want to see the files, changes, tests, and task output
an AI agent is working with on the selected GreatVibe node.

## Open The IDE

1. Select the node you want to work on.
2. Open the IDE from the dashboard workspace.
3. Choose a repository.
4. Open a file from Explorer, Search, or Changes.

The selected node is an important safety boundary. Work from another node must
not take over the IDE you are currently watching.

## Watch An Agent Work

Ask the agent to keep its work visible in the IDE. The agent can open the
repository, reveal folders and files, select content, and use the enabled IDE
commands. Its focused activity appears in the IDE while the turn is running.

Useful requests include:

- “Open the file you are changing in the IDE.”
- “Keep the terminal visible while you run the tests.”
- “Show the Changes panel after the edit.”
- “Select the code related to the bug.”

If the dashboard was closed or disconnected when the command was sent, reopen
it and ask the agent to repeat the visible action.

## Main IDE Controls

- **Explorer** browses folders and files in the selected repository.
- **Search** finds text across the repository.
- **Changes** compares current work with the Git baseline.
- **Problems** shows available diagnostics.
- **Terminal** shows approved task and test output.
- **Palette** searches enabled IDE commands.
- **IDE full screen** expands the complete IDE while keeping the prompt area.
- **Editor focus** emphasizes the active editor without changing Explorer state.

Disabled or review-only actions cannot be triggered remotely.

## Watch From More Than One Browser

Two browsers signed into the same authorized account can follow the same
account-scoped IDE session, subject to the current controller handoff rules.
Only one active controller should edit at a time.

Different user accounts do not automatically share private IDE state. This is
intentional: files, selections, and work in progress may be sensitive. A future
cross-account observer mode must use an explicit, audited, read-only sharing
permission. Do not share credentials or reuse another person's login to work
around this boundary.

## If The IDE Is Not Following The Agent

Check these in order:

1. Confirm the intended node is still selected.
2. Confirm the dashboard tab is visible and connected.
3. Confirm the correct repository is open.
4. Ask the agent to repeat the file or command action.
5. If the problem continues, capture the turn and node details for review.

## Related Guides

- `work-with-files.md`
- `review-ai-work.md`
- `understand-the-status-bar.md`
