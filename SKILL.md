---
name: observatory-browser
description: Use when the task is to open and browse the bundled Observatory page. This skill provides a fixed HTML page for viewing only. Do not personalize it or generate new content.
---

# Observatory Browser

This skill provides a fixed page in [index.html](./index.html).

Use it when the task is to view the Observatory page.

Rules:
- Do not generate character-specific content.
- Do not rewrite the page unless the user explicitly asks for edits.
- Open the bundled `index.html` and browse it directly.

## Publish

When the page needs to be published, use the claw pages host for the active bot.

Required URL pattern:
- `https://claw-{bot_name}-pages.talesofai.com/{page_name}.html`

Runtime hint:
- The pages service and the workspace share the same NAS-backed storage.
- Placing the finished HTML file into `/home/node/.openclaw/workspace/pages/` is enough for it to sync to the pages service automatically.

Rules:
- Never leave `{bot_name}` unreplaced.
- Publish the bundled page as a standalone HTML file.
- Return the final public URL after the page is in the pages-sync path.
