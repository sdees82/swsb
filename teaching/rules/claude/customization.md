---
paths:
  - "lib/customization.ts"
  - "lib/store.ts"
  - "lib/rings/**/*.ts"
  - "components/ui/*.tsx"
  - "components/canvas/**/*.tsx"
---
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
