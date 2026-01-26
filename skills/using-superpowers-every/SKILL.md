---
name: using-superpowers
description: Use for every single user request - establishes how to find and use skills, requiring Skill tool invocation before ANY response including clarifying questions
---

<CRITICAL-RULES>
## 🚨 ABSOLUTE RULES: Check Before Acting

1. **NO IMPLEMENTATION until skills are checked** — Before writing code, modifying files, or executing commands, you MUST verify if a relevant skill exists
2. **NO WORK until workflow is selected** — For complex requests, select the appropriate workflow FIRST
3. **If there's even 1% chance a skill applies, CHECK IT** — You can skip it after reading if irrelevant
4. **NO IMPLEMENTATION until user explicit request** — Do not write code until the user explicitly asks you to.

This is NON-NEGOTIABLE. NOT OPTIONAL. NO RATIONALIZING.
</CRITICAL-RULES>

---

# 🎯 Quick Decision Tree

```
User Request Received
    ↓
┌─────────────────────────────────────────────────────────┐
│ 1. WHAT role should I take? → Use `selecting-workflow`  │
│ 2. HOW should I approach this? → Use `selecting-skill`  │
│ 3. Verification complete → Begin execution              │
└─────────────────────────────────────────────────────────┘
```

---

# 🚀 Execution Steps

1. **Select Workflow**:
   - Use the `view_file` tool on `.agent/skills/selecting-workflow/SKILL.md`
   - Decide which workflow (slash command) applies.

2. **Select Skills**:
   - Use the `view_file` tool on `.agent/skills/selecting-skill/SKILL.md`
   - Pick the skills required for the task (Thinking -> Planning -> Building -> Verifying).

3. **Proceed**:
   - Load the selected workflow and skill instructions.
   - Execute strictly according to them.

---

# 👤 User Instructions

**ALWAYS:** Select Workflow → Check Skills → Execute
