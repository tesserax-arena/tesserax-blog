# Tesserax Blog — Agent Context

## Quick facts

| Attribute | Value |
|-----------|-------|
| Purpose | Markdown blog posts for Tesserax Arena |
| Live site | https://tesserax.net/blog/ |
| Parent repo | tesserax-arena (submodule at `blog/`) |
| Contact | hello@tesserax.net |

## Directory map

```
tesserax-blog/
  *.md              Published posts
  _drafts/          Draft posts (hidden from public listing)
  README.md
  AGENTS.md
```

## Workflow checklist

When adding or editing a post:

1. **Create** a file named `YYYY-MM-DD-slug.md` (slug = filename stem, used in `/blog/{slug}`)
2. **Frontmatter** must include `title`, `date`, and optional `tags`
3. **Draft?** Put the file in `_drafts/` instead of the repo root
4. **Commit and push** this repo
5. **Bump submodule pointer** in tesserax-arena (`cd blog && git pull`, commit SHA in parent)

## Constraints

- Posts are Markdown with YAML frontmatter — no HTML templates here
- Public routes are `/blog` (listing) and `/blog/{slug}` (post) on the arena app
- Do not commit secrets or internal-only content as published posts (root-level `.md` files)
