# Customization boundaries

Agent-facing rule. The reader maintains this Markdown and reviews the result; application paths scope the agent's implementation and inspection work. Do not ask the reader to hand-code source or tests.

## Read first
The active feature spec; TEXT_FIELDS; sanitizeText;
the store, ring definition, and affected scene.

## Required behavior
- Reuse the current field names and text limits.
- Keep playerNumber as text; 07 must stay 07.
- Change only the selected field or material.
- Use the ring's surfaces and camera mapping.
- Check the actual preview for visible criteria.

## Checks
npm test -- --runTestsByPath __tests__/customization.test.ts
Use the complete command on one line in a shell.
Also check affected controls and rendered views.

## Approval
Review new characters, fonts, or model assets.
Do not weaken protected acceptance checks.

Apply this guidance in the directories that contain the relevant implementation. Adapt references to your project and verify discovery in a fresh session. The command above becomes usable only after the test script and file exist.

Pinned source example: swsb/teaching/rules/codex/AGENTS.md, revision editorial-2026-10-17-r6. Leave that companion snapshot unchanged. After Loop 3, the reader copies and reviews this Markdown as my-ring-builder/lib/AGENTS.md, the working source, and derives components/AGENTS.md from it. Identify the working source and companion revision in each copy. Maintain lib/AGENTS.md in the working project, refresh the components copy with it and compare them when the policy changes. Check the selected harness in a fresh session from an affected path and an unrelated app path; save actual paths and discovery results in docs/evidence/player/scoped-guidance.md.
