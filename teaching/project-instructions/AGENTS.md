# Mature source-project guidance example

This Markdown describes the existing Ring Builder source project. Its package files, implementation and tests are not included in the companion. Use starter/AGENTS.md for the reader's starting briefing. This guidance addresses the agent: the reader authors Markdown, directs the work and reviews evidence; the agent creates/edits all application code, configuration, package files and tests. Source paths identify agent outputs or inspection points, never manual reader coding steps.

<!-- BEGIN:nextjs-agent-rules -->
# This is NOT the Next.js you know

This version has breaking changes — APIs, conventions, and file structure may all differ from your training data. Read the relevant guide in `node_modules/next/dist/docs/` before writing any code. Heed deprecation notices.
<!-- END:nextjs-agent-rules -->

# Ring Builder project guidance

## Mission
Build a browser application where someone selects a championship ring, personalizes its text, materials and artwork, and inspects the result in 3D. Its milestones are the first preview, player personalization, logo handling and independent material controls. Keep each milestone's behavior in its feature spec.

The existing application also contains a reference ring, opening mechanisms, quality controls and a design library. Those are existing capabilities; they do not expand a bounded customization assignment. The book companion excludes the reference ring and persistent design library.

## Architecture
- app/builder/page.tsx composes the page, preview and controls; app/builder/builder.css defines the builder layout.
- components/ui/ControlPanel.tsx renders the Top, Player, Team and Colors controls. LogoUpload.tsx handles accepted image files and decoding.
- lib/customization.ts defines TEXT_FIELDS and sanitizeText; lib/store.ts owns live design values and actions.
- lib/rings/registry.ts registers ring definitions. lib/rings/classic.ts defines the ring, its fields, surfaces, material zones and camera mappings.
- components/canvas/Ring.tsx draws the ring's runtime additions. Its Shoulders component passes playerName, position and playerNumber to SurfaceText.tsx. AuthoredModel.tsx loads the authored metal.
- public/models/championship-ring.glb is the ring's Draco-compressed model. public/draco holds the local decoder. lib/ring-surfaces.json, crown-profile.json, ring-opening.json and ring-model-version.json must match that export.
- TextInput → setText → sanitizeText → Shoulders → SurfaceText is the player-text path. Number is an inscription string; preserve leading zeros.

Read docs/ARCHITECTURE.md for the broader engine and docs/ASSET-PIPELINE.md for model conventions. Product requirements are indexed by SPEC.md. Do not use older technical notes to override a current feature spec.

## Stack
Use the installed Next.js 16.2.9, React/React DOM 19.2.4, TypeScript, React Three Fiber 9.6.1, drei 10.7.7, three.js 0.184, Zustand 5, Tailwind 4 and npm. package-lock.json records exact resolutions. Keep the existing stack. Explain a dependency change and obtain the reader's decision before adding an alternative. Next.js 16.2.9 requires Node >=20.9.0.

## Commands
Run from the repository root:
- Install the recorded dependencies: npm ci
- Start locally: npm run dev, then open http://localhost:3000/builder
- Lint: npm run lint
- Type check: npm run type-check
- Unit/integration tests: npm test
- Asset validation: npm run validate:assets
- Production build: npm run build
- Combined checks: npm run verify
- Browser checks: npm run test:e2e; first-time Chromium setup is npx playwright install chromium

The browser suite uses port 3210 and a separate .next-e2e output. Read docs/VERIFICATION.md before running it or updating baselines. These scripts are present in package.json; their presence is not evidence they passed in the current task. Report actual results.

## Operational Overview
Start with the active feature spec in docs/specs and inspect its implementation references. Return a bounded plan for the requested change. Reuse current state, field and surface contracts. Build and verify one step before expanding it.

Use skills/review-customization-spec/SKILL.md when checking a customization specification; skills/customization-plan-review/SKILL.md when reviewing a customization implementation plan, skills/trace-player-number/SKILL.md for an input-to-inscription investigation, and skills/verify-player-personalization/SKILL.md for a repeatable verification run. Read skills/README.md for tool discovery locations.

Bring a conflicting requirement, new character policy/font/model, shared interface change or repeated unexplained failure to the reader. Do not broaden the task to payment, discounts, persistence or a new ring. Commit, push, external writes and publication require the authority for those actions.

## Testing
Map changed behavior to the feature's AC/BR identifiers. For deterministic normalization and state, use focused tests. For visible criteria, inspect the ring and camera. A control showing 07 is not enough; both characters must appear on the shoulder.

Inspect empty and maximum-length text, independent neighboring settings, keyboard focus, relevant mobile widths and failure/recovery states. Keep assistive-technology review and unperformed checks explicit. Use e2e/fixtures and isolated browser data. Do not weaken protected acceptance tests or replace visual baselines just to make a check pass. Return changed files, checks run, results, evidence and remaining gaps. See docs/verification/player-personalization.md for the repeatable play.

## Core contract and command timing

The core areas are Player, Top and Colors. The team shoulder remains authored metal; no Team editor or teamLogo is required. Use teaching/tasks in the companion for the complete sequence. During the preview establish dev/lint/type-check/build. Loop 1 establishes real Jest tests and `verify: npm run lint && npm run type-check && npm test -- --runInBand && npm run build`. A planned or empty test suite is not passing evidence. Root AGENTS.md is authoritative; any CLAUDE.md import or derived scoped copies must point to its actual source and revision.
