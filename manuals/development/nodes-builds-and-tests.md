# Nodes, Builds And Tests

A node is the machine where an agent works. Build and test where the
repository lives. Your mesh is a workgroup: other nodes can build, test and
run whole turns for you.

## Runtimes

Each node runs the greatVibe agent service plus the Claude and Codex
command-line agents. Language runtimes depend on the node:

- Runtimes and versions differ by node. Ask "which runtimes and versions are
  installed on this node?" before you rely on one, and install what a project
  needs as part of its setup.
- On your own machine, the runtimes are whatever you have installed.
- The IDE's language features use `gopls` for Go and
  `typescript-language-server` for TypeScript when those are on the node.

## Test Discovery

The IDE and agents detect a repository's test command from its files:

| File in the repository | Test command |
| --- | --- |
| `deno.json` / `deno.jsonc` | `deno task test` if a `test` task exists, else `deno test -A` |
| `go.mod` | `go test ./...` |
| `pyproject.toml` / `pytest.ini` | `pytest -q` |
| `package.json` with a `test` script | `bun test`, `pnpm test`, `yarn test` or `npm test`, chosen by lockfile |
| `Cargo.toml` | `cargo test` |

Agent IQ's Tests space recognises runs of these commands and others such as
`deno check`/`lint`, `npm run typecheck`, `playwright test` and `make test`.
A test shows passed or failed only from a real result, never from a plan.

### Declare A Test Plan

For code changes, agents publish a test plan in Agent IQ: strategy
(targeted, full-stack, risk-based, smoke), scope, and rows by level (unit,
integration, contract, system, e2e, static, manual, performance) and stage
(this turn, after turn, pre-ship, post-deploy). Rows turn green or red only
when a matching run is observed. The ship gate counts what remains.

## Long Builds And Waits

A turn that starts a long build, upload or background process registers it
as a **tracked operation** so the dashboard shows real progress:

| Kind | Example |
| --- | --- |
| `build` | A release build in the background |
| `process` | A long-running script |
| `copy`, `download`, `s3_upload`, `api_transfer` | Moving large files |
| `sleep` | A deliberate wait, such as waiting for a deployment |

How it is measured:

- **log** probe: parses the last progress line of a log (`aws s3`, `rsync`,
  `curl` or generic).
- **file** probe: size of the destination file or folder.
- **pid** probe: is the process alive; reads its exit code from a file.
- **transfer** probe: mirrors a greatVibe file transfer.

Sampling runs every 2 seconds. With no progress for 120 seconds (adjustable)
the operation shows **stalled**. Success needs terminal evidence, such as an
exit code or the expected size, never elapsed time.

**Procedure:** ask "Build the release in the background and track it." The
agent runs the build with its output captured to a log and an exit-code file,
then registers the operation. Watch the Builds or Sleeping space.

## Use Other Nodes

| Goal | How agents do it |
| --- | --- |
| See all your nodes | List nodes across your meshes |
| Find which node has a repo | List repositories on each node |
| Run a command there | `mesh_<node>_exec_run` with a working directory and timeout (30 s default, 300 s maximum) |
| Track a long job there | `mesh_<node>_op_track_start` |
| Hand over a whole task | Start a visible turn on that node for you, then check its result |
| Copy a file between nodes | File transfer, chunked with SHA-256 and per-chunk checksums |

Each node limits which commands it will run. Ask "show this node's command
allowlist" when a command is refused.

**Procedure: test on the node that has the repo.**

1. "Which node has `my-service`?"
2. "Run its tests on that node and show the result."
3. For a long suite: "Run it in the background there and track it."

**Procedure: split independent work.** "Update the client SDK on
`node_example` while you update the server here." The agent starts a visible
turn on the other node; you see it run and it ends with its own card.

## The IDE

The v2 IDE gives you and the agent the same workspace: files, buffers,
terminals, tests, debugger and Git status. See
`../../how-to/use-and-watch-the-v2-ide.md`.

Technical points for agents:

- Sessions open **read-only**. Saving files or running terminal commands
  needs a session opened with workspace write.
- Only one client controls the view at a time through a short controller lease
  (30 seconds, renewed by heartbeat). Others watch.
- Tests: discover presets, then run one by id.
- Debugging uses the Debug Adapter Protocol. You supply the adapter
  executable (for example `dlv dap` for Go). Breakpoints can be set before the
  program starts.

## Related

- `devops-cicd-and-iac.md`
- `../../concepts/what-is-a-node.md`
- `../../how-to/view-turns-across-nodes.md`
- `../../how-to/work-with-files.md`
