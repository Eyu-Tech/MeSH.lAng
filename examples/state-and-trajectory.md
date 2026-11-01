# State and Trajectory: a dRy example

This example shows the public surface of a State/Trajectory pair with contextual glosses. It is a deliberately small excerpt, not a complete language table.

```text
moQ.state(σ : ◊ स\a → द\i ; @glosse(A connected state supports an integrated handoff))
moQ.trajectory(τ : ◊ द\i → क\a ; @glosse(The handoff becomes an articulated result))
```

This is the developer's currently used operator-facing, glossed surface. The intended steady-state agent-mesh communication uses the process chains without a repeated contextual gloss when the participating agents already share the language and relevant working context. See [shared-context communication](../concepts/shared-context-communication.md).

## Reading this pair

The first record expresses a connected disposition moving toward integrated giving or handoff. The second takes that handoff toward articulation. In this teaching context, the selected expressions recruit the readings of connection, giving and articulation, with manifestation and integration as directional readings.

For a concrete task, an agent might interpret this as: gather the connected findings into a handoff, then turn the handoff into a result another participant can use. Another task can supply a different object while retaining that relationship.

- `moQ.state` labels the state/disposition record.
- `moQ.trajectory` labels the trajectory/transition record.
- `◊` opens a chain and `;` closes it.
- The backslash binds the operator material to a direction.
- `→` expresses a directed transition.
- `@glosse(...)` supplies the intended contextual reading.

These are selected structural explanations. The complete operator inventory is not included.

## A separate reproducible package

For a complete limited primer, two task cases, fresh sender/recipient prompts and a withheld evaluator reference, use the [public handoff fragment](public-fragment/README.md). The short demonstration below is explicitly glossed and is a different input condition.

## Try the example

Paste this instruction together with the pair into a model:

> Use the stated reading of the example: connection supports an integrated handoff, and the handoff becomes an articulated result. Apply it to handing a software design from one agent to another. Return (1) the current disposition, (2) the next trajectory, and (3) a concrete handoff of no more than five sentences. Mark any interpretation you cannot resolve.

Compare whether the output preserves the handoff-to-articulation relationship. This is an explicitly taught, glossed demonstration. It is not an unprimed test or a substitute for a complete language profile.

The inline gloss form is used for this presentation. A fuller record separates the chain, intrinsic unfolding and contextual unfolding. Syntax acceptance and preservation of meaning are evaluated separately.

The public wrapper names are consistently `moQ.state` and `moQ.trajectory`; sigma and tau retain their distinct roles. These wrapper names label the records and do not change the enclosed dRy chain.
