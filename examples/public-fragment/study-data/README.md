# Public handoff study data

This attachment contains eight synthetic cases, four carrier conditions, 64 sender-to-recipient handoffs, and 128 unedited model answers. It is the completed study's reproducibility set. The package exposes these cases as reproduction material, so they must not be treated as held-out cases in new evaluations.

The original run used one model, `gpt-6-luna` with medium reasoning, for two fresh invocations per handoff. The same public primer, case facts, role tasks, and output format were used across conditions. Every case has two repetitions. Repetitions of a case are not independent cases.

## Files

- `primer.txt`, `sender.txt`, `receiver.txt`: the complete public teaching context and role tasks used by participants.
- `cases.json`: the exact participant-visible fact block for each case.
- `carriers.json`: the four condition carriers for each case. Natural prose, structured prose, dRy, and dRy with a context gloss express the same intended process relation.
- `trials.json`: the frozen execution order, condition, repetition, answer filenames, and prompt hashes.
- `answers/`: the 128 original sender and recipient answer files, copied byte for byte.
- `gold.json`: the expected facts and process route fixed before the answers. This is evaluator material.
- `scores.json`: six recipient checks for every trial, process failure reasons, and a separate carrier delivery result.
- `manifest.json`: source and export hashes for every answer and hashes for the public inputs.

## Exact prompt recipe

Read all text files as UTF-8. Concatenate with LF (`\n`) exactly as shown, retaining each file's existing trailing newline. No gold, score, another trial's answer, or original case file goes into a recipient prompt.

```text
sender_prompt =
  "Public teaching context:\n" + primer.txt
  + "\n\nProcess carrier:\n" + carriers[case_id][condition]
  + "\n\nCase facts:\n" + cases[case_id].facts_text
  + "\n\nSender task:\n" + sender.txt

receiver_prompt =
  "Public teaching context:\n" + primer.txt
  + "\n\nSender response:\n" + raw_sender_answer
  + "\n\nRecipient task:\n" + receiver.txt
```

Use one new sender invocation and one new recipient invocation for each trial, without resuming or forking a previous conversation. The recipient sees only its constructed prompt. The original answers were not edited or repaired. Compare generated prompt SHA-256 values with `trials.json`. A process error or invalid answer stays in its assigned trial; do not silently replace it.

## Scoring and limits

The six checks cover exact current goal and revision, current decision with superseded history, foreign scope, unresolved information, directed State/Trajectory relation, and a next step that follows the current decision while preserving unknowns. Paraphrases are allowed when meaning, group order, scope, and direction are preserved. Invented symbolic groups are process errors even when neighboring prose sounds similar. The carrier delivery check is separate from recipient meaning.

All six checks passed in 12/16 natural prose, 14/16 structured prose, 13/16 dRy, and 16/16 dRy with gloss trials. In 12 of the 16 gloss trials, senders omitted the gloss from their copied `process_carrier`; the dRy chains remained intact. Thus the gloss condition's recipient result must be read with a 4/16 exact carrier delivery rate. Omission refers to the copied `process_carrier` field: all twelve affected recipient inputs still included the sender's prose `state_reading`, `trajectory_reading` and `handoff`. These are successful mixed chain-and-prose handoffs, not demonstrations of a chain-only recipient input. The study used a taught primer; case facts explicitly named the current decision. It is a small one-model comparison, not evidence of a general language advantage. The reviewers were not blind to condition.

No execution events, receipts, stderr, account details, host information, or private language tables are part of this public attachment.
