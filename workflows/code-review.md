---
description: detailed code review against plan and standards
---

1. **Plan Alignment Analysis**
   - Review the relevant plan file in `docs/plans/` (or the active task context).
   - Compare the implementation against the original planning document or step description.
   - Identify any deviations from the planned approach, architecture, or requirements.
   - Determine if deviations are justified improvements or problematic departures.
   - Verify that all planned functionality has been implemented.

2. **Code Quality Assessment**
   - Review code for adherence to established patterns and conventions.
   - Check for proper error handling, type safety, and defensive programming.
   - Evaluate code organization, naming conventions, and maintainability.
   - Assess test coverage and quality of test implementations.
   - Look for potential security vulnerabilities or performance issues.

3. **Architecture and Design Review**
   - Ensure the implementation follows SOLID principles and established architectural patterns.
   - Check for proper separation of concerns and loose coupling.
   - Verify that the code integrates well with existing systems.
   - Assess scalability and extensibility considerations.

4. **Documentation and Standards**
   - Verify that code includes appropriate comments and documentation.
   - Check that file headers, function documentation, and inline comments are present and accurate.
   - Ensure adherence to project-specific coding standards and conventions (refer to `.agent/rules/` if available).

5. **Issue Identification and Recommendations**
   - Create a summary of findings.
   - Categorize issues as: **Critical** (must fix), **Important** (should fix), or **Suggestions** (nice to have).
   - For each issue, provide specific examples and actionable recommendations.
   - If meaningful deviations from the plan are found, explicitly ask for confirmation.
   - Always acknowledge what was done well before highlighting issues.
