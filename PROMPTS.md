# PROMPTS.md - my key prompts log

Keep the handful of prompts that actually moved the build. Not every message - the ones that
mattered: the system/sub-agent prompts, the ones you iterated on, the "this finally worked"
moment. Paste them here MANUALLY as you go.

Why manual? Some free Ollama cloud models do not save a local session log, so an auto audit
log may be empty. That is fine and expected (see the brief's Model Fairness section). What
guarantees your process is judged fairly is: the working plugin + reproducible report.json,
incremental git commits, this PROMPTS.md, and a short DECISIONS.md. Keep these up to date.

Format per entry:
- **Prompt** (paste it)
- **For:** what you were trying to do
- **Revised?** did you have to change it, and why

---
## My prompts

* **Prompt:** Review analyzer.py and identify the highest-impact missing feature.

* **For:** Finding the most valuable improvement with minimal code changes.

* **Revised?** No.

* **Prompt:** Implement deterministic suggested_anchor generation using page metadata.

* **For:** Replacing null recommendation anchors.

* **Revised?** Yes, title cleanup was added.

* **Prompt:** Implement cluster name generation using representative keywords.

* **For:** Replacing null cluster names.

* **Revised?** No.

* **Prompt:** Improve recommendation quality by prioritizing under-linked pages and filtering weak candidates.

* **For:** Improving recommendation relevance.

* **Revised?** Yes, a conservative threshold was used.

