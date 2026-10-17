# Ring Builder procedures

The reader authors or approves these Markdown procedures and invokes them for agent work. The agent inspects source, runs checks and returns evidence; application/test implementation remains agent work, never manual reader homework.

Canonical procedures live here. No .agents/skills or .claude/skills discovery entries are supplied. For the core walkthrough, give the agent the exact ../swsb/teaching/skills/<procedure>/SKILL.md path and ask it to read and follow that procedure. Confirm the file it read and the task boundary. Installing named skills is optional and harness-dependent; test automatic discovery separately in a fresh session if you configure it.

- [Customization plan review](customization-plan-review/SKILL.md): review a bounded implementation plan before coding.
- [Trace player number](trace-player-number/SKILL.md): investigate input, normalization, state and actual inscription behavior.
- [Verify player personalization](verify-player-personalization/SKILL.md): repeat the Chapter 7 recipe and report evidence.

In a fresh session, test a matching request with the explicit procedure path and an unrelated request that should leave the procedure unused. Confirm the path actually read. If you optionally install named skills, test their automatic discovery separately. File validation checks format and references, not runtime discovery. These procedures do not install host tools or grant permissions.

- [Customization spec review](review-customization-spec/SKILL.md): review feature decisions before planning; includes local Chapter 10 evaluation cases.
