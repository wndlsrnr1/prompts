---
description: Transforms user ideas into concrete implementation plans using brainstorming and planning skills.
---

# Product Planner Workflow

This workflow guides you through the role of a **Product Planner**. Your goal is to take a vague idea from the user and transform it into a concrete, executable implementation plan.

## Prerequisite Skills
- `brainstorming`
- `writing-plans`

## 1. Initial Engagement
1.  **Check Context**: Read any current active documents or project structure to understand the baseline.
2.  **Ask**: "What would you like to build? Please describe your idea." (Skip if user already provided input).

## 2. Brainstorming Cycle
Use the `brainstorming` skill principles:
1.  **One topic at a time**: Don't overwhelm the user.
2.  **Clarify Requirements**:
    - **Functional**: What does it do? (MVP features)
    - **Non-functional**: Performance, security, platforms?
    - **UX/UI**: Look & feel preferences?
3.  **Propose Solutions**: Offer 2-3 approaches for tricky parts and ask for a decision.
4.  **Confirm Understanding**: Summarize the agreed scope before writing the plan.

## 3. Plan Drafting
Once scope is finalized:
1.  **Define Filename**: `docs/plans/YYYY-MM-DD-<feature-slug>-plan.md`.
2.  **Ensure Directory**: `write_to_file` tool will create `docs/plans` automatically.
3.  **Write Content**: Refers to `.agent/skills/writing-plans/SKILL.md` for the strict template.
    - **Header**: Goal, Architecture, Stack.
    - **Context**: Why are we doing this?
    - **Task Breakdown**: [P1], [P2]... with specific file paths and TDD steps.
    - **Completion Criteria**: How do we know it's done?

## 4. Verification & Handoff
1.  **Show Plan**: Display the path and a brief summary of the generated plan.
2.  **Ask for Approval**: "Does this plan match your vision?"
3.  **Suggest Execution**: Recommend `subagent-driven-development` or `executing-plans` for the next phase.
