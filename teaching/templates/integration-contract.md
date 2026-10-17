# Appendix I: Integration Contract Template
Integration: Name of the connected platform, API, or MCP server.
Purpose: Why the agent needs this connection and which workflows use it.
Approved use cases: Specific retrieval or action scenarios.
Read scope: Projects, records, files, fields, and data classifications the agent may access.
Write scope: Each permitted action listed separately. Reading a ticket, adding a comment, changing priority, and closing work are different capabilities.
Identity and authentication: Account type, managed identity, OAuth scopes, credential lifetime, and rotation owner.
Data handling: Information allowed in requests, logs, caches, model context, and retained artifacts.
Human approvals: Actions requiring confirmation and the owner authorized to approve.
Audit and monitoring: Events recorded, retention period, access to logs, and alert conditions.
Limits: Rate, token, financial, or operational boundaries.
Failure behavior: Timeout, partial response, unavailable service, stale information, and recovery.
Revocation: How access is reduced or removed.
Owner and review date: Person responsible and next review.
