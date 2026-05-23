# Worklog

This file records completed Codex work sessions for TroyMD Personal Dashboard. Append new entries during the shutdown routine so future sessions can resume without prior chat context.

---

### 2026-05-23 - Codex desktop - Experimental Psych Scheduler hub card
- Completed: Added a Non-clinical dashboard card linking to the experimental Psych Scheduler Command Center at `https://troyfowlermd.github.io/non-clinical/psych-scheduler-experimental.html`.
- Completed: Preserved destination-link behavior with `target="_blank"` and `rel="noopener"`.
- In progress: Existing public-dashboard routing and future manual link retest tasks remain open.
- Blockers/notes: Pre-edit `git pull --ff-only` was skipped because escalation was not approved; local branch was clean and reported `master...origin/master` before editing.

### 2026-05-19 - Codex desktop - Power of Attorney guide routing card
- Completed: Added a Non-clinical dashboard card linking to the new Power of Attorney guide at `https://troyfowlermd.github.io/non-clinical/personal/poa-guide.html`.
- Completed: Preserved destination-link behavior with `target="_blank"` and `rel="noopener"`.
- In progress: Existing public-dashboard routing and future manual link retest tasks remain open.
- Blockers/notes: Publish verification should confirm the dashboard and new guide URLs after both repos are pushed.

## Entry Format

    ### YYYY-MM-DD - [machine/profile] - [session summary]
    - Completed: ...
    - In progress: ...
    - Blockers/notes: ...

### 2026-05-19 - Codex desktop - Repository maintenance sweep
- Completed: Fast-forward pulled `origin/master` and confirmed the working tree was clean before maintenance logging.
- Completed: Smoke-checked the public TroyMD hub live URL; it returned HTTP 200 with expected TroyMD/dashboard routing text.
- Completed: Ran a local relative href/src scan with no missing local targets found for this repo.
- In progress: Existing public-dashboard retest, card-organization review, profile pinning/About polish, and cross-portfolio docs placement tasks remain open in TASKS.md.
- Blockers/notes: No app code changed; TASKS.md and DECISIONS.md were not changed.

### 2026-05-22 - Codex desktop - Beginner-friendly repo communication preference
- Completed: Added `AGENTS.md` Owner Communication guidance so future Codex sessions explain Git, GitHub, GitHub Desktop, Codex workspace behavior, local-vs-remote state, commits, pushes, pulls, branches, and deployments with extra beginner-friendly context.
- Completed: Documented that explanations should define concepts, distinguish local files from pushed/deployed changes, and use exact paths/button names when Dr. Fowler is operating tools manually.
- In progress: Existing dashboard tasks remain unchanged.
- Blockers/notes: Instruction-only change; no app runtime code changed.

### 2026-05-22 - Codex desktop - Workflow streamlining preference
- Completed: Updated repo instructions so future Codex sessions proactively surface opportunities to streamline Dr. Fowler's workflow, including expected benefit, risk/cost, and smallest safe next step.
- In progress: Existing dashboard tasks remain unchanged.
- Blockers/notes: Instruction-only change; no app runtime code changed.

