# Internal pilot — October 26, 2026

The skill was named Own Voice when this pilot ran; Velvet is its subsequent name. The tested instructions were not changed by renaming.

## What ran

Six synthetic writing assignments, each generated once in three fresh agent sessions: a basic task prompt, the same prompt with selected examples, and the full Velvet skill with those examples. Eighteen outputs total. Tested skill commit: `d7ee3d0`.

The agents inherited the same parent model configuration. Exact sampling settings were not captured. The parent agent reviewed outputs with condition labels visible. This was not a blinded human evaluation. All style targets were synthetic assistant-authored passages; they do not establish Monty's voice.

## Results

| Task | Main check | Basic | Examples | Full skill |
| --- | --- | --- | --- | --- |
| T1: client delay email | Friday stays provisional; access request and post-test confirmation remain | Pass | Pass | Pass |
| T2: cold email | No invented relationship, detected error or savings | Pass | Pass | Pass |
| T3: personal reflection | Preserve supplied event and personal uncertainty | Pass | Pass | Pass |
| T4: punctuation-only edit | Preserve original phrasing, humor and scope | Pass | Pass | Pass |
| T5: spoken explanation | Retain required term, example and limitation | Pass | Pass | Pass |
| T6: planning materials | Exactly four body bullets; no hook or script; time savings remain untested | Pass | Pass | Pass |

All outputs met their word limits. Assertions checked word limits, exact T4 preservation, T5 required terminology, T6 bullet count and untested-status statement. Parent inspection checked remaining facts and scope. Pass means these checks passed; it is not a validated naturalness score.

## Observations

- The full-skill cold email was 31 words, versus 39 with examples and 48 with the basic prompt under the recorded counting convention. Shorter does not establish better.
- Both example-conditioned personal posts echoed the examples' dry humor. This is qualitative observation, not a measured personal voice match.
- The full skill added a low-information gloss of probabilistic model: "one that works with probabilities." The other two outputs were more economical on this phrase. That is a candidate for human review, not proof the full output is worse overall.
- All three arms left the punctuation-only passage unchanged.
- The full-skill agent reported one review pass with no concrete changes. No intermediate draft was captured to independently inspect that report.

## What this establishes

The skill can be loaded and followed on these synthetic tasks. No factual or scope failure was identified in this run. The basic prompt was already strong: the common task packet explicitly requested factual preservation and scope compliance. This pilot therefore does not demonstrate an advantage over a well-specified prompt.

It does not validate Monty's voice, measure editing time, prove consistent improvements across runs, test saved-preference retrieval across sessions, or verify automatic transcript ingestion.

## Next evaluation

Use authorized, verified examples of the actual writer's email, posts and speech. Keep new target tasks separate from calibration examples. Have the writer assess shuffled outputs for personal fit, factual fidelity and substantive edits. Compare reviewed and unreviewed versions before adding extra reviewers. For a regression test, specifically check whether explanations of technical terms add meaning rather than repeat the term.

Complete prompts, synthetic examples, outputs, counts and limitations are in [evaluation-pilot.json](evaluation-pilot.json). These outputs are test artifacts, not approved writing examples or user preferences. Do not use them to calibrate the user's voice.
