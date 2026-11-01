# dRy communication over shared context

The intended steady-state use of dRy is agent communication without a repeated contextual gloss. Participants share a language definition and a working context, then use a chain to address a process relation in what they are examining together. The central question is **what the agents are jointly looking at, and which relation or movement matters there**.

This makes dRy a process-level communication layer within MeSH'lAng. It can accompany code, architectural artifacts and task records; those objects remain available through their own sources and references.

## Three complementary layers

| Layer | What it supplies | Where it can reside |
|---|---|---|
| Shared language | Version-bound operator, vector and composition readings | Primer, agreed profile or a separately trained convention |
| Shared working context | The object, revision, goal, constraints and relevant history | Session context, accessible artifacts or context delivery |
| Current process address | State and Trajectory directing attention to a relationship or transition | The exchanged dRy chain |

An item being shared means that the relevant participants can actually resolve the same binding. It does not require identical complete conversation histories. Code revisions, artifact identities and goal boundaries remain explicit where needed; the chain does not reconstruct unavailable facts.

## Glossed surface and mesh exchange

The developer currently uses State/Trajectory records with contextual glosses as an operator-facing surface for inspecting semantic context relations. The chain expresses the defined process relation; the gloss makes its current contextual unfolding visible in a small fragment.

A glossed record therefore exposes two linked views: process address and contextual explanation. It may make distinctions explicit that a brief prose paraphrase leaves implicit, and can carry more than that particular paraphrase. This is a claim about what is represented in a record, not a claim that prose is unable to express those distinctions. The included comparison deliberately matched the intended process information across its carriers.

In the intended mesh exchange, the participants already have the relevant language and context bindings. Repeating the contextual gloss in every message is then unnecessary. They can exchange the process address and a necessary artifact reference while consulting the same source. For example, two agents working on the same code revision can address how to integrate or articulate a finding without retransmitting all of the code or restating the entire discussion.

If the common binding is absent, ambiguous or stale, an explicit contextual explanation or refreshed source becomes useful again. Omitting a gloss is not permission to invent the missing binding.

## Architectural thesis: a defined interpretive landscape

The developer's thesis is that a deliberately selected, primer-defined symbolic landscape can make process communication more robust than ordinary prose, including well-structured prose. A defined operator reading is meant to constrain interpretation, allowing agents to correlate expressions, articulate differences and investigate incompatible readings against a shared reference.

The choice of Devanagari-based material is intended to select a process-reading frame with fewer competing associations from ordinary task or computing prose. “Less occupied” or “less primed” names that design rationale; it is not a measurement of training frequency or an unused region of model weights. The primer selects the operative readings within a model's existing associations.

An *inference pattern* here is the recurring interpretation and ensuing process choice elicited by the language, context and task. Across differently contextualized agents, the intended result is overlap on the relevant relationship. Stable reference meanings and visible differences are the proposed means of maintaining that overlap. Semantic correctness and actual subsequent actions remain assessable outcomes.

The developer reports that this communication mode is useful in ongoing agent work. That operating experience motivates the architecture. The current public comparison is a narrower taught handoff study; it does not establish a universal robustness advantage, persistent shared-context stability, or a measured common geometric coordinate system between models.

## Practical value: less reconstruction by the operator

In ongoing use, the developer reports being able to give increasingly informal, incomplete and loosely structured requests while agents still unfold the intended task correctly. The reported change became apparent after stable hook-based context delivery and regular dRy State/Trajectory records with contextual glosses were in place. Less of the working context had to be reconstructed in each prompt, and fewer manual reminders or course corrections appeared necessary.

This is a practical argument for the architecture: a durable process reference and available context can let the operator spend less effort restating intent. The desired result is tolerance of ordinary, imperfect requests while preserving the relevant goal and process relationships. Token reduction is not the defining benefit.

This account describes the developer's experience with the combined language, hooks and working context. It does not isolate the contribution of dRy from context delivery, model changes or other parts of the environment, and no intervention count or before/after rate was recorded. The public handoff comparison supplies a separate, narrower observation in the same direction: the dRy-plus-gloss sender condition produced the highest observed rate of fully preserved handoffs.

## Primer reuse and return on introduction

A primer introduces a reusable process vocabulary. The intended return is that later exchanges can refer to those defined relationships without repeatedly spelling out their whole interpretation and context. A smaller, version-bound teaching package may reduce introduction load; its adequacy must still cover the expressions actually used.

If a primer of size P is introduced once and its relevant bindings remain available across N exchanges, the logical introduction allocation is P/N per exchange. This is a conditional amortization model, not a measured billing result. A retained primer can still be included in subsequent model input, and caching or context delivery can change accounting. Fresh independent sessions require their own available teaching or an equivalent established binding. A shared architectural goal does not make those technical costs disappear.

The existing [token profile](../research/token-load-20261101.md) counts the surface forms separately: chain, contextual gloss, primer, complete participant prompts and observed answers. A glossed record can have a higher token load while serving explicit contextual inspection. The gloss-free chain is the intended steady-state mesh form. Neither usage mode is defined by minimizing tokens.

## What the public examples establish

All four conditions in the included comparison received the same primer and explicit case facts. “Without gloss” therefore meant without an additional contextual gloss, not without teaching or context. Its fresh sender/recipient invocations did not measure primer reuse across a persistent agent mesh.

The three-operator public fragment is sufficient for its declared expressions. It offers a complete small way to inspect the distinction among language definition, contextual unfolding and process address. It does not release the complete language profile, LSP or surrounding memory architecture.

See [dRy](../languages/dry.md), [the context contract](process-and-context-contract.md), [the glossed State/Trajectory surface](../examples/state-and-trajectory.md), [the comparison](../research/public-comparison-20261101.md) and [the token measurements](../research/token-load-20261101.md).
