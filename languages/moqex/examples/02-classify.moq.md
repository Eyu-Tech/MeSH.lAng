// Few-shot classification with reasoning, validation, structured output.

moQ.instruct("Classify these tickets by urgency.")
   .fewShot([
     { in: "Server down", out: "P0" },
     { in: "Typo in footer", out: "P3" }
   ])
   .reason("analyze")
   .validate("each ticket has exactly one level")
   .end("json")
