# Verification guide

This companion supplies procedures and test assets, not a test implementation. Direct the agent to establish the app's scripts and tests at the milestones in MILESTONES.md. The agent runs them from the app's root and returns actual results. The reader reviews those results, inspects the app and maintains the Markdown record. The target commands are npm run lint, npm run type-check, npm test and npm run build; combine them in npm run verify once established.

The original source project's tests and browser suite are implementation references named in the feature specs. They are not bundled here. In particular, no controls.test.tsx, customization.spec.ts, test:e2e script or asset-validator implementation ships in this package. Ask the agent to implement the focused checks the feature requires; do not treat a missing suite as completed work or ask the reader to write test code manually.

Use [the player recipe](verification/player-personalization.md) for direct browser checks. The first preview needs loading, rotation/zoom, failed-model retry and WebGL fallback checks. Later personalization needs separate normalization, state, control and actual-inscription evidence. A decoder test alone does not establish usable interaction.

Use neutral fixtures and isolated browser data. Record failed, passed and unrun criteria separately, including manual accessibility work. Historical preparation evidence is recorded in ../../validation/README.md; it does not prove that a reader's new application works.

## Local accessibility acceptance

For local walkthrough acceptance, AC-11 requires keyboard-reachable areas and inputs, meaningful labels and visible focus in the desktop browser, with the same controls usable at a narrow desktop viewport. These checks are required. Screen-reader behavior and physical-phone touch/on-screen-keyboard support remain separate claims and stay not run until tested. Record the browser, viewport and operator. The agent-built clean-room run does not substitute for an independent reader trial.
