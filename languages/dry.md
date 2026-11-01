# dRy

dRy is a language for semantic addressing between AI agents. It uses Devanagari-based operators and directed bindings to express a disposition or a movement that a model can unfold in context. The [script-selection rationale](../concepts/semantic-addressing.md#why-a-shared-writing-system-matters) explains the aesthetic and process-addressing design.

dRy grew out of crY and carries forward its crystallization lineage. The **D** points to **Devanagari**, the writing-system frame selected for this line. The capitalization in crY, dRy and Bry is deliberate; see [the naming lineage](../concepts/names.md#language-names-and-capitalization).

Its aim is a **semantic invariant**: preservation of an intended relationship across different interpreters, even when their natural-language formulations differ.

The intended steady-state agent-mesh form is a chain without a repeated contextual gloss. The participants share the relevant language and working-context bindings and communicate about the process relation in what they are jointly examining. The operator-facing State/Trajectory surface currently includes a gloss to make that contextual unfolding visible. See [shared-context communication](../concepts/shared-context-communication.md).

## A complete small public fragment

The [handoff proof of concept](../examples/public-fragment/README.md) supplies three operator readings, two vectors and every instruction needed for its sample cases. It can be tried without the full profile or an LSP. Its version label is an example boundary, not a replacement full-language parser profile. The [evaluation protocol](../research/semantic-reproducibility.md) separates form, relation preservation and subsequent action.

## Public structural description

A chain has an opening marker, bound groups, relationships between groups and a closing marker. Operator material appears on the left of a binding; directional material appears on the right. The complete inventory and mapping are outside this public draft.

The surrounding registers distinguish:

- **sigma (σ):** state or disposition;
- **tau (τ):** trajectory (movement or transition).

These labels provide context around the chain. They are not additional operators inside it.

## Reading and context

The reading procedure distinguishes an intrinsic unfolding under the language definition from a contextual unfolding under a stated task. Recording both makes it possible to examine what remains stable and what shifts.

A reader who has already received a teaching primer cannot retrospectively supply an unprimed first response. Such a probe requires a fresh condition.

A contextual gloss makes the current application of a process relation explicit. A chain plus gloss carries a process address together with a small contextual explanation. When that context is already shared and resolvable, agents can use the chain without repeatedly carrying the explanation. A gloss remains part of the supplied information whenever it is present.

The [State and Trajectory example](../examples/state-and-trajectory.md) uses an inline gloss for a compact presentation. A separated record can instead keep the chain, intrinsic gloss and contextual gloss in distinct fields.

## What the studies examine

The research includes unprimed readings, explicit anchors, changes in semantic frame, interpretation of compositions and transfer after teaching. The [overview](../research/overview.md) reports selected findings and their experimental conditions.

The implementation presented here is one concrete realization of the broader semantic-addressing concept. A full profile and its tooling can be distributed under separately agreed terms; this draft does not include them.
