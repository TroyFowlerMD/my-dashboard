# Project: TroyMD Personal Dashboard

## Identity
- GitHub is the source of truth for this project: TroyFowlerMD/my-dashboard.
- Notion is no longer the operating source of truth for this repo. Historical Notion content has been migrated into docs/ and the repo memory files.
- Durable documentation lives in docs/, AGENTS.md, TASKS.md, WORKLOG.md, and DECISIONS.md.
- Work in this repo in place. Do not move folders, clone over this repo, or rewrite history unless Dr. Fowler explicitly asks.
- Default branch: master.
- Live/public target: https://troyfowlermd.github.io/my-dashboard/.

## Project Overview
- Active public TroyMD routing dashboard.
- Routes users to maintained portfolio tools and sites, including clinical dashboards, SUD education, IVC tools, psychometrics, patient education, journal club resources, and non-clinical utilities.
- Distinct from the minimal troyfowlermd.github.io root repo.

## Project Structure
- index.html - single static public routing dashboard
- docs/ - durable dashboard documentation
- Other site repos - linked destinations, not vendored into this repo

## Documentation Map
- docs/troymd-personal-dashboard.md

## Required Startup Routine
1. Run git status --short --branch in the repo root and confirm the branch sync state with origin.
2. If there are staged, modified, or untracked files, stop and report exactly what is present before editing. Summarize whether the changes appear intentional, stale, unexpected, or in need of user review. Treat those changes as user or prior-Codex work; do not discard, overwrite, pull over, or auto-clean them without explicit approval.
3. If the working tree is clean and network access is available, run git pull --ff-only before starting work. Do not merge, rebase, or force update unless explicitly approved.
4. Read AGENTS.md, TASKS.md, WORKLOG.md, DECISIONS.md, and any task-relevant files in docs/.
5. Report the current branch, repo status, active task, blockers, and proposed next action.
6. Wait for approval before editing unless the user has already given explicit implementation approval.

## Required Shutdown Routine
1. Update WORKLOG.md with what changed, what remains, and any blockers.
2. Update TASKS.md if task status changed.
3. Update DECISIONS.md if an architectural, workflow, safety, or publishing decision was made.
4. Run the relevant tests/checks, or explain why they were not run.
5. Run git status --short --branch and summarize the exact staged, modified, and untracked files, including whether any remaining local changes appear intentional, stale, unexpected, or in need of user review.
6. By default, after approved work is complete and relevant checks have passed, commit and push automatically unless Dr. Fowler explicitly says not to push yet. Stop and ask before committing or pushing if the changes are unclear, checks fail, deployment/config/secrets are involved, or the repo appears production-sensitive.
7. End every shutdown with an explicit "Shutdown Receipt" section. Do not end with a generic "Done" only.
8. The Shutdown Receipt must visibly report:
   - WORKLOG.md: updated or not updated, with a one-line summary.
   - TASKS.md: updated or not updated, with any task status changes.
   - DECISIONS.md: updated or not updated, with a one-line summary.
   - Tests/checks: commands run, or why none were run.
   - Commit: hash and commit message if a commit was made, or "not committed" with the reason.
   - Push: pushed successfully, failed with reason, or not pushed with the reason.
   - Final git status: exact final status result.

## Worklog Entry Format
Append entries to WORKLOG.md using this shape:

    ### YYYY-MM-DD - [machine/profile] - [session summary]
    - Completed: ...
    - In progress: ...
    - Blockers/notes: ...

## Command Aliases
- If Dr. Fowler says `start`, `#start`, `start <repo>`, or `#start <repo>` while working in this repo, immediately run the Required Startup Routine. Do not simply acknowledge or repeat the command.
- If Dr. Fowler says `done`, `#done`, `finish`, `shutdown`, `done <repo>`, or `#done <repo>` while working in this repo, immediately run the Required Shutdown Routine. Do not simply acknowledge or repeat the command.
- In a general or multi-repo chat, if the command names this repo, switch context to this repo before running the routine. If the target repo is ambiguous, ask one concise clarifying question.
- Treat `#start` and `#done` as stronger visual command markers, but keep plain `start` and `done` supported.

