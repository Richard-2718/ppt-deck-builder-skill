# ppt-deck-builder-skill

A Codex skill for generating polished academic PPT decks, optimized for paper-reading reports and Beijing Institute of Technology-style academic presentation layouts.

This repository contains the reusable skill instructions only. It does not include official Beijing Institute of Technology templates, school logos, seal source files, private papers, generated decks, preview images, or unauthorized copyrighted assets.

## What It Does

- Builds academic PPT outlines, slide scripts, speaker notes, and full deck plans.
- Supports paper-reading reports, research group meeting slides, thesis defense decks, CFD/COMSOL result presentations, and engineering project presentations.
- Uses a template-first workflow when the user provides a PPT template.
- Supports BIT-style presentation layouts, including green/white academic styling, cover structure, contents pages, section dividers, figure-heavy body pages, and paper-reading report layouts.
- Prioritizes original paper figures for scientific evidence and tracks sources through figure manifests or speaker notes.
- Separates formal slide content from speaker notes.
- Checks for Chinese text readability and common encoding failures such as `????`.

## Important Scope Note

"BIT-style" means a presentation layout direction inspired by Beijing Institute of Technology-style academic presentations. This skill is not an official Beijing Institute of Technology template package and does not redistribute any official template, logo, or school-owned visual asset.

Users should provide their own authorized templates and source materials when generating institution-specific decks.

## Recommended Install

Copy this repository folder into your Codex skills directory:

```powershell
$target = "$env:USERPROFILE\.codex\skills\ppt-deck-builder"
New-Item -ItemType Directory -Force -Path $target
Copy-Item -Recurse -Force .\SKILL.md $target
```

Then restart Codex or refresh skills so the `ppt-deck-builder` skill can be discovered.

## Example Prompts

```text
Use ppt-deck-builder to create a paper-reading PPT outline from the current PDF.
```

```text
Use ppt-deck-builder to generate a BIT-style academic group meeting deck. Use original paper figures for evidence slides and keep AI images only for conceptual visuals.
```

```text
Use ppt-deck-builder to review this deck for title consistency, body text size, excessive whitespace, figure readability, source tracking, and Chinese garbling.
```
## Included Template

A custom academic PPT template created by the repository author is included in:

```text
templates/

## Public Repository Hygiene

Do not commit:

- generated `.pptx`, `.pdf`, `.zip`, or preview files
- official university templates or logo source files
- private papers, thesis drafts, or unpublished research material
- extracted paper figures unless redistribution is authorized
- `.env` files, API keys, tokens, or local cache files

Use the included `.gitignore` as the default safety net before publishing.
