---
name: using-superpowers
description: Use when starting any conversation or whenever any request establishes how to find and use skills.
---

<CRITICAL-RULES>
## 🚨 ABSOLUTE RULES: Check Before Acting

1. **NO IMPLEMENTATION until skills are checked** — Before writing code, modifying files, or executing commands, you MUST verify if a relevant skill exists
2. **NO WORK until workflow is selected** — For complex requests, select the appropriate workflow FIRST
3. **If there's even 1% chance a skill applies, CHECK IT** — You can skip it after reading if irrelevant
4. **NO IMPLEMENTATION until user explicit request** — Do not write code until the user explicitly asks you to.
</CRITICAL-RULES>

---

# 🎯 Decision Process

Refer to the specialized skills for selection logic:

1. **For Role/Workflow Selection**:
   - MUST READ: `.agent/skills/selecting-workflow/SKILL.md`
   - Defines *who* you are for this task (Planner, Developer, Reviewer, etc.)

2. **For Tool/Skill Selection**:
   - MUST READ: `.agent/skills/selecting-skill/SKILL.md`
   - Defines *how* you will execute the task (Brainstorming, TDD, specific tech stacks)

---

# 🚀 How to Apply

1. **Read `selecting-workflow`** -> Pick your Role.
2. **Read `selecting-skill`** -> Pick your Tools.
3. **Read the selected Skill/Workflow files**.
4. **Execute**.
