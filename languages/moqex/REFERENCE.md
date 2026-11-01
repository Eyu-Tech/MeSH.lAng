# moQ'eX — Command Reference (v0.2-dev)

The 13 structural verbs, each with its signature. Argument convention: `"text"` = prose
for the model · `key: value` = named parameter · `[…]` = list · `{…}` = set · `?` = optional.
Aliases ride too (same meaning, same args).

---

### `.init(system?: string)` → Chain
Begin the chain; optionally set the system role/persona.
`moQ.init("You are a travel advisor.")`
*aliases:* `.start` · `.begin` · `.from` · `.prompt`

### `.context(data: object | string)` → Chain
Attach background knowledge / runtime data.
`.context({ budget: "medium" })` · `.context("uses Tokio 1.x")`
*aliases:* `.state` · `.scope` · `.memory`

### `.instruct(task: string)` → Chain
The primary instruction — what to do.
`.instruct("Plan 3 days in Lisbon.")`
*aliases:* `.role` · `.system` · `.task`

### `.fewShot(examples: [{in, out}])` → Chain
Few-shot examples for pattern sync.
`.fewShot([{ in: "Server down", out: "P0" }])`
*aliases:* `.examples` · `.template`

### `.reason(mode?: "analyze"|"infer"|"evaluate")` → Chain
Step-by-step reasoning (chain-of-thought).
`.reason("analyze")`
*aliases:* `.analyze` · `.cot` · `.infer`

### `.branch(cond, then: fn, else?: fn)` → Chain
Conditional branch. `cond` = host predicate (evaluated before the call); if `else`
omitted, chain continues unchanged.
`.branch(hasTests, s => s.instruct("Check coverage."))`
*aliases:* `.if(cond).else()`

### `.retry(n?: int, until?: string)` → Chain
Repeat the previous step.
`.retry(3)` · `.retry(5, until: "no new findings")`
*aliases:* `.iterate` · `.loop`

### `.map(fn)` → Chain
Transform / filter each element.
`.map(f => f.withSeverity())` · `.map("extract sentiment per row")`
*aliases:* `.filter` · `.reduce` · `.transform` · `.summarize`

### `.restrict(rule: string)` → Chain
Hard constraint / guardrail.
`.restrict("No speculation without a code line.")`
*aliases:* `.guard` · `.require` · `.forbid` · `.limit`

### `.validate(rule: string | schema)` → Chain
Check the result against a rule or schema.
`.validate("every ticket has exactly one level")`
*aliases:* `.verify` · `.assert` · `.ensure`

### `.format(spec: {as, schema?})` → Chain
Force the output format. *(Strongest verb — recognized by all vendors.)*
`.format({ as: "json", schema: "ReviewResult" })`
*aliases:* `.json` · `.markdown` · `.render` · `.output`

### `.critique(criteria?: string)` → Chain
Meta self-check before final output.
`.critique("Self-check: false positives removed?")`
*aliases:* `.reflect` · `.trace` · `.selfcheck`

### `.end(returnFormat?: string)` → Result
Close the chain, return the result. Terminal.
`.end()` · `.end("json")`
*aliases:* `.run` · `.build` · `.execute` · `.exec`

---

## One-line table

| # | Verb | Argument |
|---|---|---|
| 1 | `.init(system?)` | system prose, optional |
| 2 | `.context(data)` | object or prose |
| 3 | `.instruct(task)` | imperative prose |
| 4 | `.fewShot(examples)` | list `{in,out}` |
| 5 | `.reason(mode?)` | mode string, optional |
| 6 | `.branch(cond, then, else?)` | predicate + sub-chains |
| 7 | `.retry(n?, until?)` | count + stop prose |
| 8 | `.map(fn)` | transform fn or prose |
| 9 | `.restrict(rule)` | rule prose |
| 10 | `.validate(rule)` | prose or schema |
| 11 | `.format({as, schema?})` | format spec |
| 12 | `.critique(criteria?)` | criteria prose, optional |
| 13 | `.end(returnFormat?)` | format string, optional |

*moQ'eX — EthereoN · v0.2-dev (v0.1 tagged)*