## Cross-Machine Rules
- Never assume prior chat context is available. Reconstruct state from Git, TASKS.md, WORKLOG.md, DECISIONS.md, and docs/.
- Use git pull --ff-only only when the working tree is clean.
- Avoid destructive Git operations such as reset --hard, force pushes, history rewrites, or deleting untracked work unless explicitly approved.
- Keep generated context inside this repo's memory files and docs/ so another Windows account or computer can resume.
- Do not store secrets, tokens, credentials, private keys, or unnecessary sensitive data in repo docs.
- Preserve user or prior-Codex changes that are already in the working tree.

## Owner Communication
- The repo owner is new to Git, GitHub, GitHub Desktop, Codex, local-vs-remote repository concepts, commits, branches, remotes, pushes, pulls, and deployment workflows.
- When explaining repo work, include a little extra context by default: define the concept, explain why it matters, then give the specific instruction or recommendation.
- Use plain outcome language before technical terms. For example, say "this saves the change in local history" before or alongside "commit."
- Distinguish clearly between local files, local commits, pushed GitHub commits, pull requests, and live deployed website changes.
- Give step-by-step instructions with exact paths, button names, branch names, and GitHub URLs when the user is operating tools manually.
- Recommend the simplest safe option first, and name when an action is optional versus required.
- When a task reveals an opportunity to streamline Dr. Fowler's workflow, present it proactively with the expected benefit, any risk or cost, and the smallest safe next step. Keep workflow suggestions clearly separate from required task work.
- Avoid implying the live website changed unless changes were actually pushed and deployed.

## Project-Specific Rules
- Treat this repo as the real public routing hub.
- Keep troyfowlermd.github.io root-site work separate unless explicitly asked.
- Destination links should open in a new tab with target="_blank" and rel="noopener".
- In-page section jumps such as #clinical or #non-clinical can remain same-tab.
- Shareable destination pages should stand alone and should not link back to a private/main hub unless explicitly intended.
- Prefer simplified public routing cards over legacy split cards.
- Public pages should not mention repo migrations or internal consolidation history.

## Verification Guidance
- For link changes, verify target URLs and whether they should open in a new tab.
- For visible UI changes, inspect desktop and mobile layouts when feasible.
- If tests cannot run, record the reason in WORKLOG.md.

## Standing Agent Policy Bootstrap (Deduplicated)

> Single source of truth for standing AI-agent behavior in this repo. For project overview and link policy context, see README.md.

### Hard rules
- Never merge to the default branch without a green CI run on the working branch.
- Keep diffs minimal. No version bumps, no dependency upgrades, and no refactors outside the task scope unless explicitly requested.
- Use Conventional Commits (`feat:`, `fix:`, `chore:`, `docs:`, `refactor:`, `test:`, `ci:`).
- Match existing code style in touched files.
- If introducing Kotlin to a Java module, ensure `kotlinOptions { jvmTarget }` matches the existing Java `compileOptions` target.
- If a task requires touching a file listed under "Protected files," stop and ask for explicit confirmation before editing it.

### Protected files (do not modify unless explicitly requested)
- `index.html` (public routing entrypoint)
- `README.md` (public routing policy summary)
- `templates/codex/*.md` (shared cross-repo prompt templates)

### CI workflows
No CI workflows configured yet.

### Branch and PR conventions
- Base branch: `master`.
- Branch name prefix: `codex/`.
- Open as DRAFT PR until CI is green on the branch (or until reviewer sign-off when no CI exists).
- PR description must link to the relevant CI run when CI is present.
- One logical change per PR.
- PR structure: see `.github/PULL_REQUEST_TEMPLATE.md`.

### Toolchain
- Static HTML site repo; no explicit toolchain pins are currently defined in repository configs or workflows.

### Definition of done
A task is done only when all apply:
- [ ] CI workflow(s) pass green on the working branch (or CI is not configured)
- [ ] Diff touches only files required by the task
- [ ] No changes to protected files (or explicit confirmation was given)
- [ ] Commits follow Conventional Commits
- [ ] PR description summarizes what changed and links the CI run when applicable
