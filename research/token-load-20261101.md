# Token load of the handoff study material

This is a retrospective count of the existing public study material, not a new model experiment or a claim of token savings. The source is the [included study attachment](../examples/public-fragment/study-data/README.md); its manifest identifies the frozen inputs and answers. Model answers and semantic scores are unchanged.

## Measurement boundaries

The text counts use `tiktoken-rs 0.6.0`, ordinary-text encoding, with the explicitly named reference vocabularies `o200k_base` and `cl100k_base`. These are **not asserted to be the tokenizer of the tested gpt-6-luna model**. UTF-8 content is preserved without normalization. Each whole prompt is counted independently; separately counted parts need not add to an exact concatenated prompt count.

Vocabulary SHA-256:
- o200k_base: `446a9538cb6c348e3516120d7c08b09f57c36495e2acfffe59a5bf8b0cfb1a2d`
- cl100k_base: `223921b76ee99bde995b7ff738513eef100fb51d18c93597a113bcffe865b2a7`

The public prompt recipe reproduced all 64 original sender-prompt hashes and all 64 recipient-prompt hashes. Sender prompts repeated within a case/condition are counted once for their descriptive mean; all 128 frozen answers and all 64 recipient prompts are included. There are 275 non-smoke measurements in [the CSV](token-load-20261101.csv). The same measurement repeated byte-identically. All counted text passed encode/decode round-trip verification; empty text counted 0 and `hello world` counted 2 in both encodings.

## Process carrier only

Means over eight case carriers (four process routes, each appearing in two cases). The carrier includes the labels supplied in that condition; facts, primer and role instructions are excluded.

| Carrier | o200k_base mean (min–max) | cl100k_base mean (min–max) |
|---|---:|---:|
| Natural prose | 38.75 (37–41) | 39.50 (38–41) |
| Structured prose | 37.50 (36–39) | 39.25 (38–40) |
| dRy | 26.00 (26–26) | 28.50 (28–29) |
| dRy plus gloss | 62.50 (61–64) | 66.75 (65–68) |

The two dRy chains alone, with the State/Trajectory labels removed and one LF between chains, average 18.00 o200k tokens and 19.50 cl100k tokens. The isolated contextual gloss averages 33.50 and 35.25 respectively. These are different measurement boundaries, not alternative success scores.

The shared primer counts 292 o200k / 296 cl100k tokens. The sender task counts 186 / 184; the recipient task 190 / 188. Every study condition received the same primer. Thus “dRy without gloss” means **without an additional contextual gloss**, not an unprimed or context-free interpretation.

## Operating modes and primer reuse

The developer's current operator-facing State/Trajectory records include contextual glosses: a process address and its contextual unfolding are both visible. The intended steady-state mesh exchange uses chains without a repeated gloss when language and relevant artifact/goal bindings are already shared. These forms serve different communication needs; the glossed form is not an upper bound on what prose can express. The comparison carriers were designed to carry equivalent intended process information.

The primer is intended as reusable introduction. If introduced once and kept available over N exchanges, its logical introduction allocation is P/N; optimizing its teaching text may reduce P. This describes a possible amortization boundary, not an observed return on investment or a zero-cost retained context. Repeated API input, cache treatment, context refresh and language-version changes must be counted at their actual boundaries. The present study used fresh invocations and gave every condition the primer, so it did not measure this shared-context amortization. The intended return includes stable process reference and reusable interpretation, not only token reduction.

The same notation may therefore show lower or higher token load depending on whether the comparison includes only a chain, its gloss, teaching, artifact context or actual responses. See [the shared-context communication account](../concepts/shared-context-communication.md).

## Complete supplied text, using o200k_base

These counts include the actual primer, case/response and role instructions, but exclude the CLI's extra system/developer context, tool definitions and protocol framing. Means are over eight distinct sender prompts and 16 actual recipient prompts/answers per condition.

| Condition | Sender prompt | Recipient prompt | Sender answer | Recipient answer |
|---|---:|---:|---:|---:|
| Natural prose | 637.125 | 777.000 | 285.000 | 247.3125 |
| Structured prose | 635.875 | 789.875 | 297.875 | 275.3750 |
| dRy | 624.375 | 837.625 | 345.625 | 247.3750 |
| dRy plus gloss | 660.875 | 813.6875 | 321.6875 | 271.8750 |

A smaller carrier did not yield the smallest complete recipient prompt: the dRy senders produced longer answers in this dataset. This is a descriptive result, not a measured causal effect of the notation alone. Twelve of the 16 gloss-condition senders omitted the gloss from their copied carrier, so its observed recipient-prompt size does not represent uniformly complete gloss delivery.

## Historical client-reported usage

The original 128 calls reported the following means per call (32 calls per condition). Input includes cached input and the surrounding CLI context; this is a different boundary from the reference text counts above.

| Condition | Reported input/call | Reported output/call |
|---|---:|---:|
| Natural prose | 15170.12500 | 273.46875 |
| Structured prose | 15150.75000 | 295.62500 |
| dRy | 15192.06250 | 300.50000 |
| dRy plus gloss | 15147.96875 | 305.00000 |

The full study reported 1,941,149 input tokens including 1,632,384 cached tokens, and 37,587 output tokens. These are not the pure process-carrier load. Do not subtract the reference-encoding counts from these figures and call the remainder exact harness overhead: the model tokenizer mapping and full wire input are not established here. This measurement introduces no new model calls and does not measure costs or a semantic advantage.

See [the study result](public-comparison-20261101.md), [the exact public inputs](../examples/public-fragment/study-data/README.md) and [the evaluation protocol](semantic-reproducibility.md). Reference tokenizer context: [OpenAI tiktoken](https://github.com/openai/tiktoken); implementation used: [tiktoken-rs 0.6.0](https://docs.rs/tiktoken-rs/0.6.0/tiktoken_rs/).
