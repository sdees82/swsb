# Loop 2 Player controls and camera

## Goal

Connect the three Player controls and inspection camera without claiming that text is already rendered.

## Start state

Loop 1 accepted; state, normalization, defaults, test and verify exist. Preview still works.

## Files and inputs

Player spec and reviewed plan; lib/customization.ts, lib/store.ts, lib/rings/classic.ts; existing camera and scene.

## Exact request

Implement the controls/camera plan item. Create ControlPanel.tsx with Player, Top and Colors areas. Top and Colors open empty panels labeled “Not built yet”; navigation works, but no logo or material controls function until their loops are implemented. Add Player name, Number and Position, labels, limits, counters and visible keyboard focus. Use setText for updates. Focusing a Player field chooses right-shoulder and stops automatic rotation. Switching to Top and back preserves design state. Reset design restores the complete defaults and hero view. Add focused controls tests. Do not add editable Team fields, a ring selector, logo handling or materials controls. Keep inscription rendering open for loop 3.

## Expected result

components/ui/ControlPanel.tsx and supporting controls; camera/store/definition connections; __tests__/controls.test.tsx.

## Checks to run

npm test -- --runTestsByPath __tests__/customization.test.ts __tests__/controls.test.tsx --runInBand; npm run verify.

## What to inspect yourself

Use keyboard and pointer. Enter harper, 07 and captain; check labels, counters, area switching, right-shoulder focus and Reset. Check desktop and narrow width. Input success does not close visible scene criteria.

## Stop conditions

Apply [the shared stop conditions](SHARED-STOP-CONDITIONS.md). A proposed Team editor or broader field policy needs a separate decision.

## Evidence to save

Control/camera parts of AC-01/02/08/09/10/11/12 in docs/evidence/player/02-controls.md; viewport and manual accessibility gaps; update progress.

## State required for the next step

Accepted controls and camera with persistent Player strings. Visible AC-01/02/03/05/06 remain open.
