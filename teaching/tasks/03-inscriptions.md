# Loop 3 Rendered inscriptions and fit

## Goal

Finish the Player path from real controls to the declared ring surfaces.

## Start state

Loops 1–2 accepted; working controls/camera and matching supplied model metadata.

## Files and inputs

Player spec/plan; ring-surfaces.json, crown-profile.json, ring-opening.json and ring-model-version.json; supplied fonts; actual controls/store/scene.

## Exact request

Implement the inscription/fit plan item. Create lib/ringSurface.ts and SurfaceText.tsx, extend the ring definition and connect Ring.tsx/Shoulders to the live Player strings. Place name, position and number on their declared surfaces; retain 07 as text. Use the matching charts and supplied fonts, trim surrounding whitespace for rendering and draw no inscription for an empty field. Check short and maximum-length values. Preserve model geometry and the accepted preview/camera behavior. Add focused mapping/fit checks where they can detect a real defect. Return actual rendered-view evidence separately from store tests.

## Expected result

Ring.tsx/Shoulders, SurfaceText.tsx, ringSurface.ts and definition mappings; necessary local helper/types and focused tests within the plan.

## Checks to run

npm run verify; direct /builder interactions for AC-01/02/03/05/06 and BR-04. Read ../swsb/teaching/skills/trace-player-number/SKILL.md and follow it against the implementation now that the path exists.

## What to inspect yourself

Inspect HARPER / 07 / CAPTAIN on the actual right shoulder, ABCDEFGHIJKL at 12/12, O'NEIL, cleared fields, and Reset. Look for clipping, reversed text, overlap and wrong surfaces. Perform this yourself if the agent lacks browser tools.

## Stop conditions

Apply [the shared stop conditions](SHARED-STOP-CONDITIONS.md). Return a font, surface or model limitation that prevents the agreed inscription; do not drop a character or move it to another surface.

## Evidence to save

docs/evidence/player/03-inscriptions.md with entered values, view, browser, viewport and observations. Map visible criteria separately. Record any assistive-technology check still open.

## State required for the next step

Player AC-01–12 and BR-01–06 are accepted for the required local scope. A failed or missing required observation blocks Loop 4. Desktop and narrow-viewport keyboard, focus and label checks are required; screen-reader and physical-device claims remain not run until tested.

Now the reader copies and reviews the Markdown for the chosen harness. Claude Code: ../swsb/teaching/rules/claude/customization.md to .claude/rules/customization.md. Codex: ../swsb/teaching/rules/codex/AGENTS.md to lib/AGENTS.md as the working source, then derive components/AGENTS.md from it. Record source and companion revision; keep the companion unchanged. In fresh sessions, check an affected customization path for the scoped rule and 07/string contract, then an unrelated app path where it should not apply. Save actual paths, results and discovery gaps in docs/evidence/player/scoped-guidance.md. Resolve a failed discovery check before relying on the rule.
