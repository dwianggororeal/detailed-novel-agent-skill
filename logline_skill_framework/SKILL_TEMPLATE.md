---
name: custom-skill-name
description: >-
  [MANDATORY] Clearly describe when the agent MUST use this skill and when it
  MUST NOT be used. Use third-person perspective.
  Example: "Use this skill when the user asks to generate slowburn narrative loglines or structure RPG world rules."
---

# [Custom Skill Name]

Summary of the core capabilities and workflows provided by this skill.

---

## 1. Prerequisites & Environment Setup

- Required tools / dependencies: `[List tools]`
- Configuration files or directories to verify.

---

## 2. Core Workflow (Execution Steps)

### Step 1: Preparation & Input Validation
- Validate user arguments.
- Read referenced guides:
  - Deep guide: [detailed_rules.md](./references/detailed_rules.md)
  - Implementation examples: [standard_example.md](./resources/standard_example.md)

### Step 2: Main Execution
1. Execute helper scripts if present:
   ```bash
   python ./scripts/helper.py --arg value
   ```
2. Write or modify target files adhering to design specifications.

### Step 3: Self-Check & Verification
- Verify output validity, syntax checks, and linter constraints.

---

## 3. Strict Rules & Constraints (DOs & DON'Ts)

### DO:
- [Rule 1]
- [Rule 2]

### DON'T:
- [Constraint 1]
- [Constraint 2]

---

## 4. Error Handling & Fallbacks

| Error Condition | Recovery Action |
| :--- | :--- |
| **Tool / Command Failure** | [Recovery step or clarification request] |
| **Ambiguous / Missing Input** | [Ask targeted multi-choice questions] |
