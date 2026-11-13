# Door 38: Turn an idea into an editable Excalidraw diagram

This door's gift is a skill by Cole Medin. It lives in his repo:

https://github.com/coleam00/excalidraw-diagram-skill

## Credit and license

The excalidraw-diagram skill is Cole Medin's work (coleam00 on GitHub). His repo has no license file, so this page links to his repo and copies none of his files. Install the skill from his repo, and do not republish his files. The two example files below were made for this page.

## What it does

You describe an idea in plain words. A coding agent that reads skills from `.claude/skills/`, such as Claude Code, writes an Excalidraw file, renders it to a PNG with Playwright, looks at the image and fixes the layout until it reads right. You keep the editable `.excalidraw` file and the PNG.

## Install it from Cole Medin's repo

Run these in your project folder. The renderer needs [uv](https://docs.astral.sh/uv/), and the last line downloads Playwright's Chromium. His README's copy step needs a `.claude/skills` folder to exist, so the second line makes it first.

```bash
git clone https://github.com/coleam00/excalidraw-diagram-skill.git
mkdir -p .claude/skills
cp -r excalidraw-diagram-skill .claude/skills/excalidraw-diagram
cd .claude/skills/excalidraw-diagram/references
uv sync
uv run playwright install chromium
```

Then ask your agent for a diagram. To render a file yourself, use the command from the skill's SKILL.md:

```bash
cd .claude/skills/excalidraw-diagram/references && uv run python render_excalidraw.py <path-to-file.excalidraw>
```

## Known issue, checked 2026-11-13

Line 16 of the renderer's template, `references/render_template.html`, imports `https://esm.sh/@excalidraw/excalidraw?bundle` with no version, which today loads Excalidraw 0.18.1. One file that build imports, `@braintree/sanitize-url@6.0.2/es2022/dist/constants.mjs`, returned HTTP 404 from esm.sh on three tries of three, so the render step times out. Changing that import in your copy to `https://esm.sh/@excalidraw/excalidraw@0.18.0?bundle` renders. The example image below was made that way.

## The two example files

- [example.png](example.png): the image, 5440 by 2480 pixels.
- [example.excalidraw](example.excalidraw): its editable source. Open it at https://excalidraw.com with Open in the main menu, or drag the file onto the page.

![Diagram of the skill's loop, left to right: your idea in plain words, Claude writes Excalidraw JSON, render to PNG with Playwright, a diamond asking whether it reads right, then an editable file plus PNG. A red arrow loops back from the check: fix the JSON, render again. Below sit a sample of the JSON, the render command and a credit line for Cole Medin.](example.png)

How they were made, on 2026-11-13: the drawing source was written for this page in the skill's JSON format and color palette, not produced by running the skill in an agent session. `example.png` is that file rendered by the skill's own `render_excalidraw.py` at its defaults (scale 2, width 1920), with the template import pinned as above.

Door 38 of [100 Doors](https://github.com/LucasCooperBey/100-doors).
