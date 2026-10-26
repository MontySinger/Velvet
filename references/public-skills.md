# Public writing skills: comparison and reusable lessons

Reviewed 2026-10-26. Scope: ten sources, comprising skill entrypoints in nine distinct public repositories and one author's process walkthrough. This is an implementation review, not an exhaustive audit of every repository file, a popularity ranking, or a comparative generation benchmark. Related humanizer projects may share ideas or ancestry; distinct repositories do not necessarily represent independent approaches.

| Source | Approach observed | Useful design choice |
| --- | --- | --- |
| [blader/humanizer](https://github.com/blader/humanizer/blob/main/SKILL.md) | Pattern-based editing with sample matching and a meaning check | Let the user's sample override generic pattern advice, including punctuation preferences. |
| [milock/humanizer](https://github.com/milock/humanizer/blob/main/SKILL.md) | Channel detection, author or brand profile, structural scan, rewrite and audit | Resolve whose voice applies; edit structure before swapping vocabulary. |
| [hannsxpeter/humanizer](https://github.com/hannsxpeter/humanizer) | Cleanup plus voice matching from samples or a project guide | Make customization reusable through a profile rather than repeating all guidance each time. |
| [Sam Dumont's voice-skill walkthrough](https://dropbars.be/blog/building-custom-voice-skill-claude-code/) | Corpus analysis across formats followed by iterative calibration | Distinguish personal habits from channel conventions; review inferred rules with the writer. His sample-count thresholds are practitioner heuristics. |
| [rangrot/mydamnvoice](https://github.com/rangrot/mydamnvoice/blob/main/SKILL.md) | Interview, sample analysis, profile synthesis and export | Combine what people say they want with evidence from examples; provide a portable profile. |
| [obra/the-elements-of-style](https://github.com/obra/the-elements-of-style/blob/main/skills/writing-clearly-and-concisely/SKILL.md) | Composition principles drawn from Strunk: specific language, active voice, related words together, fewer needless words | Add a clarity check while preserving intentional rhythm and genre. This is a general copyediting skill, not a personal voice profiler. |
| [affaan-m/ECC brand-voice](https://github.com/affaan-m/ecc/blob/main/.agents/skills/brand-voice/SKILL.md) | Source-derived reusable profile; recent examples; public and private modes; observable features such as question frequency | Keep a compact profile that other writing workflows can consume. Its author-specific defaults should not become everyone's voice. |
| [brand-voice-pass submission in microsoft/cat-agent-skills](https://github.com/microsoft/cat-agent-skills/blob/main/submissions/brand-voice-pass/SKILL.md) | Editing that preserves argument, evidence, confidence, terminology and regional language | Check meaning drift and language variant independently of stylistic cleanup. Hosting in a Microsoft repository is not proof of endorsement or measured effectiveness. |
| [naomimetzger/brand-voice](https://github.com/naomimetzger/brand-voice/blob/main/SKILL.md) | Short setup interview, favorite examples, mechanical habits, CTA preferences and preferred collaboration mode | Record how the creator wants to collaborate as well as how they write. Preserve characteristic spellings when intentional. |
| [spuvr/humanizer](https://github.com/spuvr/humanizer/blob/main/SKILL.md) | Reader-oriented editing emphasizing rhythm, specificity and less redundant explanation | Use reader knowledge to decide what explanation earns its place. Treat its broad claims about human and AI writing as editorial opinions, not scientific findings. |

## Additional choices adopted after the expanded review

- Match the requested regional spelling and protect required terminology during editing.
- Use audience knowledge to remove redundant explanation without deleting information the reader needs.
- Prefer current examples, unless the user identifies an older sample as the better target.
- Keep collaboration preferences in the profile: materials versus drafts, hooks authored by the user, and revision scope.

Some of these were already present in Velvet; repeated advice reinforced them without requiring additional rules. We did not import entire skills, author-specific bans, or prose examples.

## Commonalities worth using

1. **Use evidence.** Samples can ground preferences in actual wording. Interview answers add intent, but do not prove habitual behavior.
2. **Separate person from situation.** A stable voice guide needs channel- and relationship-specific choices. An email and a spoken script require different calibration.
3. **Describe behavior.** Sentence rhythm, openings, concrete detail and information order are more actionable than a lone adjective such as authentic.
4. **Review meaning separately.** A smoother rewrite can still invent a fact, erase uncertainty or change the ask.
5. **Calibrate with the writer.** Treat inferred characteristics as hypotheses. Use explicit corrections and save their scope.

These are our synthesis of implementation patterns, not experimentally established rankings of what matters most.

## What not to inherit automatically

- Universal word or punctuation bans: the user's intended style and context can justify them.
- Invented anecdotes, opinions or numbers used to manufacture personality.
- Exact sample minimums presented as validated requirements.
- AI-detection scores presented as evidence that the user likes the output.
- Multiple reviewers by default: begin with one focused check; add review only for an identified failure.
- Creator testimonials or repository popularity presented as independent outcome evidence.

## Scientific boundary

[Wang et al., Findings of EMNLP 2025](https://aclanthology.org/2025.findings-emnlp.532/) evaluated personal-style imitation across more than 400 authors and several domains. The tested models approximated some structured formats more effectively than nuanced informal writing. This supports testing on the actual genre and writer; it does not validate these skills or guarantee our workflow succeeds.

## Transfer beyond writing

For other skills, separate **examples**, **standing rules**, and **task context**. Turn broad objectives into observable choices. Keep checks specific to the failure being prevented. Treat user corrections as evidence with scope, and test on new tasks rather than reproducing the calibration examples.
