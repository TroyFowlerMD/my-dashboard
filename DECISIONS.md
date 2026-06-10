# Decisions

This file records durable architectural, workflow, safety, and publishing decisions for TroyMD Personal Dashboard. Each entry should include Context, Decision, Rationale, and Consequences.

---

### 2026-06-09 - Follow The Canonical Schedule Route Registry For Dashboard Schedule Cards
Context: The schedule apps now span GitHub Pages and Vercel, and the live dashboard already depends on `non-clinical` for those destinations.
Decision: Treat `C:\Users\troyf\Documents\Codex\Projects\non-clinical\docs\schedule-app-canonical-routes.md` as the authoritative source for schedule-app destinations. Update dashboard schedule cards only in the same change set that updates the registry and any legacy-forwarder behavior.
Rationale: This keeps the dashboard from drifting away from the actual current schedule-app URLs or accidentally reviving retired paths.
Consequences: Future schedule-card edits in this repo should start with a registry check and should not invent independent schedule-route truth here.

### 2026-05-15 - Treat my-dashboard As The Active Public Hub
Context: `troyfowlermd.github.io` exists as the root-site repo, but the active dashboard lives elsewhere.
Decision: Use `my-dashboard` as the real public routing hub for maintained TroyMD portfolio links.
Rationale: Local review confirmed this repo is the actual dashboard users navigate from.
Consequences: Public routing changes should land here first unless the user explicitly asks to change the root-site repo.

### 2026-05-15 - Make Consolidated Repos Public For GitHub Pages
Context: A GitHub API probe showed the current plan did not support GitHub Pages for private consolidated repos.
Decision: Keep the consolidated repos needed by the public dashboard public with GitHub Pages enabled.
Rationale: The dashboard depends on live public Pages targets.
Consequences: Dashboard link checks must verify live public URLs, not only local paths.

### 2026-05-16 - Destination Links Open In New Tabs
Context: The dashboard routes users away to separate maintained tools and sites.
Decision: Destination links should open in a new tab with `target="_blank"` and `rel="noopener"`, while same-page section jumps can remain same-tab.
Rationale: Users keep the hub available while exploring separate tools.
Consequences: Future card additions should apply this policy by default.

### 2026-05-15 - Use Simplified Public Routing Cards
Context: Dashboard routing had legacy split cards and stale destinations.
Decision: Prefer simplified public routing cards, including one general Patient Education card and one Psychometrics Hub card.
Rationale: The dashboard should help users choose working destinations quickly rather than exposing consolidation history.
Consequences: Avoid reintroducing old repo-path cards or public migration language.

### 2026-05-22 - Explain Repo Work With Beginner Context
Context: Dr. Fowler is new to Git, GitHub, GitHub Desktop, Codex, and local-vs-remote repository workflows.
Decision: Codex should explain repo work with extra beginner-friendly context by default, including definitions, why each step matters, exact local paths/button names when useful, and a clear distinction between local files, local commits, pushed GitHub commits, pull requests, and deployed site changes.
Rationale: Better context reduces accidental duplicate clones, OneDrive/Git confusion, and uncertainty about whether work is local, synced, or live.
Consequences: Future repo instructions and shutdown summaries should favor plain outcome language and step-by-step guidance over unexplained Git shorthand.

### 2026-05-22 - Surface Workflow Streamlining Opportunities
Context: Dr. Fowler wants Codex to notice chances to make his coding, GitHub, GitHub Desktop, deployment, and cross-machine workflows smoother.
Decision: When Codex sees a practical workflow improvement, it should present the opportunity proactively with the expected benefit, any risk or cost, and the smallest safe next step.
Rationale: Small workflow improvements compound, especially while Dr. Fowler is learning Git and using Codex across multiple machines.
Consequences: Future sessions should separate optional workflow suggestions from required task work so recommendations help without derailing the current task.

### 2026-06-04 - Treat Schedule Apps As A Top Dashboard Category
Context: Dr. Fowler uses the schedule apps frequently and wanted them visible before the rest of the portfolio routing cards.
Decision: Keep a first-page `Schedules` section for `JFK Psych Schedule`, `JFK Med Staff Schedule`, and the experimental `Psych Scheduler Command Center`.
Rationale: The main hub should prioritize the highest-frequency workflow before broader clinical, education, journal, and utility destinations.
Consequences: Future schedule-related destination cards should be reviewed for placement in `Schedules` before adding them to `Non-clinical`.

### 2026-06-04 - Keep Lower-Use Utility Links Off The Main Hub
Context: Dr. Fowler rarely uses the direct `IVC Suite` route and can access it through the `JFK Clinical Dashboard`; he also no longer needs `Dev & Templates` or `Quick Access` on the public hub.
Decision: Remove those direct sections and links from the main dashboard.
Rationale: The hub should stay focused on destinations Dr. Fowler actually uses from the first-level page.
Consequences: Future hub additions should avoid restoring direct IVC, dev-template, or quick-access link clusters unless Dr. Fowler explicitly asks for them.
