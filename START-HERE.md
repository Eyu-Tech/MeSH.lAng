# Start here: understand, try, evaluate

This repository contains language concepts and examples for AI agents. Start with the task you want to accomplish. The public exercises include their required definitions and need no private profile, LSP or surrounding framework.

## Choose a route

| What you want | Start here | What to expect |
|---|---|---|
| Understand the idea | [README.md](README.md), then [semantic addressing](concepts/semantic-addressing.md) | An explanation of process references, their meaning and context |
| Structure a task | [moQ’eX guide](languages/moqex/README.md) and [primer](languages/moqex/PRIMER.md) | A model-produced result following a fluent prompt chain |
| Inspect State and Trajectory | [Worked expression](examples/state-and-trajectory.md) | A contextual interpretation of a process expression |
| Test transfer to a fresh agent | [Public dRy handoff guide](examples/public-fragment/README.md) | Frozen sender/recipient answers and six separately reported checks |

If someone asks for an explanation, explain first. Run an exercise when requested.

## Explain the idea

A language definition selects operative readings from a model's learned associations. An expression addresses a relationship in the context the agent has; it does not supply unavailable facts. Different agents can express that relationship in different words while preserving its function.

For the public examples, moQ’eX organizes task steps and dRy addresses process orientation and directed State/Trajectory relations. crY and Bry are described separately, without full public profiles. The [context contract](concepts/process-and-context-contract.md) explains definitions, referents, revisions and consequences. [Shared-context communication](concepts/shared-context-communication.md) explains glossed records and the intended exchange over shared bindings.

## Try the selected example

For moQ’eX, give the model the interpreter instruction and a chain. Check whether the requested artifact was produced and facts and assumptions remain distinct. The model interprets the prompt notation; this is not execution by a bundled software runtime.

For dRy, follow the example guide's exact role-specific input lists and output format. Use fresh participant conversations. A coordinator can prepare allowed inputs, but cannot treat its shared history as an independent recipient.

## Evaluate after the answers are frozen

Open the corresponding evaluator material only after both participant answers are frozen. Keep unknowns unknown; report each check as pass, fail or unscorable. Report copying of the process carrier separately from interpretation. Do not silently repair an answer or replace an unsuccessful run.

The [study report](research/public-comparison-20261101.md) and [attachment](examples/public-fragment/study-data/README.md) expose cases, raw answers and scores. The [protocol](research/semantic-reproducibility.md) explains the measurement boundary. The [token profile](research/token-load-20261101.md) separately describes text load.

Participant inputs for a new experiment must exclude its gold answers, scores and earlier responses. Included study cases are reproduction material, not unseen test cases.

## Explore further

The [family overview](README.md#what-the-languages-do), [composable semantic spectra](concepts/semantic-addressing.md#composable-semantic-spectra) and [naming background](concepts/names.md) provide further context. [Webstuhl](case-studies/webstuhl.md), [Geotopie measurements](research/webstuhl-geotopie.md) and [correction transfer](case-studies/correction-transfer.md) show applications around the language work.

For reuse, see [CC BY 4.0 terms](LICENSE.md) and [citation guidance](CITATION.md). Creator attribution as **Jonathan Honnert** is sufficient; the artistic profile name is optional. [Access and collaboration](ACCESS.md) describes private profiles and integration inquiries.
