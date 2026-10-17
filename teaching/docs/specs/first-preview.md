# Display and inspect the ring

The reader authors or approves this Markdown contract, directs the agent and reviews the returned evidence. The agent creates or edits the application implementation, configuration and tests. Technical paths below name expected agent outputs or inspection points, not files the reader must hand-code. Use the milestone map to distinguish existing files from outputs still to be produced.


Contract version: editorial-2026-10-17-r3. This is the Chapter 3 practice rep before the full feature loop.

## Outcome
Open /builder and inspect the ring before adding player text, image uploads or material controls in the reader's implementation.

## Included
Next.js, TypeScript and React Three Fiber; public/models/championship-ring.glb; local /draco/ decoding; a lit scene; camera inspection; loading, model failure/retry and WebGL fallback behavior.

## Acceptance criteria
- PV-01: The model loads, with all 14 authored meshes and the correct material slots.
- PV-02: The reader can rotate and zoom to inspect the top and shoulders.
- PV-03: Loading is communicated while assets are unavailable; a failed model request presents a useful message and a retry path.
- PV-04: A browser without WebGL receives a useful fallback.
- PV-05: Model structure, required decoders and the distinction between authored metal and runtime additions are recorded in project guidance.

## Implementation references
lib/rings/classic.ts; components/canvas/AuthoredModel.tsx; RingCanvas.tsx; Lighting.tsx; CameraRig.tsx; public/draco; lib/assets/validateRing.ts. The mature Ring.tsx includes later customization; it is a worked reference, not a requirement to build every feature in this milestone.

## Verification
The agent inspects and records the asset structure; no validate:assets script is assumed. Open /builder and inspect the model and camera, then exercise missing-model and fallback paths in an isolated test context. Record browser evidence separately from decoder results.

## Excluded
Player controls, logos, materials UI, payments, discounts, persistence and CAD export. Do not require Blender MCP.

## Reader-stage command availability
The starter supplies Markdown and assets, not application tooling, lib/assets validators or feature tests. Follow MILESTONES.md in the companion. No validator code is supplied. Have the agent create its complete dependency set before reporting that command as a result for the reader app. The first preview is checked through its scaffold commands and actual loading/inspection/failure behavior.
