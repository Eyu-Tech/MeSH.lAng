# Research overview

The research question is whether defined symbolic addresses can preserve semantic relationships across interpretations and applications. The development record includes cold readings, explicit teaching, contextual shifts, composition and application probes.

According to the developer's account, development, use and evaluation of the language family have been ongoing since at least June 2026. The dated reports below are selected later checkpoints, including tests against the models available at those times; their dates do not mark the beginning of the work. This page is not an exhaustive development chronology.

This first publication draft summarizes selected existing reports. The source identifiers below connect the narrative to an internal provenance map. Raw prompts, full profiles and response archives are not bundled in this draft, so it is not yet a standalone reproduction package.

## Unprimed and explicitly anchored readings

**R1 — Prior-landscape study, 11 September 2026.** The report describes 128 Devanagari units examined in nine fresh sessions: three Terra-low, three Sonnet-adaptive-low and three Sonnet-off sessions. Under the minimal prompt, dominant readings were mostly character names, phonetic values or Unicode-like classifications.

**R2 — Anchored study, 11 September 2026.** Three few-shot examples and nine explicit operator anchors preceded the same inventory in fresh sessions. All nine sessions matched all nine explicitly taught target readings; the report records 0/9 target matches in their unanchored counterparts.

This establishes a local effect of explicit anchoring in the tested conditions. The joint contribution of examples and definitions was not isolated. It also explains why language definition and selected priors belong together in this approach.

## Context, position and semantic direction

**R3 — Field-tilt study, 11 September 2026.** The main report covers three semantic directions, anchor counts of zero, three and nine, and two anchor positions for nonzero conditions. It reports 45 runs across the three model conditions. Two runs were refusals; the rest were complete.

The study explores how interpretations shift when the semantic frame and placement of anchors change. Its lexical field counts are indicators of response content, not direct measurements of model weights.

## Teaching and application

**R4 — Consolidated audit, 15 September 2026.** The audit distinguishes inventories, experimental runs, derived projections and technical controls. Selected findings include:

| Probe | Reported finding | Meaning of the count |
|---|---|---|
| Taught glyph readings in the Terra ladder | 741/745 evaluable responses preserved the reference core | Four readings narrowed the reference; 747 were planned and two were technically missing |
| Fully taught applications | 119/120 relations preserved | These are interpreted relations |
| Consequences in fully taught applications | 120/120 fitted the unfolded relation | Proposed consequences, not executed work processes |
| Applications without full teaching | 85/96 unresolved; 11/96 generically shifted | These do not establish preservation of the target relation |

These findings support the usability of taught semantic addresses in those probes. The audit identifies functional retention after one introduction across a session as a distinct next research question; cold repetitions do not answer it.

## Cross-provider development

The development history includes Gemini, Claude and OpenAI models through Codex. **R5**, a June 2026 Claude/Gemini trajectory comparison, records both convergence and divergence in the wider crY/dRy/moQ research lineage. It is a historical comparison rather than a matched third provider arm in R1–R4.

Provider, exact model version, harness, teaching exposure and task must accompany a comparison. A family label in an older report is retained here as its recorded label rather than expanded into an unverified current model ID.

## What matters in evaluation

The primary outcomes are intended-relationship preservation, contextual interpretation, transfer and subsequent behavior. Intrinsic and contextual readings are kept separate. Blind comparisons and explicit reference relationships help distinguish functional agreement from similar wording.

Token counts can be recorded as a secondary measure. They do not define success for semantic addressing.

## Source register

| ID | Existing source report |
|---|---|
| R1 | Stage 1: raw Devanagari prior landscape, 11 September 2026 |
| R2 | Stage 2: anchored Devanagari prior landscape, 11 September 2026 |
| R3 | Directed field tilt, main run 001, 11 September 2026 |
| R4 | Consolidated dRy audit, 15 September 2026 |
| R5 | Claude/Gemini cross-provider movement comparison, consolidated 17 June 2026 |

Raw response excerpts for R1–R5 remain to be selected without disclosing the withheld language tables. The separate [public handoff fragment](../examples/public-fragment/README.md) now supplies a fully specified small example and evaluation materials; it does not retrospectively reproduce R1–R5. No new model experiment was run to prepare this summary or the fragment. See the [semantic reproducibility protocol](semantic-reproducibility.md) and [clean-room testing guide](clean-room-testing.md).

## From language probes to implemented processing

The [Webstuhl and Geotopie measurements](webstuhl-geotopie.md) show calibrated symbolic comparisons, paired trajectories and native tensor/storage examples. The [correction-transfer case](../case-studies/correction-transfer.md) connects stored records, source-bound analysis and context delivery with a later changed action in its recorded technical scope.
