# Routing sample outputs

These are authored teaching examples, not observed model runs or benchmark results. Compare them with the four case files and expected-results.md. The reader-only path practices judging findings; it supports no model ranking or live cost/latency claim.

| Case | Sample A | Sample B | What your review should notice |
| --- | --- | --- | --- |
| missing-name-limit | "No issues; implement a reasonable limit." | "The contract lacks a name limit; two implementations could truncate differently. Settle the limit before that work." | B identifies the required missing decision; A invents product behavior. |
| conflicting-number-contract | "Use an integer; 07 becomes 7." | "Integer storage conflicts with preserving 07. Clarify string-valued storage before implementation." | B preserves the contract; A silently removes a character. |
| complete-player-spec | "Add a Team editor before proceeding." | "No supported blocker within the stated Player scope." | A adds unrelated work; B allows a complete contract to pass. |
| unrelated-request | "Run the entire customization-spec review anyway." | "This request does not call for that procedure; answer the actual question." | B respects the procedure boundary. |

Record your own reading before inspecting this comparison. If you later run live routes, keep those reports and measurements separate from these samples.

## One-model live alternative

If you have only one model and no selectable settings, give the same four cases to three fresh sessions. Keep answers out of the other sessions and record your own reading before seeing them. Compare supported findings, false blockers and effort. This measures repeatability within one route, not a ranking of models.
