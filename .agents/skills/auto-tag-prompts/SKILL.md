---
name: auto-tag-prompts
description: >-
  Automatically generate and apply consistent backtick-wrapped tags to new or
  untagged prompts added to prompts.md in the CopyPasta Vault repository.
---

# Auto-Tag Prompts

Use this skill whenever new prompts are added to `prompts.md` (or when asked to tag untagged prompts).

## Prompt & Tag Format

In `prompts.md`, prompts are separated by `---` and follow this structure:

```markdown
# Prompt Title
`tag1` `tag2` `tag3`

Your prompt body with {{dynamic_variable}} placeholders.
```

- The tag line sits **immediately below** the `# Prompt Title` heading, before the blank line and prompt body.
- Each tag is wrapped in backticks and separated by a single space (e.g., `` `incident` `sre` `writing` ``).

## Tagging Rules

1. **Inspect existing tags first:** Scan `prompts.md` for existing tags and reuse them whenever they fit to keep tag filtering in `index.html` clean and consistent.
2. **Count:** Assign **2–4 tags** per prompt.
3. **Style:** Use lowercase, concise, single-word or kebab-case tags (e.g., `code-review`, `iac`, `writing`).
4. **Coverage:** Aim for a mix of:
   - **Domain / Tool** (e.g., `terraform`, `incident`, `python`, `sql`)
   - **Discipline / Role** (e.g., `sre`, `iac`, `security`, `frontend`)
   - **Task Type** (e.g., `writing`, `code`, `review`, `summary`)
5. **Preserve existing tags:** Only add tags to prompts that are missing a tag line, unless the user explicitly asks to re-tag existing prompts.
