---
name: customization-plan-review
description: >-
  Review a customization plan against its approved
  spec and current controls, state, and ring scene.
  Use before coding a customization change.
---
# Review a customization plan

This procedure is performed by the agent. The reader supplies or approves Markdown guidance and reviews your evidence. Application paths are inspection points or expected agent outputs, never instructions for the reader to hand-code files. Respect this procedure's read/review/verification scope; implementation belongs to a separately authorized agent task.


## Read first
AGENTS.md; the active docs/specs feature and plan;
field definitions, store, ring definition,
controls and scene; nearest existing tests. If a path is not yet present at the current milestone, identify it as an expected agent output and check that the plan creates its dependencies. Do not send the reader away to write it.

## Review
1. Map each criterion to a step and a check.
2. Trace 07 from its input to the inscription.
3. Check limits, empty values, and independence.
4. Inspect actual surfaces and related contracts.
5. Separate current behavior from open decisions.
6. Check isolation, recovery, and permissions.

## Return
Supported findings with spec and file references.
Separate required fixes from suggestions.
Name missing checks and decisions that block work.

## Boundary
Do not edit code, choose policy, or replace assets.
Do not mark a plan ready with unresolved blockers.
The runtime controls model selection and tools.

## Project checks
Use npm test -- --runTestsByPath __tests__/customization.test.ts for text-policy evidence. For visible criteria during Chapter 4 plan review, use the accepted feature spec and, when useful, read the companion recipe at ../swsb/teaching/docs/verification/player-personalization.md. Chapter 7 later copies that recipe to docs/verification/player-personalization.md. Identify the planned checks; do not claim to have run them.
