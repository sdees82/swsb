# Correction ledger

## Entry [ID]
Date/owner: [date/name]
Problem: [observed defect or clearly identified teaching case]
Layer/cause: [requirement/context/plan/implementation/check]
Correction: [smallest useful change and authoritative path]
Before evidence: [actual report/result]
After evidence: [same case, fresh session, actual result]
Model/input revision: [record]
Other cases: [regression/false-blocker checks]
Decision: [keep/revise/remove]
Recheck: [trigger/date]

## Completed teaching example RB-07
Date/owner: 2026-10-17 / walkthrough reader example
Problem: the supplied conflicting-number-contract fixture simultaneously calls Number an integer and requires 07 to remain 07. This is teaching data, not an observed application failure.
Layer/cause: contradictory feature requirements.
Correction: in a disposable corrected fixture, replace integer storage with a string contract; keep BR-02 in the authoritative Player spec. Link the scoped rule to BR-02 rather than repeating another normalization policy.
Before result: the two statements permit incompatible representations; review must report the conflict and hold that decision.
After result: the corrected fixture consistently requires string storage; a content comparison shows the contradiction removed. Fresh-session review and application tests still need actual run records.
Comparison record: [before review link], [after review link], [model/settings], [findings], [intervention].
Decision: retain only after the fresh-session comparison finds the conflict before correction, accepts the corrected contract, and introduces no false blocker on the complete case. No measured model improvement is claimed by this example.
