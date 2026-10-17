# Personalize the ring's player shoulder


## Objective
Let someone judge a ring carrying their own player
name, number, and position in the live preview.

## Intended outcome
Player inputs change the corresponding inscriptions.
Keep 07 as 07 throughout the application.

## Scope
### Included
- ring; Player name, Number, Position.
- Current text rules, field limits, and counters.
- Player camera focus and rendered inscriptions.
- Independent edits; current Reset behavior.
### Excluded
- New model assets, fonts, or character policies.
- Logo upload and material selection; separate specs.
- CAD export, accounts, and persistence.

## User stories and acceptance criteria

### US-01 Make the ring personal
As someone choosing a ring, I want to inspect
my player details on its shoulder.
- AC-01: Player: entering harper shows
  HARPER in the control and on the player shoulder.
- AC-02: Position captain becomes CAPTAIN on its
  own caption surface; name and number remain.
- AC-03: Name accepts at most 12 characters;
  an alphabet paste displays ABCDEFGHIJKL.

### US-02 Keep the inscription accurate
As a user, I want the displayed text to match
the supported value I entered.
- AC-04: Number keeps at most 3 digits.
  9a8 becomes 98; pasting 12345 gives 123.
- AC-05: Entering 07 retains both characters
  in state, the control, and the player inscription.
- AC-06: O'Neil becomes O'NEIL; an empty field
  produces no inscription on that surface.

### US-03 Make independent changes
As a user, I want each edit to change the part
of the design I selected.
- AC-07: Editing player text leaves team text,
  top inscriptions, artwork and materials unchanged.
- AC-08: Switching to Top and back retains the
  current Player values within the live editor.
- AC-09: Focusing a Player field frames its
  declared view and stops automatic rotation.

### US-04 Use the controls
As a keyboard user, I want to reach and identify
the fields and inspect the resulting design.
- AC-10: Labels, limits and counters match
  TEXT_FIELDS; Position is limited to 18 characters.
- AC-11: Tabs and inputs work with a keyboard;
  focus is visible. Record assistive-tech review.
- AC-12: Reset uses the ring's defaults.
  Defaults: DEES / 23 / QUARTERBACK.

## Business rules and failure behavior

### BR-01 Text policy
Reuse TEXT_FIELDS and sanitizeText. Nonnumeric
fields uppercase and keep the current ASCII set:
A-Z, 0-9, space, apostrophe, ampersand, period,
and hyphen. Apply each field's length limit.
Do not claim support for every person's name.

### BR-02 Number is text
Remove nondigits; retain at most three digits.
Do not parse the result as an integer.
A leading zero is part of the inscription.

### BR-03 Field independence
Only the target text field changes. Retain the
other inscriptions, artwork and material choices.
Changing the view does not change the design.

### BR-04 Placement
Use the ring's player-name, player-caption
and player-crest surfaces. Inspect fit and legibility
with empty, short and maximum-length values.

### BR-05 View and reset
Use the ring definition's field-to-view mapping.
The Player fields use right-shoulder.
Current Reset restores the whole design,
not just the three Player fields.

### BR-06 Other rings and related features
Each ring owns its field and surface declarations.
Do not move another ring's number to this shoulder
just to make a shared form test pass.
Logo and material changes have separate contracts.

## Technical constraints and agreed decisions
- Reuse lib/customization.ts and lib/store.ts.
- Inspect lib/rings/classic.ts and Ring.tsx.
- Use SurfaceText for the existing inscription path.
- Keep the playerNumber contract as a string.
- Use neutral fixtures and isolated browser data.
- No asset replacement or new dependencies in scope.

## Verification
- Normalization: AC-03/04/05/06/10, BR-01/02.
  Exercise sanitizeText and the public store action.
- Controls: AC-01/02/07/08/09/12. Check labels,
  field updates, camera and unchanged neighboring state.
- Scene: AC-01/02/05/06, BR-04. Inspect the actual
  Player view with 07 and a maximum-length name.
- Keyboard and accessibility: AC-10/11. Record
  completed checks and remaining manual reviews.

## Open questions and approval blockers
No unresolved decision within this feature's scope.
A request for additional writing systems must name
its owner and block only that character-policy change.
It is not implied by the current name control.

## References
- lib/customization.ts; lib/store.ts
- lib/rings/classic.ts; components/canvas/Ring.tsx
- components/canvas/SurfaceText.tsx
- __tests__/customization.test.ts; controls.test.tsx
- e2e/customization.spec.ts; docs/VERIFICATION.md
