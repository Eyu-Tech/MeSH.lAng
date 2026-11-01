# moQ’eX: the explicit workflow layer

moQ’eX is part of MeSH’lAng. It is a fluent prompt notation: a person writes a chain of operations, and a language model interprets that chain and carries out the work.

Its familiar verbs address associations models already have about tasks and reasoning procedures. dRy addresses semantic orientation through a different notation; crY addresses mathematically oriented construction. This common idea of an interpretable expression connects the family.

## Language guide and reference

moQ’eX is maintained here as the explicit workflow member of MeSH’lAng. Its language area, including this guide, is offered under CC BY 4.0 in this edition:

- [Specification — v0.2-dev](SPEC.md)
- [Command reference](REFERENCE.md)
- [Primer and interpreter instruction](PRIMER.md)
- [Simple example](examples/01-simple.moq.md)
- [Classification example](examples/02-classify.moq.md)
- [Reasoning choreography](examples/03-reasoning-choreography.moq.md)
- [Current publication license](../../LICENSE.md)


This is the maintained moQ’eX language area within MeSH’lAng. The [research overview](../../research/overview.md) identifies the selected studies and their conditions.

## A first chain

```text
moQ.init("You are reviewing a software design.")
   .context("A producer passes records to a consumer.")
   .instruct("Identify the interface and its failure conditions.")
   .validate("Separate stated facts from assumptions.")
   .format({ as: "markdown" })
   .end()
```

Ask a model to act as the moQ’eX interpreter and carry out each operation, then paste the chain. Return the review rather than a description of the notation.

The notation itself needs no compiler or runtime. Editor tools and executable integrations can add capabilities around it.

## Two kinds of structure

The specification distinguishes a closed structural core of 13 verbs from an open class of cognitive operations such as challenging assumptions, comparing alternatives or revising a proposal.

A chain makes the sequence inspectable. It does not turn an instruction into a guaranteed result; validation still examines what was produced.

## State and Trajectory records

The [dRy example](../../examples/state-and-trajectory.md) uses `moQ.state(σ : ...)` and `moQ.trajectory(τ : ...)` as public record wrappers. Those wrappers label a state and a transition around a dRy chain.

The command reference also lists `.state` as an alias of `.context`. That original alias and a State record belong to different usage contexts. The record examples are a contextual presentation convention, not an addition of sigma/tau syntax to the moQ’eX command grammar.

The specification retains the imported language definitions. A unified executable profile for mixed-language records would need its own explicit version.
