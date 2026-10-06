<!-- v1.0 | 1129 20261006 | Add conservative Ninja Dev continuity guidance. -->

# Repository Agent Instructions

Preserve the existing Astro site architecture, content intent, legal pages, and deployment configuration. Work on a focused branch and use a pull request; do not commit directly to `dev` or `main`. Never commit credentials, environment files, patient information, health data, or secret values. Do not change Netlify, DNS, analytics, or another external service without separate authorization.

## Ninja Dev Command Center Project State

- Read `docs/PROJECT_STATE.md` before resuming work.
- Reconcile recorded working, integration, and production branches and commits with GitHub evidence.
- Before handoff, update the exact stopping point, next concrete action, blockers, human decisions, verification, and evidence.
- Keep agent-reported completion separate from independently verified completion.
- The Command Center does not authorize deployment, external-infrastructure changes, or direct updates to `dev` or `main`.
