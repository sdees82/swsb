# Run a practice rep and build the preview

## Goal

Create an inspectable /builder preview satisfying PV-01–05. This bounded setup rep establishes a baseline before Part III runs the full feature loop.

## Start state

Chapter 2 read-only retrieval passed. The working folder contains reviewed AGENTS.md and docs/specs/first-preview.md, with no application. Authority preflight accepted.

## Files and inputs

AGENTS.md; docs/specs/first-preview.md; ../swsb/SETUP.md, MODEL-INSPECTION.md and starter assets.

## Exact request

Read those inputs and propose the small preview plan before editing. After I accept the plan, inspect the GLB and matching JSON, copy the model/fonts and four JSON assets into this project, and scaffold the recorded Next.js stack. Obtain the local Draco decoder from installed three.js. Create /builder with the lit model, orbit/zoom, loading, failed-load retry and WebGL fallback. Create dev, lint, type-check and build scripts; use webpack as SETUP.md records. Keep Player, logo and material controls for Chapter 5. Implement the application, configuration and checks yourself. Return the actual paths, commands, outcomes and gaps.

## Expected result

app/layout.tsx, app/globals.css, app/page.tsx, app/builder/page.tsx; components/canvas/{RingCanvas,AuthoredModel,Lighting,CameraRig}.tsx; lib/rings/classic.ts; copied assets/JSON; package/configuration/lockfile. Small supporting files are allowed within this plan.

## Checks to run

npm run lint; npm run type-check; npm run build; npm run dev. Record model structure and decoder requests. No test or verify script is assumed yet.

## What to inspect yourself

Open the returned local /builder URL. Inspect the top and shoulders, orbit and zoom. In an isolated check, fail the model request, restore it and retry. Check the no-WebGL fallback. Agent browser tools are optional; perform these interactions yourself if unavailable.

## Stop conditions

Stop for a conflicting spec, missing or mismatched asset, changed dependency/character policy, work outside my-ring-builder, or a required check that cannot be completed. Preserve the result and explain the affected work. Do not commit, push, deploy, access production or write to an external service. Routine corrections within this contract may continue.

## Evidence to save

PV-01–05 observations, actual command output, browser/environment and unavailable checks. Save docs/evidence/preview/build.md.

## State required for the next step

Accepted preview and current briefing. You inspect Git ignores and create a local baseline commit yourself. No push. Chapter 4 begins with this preview; no customization helpers or feature suite exists.
