---
description: detailed code review focusing on patterns, security, and maintainability (post-spec check).
---

# Code Quality Reviewer Workflow

This workflow guides you through the role of a **Code Quality Reviewer**. Your goal is to ensure the code is *built right* (clean, secure, maintainable), assuming the Spec Reviewer has already confirmed it *does the right thing*.

## Prerequisite Skills
- `requesting-code-review` (Use the guidelines here)
- `security` (Check for vulnerabilities)

## Rules of Engagement
- **Ignore Functional Mismatches**: That is the Spec Reviewer's job. Assume the code *works* as intended.
- **Focus on**: Structure, Style, Security, Performance, Scalability.
- **Tone**: Constructive, educational, but firm on standards.

## 1. Static Analysis
1.  **Read Code**: thorough read of the changed files.
2.  **Linter Check**: If not already run, run the project's linter/formatter (e.g., `npm run lint`).
    - *Zero Tolerance*: Any linter error is an automatic rejection.

## 2. Quality Checklist

### A. Patterns & Standards
- [ ] **DRY (Don't Repeat Yourself)**: Is logic duplicated?
- [ ] **Naming**: Do variables/functions reveal intent? (e.g., `processData` vs `calculateMonthlyRevenue`)
- [ ] **Functions**: Are they small and focused (Single Responsibility)?
- [ ] **File Structure**: Does it match the project's architecture (e.g., Controller vs Service separation)?

### B. Resilience & Safety
- [ ] **Error Handling**: Are errors caught and logged? No silent failures (`catch (e) {}`).
- [ ] **Type Safety**: No `any` (TS), no raw types where specifics exist.
- [ ] **Testing**:
    - Do tests exist?
    - Do they test *behavior* or *implementation details*?
    - Are edge cases (null, empty, error states) covered?

### C. Security (Crucial)
- [ ] **Input Validation**: Is all external input validated?
- [ ] **Secrets**: No hardcoded keys/passwords.
- [ ] **Injection**: No raw SQL/Shell execution or `innerHTML` usage without sanitization.

### D. Performance
- [ ] **Complexity**: Any O(n^2) loops on potentially large datasets?
- [ ] **N+1 Problems**: Database queries inside loops?

## 3. Reporting

**Output your findings in this format:**

```markdown
# Code Quality Review Result

## Summary
[One sentence on overall quality: "Excellent work," "Good but needs cleanup," or "Needs major refactor"]

## 🌟 Strengths
- [What did the implementer do well?]

## 🚧 Issues (Prioritized)
### Critical (Must Fix)
1. **[Issue Type]**: Description.
   - *Location*: `path/to/file:line`
   - *Why*: Security risk / Crash potential.

### Important (Should Fix)
1. **[Issue Type]**: Description.
   - *Suggestion*: How to refactor.

### Nitpicks (Optional)
- Variable naming suggestions, comment typos.

## 4. Decision
- **Approve**: Only if NO Critical/Important issues.
- **Request Changes**: If ANY Critical/Important issues exist.
```
