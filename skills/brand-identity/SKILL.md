---
name: brand-identity
description: Provides the single source of truth for brand guidelines, design tokens, technology choices, and voice/tone. Use this skill whenever generating UI components, styling applications, writing copy, or creating user-facing assets to ensure brand consistency.
---

# Brand Identity & Guidelines

**Brand Name:** [INSERT BRAND NAME HERE]

This skill defines the core constraints for visual design and technical implementation for the brand. You must adhere to these guidelines strictly to maintain consistency.

## Reference Documentation (Resources)

Depending on the task you are performing, use `view_file` to consult the specific resource files below. Do not guess brand elements; always read the corresponding file.

### 1. For Visual Design & UI Styling (`resources/design-tokens.json`)
Read this when you need exact values for:
- **Colors** (Primary, Secondary, Backgrounds)
- **Typography** (Font stack, sizes, line heights)
- **Spacing** & **Border Radii**

### 2. For Coding & Tech Stack (`resources/tech-stack.md`)
Read this when you are generating boilerplate or choosing libraries:
- **Frameworks** (Next.js, React, etc.)
- **Styling Libraries** (Tailwind, Styled-components)
- **State Management** & **Data Fetching** rules

### 3. For Copywriting & Voice (`resources/voice-tone.md`)
Read this when you are writing user-facing text:
- **Tone**: Formal vs Casual, Friendly vs Professional
- **Vocabulary**: Allowed/Banned terms
- **Persona**: How the AI should sound

## Usage Instructions

1.  **Identify the nature of the task** (UI? Code? Copy?).
2.  **Read the specific resource file** listed above.
3.  **Apply constraints strictly**. Do not invent new colors or fonts.
4.  If a value is missing, **ask the user** or check existing code patterns.
