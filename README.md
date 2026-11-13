# CopyPasta Vault

A zero-build, static Markdown prompt library with live `{{variable}}` interpolation, clickable tag filtering, inline editing, and one-click clipboard copy.

## Files
- `index.html` — Single-file UI engine, search/tag filter, and variable parser.
- `prompts.md` — Your prompt library (edit directly via GitHub or Git).

## Quick Deploy
1. Push `index.html` and `prompts.md` to a GitHub repository.
2. Enable **GitHub Pages** (or connect the repo to **Cloudflare Pages** for private repo support).
3. Bookmark the URL on your work browser.

## Adding Prompts
Separate each prompt in `prompts.md` with `---`:

```markdown
# Prompt Title
`tag1` `tag2`

Your prompt body with {{dynamic_variable}} placeholders.
```
