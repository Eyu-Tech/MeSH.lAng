// Simple — role, task, format. The minimal useful chain.

moQ.init("You are a travel advisor.")
   .instruct("Plan 3 days in Lisbon.")
   .context({ budget: "medium" })
   .format({ as: "markdown" })
   .end()
