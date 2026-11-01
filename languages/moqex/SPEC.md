# moQ'eX — Specification (v0.2-dev)

> Maintained within MeSH’lAng on the v0.2-dev language line. See [the guide](README.md).

A fluent prompt language: `moQ.verb(args).verb(args).end()`. Human → model.
Earlier source reports describe cross-vendor read validation (Claude · Gemini · GPT · DeepSeek). These historical statements are separate from the scoped [MeSH’lAng research](../../research/overview.md).

---

## 1. Shape

```
moQ                         entry, always
   .verb(args)              an operation (a step in the chain)
   .verb                    same as .verb() when it takes no argument
   .end() / .end            close
   .exec / .deliver()       run and return the result
```

Operators are chained left-to-right and read as a sequence. The chain *is* the prompt.

## 2. Two operator classes

### a) Structural core (closed, 13 verbs)

These configure the prompt. Stable, cross-vendor.

| Axis | Verb |
|---|---|
| start | `init` |
| context | `context` |
| instruction | `instruct` |
| examples | `fewShot` |
| reasoning | `reason` |
| branch | `branch` |
| iterate | `retry` |
| transform | `map` |
| constraint | `restrict` |
| validate | `validate` |
| format | `format` |
| meta | `critique` |
| terminal | `end` |

Full signatures: [`REFERENCE.md`](REFERENCE.md).

### b) Cognitive operators (open, extensible)

These turn a chain into a **thinking choreography** — structured reasoning the model
performs step by step:

```
hypothesis · assumptions · evidence · counterEvidence · unknowns · confidence ·
decision · challenge · findBlindSpots · revise · steelman · premortem · tradeoffs ·
secondOrderEffects · firstPrinciples · decompose · rootCause · falsify · reframe ·
analogize · extrapolate · invert · rank · calibrate · narrate · compress · next
```

Flow operators for choreography: `repeat(n, cycle => …)` · `fork([perspectives])` ·
`debate()` · `merge()` · `question("…")`.

**Extension rule.** Any operator that is a **transparent English cognitive verb** is
understood without definition (~95%). Avoid: abbreviations (`.rEq`) and names with a
strong foreign prior (`quantize` reads as *temperature*, not *reduce*).

## 3. Arguments

| Form | Example |
|---|---|
| positional | `.context("api docs")` |
| named (`key:`) | `.format(as: "json")` |
| object `{}` | `.validate(of: {request, response})` |
| lambda | `.map(f_x => "wrap " + x)` |
| none | `.reason` |

## 4. The 14 conceptual axes a complete chain covers

start · context · instruction · examples · reasoning · branch · iterate · parallelism ·
transform/query · constraint · validate · format · meta · terminal.

(Parallelism — `fork`/`merge` — is the weakest axis cross-vendor; treat as experimental.)

## 5. Execution

A model **describes** a chain by default. With the interpreter hat (see [`PRIMER.md`](PRIMER.md))
it **executes** it. `.exec` / `.deliver()` produce the real result.

## 6. Open points (toward v1.0)

- `.branch(cond, then, else?)` — `cond` is a host-side predicate evaluated before the call;
  if `else` is omitted, the chain continues unchanged.
- Order semantics — whether `.falsify.decide` differs from `.decide.falsify` needs convention.
- `.input(data)` for chains without `.from()`.

---

*moQ'eX — EthereoN · v0.2-dev (v0.1 tagged)*
