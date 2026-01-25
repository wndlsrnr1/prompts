---
description: Implements features using strict Test-Driven Development (TDD) and systematic debugging.
---

# Implementer Workflow

This workflow guides you through the role of an **Implementer**. Your goal is to write high-quality, working code that satisfies requirements using strict TDD practices.

## Prerequisite Skills
- `test-driven-development` (MANDATORY)
- `systematic-debugging` (For fixing issues)
- `verification-before-completion`

## 1. Task Acquisition
1.  **Identify Scope**:
    - If working from a Plan (`docs/plans/...`), identify the specific Task ID (e.g., `[P1]`) to work on.
    - If standalone, clarify the specific feature requirements with the user.
2.  **Context Check**:
    - Read related files (`view_file`).
    - Check existing tests to understand the test harness.
    - Review `Design Specs` if UI implementation is involved.

## 2. The TDD Cycle (Red-Green-Refactor)
**You must follow this cycle for EVERY logical unit.**

### A. RED (Write Failing Test)
1.  Create or modify a test file (`*.test.ts`, `*_test.py`, etc.).
2.  Write a test case that captures the *requirements* of the feature.
3.  **RUN** the test and **CONFIRM** it fails with the expected error (e.g., "function not defined" or assertion error).
    - *Do not proceed if it passes unexpectedly.*

### B. GREEN (Make it Pass)
1.  Write the *minimum* amount of code necessary to pass the test.
2.  **RUN** the test again.
3.  If it fails, read the error, fix the code, and retry.
4.  Once it passes -> **COMMIT** (`git commit -m "feat: pass test for X"`).

### C. REFACTOR (Clean Code)
1.  Look for code smells, duplication, or magic numbers.
2.  Refactor while keeping tests passing.
3.  **Verify** by running tests again.

## 3. Iteration
- Repeat the TDD Cycle for the next small chunk of functionality.
- Do not attempt to implement the entire feature in one go. Break it down.

## 4. Final Verification & Handoff
1.  **Full Suite Run**: Run ALL tests (not just the new one) to ensure no regressions.
2.  **Linter Check**: Run project linters/formatters.
3.  **Self-Review**:
    - Does the code meet the functional requirements?
    - Are edge cases covered?
4.  **Completion**:
    - "Task `[P1]` is complete. Tests passed. Ready for review."
    - Suggest running `/code-review` or switching to `Spec Reviewer` role.
