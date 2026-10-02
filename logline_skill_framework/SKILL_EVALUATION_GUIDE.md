# Skill Evaluation Framework & Standards (Antigravity IDE)

This document defines benchmarks, quality rubrics, and evaluation protocols for assessing the reliability of Custom Skills.

---

## 1. The 5-Dimension Skill Evaluation Rubric

| Dimension | Weight | Description | Passing Standard (Min. 4/5) |
| :--- | :---: | :--- | :--- |
| **1. Trigger Precision** | 25% | Agent activates the skill only when relevant and ignores non-relevant prompts. | 0 False Positives on negative tests; 100% activation on positive tests. |
| **2. Instruction Adherence** | 25% | Agent complies with all negative constraints and formatting rules without deviation. | Follows all DOs and DON'Ts without hallucinated syntax. |
| **3. Tool Usage Efficiency** | 20% | Agent selects optimal tools without infinite loops or redundant calls. | Shortest valid execution toolchain. |
| **4. Error Recovery & Edge Cases** | 15% | Agent handles tool failures or ambiguous inputs gracefully. | Built-in fallback strategies executed reliably. |
| **5. Output Quality & Completeness** | 15% | Final output is structured, valid, and fully addresses user requirements. | Ready-to-use output free of syntax or semantic flaws. |

---

## 2. Pre-Deployment Verification Checklist

- [ ] Valid YAML frontmatter (`name` lowercase-hyphenated, `description` third-person).
- [ ] Description specifies both *when to use* and *when not to use*.
- [ ] Bulky reference documentation separated into `references/` or `resources/`.
- [ ] Features autonomous self-verification checks for the agent.
- [ ] Tested against the benchmark suite in `SKILL_TEST_CASES_AND_BENCHMARKS.md`.
