# Decisions

This file records durable architectural, workflow, safety, and publishing decisions for TroyMD Personal Dashboard. Each entry should include Context, Decision, Rationale, and Consequences.

---

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
