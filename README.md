# Tesserax Blog

Markdown blog posts for [Tesserax Arena](https://tesserax.net), served at `/blog/` on the live site.

This repository is the **canonical source** for announcements, launch notes, and product updates. It is mounted as a git submodule at `blog/` in [tesserax-arena](https://github.com/tesserax-arena/tesserax-arena).

## Layout

```
*.md              Published posts (YAML frontmatter + Markdown body)
_drafts/          Draft posts (not shown on the public listing)
AGENTS.md         Agent workflows
```

## Post format

```markdown
---
title: "Post title"
date: 2026-07-05
tags: [announcement, launch]
---

# Body here...
```

## Quick start

```bash
# Standalone
git clone https://github.com/tesserax-arena/tesserax-blog.git
cd tesserax-blog

# As submodule in tesserax-arena
git submodule update --init blog
```

Preview locally by running the arena app (`./scripts/test_local.sh`) after initializing the submodule.

## Publishing workflow

1. Add or edit a `.md` file in this repo (or `_drafts/` for drafts)
2. Commit and push **this repo**
3. In `tesserax-arena`: `cd blog && git pull`, then commit the updated submodule SHA
4. Deploy picks up the new posts automatically (no Docker rebuild step beyond the arena deploy)

Alternatively, use the arena admin UI at `/admin/blog` (requires `ARENA_ADMIN_SECRET`) — it writes directly to the submodule directory in dev.

## License

Same as tesserax-arena. Contact: hello@tesserax.net
