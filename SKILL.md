---
name: claude-skill-design
description: |
  Guidelines for creating highly discoverable Claude Code skills by embedding trigger phrases and using imperative instructions. Use when you need to improve skill discovery or structure complex skill logic. Use when user says: "improve skill triggering", "fix skill discovery", "optimize my skill description", "make my skill trigger more often".
source: "/tmp/test-transcript.md"
extracted: "2026-02-20"
---

# Claude Code Skill Development

## Core Rules

- Embed exact trigger phrases in the description that users would naturally say.
- Use the three-level loading system (description, SKILL.md, references/) for progressive disclosure.
- Write all instructions in imperative form (active voice, direct commands).
- Test trigger discovery by trying 10 different user requests and aiming for at least 6 successes.
- Adhere to the 'One Skill, One Job' principle to ensure focus and reliability.

## When to Apply

- When a skill is not triggering correctly for natural language requests.
- When a skill description is too vague for Claude to select.
- When a skill body exceeds 500 lines and needs refactoring.
- When multiple unrelated functions are mixed into a single skill.

## Anti-Patterns

- Avoid descriptions that only state what the skill does without mentioning when to use it.
- Don't keep skill bodies over 500 lines; move detailed content to the references/ directory.
- Avoid omitting concrete trigger phrases from the skill description.
- Don't mix unrelated functionality into a single skill.
- Avoid referencing non-existent files in the SKILL.md or references.

## Workflow

1. Identify 5 concrete examples of requests the skill should handle.
2. Write the skill description last, ensuring it includes the identified trigger phrases.
3. Construct the SKILL.md body using imperative instructions.
4. Move any topic-specific content exceeding 50 lines to the references/ directory.
5. Test 10 potential trigger phrases and iterate on the description until at least 6 work reliably.

## Examples

- For a PDF merging skill, ensure the description contains 'merge' and 'PDFs'.
- Instead of 'you should extract text', use 'Extract the text using...'.
- Test a PDF skill with 10 variations like 'combine these docs' or 'join these PDFs' to verify discovery.
