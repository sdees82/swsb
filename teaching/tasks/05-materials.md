# Loop 5 Independent materials

## Goal

Change ring metal, lettering metal, top stones and side stones independently in state and preview.

## Start state

Player and top logo accepted. All four material defaults exist. Colors navigation still opens an empty panel; no material controls have been built.

## Files and inputs

docs/specs/material-customization.md; current state/definition/scene; model material slots and matching crown/opening data.

## Exact request

Review a bounded MT-01–05 plan, then implement the four independent Colors controls. Create FinishPicker.tsx and StonePicker.tsx and the constants/material/zone helpers and runtime stones needed by this scene. Wire finish/setFinish to ring metal, accentFinish/setAccentFinish to lettering, accentStone/setAccentStone to pavé and halo, and stone/setStone to side stones. Keep allowed values and defaults in the ring definition. Verify Rose gold ring, White gold lettering, Ruby top stones and Emerald side stones together, retaining Player and topLogo. Add state/control checks for independence; inspect each corresponding rendered region. Do not add prices, payment or new assets.

## Expected result

Colors controls, four separate state actions, material mappings, runtime stones and focused tests. Small scene helpers must stay inside this feature plan.

## Checks to run

npm run verify; MT-01–05 actual Colors scenario; keyboard labels/selected states; return to Player and Top; whole-design Reset.

## What to inspect yourself

Select each material in turn and confirm only its own region changes. Compare labels/selected state as well as color. Inspect at desktop/narrow widths. Color judgments need the running color app or companion color figures.

## Stop conditions

Apply [the shared stop conditions](SHARED-STOP-CONDITIONS.md). A new finish/stone, pricing feature or change to the model requires a separate assignment.

## Evidence to save

docs/evidence/materials/01-independent-materials.md with state and corresponding scene observations, retained text/logo, keyboard checks and open assistive-technology work.

## State required for the next step

All five feature loops accepted; core editor implemented. Chapter 6 deepens the authority map; Chapter 7 builds the complete evidence matrix. No release is implied.
