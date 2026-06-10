<!-- last-reviewed: 2026-05-18 -->
<!-- source: notion -->

# TroyMD Personal Dashboard

## Snapshot
Public-facing TroyMD hub page. The actual active dashboard lives in the `TroyFowlerMD/my-dashboard` repo and is published at `https://troyfowlermd.github.io/my-dashboard`. It serves as the main entry point to personal/non-clinical tools plus selected clinical portfolio links.

## Current Status
Local review confirmed that this page is the real active dashboard repo, while `troyfowlermd.github.io` itself is currently minimal and mainly functions as the root-site repo.

A portfolio-consolidation polish pass has now been committed and pushed:
- important dashboard links were repointed toward the new merged destination repos where applicable
- frequent schedule apps now appear first in a dedicated Schedules section
- non-clinical cards were cleaned up to keep general utility links separate from the schedule apps
- lower-use direct IVC, dev-template, and quick-access links were removed from the first-level public hub
- Perplexity branding/footer references were removed
- the Phenobarbital for AWS card now points to `sud-education-hub/alcohol-benzodiazepines/phenobarbital-aws.html`

GitHub now matches the intended routing update for this dashboard repo.

Schedule-app routing truth now lives in `TroyFowlerMD/non-clinical` under `docs/schedule-app-canonical-routes.md`. This dashboard should mirror that registry for `JFK Psych Schedule`, `JFK Med Staff Schedule`, and `Psych Scheduler Command Center` instead of maintaining an independent URL list.

## Architecture Map
- Repo: `TroyFowlerMD/my-dashboard`
- Live URL: `https://troyfowlermd.github.io/my-dashboard`
- Stack: single static `index.html` dashboard page on GitHub Pages
- Role: portfolio routing page, not a backend app

## Relationship To Consolidation
This page is one of the key public routing layers for the new destination-repo structure.

Destination targets now wired into the pushed dashboard include:
- `sud-education-hub`
- `clinical-dashboards`
- `psychometrics-hub`

`IVC-Suite` remains available through the JFK clinical dashboard rather than as a first-level hub card.

## 2026-05-15 Consolidation Addendum
- The dashboard `index.html` routing update has now been committed and pushed in the intended repo sequence.
- The Phenobarbital for AWS card now points to the consolidated `sud-education-hub/alcohol-benzodiazepines/phenobarbital-aws.html` path instead of the old standalone repo path.
- A final legacy-link sweep did not find any remaining old public repo-path links inside the dashboard that would block the consolidation sync.
- This repo was committed after the destination repos and now reflects the pushed consolidation state.

## Next Steps
- manually retest the public dashboard links now that the consolidated repos are public and GitHub Pages is enabled
- decide whether any profile pinning or additional About-panel polish is needed
- keep using this page as the public-facing routing layer for the consolidated portfolio

## 2026-05-15 Pages Visibility Note
An authenticated GitHub API probe showed the current plan does not support GitHub Pages for private consolidated repos. After dashboard link review, the consolidated repos needed by the public dashboard were made public and GitHub Pages was enabled. The previously broken public dashboard targets now return `200`.

## 2026-05-15 Link Sweep
- Full dashboard link sweep found one remaining broken link: `moud-patient-education`, which does not exist as a GitHub repo.
- `my-dashboard/index.html` was patched so the MOUD Patient Education card and quick link now point to the working `sud-patient-education` site.
- The fix was committed and pushed to `my-dashboard`.
- The live dashboard HTML no longer contains the old `moud-patient-education` URL.
- Final sweep of dashboard links returned no remaining HTTP failures.

## 2026-05-16 Mobile And Link Policy Update
- Dashboard destination links should open in a new tab by default with `target="_blank"` and `rel="noopener"` unless a future change explicitly calls for same-tab behavior. In-page section jumps can remain same-tab.
- Local dashboard updates improved phone layout by keeping cards in a vertical single-column flow, removing horizontal navigation overflow, adding `A-` / `A` / `A+` text-size controls, and making section labels more visible in dark mode.
- A repo README now documents the default new-tab link policy for future dashboard additions.

## 2026-05-23 Experimental Scheduler Link
- Added a Non-clinical dashboard card for the experimental Psych Scheduler Command Center at `https://troyfowlermd.github.io/non-clinical/psych-scheduler-experimental.html`.
- The card preserves destination-link behavior with `target="_blank"` and `rel="noopener"`.

## 2026-06-04 Schedule-First Dashboard Update
- Added a first `Schedules` section with `JFK Psych Schedule`, `JFK Med Staff Schedule`, and `Psych Scheduler Command Center`.
- Removed the large hero copy, hero destination buttons, and top-bar section navigation to reduce the height of the dashboard header.
- Removed duplicate schedule cards from the `Non-clinical` section while keeping general non-clinical utilities there.

## 2026-06-04 Hub Simplification Update
- Removed the direct `IVC Suite` card from `Clinical Tools`; the IVC tools remain reachable through `JFK Clinical Dashboard`.
- Removed the `Dev & Templates` section.
- Removed the `Quick Access` section.
