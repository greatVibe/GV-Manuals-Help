# Git And Repositories

Agents work with Git through greatVibe's Git tools, not raw shell commands.
The tools return structured results, use the credentials you saved, and
keep an audit trail.

## Repository Identity

- Repositories under the node's workspace folder are discovered
  automatically. A rescan runs at startup and periodically; ask "rescan
  repositories" after cloning by hand.
- A repository outside that folder can be registered by its path.
- Every repository has a `repo_id`: its folder name, for example `my-service`.
  Tool parameters use `snake_case` (`repo_id`, not `repoId`).

## Tool Map

| Task | Tool |
| --- | --- |
| List repos, find dirty ones | `git_list_repos` (filters: dirty, remote, branch) |
| Status of one repo | `git_repo_status` |
| Diff, staged or between refs | `git_diff` |
| History | `git_commit_log`, `git_show`, `git_blame` |
| Branches | `git_list_branches`, `git_checkout` (create with `create: true`), `git_branch_delete` |
| Stage and commit | `git_add`, `git_commit` |
| Sync | `git_fetch`, `git_pull`, `git_push` |
| All repos at once | `git_pull_all`, `git_push_all`, `git_merge_all` |
| Merge a branch and push | `git_merge_to_branch` |
| Undo | `git_revert`, `git_reset`, `git_stash` |
| Tags | `git_tag` |
| New repo on the node | `git_clone`, `git_register_repo` |
| Build repo context | `git_analyze` |

## Behaviour You Can Rely On

- **Pulls are fast-forward only by default.** A pull that would need a merge
  stops and reports a conflict instead of creating merge commits.
- **Bulk operations run every repository in parallel** and report per-repo
  results. Use them instead of looping: "push all repos", "pull all repos".
  Skip some with "skip `repo-a`".
- **Rejected pushes retry once.** If the remote moved, the push tool fetches,
  integrates the remote change, then pushes again.
- **Force push is off by default.** When a node allows it, it is always
  `--force-with-lease`, never a raw force. Agents ask you first.
- **`git_merge_to_branch`** checks out the target, pulls it, merges the source,
  pushes and returns to your branch. On conflict it aborts the merge and puts
  you back where you were.
- **Commit with nothing staged** returns "nothing to commit" rather than an
  empty commit.

## Credentials

- HTTPS remotes use a saved personal access token; SSH remotes use a saved SSH
  key. The provider is detected from the remote (GitHub, GitLab, Bitbucket).
- Name a specific credential when you have more than one.
- Temporary key files are removed after each operation.
- Set up private GitHub access with `../../how-to/add-github-credential.md` and
  `../../how-to/connect-a-private-github-repository.md`.

## Branching Patterns That Work Well

greatVibe does not impose a branching model. These patterns fit the turn loop:

| Pattern | How |
| --- | --- |
| Trunk with short branches | `feature/<topic>`, `fix/<topic>` per change; merge when the audit is clean |
| Release branch | Keep a long-lived release branch; use `git_merge_to_branch` from your work branch |
| Parallel agents | One Git worktree per concurrent task so agents never share a working tree |

Worktrees: create them with `git worktree add` on the node. The Git tools act
on the main checkout; run worktree commands through the node's command tool,
and keep worktrees outside the scanned workspace if you don't want them listed
as separate repositories.

## Procedure: Ship A Change

1. "Show the status of `my-service`." Confirm the branch and that only the
   expected files changed.
2. "Commit with a `Turn:` message." The agent commits code and ACE together.
3. Audit if the card says `audit_required`.
4. "Push `my-service`." Or "Merge `feature/pagination` into `main` and push."
5. Watch the CI/CD space. See `devops-cicd-and-iac.md`.

## Procedure: Recover From A Bad Commit

| Situation | Ask for |
| --- | --- |
| Not pushed, want to keep changes | "Soft reset `my-service` to the previous commit." |
| Already pushed | "Revert commit `<sha>` in `my-service` and push." |
| Messy working tree | "Stash the changes in `my-service`." |

Hard resets and force pushes discard work. Agents confirm with you before
either.

## Related

- `turn-lifecycle-and-sdlc.md`
- `devops-cicd-and-iac.md`
- `security-and-secrets.md`
