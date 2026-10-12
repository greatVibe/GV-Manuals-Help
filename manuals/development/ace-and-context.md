# Design-Led Coding With ACE And Context

greatVibe agents design before they code. Every code folder has a
`folder.ace` and every code file has a `{file}.ace` companion. The ACE note is
updated first, and code plus ACE are committed together.

For the idea behind ACE, read `../../concepts/what-is-ace.md`. This chapter is
the procedure.

## The Rule

| Action | Order |
| --- | --- |
| Read a file | `folder.ace` → `{file}.ace` → code |
| Edit a file | `folder.ace` → `{file}.ace` → update the ACE → edit the code |
| New file | `folder.ace` → write `{file}.ace` → write the code |
| Enter a folder | Read `folder.ace` first. Create it if missing |
| New folder | Write `folder.ace` first, then the files |
| Commit | Code and ACE together. Never one without the other |

Why the folder note first: it holds the module's purpose, dependencies and
design intent. A file note alone misses that context.

## ACE File Format

```yaml
file: orders.ts
consumers: [routes/orders.ts, jobs/reconcile.ts]
produces: [listOrders, createOrder, ORDER_NOT_FOUND]
---
# Purpose
Order queries and creation for the public API.

# Key Functions
- listOrders(filter, page) — paged, newest first.
- createOrder(input) — validates input, returns the created order.

# Dependencies
- db/pool.ts for connections.

# Gotchas
- Page size is capped at 100; callers must not assume more.

# Change History
- 2026-10-12: Added pagination to listOrders.
```

A `folder.ace` uses the same shape with `folder:` and `parent:` keys and
describes the module rather than one file.

## When To Update An ACE

| Change | Update the ACE? |
| --- | --- |
| New or changed exports, dependencies or gotchas | Yes |
| Breaking change | Yes, and say who must change |
| Internal refactor with the same behaviour | Change history line only |
| Tests | Yes: tests have their own `{file}.test.ts.ace` describing strategy and gaps |

## Tests Every Code Turn

Every turn that changes code checks that tests exist and runs them:

1. Read `{file}.test.ts.ace`, then the test file.
2. Run the relevant tests (`deno test`, `go test ./...`, `pytest`, …).
3. Fix failures before the commit. Never commit failing tests.
4. A new file gets tests in the same turn: imports work, exports exist, the
   happy path, and at least one error case.

Doc-only, config-only and read-only turns are exempt, as is a turn where you
say "skip tests".

## Coding Standards Agents Apply

| Area | Rule |
| --- | --- |
| Errors | Wrap with context. Don't log and return the same error. Export sentinel errors such as `NOT_FOUND`. Never panic in libraries. Clean up with `finally`/`defer` |
| Logging | Structured JSON, `snake_case` fields, never secrets or personal data |
| Security | No hardcoded secrets. Validate all input. Deny by default. Redact before storing |
| Quality | Clarity over cleverness. Fail fast. Functions under about 30 lines. Named constants, no magic numbers |

## gvContext: What Every Agent Starts With

Before a turn starts, greatVibe compiles **gvContext** into the agent's
instructions (`CLAUDE.md` for Claude, `AGENTS.md` for Codex). It is made of
layered assets:

| Layer | Contains |
| --- | --- |
| Kernel | The turn loop, ACE-first, testing per turn, output rules |
| Rules and SDK | Safety, secrets, brand voice, tool references |
| UI | Card styling and visual components |
| Repository | What this specific repository is and how it is built |

Each turn also receives a short turn context: the session, the turn number,
recent work, outstanding cards to tidy and reminder rules that grow stricter
as a session gets longer. You don't need to restate these rules in prompts.

### Give A Repository Its Own Context

When a repository is new to your node, ask:

> "Analyse `my-service` and build its context."

The agent runs a repository analysis (quick, standard or deep). The result
becomes a repository context asset, and greatVibe writes a `CLAUDE.md` into
the repository so later turns start with its architecture, commands and
conventions. Re-run the analysis with "force" after big structural changes.

The platform's own system rules are fixed per release. You cannot recompile
them from a turn; they refresh when the node updates.

## Procedure: Add ACE To An Existing Repository

1. "Create `folder.ace` files for every source folder in `my-service`, from the
   code. Don't change code."
2. Review the notes in the card; correct any purpose that is wrong.
3. "Add `.ace` companions for the files in `src/api/`." Work folder by folder.
4. From then on, ask for normal work; the agent keeps the notes current.

## Related

- `turn-lifecycle-and-sdlc.md`
- `../../concepts/what-is-ace.md`
- `../../concepts/what-is-gvcontext.md`
