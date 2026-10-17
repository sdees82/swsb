# Loop 1 Normalization and state

## Goal

Close deterministic Player normalization and independent state updates while keeping visible criteria open.

## Start state

Accepted preview; spec reviewed, then player-personalization-plan.md created and reviewed in Chapter 4. No Player implementation yet.

## Files and inputs

AGENTS.md; docs/specs/player-personalization.md; player-personalization-plan.md; existing preview descriptor; ../swsb/SETUP.md.

## Exact request

Implement only normalization and state from the reviewed plan. Create TEXT_FIELDS and sanitizeText in lib/customization.ts, setText in lib/store.ts and focused tests in __tests__/customization.test.ts. Use the three Player fields and initial design from the spec; keep playerNumber a string. First establish Jest and its TypeScript configuration from SETUP.md. Add test and verify scripts exactly as SETUP.md defines. Demonstrate a meaningful failing behavior check before implementing the behavior, then rerun it. Check uppercasing, limits, empty values, O'Neil, 07, independent updates and whole-design defaults. Do not create controls or inscriptions in this loop. Return changed paths, actual results and still-open visible criteria.

## Expected result

Normalization, string-valued design state, focused tests/configuration; package scripts test and verify. No controls or scene changes.

## Checks to run

Before editing: npm run lint, npm run type-check, npm run build. Focused: npm test -- --runTestsByPath __tests__/customization.test.ts --runInBand. Closing: npm run verify, defined as lint then type-check then tests then build, stopping on failure.

## What to inspect yourself

Read tests and diff. Confirm that assertions exercise the public store action, preserve neighboring values and retain 07. An import failure is test setup work, not the intended red behavior. The preview should still load.

## Stop conditions

Apply [the shared stop conditions](SHARED-STOP-CONDITIONS.md). Keep controls and rendered inscriptions outside this state-only step.

## Evidence to save

AC-03/04/05/06/07/10 deterministic evidence and BR-01/02/03 coverage; test output and gaps in docs/evidence/player/01-state.md. Start player-personalization-progress.md.

## State required for the next step

Accepted state layer and working verify command. Controls, camera and visible inscription claims remain open.
