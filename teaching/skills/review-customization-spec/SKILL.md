---
name: review-customization-spec
description: Review a Ring Builder customization feature specification for missing decisions, conflicting number/text contracts and verifiable acceptance criteria. Use for specification review before implementation planning, including the book's Chapter 10 cases.
---
# Review a customization specification

This procedure is performed by the agent. The reader supplies or approves Markdown guidance and reviews your evidence. Application paths are inspection points or expected agent outputs, never instructions for the reader to hand-code files. Respect this procedure's read/review/verification scope; implementation belongs to a separately authorized agent task.


Read the supplied feature spec and the relevant project field/state/scene definitions. Identify missing limits, contradictory rules and visible claims with no verification route. Distinguish a missing requirement from a source fact that is already settled; cite the evidence rather than inventing a new blocker.

For player personalization, inspect TEXT_FIELDS and sanitizeText in lib/customization.ts and the playerNumber string path. A contract that calls the number an integer while requiring 07 to remain 07 is contradictory. Report the conflict; do not silently drop the zero or rewrite the accepted policy.

Return supported findings, their consequence and the smallest clarification needed. A complete specification should receive no invented blocker. Do not edit code or product requirements during review. This procedure does not apply to unrelated requests.

For a local behavioral comparison, use evals/cases and evals/expected-results.md. Keep expectations out of the reviewing session; use them afterward to assess the answer. Repeat with skill enabled and disabled under the same model, source revision and permissions. Record invocation separately from review quality. No evaluation plugin is required.
