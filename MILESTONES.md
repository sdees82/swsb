# Milestones and responsibilities

Revision: editorial-2026-10-17-r3. Read BEFORE-YOU-BEGIN.md, then follow the complete tasks below. The reader maintains Markdown and accepts each result. The agent creates all application source, configuration, package files and tests. No implementation checkpoint is supplied.

| Stage | Existing state | Task and next gate |
| --- | --- | --- |
| Read-only | Reviewed Markdown; no app | Confirm actual revision/assets, PV-01–05 and local boundaries |
| Practice preview, Chapter 3 | Read-only retrieval accepted | teaching/tasks/00-preview.md; accept loading, camera and failure paths |
| Spec and plan, Chapter 4 | Preview accepted | Review spec; resolve defects; create plan; review plan; reader accepts |
| Loop 1, Chapter 5 | No Player helpers/tests yet | teaching/tasks/01-state.md; create normalization/state, Jest and verify |
| Loop 2 | State accepted | teaching/tasks/02-controls.md; controls/camera, direct interaction |
| Loop 3 | Controls accepted | teaching/tasks/03-inscriptions.md; actual Player inscriptions and fit |
| Loop 4 | Player accepted | teaching/tasks/04-logo.md; top-only image handling, recovery/races/resize |
| Loop 5 | Logo accepted | teaching/tasks/05-materials.md; four independent material regions |
| Evidence and learning | Five loops accepted | Authority map, evidence matrix, route cases, autonomy and correction records |
| Capstone, Chapter 11 | Current accepted feature evidence | teaching/tasks/06-handoff.md; one local revision, report and next action |

The core areas are Player, Top and Colors. The team shoulder is authored metal. Ring selection, editable Team fields, a Team logo, other rings, new fonts/assets, persistence, payment, manufacturing output and publication are outside this walkthrough. Technical registry ID classic and asset filenames remain unchanged.

Every task has Goal, Start state, Files and inputs, Exact request, Expected result, Checks to run, What to inspect yourself, Stop conditions, Evidence to save and State required for the next step. A required failed or unrun check blocks that milestone; later prose is not evidence that it passed. If browser tools are unavailable, the reader performs the exact interactions and records the environment and operator.

The agent creates dev/lint/type-check/build in the practice preview. Loop 1 adds the real test suite and combined verify script defined in SETUP.md. No validate:assets or test:e2e command is assumed. A future task may create an asset validator or browser suite, but it must establish its implementation before reporting a run.
