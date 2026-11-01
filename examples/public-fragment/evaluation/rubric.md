# Evaluator rubric

Freeze sender and recipient answers before opening these materials. A tested agent must not receive this directory. Score the recipient against [reference.json](reference.json); use the sender response to locate where an error entered.

Before semantic scoring, compare the sender's preserved process_carrier with the supplied carrier. Record any missing or changed operator, vector or direction as a delivery error; retain the semantic scores separately. Layout-only differences may be recorded without treating them as a change of relation.

## Six separately reported checks

| Check | Pass condition |
|---|---|
| Goal and revision | Exact current goal and current revision are retained. |
| Decision and history | The current decision is correctly described; the superseded revision remains historical. |
| Foreign scope | The foreign revision is identified without adopting its decision into the current goal. |
| Unknown information | The named unresolved item remains unresolved; no mechanism/duration is invented. |
| Process relation | The State and Trajectory preserve the case-specific directed groups in `reference.json`. For case 01, connection leads to an integrated handoff, then an articulated result. For case 02, connection leads to integrated articulation, then an explicit handoff. Wording may differ. |
| Next action | A concrete next step supports the current decision and preserves the unresolved item, rather than implementing the superseded or foreign decision. |

Report each check as pass/fail/unscorable with the answer span and a short reason. Do not turn unscorable into pass. Critical failures include reversed current/superseded status, importing the foreign goal, invented resolution of the unknown, or reversal of the process direction. Report them individually even if other checks pass.

Exact IDs are compared exactly. The semantic fields require human judgement; a JSON parser or language-syntax checker does not decide them. Two independent evaluators should score without knowing carrier condition/model where feasible, then retain disagreements. An LLM judge is an additional recorded judgement, not ground truth.

A demo pass requires all six checks and no critical failure. It supports only this taught, explicit-fact handoff in its recorded conditions. It does not prove intrinsic interpretation, universal invariance, a dRy advantage over prose, hidden-fact recovery or actual code execution. The next_step here is a proposed action; behavior claims require a separate executed task.

## Interpretation of failure

Keep malformed output, missing items and technical errors in the run record. Distinguish delivery failure, carrier misreading, dropped task fact, unsupported inference and evaluator disagreement. Do not silently repair answers or count a retry as the original trial.

For a prospective blind study, keep new cases and expected relations outside the participant-visible repository. Public sample cases can be inspected or learned and are not a permanently held-out benchmark.
