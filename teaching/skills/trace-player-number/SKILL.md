---
name: trace-player-number
description: Explain how Ring Builder's player Number input reaches the shoulder inscription, with source evidence. Use for investigation or a leading-zero regression before planning edits.
---
# Trace the player number

This procedure is performed by the agent. The reader supplies or approves Markdown guidance and reviews your evidence. Application paths are inspection points or expected agent outputs, never instructions for the reader to hand-code files. Respect this procedure's read/review/verification scope; implementation belongs to a separately authorized agent task.


Read AGENTS.md and docs/specs/player-personalization.md. Inspect TextInput in components/ui/ControlPanel.tsx, setText in lib/store.ts and sanitizeText in lib/customization.ts. Follow playerNumber through Shoulders in components/canvas/Ring.tsx into SurfaceText.tsx and classicSurfaces.playerCrest in lib/rings/classic.ts. Check the right-shoulder camera mapping. If personalization has not been implemented yet, report the missing path and current milestone; do not invent a trace or ask the reader to create the source manually.

Return the path with file/function references, explain where digits are filtered and limited, and identify any numeric conversion that could turn 07 into 7. Explain scene terms in plain language. Separate code facts from assumptions. Cite tests as code evidence; inspect an actual Player view before claiming a visible result.

This is an investigation. Do not edit product code, change text policy, replace the model or mark an unrun check passed. Return the likely defect and a bounded next step if the trace reveals a gap.
