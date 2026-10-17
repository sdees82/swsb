# Personalize the ring's player shoulder

Contract version: editorial-2026-10-17-r4. The reader maintains this Markdown. The agent creates all source, configuration and tests. Paths are expected outputs and inspection points.

## Objective and outcome
Let someone inspect their Player name, Number and Position on the ring's right shoulder. Preserve 07 as inscription text through input, state and rendering.

## Scope
One ring, three Player fields, counters, keyboard access, camera focus, inscriptions and whole-design Reset. The core interface has Player, Top and Colors areas. The Team shoulder is authored metal in the model; editable Team fields and a Team logo are outside this walkthrough. Do not create a Team editor or ring selector. Top logo and independent material controls are separate contracts.

## Field contract
| Field | Identifier | Limit | Default | View | Surface |
| --- | --- | ---: | --- | --- | --- |
| Player name | playerName | 12 | DEES | right-shoulder | player-name |
| Number | playerNumber | 3 digits | 23 | right-shoulder | player-crest |
| Position | position | 18 | QUARTERBACK | right-shoulder | player-caption |

## Acceptance criteria
- AC-01: Entering harper shows HARPER in the Player name control and on its shoulder surface.
- AC-02: Entering captain shows CAPTAIN on the separate caption surface; the other Player values remain.
- AC-03: Pasting the alphabet into Player name retains ABCDEFGHIJKL, displays 12/12 and fits the declared surface.
- AC-04: Number removes nondigits and keeps at most three digits: 9a8 becomes 98; 12345 becomes 123.
- AC-05: Entering 07 retains both characters in the control, state and rendered inscription.
- AC-06: O'Neil becomes O'NEIL. Clearing a field removes only its inscription. Surrounding whitespace is trimmed for rendering.
- AC-07: A Player edit changes only that text field; other Player values, accepted top logo and material choices remain unchanged. Before those later features exist, preserve their declared initial state.
- AC-08: Switching from Player to Top and back retains Player values. Switching areas does not reset the design.
- AC-09: Focusing a Player field frames right-shoulder and stops automatic rotation; view changes do not edit text.
- AC-10: Labels, limits and live counters match the field table and TEXT_FIELDS.
- AC-11: In the local desktop browser, areas and inputs are keyboard reachable, have visible focus and meaningful labels. The controls remain usable at a narrow desktop viewport. These checks are required for local walkthrough acceptance. Screen-reader and physical-phone support are separate environment claims; mark them not run until tested.
- AC-12: Reset design restores the whole initial design: DEES / 23 / QUARTERBACK; white-gold ring, yellow-gold lettering, diamond top stones, sapphire side stones, no top logo and no Logo emblem selection. Reset returns the hero view and automatic rotation.

## Business rules
- BR-01: Nonnumeric fields uppercase and retain A–Z, 0–9, space, apostrophe, ampersand, period and hyphen, then apply the field limit. This ASCII policy does not support every person's name.
- BR-02: Number is a string. Remove nondigits and truncate to three characters; never parse it as an integer.
- BR-03: Updates are independent. Camera state and active area are separate from design values.
- BR-04: Use the matching ring-surfaces.json charts for player-name, player-caption and player-crest. Inspect empty, short and maximum-length text for fit and legibility. A changed asset or font requires review.
- BR-05: The field/view declarations and defaults belong to this ring definition. Reset restores the entire design described in AC-12.
- BR-06: Logo and materials follow their separate contracts. No ring selection, Team editor, new assets, new character policy, persistence, accounts, payments or manufacturing export is included.

## Walkthrough decisions supplied for this project
The agent creates lib/customization.ts (TEXT_FIELDS, sanitizeText), lib/store.ts (setText with a field and string), components/ui/ControlPanel.tsx, lib/ringSurface.ts and components/canvas/SurfaceText.tsx. It extends lib/rings/classic.ts and the Ring.tsx/Shoulders scene. These are tutorial architecture decisions, not a universal feature-spec template. The agent may create small supporting types/helpers within the reviewed plan. Inspect actual imports together; no source checkpoint is supplied.

## Verification
Normalization/store tests cover AC-03/04/05/06/07/10 and BR-01/02/03. Controls tests cover labels, counters, persistence across areas, camera intent and Reset. Direct scene inspection closes visible AC-01/02/03/05/06 and BR-04. Keyboard and assistive-technology results are recorded per environment. Store or mocked-canvas assertions never close rendered-fit criteria.

## Decisions and references
No open product decision in this scope. If actual model/font evidence conflicts with it, stop affected work and return the conflict. See first-preview.md, ring-logo.md, material-customization.md, ../../tasks/README.md and ../verification/player-personalization.md.
