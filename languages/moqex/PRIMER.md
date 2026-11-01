# Primer

Paste this block at the top of any chat. It teaches a language model moQ'eX in **one turn** —
by declaring what it is and showing the full syntax range at once (no rules needed).

```
moQ'eX := LLM-Prompt :: Fluent-API
moQ.verb.verb(value).end()
moQ.verb("value").verb(a: "valA", b: "valB").end.exec()
moQ.verb(a: "val", f_a => "use a here").exec
moQ.context("topic").instruct("do X").format(".md").validate(has: "examples").end.exec
```

That's it. After this block, the model reads moQ'eX natively.

## Make it *run*, not just describe

By default a model will *explain* what a chain would do (it sees code). To make it
**execute** the chain — each operator as a real cognitive step — give it the interpreter hat:

```
You ARE the moQ'eX interpreter. Run the chain below — each .verb() as a real
operation, not a description. On .end()/.deliver(), output the real result.
```

## Argument forms (all shown in the primer)

| Form | Example |
|---|---|
| positional | `.context("api docs")` |
| named | `.format(as: "json")` |
| object | `.validate(of: {functions, types})` |
| lambda | `.map(f_x => "wrap " + x)` |
| none | `.reason` ≡ `.reason()` |

## Brackets

Brackets around **arguments** stay (`init("X")`). Brackets on **empty** operators are
optional once the model is primed: `.reason.critique.deliver` ≡ `.reason().critique().deliver()`.

---

*moQ'eX — EthereoN*
