# Taught handoff comparison: initial result

This small comparison tested whether a process relation and case facts survived a sender-to-recipient handoff. All conditions received the same complete public primer and the same case facts; only the process carrier changed. The four carriers were natural prose, structured prose with State/Trajectory, dRy, and dRy with a short contextual gloss. The six semantic checks were frozen before responses and reviewed independently.

| Carrier | Handoffs passing all six semantic checks |
|---|---:|
| Natural prose | 12/16 |
| Structured prose | 14/16 |
| dRy | 13/16 |
| dRy plus gloss | 16/16 |

The run comprised eight new cases, four conditions and two repeats per case: 64 handoffs and 128 fresh sender/recipient calls with `gpt-6-luna` at medium reasoning. The repeats are **not** 16 independent cases per condition. The carrier was copied exactly in 52/64 handoffs. In the remaining 12, all in the dRy-plus-gloss condition, the gloss was omitted while the core chain remained. Carrier delivery and semantic success are separate observations. Here, omission means omission from the copied `process_carrier` field. In all twelve such handoffs, the recipient still received the sender's prose `state_reading`, `trajectory_reading` and `handoff` alongside the chains; these were not chain-only recipient inputs.

Within this experiment, the dRy-plus-gloss sender condition had the highest observed all-six success rate: 100%, compared with 75% for natural prose, 87.5% for structured prose and 81.25% for dRy. One possible explanation is that the initial gloss helped stabilize the sender's unfolding, which was then carried into the recipient input. The experiment did not isolate that mechanism or the chain's contribution from the accompanying readings.

These fractions are descriptive. With only eight case clusters, repeated observations and one model family, differences between conditions are uncertain; a confidence interval calculated as though all 16 handoffs per condition were independent would be misleading. The perfect 16/16 dRy-plus-gloss result is therefore not evidence of a general advantage. The primer taught the notation in every condition, and explicit case facts already carried much of the decision. The run used fresh empty work directories and ephemeral processes on one laptop, with a reused authenticated profile and standard harness. It did not test unprimed reading, cross-provider transfer or broad autonomous software work.

## Reproduce the public scope

The [public study attachment](../examples/public-fragment/study-data/README.md) now contains the eight synthetic cases, four carriers per case, the exact prompt recipe and hashes, 128 unchanged raw answers, evaluator expectations, and six individual scores plus carrier status for all 64 handoffs. These previously held-out cases are included as reproduction material in this package; they are not a held-out set for new runs. The attachment permits independent inspection and prompt reconstruction, though a fresh model run may produce different answers. Keep `gold.json` and `scores.json` out of participant inputs.

For a smaller trial, use the [complete two-case public fragment](../examples/public-fragment/README.md) and its [clean-room procedure](clean-room-testing.md). Give each fresh sender only the public primer, its carrier, case facts and sender instruction. Give each fresh recipient only the primer, recipient instruction and frozen sender answer. Open evaluator references only after both answers are frozen. The [semantic reproducibility protocol](semantic-reproducibility.md) explains scoring and reporting.

A separate fresh-agent onboarding test of the public case-01 example passed five of six checks. Its next step did not concretely address or explicitly defer unresolved authentication; this test is not part of the 64 handoffs above.

After the public recipient instruction was clarified, one new sender/recipient pair passed all six semantic content checks, including a concrete request to clarify authentication. The sender nevertheless copied a case sentence instead of the process chain into `process_carrier`, and the recipient did not flag that change. The separate carrier-delivery check failed, so the full onboarding workflow still did not pass. This follow-up does not replace the earlier 5/6 result or enter the 64-handoff comparison.

A separate case-02 application probe made the same expected edit to an isolated file under structured prose and dRy. The same executor handled both conditions, and the case facts identified the current decision. It verifies a narrow action path, not a carrier effect or general software capability.


A separate [token-load profile](token-load-20261101.md) counts the frozen public text with two named reference encodings and separates those counts from historical client-reported usage. No new model calls were made for that measurement.
