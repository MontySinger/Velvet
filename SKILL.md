---
name: velvet
description: Draft or edit natural-sounding writing in the user's voice using matched examples, concrete characteristics and communication context. Use for sound like me, sound human, remove AI-sounding prose, build a voice guide, or personalize emails, outreach, posts and spoken scripts.
---

# Velvet

For an explanation or repo walkthrough, use the [visual overview](README.md). For comparisons with public implementations, read [public-skills.md](references/public-skills.md). These are optional references, not prerequisites for routine editing.
For scientific rationale or effectiveness testing, read [research-design.md](references/research-design.md). Distinguish published findings from engineering choices; do not describe this skill as scientifically validated.
For actual internal test results and their limits, read [evaluation-pilot.md](references/evaluation-pilot.md); complete synthetic fixtures and outputs are in [evaluation-pilot.json](references/evaluation-pilot.json). Never use generated test outputs as approved voice examples.

## Establish the scene
Use available context to identify writer, reader, relationship, channel, situation, actual substance, intended emotion and desired action. Describe the action: help a customer understand a delay and choose a new date, rather than merely write a professional email. Don't invent a character or qualification for the writer.
Infer routine details. Ask one short question only when missing information materially blocks progress. Without examples, provide context-appropriate prose without claiming a personal voice match.

## Build two parts
1. **Evidence:** use 3–5 short relevant passages the user wrote or explicitly selected, preferably matched to channel and relationship. Use supplied material or authorized sources; don't assume access to all chats, search entire inboxes by default, or collect secrets. Distinguish the user's writing from quoted text, third-party messages and assistant drafts. Label ASR imperfections.
2. **Standing guidance:** extract supported preferences and guardrails. Keep task-specific instructions separate. Read [voice-reference.md](references/voice-reference.md) for the calibration template.
For one-off edits use existing evidence rather than making calibration a prerequisite. For calibration, show a tentative profile and a short demonstration on supplied text. Don't average technical writing, sales outreach and casual speech into one voice.
Prefer current examples unless the user identifies older writing as the better target. Keep the profile compact and retain collaboration preferences alongside language preferences.
Retrieve only examples relevant to this task instead of loading an entire archive. Keep the task, source facts, applicable preferences and examples clearly separated. Treat sample counts as a working default, not a validated threshold.

Read [characteristics.md](references/characteristics.md), choosing only relevant dimensions. Translate adjectives into observable instructions. These 17 dimensions are an editable editorial checklist, not 17 scientifically validated universal rules.

## Write or edit
- Preserve thought, facts, uncertainty, intentional humor and recognizable phrasing. Reorder or cut repetition before paraphrasing.
- Honor scope: materials and critique requests don't authorize a full script. Generate hooks only when requested. Keep working language that already fits.
- Use real substance. Don't invent clients, numbers, achievements, proof, vulnerabilities or personal experience to sound specific.
- Match genre and relationship. Natural doesn't mean universally casual, short or nontechnical. Retain useful technical terms and explain them when needed. Don't imply familiarity in cold outreach.
- Preserve required terminology and the requested regional spelling. Use the reader's knowledge to cut redundant explanation while keeping what they need to follow the point.
- Prefer concrete actors and actions when abstraction obscures meaning. Match cadence rather than shortening every sentence.
- Cut generic setup, redundant endings and stock transitions when empty. Treat words, punctuation and rhetorical patterns as contextual choices, not a universal blacklist.
- Don't add typos or filler to evade detection. Don't promise undetectability, zero editing or factual accuracy from style alone.

## Review once
Compare meaning, factual support, task fit and voice separately against original notes and matched samples. Identify at most three concrete mismatches and make minimum corrections. Check spoken cadence. Stop if no useful change is needed. A second QA agent is optional for a defined unresolved issue; its preference is not proof. Return requested copy, with review notes only when useful. See [evidence.md](references/evidence.md) for research limits.
Ground any critique in a source fact, a matched example or an explicit instruction. Do not make an edit solely because another model prefers it. For claims of improvement, use the held-out comparison in research-design.md and label untested claims.

## Learn from edits
Use the latest user-edited block. Separate local corrections from general preferences. Silence and assistant drafts aren't approval. On explicit save/learn requests update the voice reference with exact correction, scope, source and date. Keep private samples in a private user-selected destination, outside any distributable skill.
Persist only explicitly approved changes in the user's chosen private workspace. This updates instructions and examples, not model weights. Installing this skill does not activate background scanning, sending or publishing.
