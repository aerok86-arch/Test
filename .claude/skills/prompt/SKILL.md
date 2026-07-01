---
name: prompt
description: Help users craft high-quality prompts through friendly, one-question-at-a-time conversation. Use when the user asks to build a prompt, improve a prompt, or wants help writing instructions for an AI task.
---

# Prompt Builder Skill

Help users craft high-quality prompts through friendly, one-question-at-a-time conversation. Output only the finished prompt at the end.

## Core Philosophy

Great prompts provide Claude with:
- **Role/persona** — who should Claude be?
- **Task** — what exactly should it do?
- **Context** — relevant background information
- **Output format** — what should the result look like?
- **Constraints** — what to avoid or keep in mind
- **Tone** — appropriate voice or style
- **Examples** — few-shot examples to anchor output

## Conversation Flow

**Step 1**: Start with: "What do you want the prompt to accomplish? Just describe it naturally."

**Step 2**: Ask task-specific follow-ups one at a time based on task type:
- *Writing*: audience, tone, length, inclusions/exclusions, style examples
- *Coding*: language/framework, exact functionality, edge cases, constraints, explanation level
- *Analysis*: source material, output type, depth level, analytical angle
- *Brainstorming*: quantity target, practical vs. creative, constraints, format
- *Roleplay*: character/persona, scenario, character rules, user's role
- *Data tasks*: input format, output format, transformation rules

**Step 3**: Check universal elements (role, examples, format, constraints).

**Step 4**: Stop asking when you have enough information (typically 3–6 questions).

**Step 5**: Output only the finished prompt — no preamble or explanation.

## Construction Best Practices

- Lead with role if helpful
- State task clearly with action verbs
- Include context inline
- Specify format explicitly
- Add constraints as needed
- Use XML tags for user-supplied content
- Invite reasoning for analytical tasks
- Be specific, not vague
- Use clean formatting with line breaks
