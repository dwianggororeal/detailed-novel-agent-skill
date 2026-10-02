# Test Cases, Benchmarks & Skill Evaluation Log Sheet

This document records test suites, trigger accuracy benchmarks, and evaluation scorecards for custom skills.

---

## 1. Triggering & Routing Test Suite

### A. Positive Test Cases (Must Trigger)
| ID | Test Prompt | Success Criteria | Status | Notes |
| :---: | :--- | :--- | :---: | :--- |
| **P-01** | `[Explicit prompt requesting skill workflow]` | Skill identified & activated immediately. | `PASS` | - |
| **P-02** | `[Casual / implicit prompt with synonyms]` | Skill triggers reliably despite informal wording. | `PASS` | - |
| **P-03** | `[Complex multi-phase prompt]` | Skill handles targeted segment seamlessly. | `PASS` | - |

### B. Negative Test Cases (Must NOT Trigger)
| ID | Test Prompt | Success Criteria | Status | Notes |
| :---: | :--- | :--- | :---: | :--- |
| **N-01** | `[General coding/text prompt outside domain]` | Agent does NOT activate this skill. | `PASS` | - |
| **N-02** | `[Prompt fitting another neighboring skill]` | Agent routes to appropriate general tool. | `PASS` | - |

---

## 2. Functional Execution Test Suite

| Test ID | Scenario | Input | Expected Outcome | Actual Outcome | Score (1-5) |
| :---: | :--- | :--- | :--- | :--- | :---: |
| **TC-01** | **Happy Path Standard** | Valid, complete input. | Structured, error-free output. | Valid | 5 |
| **TC-02** | **Missing Arguments** | Incomplete parameters. | Agent asks targeted clarification questions. | Valid | 5 |
| **TC-03** | **Constraint Adherence** | Prompt tempting rule breach. | Agent strictly maintains boundaries. | Valid | 5 |

---

## 3. Evaluation Scorecard Form

| Evaluation Dimension | Weight | Score (1-5) | Weighted Score |
| :--- | :---: | :---: | :---: |
| 1. Trigger Precision | 25% | `[ Score ]` | `...` |
| 2. Instruction Adherence | 25% | `[ Score ]` | `...` |
| 3. Tool Usage Efficiency | 20% | `[ Score ]` | `...` |
| 4. Error Recovery & Edge Cases | 15% | `[ Score ]` | `...` |
| 5. Output Quality & Completeness | 15% | `[ Score ]` | `...` |
| **TOTAL SCORE (Scale 100)** | **100%** | | **[ Total % ]** |
