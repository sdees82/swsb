# Change ring materials independently

The reader authors or approves this Markdown contract, directs the agent and reviews the returned evidence. The agent creates or edits the application implementation, configuration and tests. Technical paths below name expected agent outputs or inspection points, not files the reader must hand-code. Use the milestone map to distinguish existing files from outputs still to be produced.


Contract version: editorial-2026-10-17-r4. The choices below are the walkthrough contract.

## Outcome and scope
On Colors, change Ring metal, Lettering metal, Top stones (pavé and halo), and Side stones independently and inspect the matching preview region. Keep text and artwork intact. No pricing, payment, new materials library or new asset authoring is in scope.

## State and rules
- Ring metal uses finish/setFinish; Lettering metal uses accentFinish/setAccentFinish.
- Top stones use accentStone/setAccentStone; Side stones use stone/setStone.
- Each control obtains allowed choices from the ring definition. FINISHES and STONES in lib/customization.ts define the supported values.
- Defaults come from CLASSIC_DESIGN: white-gold body, yellow-gold lettering, sapphire side stones and diamond top stones. Reset restores the whole design.

## Acceptance criteria
- MT-01: Rose gold Ring metal changes finish and the ring-metal region without changing accentFinish, stone, accentStone, text or logos.
- MT-02: White gold Lettering metal changes accentFinish and the lettering treatment while preserving the ring-metal selection and other design values.
- MT-03: Ruby pavé and halo changes accentStone; Emerald side stones changes stone. Both selected controls and matching preview regions show the independent values.
- MT-04: Returning to Player and Top preserves the text and artwork while these material choices remain selected.
- MT-05: Controls have fieldset/legend context, accessible labels, selected state and keyboard reachability. Record direct interaction and remaining assistive-technology checks.

## References and verification
Inspect components/ui/FinishPicker.tsx, StonePicker.tsx, ControlPanel.tsx; lib/store.ts; lib/constants.ts; lib/materials.ts; lib/zoneMaterials.ts; lib/rings/classic.ts; components/canvas/Ring.tsx and BrilliantStones.tsx. Use __tests__/customization.test.ts and controls.test.tsx where applicable, then inspect the actual Colors scenario in the browser. A store assertion does not prove that the correct preview region changed. See docs/verification/player-personalization.md for the related checks.

## Decisions outside scope
A new finish/stone or changed visual contract requires a specific decision and revised criteria.
