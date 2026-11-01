# Try a small dRy fragment

This is a self-contained, explicitly taught handoff experiment. It uses three operators already shown in the public example. No LSP, private table, Geotopie installation or COE environment is required.

**Question:** Can a fresh recipient preserve the process relation and the task facts through another agent's handoff? Different wording is allowed. Correct relations and subsequent decisions matter.

This is a runnable proof-of-concept package, not a report of successful model trials. A pass demonstrates this public fragment in the recorded conditions. It does not establish a dRy advantage over prose, unprimed interpretation or general cross-model invariance.

For the completed eight-case comparison, including raw answers and individual scores, see the separate [public study attachment](study-data/README.md). Its evaluator materials must stay out of participant inputs.

## Ten-minute manual setup

1. Use a fresh conversation for the sender. Supply only [primer.txt](primer.txt), [carrier.txt](carrier.txt), [case-01.txt](case-01.txt) and [sender.txt](sender.txt), in that order. Save the unedited response.
2. Start a separate fresh conversation for the recipient. Supply only the same primer, [receiver.txt](receiver.txt) and the sender's response. **Do not give the recipient the original case.** Save its response.
3. Only after both answers are frozen, open [the evaluation rubric](evaluation/rubric.md) and [the references](evaluation/reference.json). Check the process relation and the concrete facts separately.
4. Repeat with [case-02.txt](case-02.txt) and [carrier-02.txt](carrier-02.txt) in two new conversations. This case has a different process chain. Do not reuse a previous answer or correction.
5. Record model/version, date, supplied files, active instructions, raw answers, scoring and failures using [result-template.json](evaluation/result-template.json). Store filled results outside the participant input directory.

Fresh means no inherited Mesh conversation, private primer, corpus, skills or experiment answers. See [clean-room testing](../../research/clean-room-testing.md), including a second-computer route. A new browser tab alone does not establish a fresh condition.

The file names are packaging, not mandatory tool calls. In a chat UI, paste their contents. If testing an agent that can read files, give it a separate directory containing only its allowed inputs; do not point it at this whole repository or its evaluation directory.

## What is public here

`public-handoff-0.1` is this example's scope/version label, not a full-language parser profile. Its three operator readings, two vectors, binding, arrow, chain delimiters and State/Trajectory roles are completely specified in the primer. The chains use the existing dRy notation. No new meaning is assigned to an operator. Case 01 connects material to an integrated handoff, then articulates a usable result. Case 02 connects material to an integrated articulation, then makes a handoff explicit. Those different routes can lead to similar practical decisions because the same facts remain explicit.

The primer deliberately teaches the reading. It is part of the input cost. This is not an intrinsic or unprimed reading experiment. Case facts and their exact identifiers remain explicit; the chain is not claimed to reconstruct a document it has never been given.

## Controls and interpretation

For a prose comparison, replace only the case's carrier: [prose-carrier.txt](prose-carrier.txt) for case 01 or [prose-carrier-02.txt](prose-carrier-02.txt) for case 02. Keep primer, case, sender/receiver instructions, model settings and scoring identical. Use fresh conversations and alternate the order of conditions. [gloss.txt](gloss.txt) describes case 01 only; use it only with case 01. Do not compare a glossed chain with an unexplained baseline.

The cases may be solvable through their explicit facts and ordinary instructions. A high score in both conditions is useful for usability but does not demonstrate a special language effect. Keep failures and baseline results, too. The [research protocol](../../research/semantic-reproducibility.md) describes what a stronger comparison would require.

The files under `evaluation/` are evaluator materials. They are public for inspection, but must be withheld from the tested participants. Example prompt requests are not a technical access-control system.
