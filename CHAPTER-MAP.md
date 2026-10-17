# Chapter and feature map

The companion ships only Markdown and assets. Readers author Markdown, direct the agent and review its results; the agent creates the implementation through these milestones; no app, source code, executable scripts, package files or decoder implementation is bundled.

| Chapter | Companion material | Expected agent outputs / reader review |
| --- | --- | --- |
| 2 | starter/AGENTS.md; SETUP.md | Empty working folder; fixed dependencies and configuration after setup is authorized |
| 3 | MODEL-INSPECTION.md; teaching/docs/specs/first-preview.md | /builder, loader, scene, lighting, camera, loading/failure behavior |
| 3 | teaching/rules; teaching/skills | Scoped guidance and discovered procedures, introduced as relevant code appears |
| 4–5 | teaching/docs/specs/player-personalization.md | TEXT_FIELDS, sanitizeText, store, Player controls, surface text and focused tests |
| Later customization | teaching/docs/specs/ring-logo.md | File validation, decoding/resizing, logo state and scene placement |
| Later customization | teaching/docs/specs/material-customization.md | Independent ring/lettering metal and top/side stone controls |
| 5 | teaching/templates; teaching/examples/player-personalization-progress.md | Evidence-backed progress and next action |
| 6 | Task and integration contract templates | Bounded authority for the current local feature |
| 7 | teaching/docs/VERIFICATION.md; teaching/docs/verification/player-personalization.md | Real test/browser evidence and the reusable verification play |
| 8–10 | teaching/skills/review-customization-spec/evals | Local review comparisons with separately recorded invocation and answer quality |
| 11 | Completion, autonomy and correction templates | Concrete feature handoff and remaining checks |

Read [MILESTONES.md](MILESTONES.md) for starting-file availability and the expected agent output paths for each stage. Read [SETUP.md](SETUP.md) for exact installed-version choices and dependency setup. PV-01–05, AC-01–12 / BR-01–06, LG-01–05 and MT-01–05 remain the stable feature identifiers.

The model is starter/public/models/championship-ring.glb, with matching starter/model-metadata JSON. Optional GLB inspection is described in optional/model-source/README.md; the private Blender master is not included. No textures are missing from the GLB; its material definitions are embedded. The required Draco runtime is obtained through dependencies as setup describes. Companion: https://github.com/sdees82/swsb. Read VERSION.md and MANIFEST.md for the package revision and inventory.
