# Review case: contradictory Number policy

Illustrative Chapter 10 case, not an observed defect. Review this contract before implementation planning.

The Player name uses the current 12-character supported ASCII policy; Position uses the current 18-character policy. Number accepts three digits. Store Number as an integer and parse it with parseInt. The controls, state and player shoulder must retain the exact string 07 as 07. Empty values produce no inscription. Other fields and materials remain unchanged. Inspect the actual Player view as well as focused tests.
