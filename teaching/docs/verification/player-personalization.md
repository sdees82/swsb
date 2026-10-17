# Verify player personalization

Recipe version: editorial-2026-10-17-r3, prepared 2026-10-17. Authority: Chapter 4's player-personalization spec. This is a reusable procedure; record each run separately using the completion-report template. It does not report a completed feature in the reader's project.

## Setup

Ask the agent to start the app using its verified command. The verification agent runs authorized tests and follows repeatable interactions; the reader inspects the visible result, makes review decisions and maintains this Markdown recipe. Neither role requires the reader to create source or tests manually. Once the reader app exists, open `/builder`, choose Reset design. Use a fresh browser profile and record the app revision, recipe version, viewport, browser and ring view. Authorize only local fixture-based checks. Stop for a spec conflict or an action outside that scope.

## Player checks

1. Open Player. Enter `harper`, `07`, and `captain`. Inspect `HARPER`, `07`, and `CAPTAIN` on their actual shoulder surfaces. The control alone does not close AC-01/02/05.
2. Enter an alphabet string in Player name and inspect `ABCDEFGHIJKL` and the 12/12 counter. Check fit, not just truncation (AC-03/10, BR-04).
3. Enter `9a8` and then `12345` in Number. Expect `98` and `123` under the current input and normalization contract. Separately exercise the public store action (AC-04, BR-01/02).
4. Try `O'Neil`, then clear each Player field. Inspect the supported text and the cleared inscription (AC-06). The renderer trims surrounding whitespace.
5. Confirm that other Player text, the top logo and material choices remain unchanged. Switch to Top and back and verify the current Player values remain (AC-07/08).
6. Focus each Player field and inspect its declared camera view and stopped automatic rotation (AC-09, BR-05).
7. Reach tabs and fields with a keyboard; check labels, visible focus, field counters and narrow layouts. Record assistive-technology review separately (AC-10/11).
8. Reset design and inspect the whole design. The design returns to DEES / 23 / QUARTERBACK. Reset is broader than the Player tab (AC-12, BR-05).

## Related logo and material checks

Choose Top, select Logo and use `fixtures/logo/logo-shield.png`. Inspect the face. Then choose `notes.md` and `not-an-image.png` in separate attempts. Confirm distinct unsupported-file and decode messages, with the accepted image retained. Choose a valid file again and confirm recovery. Remove logo and check that the Logo emblem selection remains. Race and resize checks need their own evidence (LG-01–05).

Select Rose gold Ring metal, White gold Lettering metal, Ruby Top stones (pavé and halo), and Emerald Side stones. Inspect each selected control and the matching preview region. These are independent settings; this check does not create a new feature contract.

## Evidence

For every criterion, record passed, failed or not run and link its evidence. Keep normalization, store, control and rendered-scene findings separate. Record unavailable browser automation, manual accessibility work, model failures and remaining decisions. Do not relax the spec to make a failed check pass.

Use only the core Player, Top and Colors areas. Record any missing direct observation as not run. Exactly 5,242,880 bytes is 5 MiB; the size boundary and stale-read/resize cases are defined in ring-logo.md and teaching/tasks/04-logo.md.

## AC-11 local boundary

For local walkthrough acceptance, AC-11 requires keyboard-reachable areas and inputs, meaningful labels and visible focus in the desktop browser, with the same controls usable at a narrow desktop viewport. These checks are required. Screen-reader behavior and physical-phone touch/on-screen-keyboard support remain separate claims and stay not run until tested.
