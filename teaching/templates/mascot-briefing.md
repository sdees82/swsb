# Appendix H: MASCOT Project Briefing Template
Mission
Describe the following in a few sentences:
Who the product serves.
Which problem it solves.
Which outcomes matter.
Which product or domain terms have special meaning.
Architecture
Major applications, services, packages, and responsibilities.
Important data flows and external dependencies.
Protected boundaries and ownership.
Closest examples for common changes.
Links to architecture decisions and diagrams.
Check that the briefing introduces the whole product and lets the agent locate changes, reuse existing patterns, and recognize protected areas. Ring Builder's mission covers the preview, personalization, and the 3D preview; player-text limits belong in the feature spec. Use these same six headings for AGENTS.md or CLAUDE.md, according to the tool.
Stack
Languages and supported versions.
Frameworks and runtime versions.
Package manager and lockfile policy.
Approved major libraries and services.
Dependencies that are prohibited or require approval.
Commands
Install.
Start locally.
Focused tests.
Full tests.
Lint and format.
Type-check.
Build.
End-to-end validation.
Full completion check.
Write the exact commands and the setup they require. Keep secrets out of the briefing.
Operational Overview
When a written plan is required.
How task complexity affects model routing.
Which skills or procedures must run.
How implementation is divided and reviewed.
What requires independent review.
Stop conditions and escalation owners.
Human checkpoints.
What must be recorded before completion.
Testing
Required layers by type of change.
Protected acceptance tests.
Fixtures and network policy.
Accessibility, security, privacy, and visual expectations.
Manual checks automation cannot replace.
Evidence required in the completion report.
