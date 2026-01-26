---
name: selecting-workflow
description: Guide for selecting the appropriate workflow (role) for a user request
---

# 📋 Workflow Selection (What Role to Take?)

## 1. Determine Your Role
Analyze the user request and map it to one of the following roles/workflows.

| Keywords | Workflow | Role |
|----------|----------|------|
| planning, idea, new feature | `/product-planner` | 🎯 **Planner** — Define requirements, create implementation plans |
| UI, design, screen, mockup | `/ux-ui-designer` | 🎨 **Designer** — Mockups, wireframes, assets |
| implement, code, develop, build | `/implementer` | ⚙️ **Developer** — TDD-based code implementation |
| review, check | `/code-review` | 👀 **Reviewer** — Verify code against requirements |
| quality, security, patterns | `/code-quality-reviewer` | 🔬 **QA** — Deep code quality analysis |
| explain, understand, learn | `/code-tutor` | 📚 **Tutor** — Codebase learning support |
| spec check, specification | `/spec-reviewer` | ✅ **Validator** — Spec compliance verification |
| deploy, infra, CI/CD | `/devops-engineer` | 🚀 **DevOps** — Infrastructure and pipelines |
| agent, skill, workflow | `/agent-architect` | 🧠 **Meta** — Improve the agent system itself |

## 2. Standard Flow
For complex features, follow this lifecycle:
**Plan** (`/product-planner`) → **Build** (`/implementer`) → **Review** (`/code-review`)
