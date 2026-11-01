# Evaluating semantic reproducibility

The primary question is whether a defined process relation survives interpretation and application under recorded language, teaching and task conditions. Token use is a separate resource measure.

## Available evidence

| Material | Status | Supported interpretation |
|---|---|---|
| [Earlier studies](overview.md) | Selected internal reports summarised publicly. | Taught readings and interpreted relations in their recorded conditions. |
| [Public handoff fragment](../examples/public-fragment/README.md) | Complete sample inputs and evaluator reference. | Readers can conduct and report a limited taught handoff trial. |
| [Initial taught comparison](public-comparison-20261101.md) | Eight new cases, four carriers, two repeats, one model family; [public study attachment](../examples/public-fragment/study-data/README.md) includes inputs, raw answers and individual scores. | A scoped comparison under a shared primer, with no established general carrier advantage. |
| [Correction-transfer infrastructure case](../case-studies/correction-transfer.md) | Technical route internally checked; blinding failed. | Selected stored correction reached a later agent and its own action changed in that scope. |
| sHieNtAmE local-agent development | Partial implementation; operator-stopped. | Runtime and local inference progress, not a completed semantic or autonomous-code benchmark. |

Do not substitute test counts, valid syntax, model agreement or retrieved-byte identity for semantic preservation.

## Define success before interpreting answers

Represent the expected relation independently: relevant objects and goal, current/superseded revision, directed transition, conditions/negations, foreign scope, unknowns and permitted next action. Seal this reference before model answers in a prospective study. Report the matching source/answer spans and evaluator disagreements.

Assess separately:

- intended relations preserved, missing or falsely added;
- direction, negation and revision reversals as individual critical errors;
- correct binding to the new task or session;
- reconstruction and later application of an earlier correction;
- actual execution when the claim concerns behavior, rather than a proposed next action;
- manual interventions needed to restore the intended goal, with an explicit intervention definition.

An embedding-similarity score or fluent paraphrase cannot by itself decide these questions. An LLM judge is an additional evaluator whose judgement and disagreements must be retained.

## A controlled comparison

The sample package provides chain, prose and gloss carriers. A controlled comparison should keep one common versioned primer, task facts, roles, output contract and available tools fixed, changing only the carrier condition. The [initial run](public-comparison-20261101.md) used:

1. natural prose;
2. structured prose with State/Trajectory;
3. dRy without an added contextual gloss;
4. dRy plus a short contextual gloss.

This estimates carrier effect *after the same teaching*. A separate unprimed condition answers a different question and must not be mixed into that comparison. A gloss-only condition could further isolate the gloss contribution but was not part of this run. Match intended information before collecting answers, not after seeing which condition succeeded. The transfer prompt must not itself supply the correction or answer whose recovery is being tested.

Use new sender/recipient sessions, new held-out cases, repeated trials and recorded model versions/settings. Counterbalance condition order. Preserve refusals, malformed answers, failures and retries. Separate within-model repeatability from cross-model agreement, and agreement from correctness. Sample size and uncertainty estimates must accompany any general claim; the public two-case demo is not that study.

The historical memory pilot used a shared prose teaching history plus unequal reminder packages. Its 916 versus 706 token comparison measured those whole teaching packages, not equivalent standalone dRy/prose carriers. Both taught arms transferred a correction; a specific chain advantage remained unproven. These observations motivate a better comparison rather than a token-efficiency claim.

## Input and token accounting

Record the one-time primer, chain, gloss, task facts, retrieved sources, tool results and provider/harness overhead separately where observable. Distinguish disk bytes, initially delivered model input and actually read information. Use a named tokenizer or provider usage; do not infer tokens from file size. State amortisation assumptions explicitly and include failed trials. A smaller carrier is useful only alongside adequate relation preservation.

## Reproduction boundary

The full private language profile is unnecessary for the public fragment because every definition it uses is included. A result that depends on withheld definitions, prompts or raw responses must instead be labelled internally documented. Public examples are inspectable and may eventually enter training data; keep genuinely held-out evaluation cases separate.

[Clean-room testing](clean-room-testing.md) addresses environment contamination. Methodological context: [HELM](https://crfm.stanford.edu/2022/11/17/helm.html) motivates standardised conditions and multiple separately reported metrics; this page proposes a domain-specific protocol, not a HELM result.
