# Stop Watching, Start Building: reader companion

The companion provides Markdown guidance, a 3D ring model and supporting assets for the book's Ring Builder. You author Markdown guidance, direct the agent and review the results. The agent scaffolds the project and writes all application code, configuration, package files and tests; you never need to hand-code TSX or paste an implementation. No app implementation, executable scripts, package manifest, lockfile, installed dependency or Draco decoder implementation is supplied.

Start with [How to use the book and companion](BEFORE-YOU-BEGIN.md) and confirm [the revision](VERSION.md), then read [SETUP.md](SETUP.md), then follow [MILESTONES.md](MILESTONES.md). The milestones distinguish the Markdown you author from the implementation the agent produces, and state when controls, state, rendering helpers and tests become available. The fixed stack and source paths come from the inspected Ring Builder project.

## Files by activity

| Activity | Files |
| --- | --- |
| Chapter 2: understand this project | [Setup](SETUP.md), [starting briefing](starter/AGENTS.md) |
| Chapter 3: MASCOT and model inspection | [Project guidance example](teaching/project-instructions/AGENTS.md), [model inspection](MODEL-INSPECTION.md), [first-preview spec](teaching/docs/specs/first-preview.md) |
| Chapter 3: scoped context and procedures | [Rules](teaching/rules), [skills index](teaching/skills/README.md) |
| Chapter 4: feature contracts | [Player](teaching/docs/specs/player-personalization.md), [logo](teaching/docs/specs/ring-logo.md), [materials](teaching/docs/specs/material-customization.md) |
| Chapter 5: plan and resume | [Plan review](teaching/templates/plan-review.md), [task contract](teaching/templates/task-contract.md), [Markdown handoff example](teaching/examples/player-personalization-progress.md) |
| Chapter 6: authority and checkpoints | [Task contract](teaching/templates/task-contract.md), [integration contract](teaching/templates/integration-contract.md) |
| Chapter 7: actual evidence | [Verification guide](teaching/docs/VERIFICATION.md), [player recipe](teaching/docs/verification/player-personalization.md), [logo fixtures](fixtures/logo) |
| Chapters 8–11: routing and corrections | [Autonomy assessment](teaching/templates/autonomy-assessment.md), [correction ledger](teaching/templates/correction-ledger.md), [local Chapter 10 review cases](teaching/skills/review-customization-spec/evals) |
| Optional Blender inspection | [Model inspection](optional/model-source/README.md) |

The model file is `championship-ring.glb`. The GLB embeds its materials and has no external texture images. The supplied font files and model metadata are data assets, not an application implementation. The compressed GLB needs the decoder dependency described in setup.

[CHAPTER-MAP.md](CHAPTER-MAP.md) gives manuscript-facing paths. [MANIFEST.md](MANIFEST.md) inventories final files and hashes. [Provenance](provenance/README.md) and [validation evidence](validation/README.md) describe what was inspected locally. The temporary app used for validation is outside this companion.

Attribution, rights confirmation and remaining third-party release items are recorded in [provenance](provenance/README.md) and [the release checklist](RELEASE-CHECKLIST.md). No specific public reuse license is assigned by this companion; preserve the included font notices.

The complete copy-ready assignments are in [teaching/tasks](teaching/tasks/README.md). The core has Player, Top and Colors; editable Team fields, a Team logo and ring selection are excluded. [SOURCES.md](SOURCES.md) records current tool documentation.

## Companion, updates and corrections

https://github.com/sdees82/swsb is the companion address. Read VERSION.md and compare MANIFEST.md before setup. When reporting a problem, include the companion revision, chapter/task, requirement ID, environment, exact action and observed result. Report corrections through https://github.com/sdees82/swsb/issues.
