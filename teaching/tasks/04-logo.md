# Loop 4 Top logo validation and recovery

## Goal

Accept, render, remove and recover from local image selections without stale reads replacing newer intent.

## Start state

Player accepted; Top navigation opens an empty panel. topLogo is null and mode is none. No logo control or Team-logo state exists.

## Files and inputs

docs/specs/ring-logo.md; existing store/Top controls/scene; matching crown metadata; ../swsb/fixtures/logo/{logo-shield.png,notes.md,not-an-image.png}.

## Exact request

1. Review a bounded plan against LG-01–05 before coding. Implement only that contract.

2. Create LogoUpload.tsx, LogoImage.tsx, a top-only setLogo action and center-face placement in Ring.tsx. Preserve Player text and material values.

3. Accept PNG/JPEG/WebP up to 5,242,880 bytes. Use the exact 5 MiB helper and error messages in the spec. Replace the accepted image only after the new file decodes successfully.

4. Resize the longest side to at most 1,024 pixels, preserve aspect ratio and store PNG data. Retain the accepted image after type, size or decode errors.

5. Make Remove clear the image while leaving Logo selected. Invalidate older work after a new selection, removal, Reset or unmount.

6. Create boundary, resize and delayed-read fixtures and tests. Return the changed paths, actual results, rendered observations and remaining gaps.

## Expected result

Top upload/control/scene, topLogo action and local focused tests/fixtures. No teamLogo, external upload or drag positioning.

## Checks to run

npm run verify; real file-input valid/unsupported/corrupt/recovery/removal checks; exact-size gate, oversized rejection, decoded resize and delayed A→B/A→Remove/A→Reset/rejection/unmount checks.

## What to inspect yourself

Upload shield, then notes.md and corrupt PNG separately. Compare exact messages and retained shield. Choose a new valid image, remove it, then Reset. Inspect the center face and unchanged Player inscription. Deterministic race tests supplement this interaction pass.

## Stop conditions

Apply [the shared stop conditions](SHARED-STOP-CONDITIONS.md). Changed file limits/types, external upload or placement outside the center face requires a revised contract.

## Evidence to save

LG-01–05 in docs/evidence/logo/01-top-logo.md; fixture names, byte limits, resize dimensions, race order, messages and rendered observations; update progress.

## State required for the next step

Accepted top-logo behavior, error recovery and race/resize evidence. Required failed or unrun LG checks remain blockers, not a completed logo milestone.
