# Appendix B: Specification Template
Use Chapter 4's nine sections, with the status, owner, and revision or retrieval details near the title. A small task may need only a sentence in some sections. Record exclusions and unresolved decisions plainly so a completed template doesn't conceal an unanswered question.
Objective
Describe the problem, who encounters it, and why it needs to change. Leave the proposed implementation for the sections where it belongs.
Intended outcome
Describe the experience someone should have when the work is complete. Put the detailed checks with the user stories and business rules below.
Scope
Identify the users, systems, data, and scenarios included in the assignment. State the exclusions too, including adjacent work deliberately deferred.
User stories and acceptance criteria
Place observable acceptance criteria beside the capability they establish. Give stories and criteria identifiers such as US-01 and AC-01 so tests and review findings can refer to them. Include relevant failure and accessibility behavior. For an internal change, describe the behavior to preserve; there's no need to invent a customer story.
Business rules and failure behavior
Record each shared rule once and assign an identifier such as BR-01. Include calculations, boundaries, state transitions, retries, and degraded behavior where they affect the feature. Have the relevant acceptance criteria refer to those rules.
Technical constraints and agreed decisions
Record the approved interfaces, architectural boundaries, dependencies, and data-handling decisions. Link to the project's standing guidance. Keep settled decisions distinct from implementation ideas that still require investigation.
Verification
Connect each criterion and rule to a test or review. Specify the environment, fixtures, commands, and manual inspection needed. State what each check can establish and where further evidence is required.
Open questions and approval blockers
Name the owner of each open question and the work waiting on its answer. When a decision is approved, record it and update the current rules and criteria so readers can find the answer there.
References
Link the authoritative assignment, designs, project rules, and relevant decisions. Note any conflicts or sources you cannot access. Label a ticket snapshot with its source and retrieval details, and explain how later updates will be reconciled.
