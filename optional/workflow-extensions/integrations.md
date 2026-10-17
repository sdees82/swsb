# Optional extension

This material is outside the core Ring Builder path. It grants no tool access or authority. Check current documentation before using it.

Connect the Systems That Own the Truth

The core Ring Builder walkthrough uses local Markdown, assets, and the application we'll build. It needs no Jira or Figma account. In other work, requirements may live in a tracker, designs in Figma, and operational evidence in logs. Connect one of those sources when a task actually needs it, and give the agent enough direction to retrieve the relevant material.

The harness can reach those sources through structured integrations, APIs, or MCP servers. For now, local files may contain everything you need. When a task does call for another connection, work through these questions before adding it:

Why does the integration exist?

What can the agent read?

What can it write?

Which data is allowed?

How does authentication work?

Which actions are logged?

What limits apply?

Which actions require approval?

What happens when the integration fails?

Begin with read-only access so you can verify retrieval before allowing changes to shared information. Review write operations separately when a task requires them. Chapter 6 covers those permission decisions.
