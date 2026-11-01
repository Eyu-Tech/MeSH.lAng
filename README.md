# MeSH’lAng

**Shared process references for AI agent workflows.**

When a task or decision changes, another agent needs to recover what is current, which relationships matter and what should happen next. MeSH’lAng explores **semantic space addressing through defined priors**: a model interprets a language-defined expression within the working context, and different agents can unfold it while preserving the intended process relationship.

Developed by **Jonathan Honnert**, system architect. Questions, implementation inquiries and reports of what you build are welcome at [j.honnert@outlook.com](mailto:j.honnert@outlook.com).

## Start with your agent

> Read START-HERE.md. Explain what I can do with this repository. Help me choose a small example, guide me through it when I ask, and explain what its result demonstrates.

The [guided entry](START-HERE.md) serves people and agents. No installation, private language server or surrounding framework is needed for the public examples.

- **Try a fluent prompt:** use the [moQ’eX guide](languages/moqex/README.md) to structure a task and ask a model to carry it out.
- **Test a handoff:** run the [complete small dRy exercise](examples/public-fragment/README.md) in fresh sender and recipient conversations. The package includes every definition used in that exercise.
- **Inspect the evidence:** read the [handoff comparison](research/public-comparison-20261101.md), [original answers and scoring](examples/public-fragment/study-data/README.md), or the separate [token measurements](research/token-load-20261101.md).

## What the languages do

| Part | Role | Available here |
|---|---|---|
| [moQ’eX](languages/moqex/README.md) | A fluent builder-style prompt notation for tasks and workflows | Specification, primer, reference and examples |
| [dRy](languages/dry.md) | Process orientation, State and Trajectory through defined symbolic expressions | Concepts and a complete limited handoff exercise |
| [crY](languages/cry.md) | Mathematically oriented operations and architectural composition | Conceptual introduction |
| [Bry](languages/bry.md) | Exploration of a Bengali-script form | Overview of the conceived/explored line |

The family addresses [composable semantic spectra](concepts/semantic-addressing.md#composable-semantic-spectra): selected process relationships, operations and interpretive frames. Each language keeps its own definitions. The model interprets the notation; this repository does not supply a universal mixed-language runtime.

## Why a process language?

The aim is shared attention: agents refer to the relationship that matters in what they examine together. With a shared language definition and working context, the intended mesh mode exchanges process addresses without repeatedly spelling out their contextual gloss. A glossed State/Trajectory record makes that interpretation visible to the operator. See [shared-context communication](concepts/shared-context-communication.md).

The developer reports needing less carefully reconstructed prompts and fewer manual course corrections after context delivery and glossed records became stable. That operating experience motivates the architecture alongside the separately reported experiments. Token reduction is not its defining benefit.

## Concepts, applications and research

- [Semantic space addressing and script choice](concepts/semantic-addressing.md)
- [Process and context contract](concepts/process-and-context-contract.md)
- [Language, memory and runtime](concepts/language-memory-runtime.md)
- [Webstuhl: an analysis architecture across backends](case-studies/webstuhl.md)
- [Webstuhl and Geotopie measurements](research/webstuhl-geotopie.md)
- [Correction transfer into a later agent action](case-studies/correction-transfer.md)
- [Research overview](research/overview.md), [evaluation protocol](research/semantic-reproducibility.md) and [clean-room guide](research/clean-room-testing.md)

Development and evaluation have been ongoing since at least June 2026 according to the developer's account. The research pages describe selected checkpoints and their model conditions. Webstuhl and Geotopie illustrate the larger architectural use; their private implementations are not dependencies of the public exercise.

## Names, origin and reuse

The names identify parts of the work. [Their meanings and capitalization](concepts/names.md) are optional background, along with [LamutikA](concepts/lamutika.md), the private originating process language, and the EtheReoN framework. The artistic signature **EyU PaTanA RaMaSH** may be used voluntarily; **Jonathan Honnert** is sufficient for creator attribution.

The original publication content is offered under **CC BY 4.0**. See [LICENSE.md](LICENSE.md), [citation guidance](CITATION.md) and [access and collaboration](ACCESS.md). Complete private profiles, full dRy/crY tables, LSP implementations and LamutikA are outside this publication.
