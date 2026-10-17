# Place a logo on the ring

Contract version: editorial-2026-10-17-r4. The reader maintains Markdown and accepts results; the agent creates implementation and tests.

## Outcome and scope
In Top, choose Logo, select a local file and inspect it on the generated center face. This contract covers topLogo only. No Team image state, Team upload, free dragging, cloud upload or asset authoring is included. Initial topLogo is null and emblem mode is none. Selecting Logo changes the mode to logo. An accepted upload sets topLogo and keeps that mode.

## Accepted file contract
Accept MIME types image/png, image/jpeg and image/webp at no more than 5,242,880 bytes (5 MiB). Helper text: "PNG, JPEG or WebP. Up to 5 MiB." Validate type and byte size before decoding. Decode the actual contents before acceptance, preserve aspect ratio and reduce the longest side to at most 1,024 pixels. Store PNG image data. A correctly declared type alone does not establish a decodable image.

## Acceptance criteria
- LG-01: A valid logo-shield.png appears on the center face with its aspect ratio preserved. A fresh valid choice after an error clears that error and restores ordinary editing.
- LG-02: Unsupported type or more than 5,242,880 bytes shows "Choose a PNG, JPEG or WebP image up to 5 MiB." The previously accepted logo remains. Exactly 5,242,880 bytes passes the size gate; it must still decode successfully.
- LG-03: Corrupt image data shows "This image could not be opened. Choose another image." The previously accepted logo remains.
- LG-04: Remove logo clears topLogo while leaving Logo selected. Reset design restores topLogo to null and mode to none, with all other defaults from the Player contract.
- LG-05: A newer selection, removal, Reset or unmount invalidates any older pending read/decode before it can set state. A rejected newer selection also prevents an older pending read from later replacing the previously accepted image.

## State, placement and checks
The agent creates LogoUpload.tsx, LogoImage.tsx and a top-only setLogo action. It generates the center-face placement in Ring.tsx from crown-profile.json, ring-opening.json and matching version data. Preserve Player text and material values. Do not introduce teamLogo or silently broaden setLogo's scope.

Use the companion's logo-shield.png, notes.md and not-an-image.png through real file input. The agent creates isolated test data for exact/over-limit sizes, a large decodable image for resize, delayed A then B reads, delayed read then Remove, delayed read then Reset, rejection during a pending read and unmount. These generated fixtures/tests belong in the working project, outside the companion. Direct browser observations establish the messages and retained image; deterministic checks establish resize and stale-read ordering. Report each separately.
