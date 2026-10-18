# Ring Builder reader project

Audience: the implementation agent. The reader authors Markdown guidance, directs bounded tasks and reviews your results. You scaffold the project and create or edit application code, configuration, package files and tests. Application paths are expected outputs or inspection points; never ask the reader to create TSX manually or paste implementation code.

Paths are relative to the working-project root, my-ring-builder. The pinned companion is the sibling ../swsb directory.

## Mission
Build the book's browser Ring Builder: inspect the ring, create its preview, then add player personalization, logo handling and independent material controls. The complete product lets someone personalize a championship ring and inspect its design in 3D. Start with one ring.

## Architecture
Create app/builder/page.tsx for /builder, components/ui for controls, components/canvas for the scene, lib/store.ts for live design state and lib/rings for the ring's definition. lib/customization.ts will define fields and normalization. These are implementation targets; this companion supplies Markdown and assets, not those source files.

The supplied public/models/championship-ring.glb requires a Draco decoder. Install it through the project dependencies and serve its decoder files locally as ../swsb/SETUP.md describes; no decoder implementation is bundled here. Keep the four supplied model JSON assets together. Inspect the actual nodes/materials and record the authored metal, surface mappings and runtime additions before coding.

## Stack
Use Next.js 16.2.9, React/React DOM 19.2.4, TypeScript 5.9.3, React Three Fiber 9.6.1, drei 10.7.7, three.js 0.184.0, Zustand 5.0.14, Tailwind 4.3.1 and npm. Next.js requires Node >=20.9.0. You, the agent, create the package manifest, configuration and lockfile during authorized implementation. Use these concrete project choices rather than selecting another framework.

## Commands
After local preview setup is authorized, establish dev, lint, type-check and build as ../swsb/SETUP.md describes. Loop 1 adds the first real Jest suite, test and verify. Run them from the reader app's root after the relevant implementation exists. There is no supplied package.json, lockfile, application or passing feature-test suite. Record actual results. The target local route is http://localhost:3000/builder.

## Operational Overview
Follow ../swsb/MILESTONES.md: inspect the ring; build its preview; create player text/state/controls/renderer/tests; add logos; add independent material controls; preserve verification evidence. Use the matching task under ../swsb/teaching/tasks/ and the active contract under docs/specs/. Use the supplied Markdown review/investigation procedures. Preserve unrelated work. Bring conflicting requirements or dependency, asset and character-policy changes to the reader. Commit, push, external writes and release require separate authority.

## Testing
For the first preview, inspect loading, rotation/zoom, model-load failure/retry and WebGL fallback. For later features, map checks to their criteria. Inspect 07 on the actual shoulder, empty and maximum-length values, independent settings, keyboard use, narrow layouts and upload failure/recovery. Record manual accessibility review and unrun checks. Do not weaken criteria to make a check pass.

## Core contract and command timing

The core areas are Player, Top and Colors. The team shoulder remains authored metal; no Team editor or teamLogo is required. Use ../swsb/teaching/tasks for the complete sequence. During the preview establish dev/lint/type-check/build. Loop 1 establishes real Jest tests and `verify: npm run lint && npm run type-check && npm test -- --runInBand && npm run build`. A planned or empty test suite is not passing evidence. Root AGENTS.md is authoritative; any CLAUDE.md import or derived scoped copies must point to its actual source and revision.
