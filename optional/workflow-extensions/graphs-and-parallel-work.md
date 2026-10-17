# Optional extension

This material is outside the core Ring Builder path. It grants no tool access or authority. Check current documentation before using it.

Optional Extension: Mapping Execution With Graphs

A graph can help when a written sequence leaves you unsure what should happen next. Draw the paths after a passing check, a failed check, or a request for a decision, using the bounded loop and saved state we've just established.

Representing Steps and Connections

In a graph, nodes represent steps and edges connect them. A node can run a check, call a model, or carry out another operation. The edges specify what follows, including paths that depend on a result. A graph-based runtime can pass state between steps, such as the approved specification and current test results. LangGraph is one framework that uses this model. Its Graph API overview explains nodes, edges, and state.

A validation node might send the change to you for review when checks pass, or send the failure details back to implementation when another attempt remains within the task's limits. Drawing that flow can reveal missing decisions before any automation is built. The graph describes the paths; a graph-based runtime can execute them. A node need not contain an agent, and an agent workflow need not use a graph framework.

Branches, Retries, and Human Reviews

Plan for outcomes besides success. A temporary service failure may justify a bounded retry, whereas an unanswered product question should stop the work until you resolve it or obtain the required decision. Some runtimes can preserve execution state at a checkpoint and continue after human input. LangGraph's interrupt documentation describes one approach.

Before a step resumes, know which actions it will repeat. Running a local check again differs from sending another external notification. Decide what is safe to retry and how completed actions are recorded. A fixture-based personalization test can send work back to implementation. Publishing a release remains a separate action requiring its own authorization.

For every route back through the loop, define what the next attempt will receive and what will end the retries. If the agent reaches the retry limit or finds an unresolved requirement, it should preserve the evidence and ask the engineer for a decision. Show those stopping points as clearly as the route to success.

Optional Extension: Parallel Work

Consider splitting personalization between two agents. One handles the controls and state; the other connects the shoulder scene. If the first preserves playerNumber as a string while the second tests only 23 and converts it to a number, both local checks can pass while the combined application renders 07 as 7.

Settle the field contract before splitting the work: playerNumber is text, and setText receives a field identifier and string. Give both workers fixtures for 07, a maximum-length name, and empty text, along with the ring's surfaces. Keep disputed contracts sequential until someone resolves them.

Give one worker a bounded change to the controls and its tests, and another the corresponding scene work. Protect the shared field definitions and store contract from independent edits. Use separate worktrees or sandboxes, preview ports, and evidence paths. Browser contexts need isolation too; a Git worktree doesn't isolate a browser profile or the design currently open in it.

Review each diff and its real output, then exercise the connected application. Enter 07 and inspect the ring's player shoulder. Try an empty field and a maximum-length name, and confirm that team text and material choices remain intact. Passing local tests leave these connections untested until the integration actually exercises them.
