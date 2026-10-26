# Research-informed design

Reviewed October 26, 2026. Distinguish architecture, empirical findings, practitioner methods and our engineering choices. This skill has not been scientifically validated. Relevant evidence comes from machine learning and computational linguistics, not clinical trials.

## Model mechanism

Transformer attention constructs context-dependent representations. In an autoregressive language model, generation predicts successive tokens conditioned on the preceding context. Training and post-training influence the available patterns; a prompt can steer which patterns appear without updating the model's parameters. A saved writing guide is persistent context supplied by a system, not retraining.

Sources: [Vaswani et al., Attention Is All You Need, NeurIPS 2017](https://arxiv.org/abs/1706.03762); [Brown et al., Language Models are Few-Shot Learners, NeurIPS 2020](https://arxiv.org/abs/2005.14165). The former establishes the architecture; the latter demonstrates task conditioning through text examples without gradient updates. Neither establishes a universal recipe for natural personal writing. Do not attribute all stylistic habits to attention or next-token prediction alone.

## Findings mapped to choices

| Evidence | Finding in scope | Our design choice | Limit |
| --- | --- | --- | --- |
| Brown et al. (2020), linked above | GPT-3 performed numerous tasks using text instructions and examples without fine-tuning | Include relevant examples alongside explicit instructions | Not proof that 3–5 examples is optimal or that voice is faithfully reproduced |
| [Wang et al., Findings of EMNLP 2025](https://aclanthology.org/2025.findings-emnlp.532/) | Personal-style imitation varied by domain; nuanced informal writing remained challenging | Maintain separate modes and test on unseen tasks from each intended genre | Does not validate this skill or establish that explicit profiles solve the problem |
| [Liu et al., Lost in the Middle, TACL 2024](https://aclanthology.org/2024.tacl-1.9/) | Relevant-information position affected retrieval and question-answering performance in tested long contexts | Retrieve a small relevant subset; keep task, facts and applicable rules easy to locate | Extrapolation to writing is an engineering hypothesis; effects vary by model and task |
| [Zamaraeva et al., ACL 2025](https://aclanthology.org/2025.acl-long.443/) | Six models' generated NYT-style text differed syntactically from human NYT text | Evaluate rhythm and structure as well as vocabulary | News-domain evidence does not define universal human-writing rules |
| [Madaan et al., Self-Refine, NeurIPS 2023](https://arxiv.org/abs/2303.17651) | Iterative self-feedback improved results across the authors' tested tasks | Permit targeted feedback followed by revision | Does not prove a second agent improves this user's voice |
| [Kamoi et al., TACL 2024](https://aclanthology.org/2024.tacl-1.78/) | Survey identifies serious limits to prompted self-correction and stronger conditions involving reliable external feedback | Ground critique in original facts, matched samples and explicit user corrections; keep human evaluation | A model-generated review is not independent verification |

These are design motivations and limits. The specific combination, review limit and sample working set are choices to evaluate, not conclusions directly established by the papers.

## The combined workflow

1. **Resolve the task.** Identify reader, relationship, channel, actual facts, intended feeling and requested action. Infer routine details; ask only about material gaps.
2. **Retrieve matched examples.** Select relevant passages from an authorized archive, with provenance. Use a compact profile rather than the entire archive. Do not use private examples in a shareable package.
3. **Choose applicable characteristics.** Turn broad traits into a few observable directions. Keep standing preferences separate from this task's scene. Avoid contradictory rules and universal punctuation bans.
4. **Draft within the facts.** Keep numbers, commitments, uncertainty, point of view and required terminology intact. Preserve useful original phrasing. A realistic scene supplies communication context, not invented identity or experience.
5. **Check distinct failures.** Compare meaning with the factual source, voice with examples, and task fit with the scene. Correct up to three concrete mismatches. Stop when no useful correction is identified.
6. **Learn from explicit feedback.** Record approved general preferences with source, date and scope. A correction to one email is not automatically a global rule. No approval is inferred from silence.

## Evaluation before claiming effectiveness

Use a manageable pilot of six unseen tasks: two client emails, two personal posts and two spoken-script edits. This count is a practical pilot choice, not a powered scientific study. Monty authors the initial notes and hooks where applicable.

Compare the same model/version and same task facts under:

- A: a basic request to write naturally in the user's voice.
- B: that request plus matched examples.
- C: the full skill with the same examples.

Rotate or randomize output order, conceal labels during evaluation, and preserve model/settings and prompts. A human reviewer judges factual fidelity first, then task fit and personal voice, and records substantive edits and editing time. A small pilot supports local conclusions only. Repeat sampling if a decision depends on consistency; do not select only the best-looking run.

To decide whether a reviewer helps, compare the initial full-skill draft with its reviewed version using the same criteria. Keep the review only if it adds value. To identify which component matters, remove one component at a time while holding the others constant.

Status: a six-task, three-condition synthetic pilot was completed October 26, 2026; see evaluation-pilot.md and evaluation-pilot.json. All conditions passed factual/scope checks. No superiority or personal voice match was established. A blinded writer-rated comparison with real matched samples remains pending. Never present illustrative before/after prose as experimental evidence.
