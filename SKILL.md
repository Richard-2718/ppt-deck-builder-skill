---
name: ppt-deck-builder
description: Use this skill when Codex needs to create, outline, polish, restructure, review, or generate academic PPT decks, PowerPoint slides, paper-reading reports, thesis defense presentations, research group meeting decks, CFD/COMSOL result presentations, engineering project decks, or Beijing Institute of Technology-style academic presentations. Supports template-first workflows, figure/source tracking, speaker notes separation, Chinese text validation, and BIT-style presentation layouts without distributing official templates or logos.
---

# PPT Deck Builder

Build polished academic presentation decks with strong narrative logic, readable layouts, reliable figure handling, and source-aware workflows.

Default behavior:
- Reply in the user's language unless they ask otherwise.
- Be direct, practical, and presentation-oriented.
- Start with slide logic before visual details.
- Prefer template-first generation when the user provides a PPT template.
- Do not include official university templates, logo source files, private papers, private images, API keys, or unauthorized copyrighted assets in reusable skill resources.

## Core Use Cases

Use this skill for:
- paper-reading reports and literature review decks
- academic group meeting presentations
- thesis defense presentations
- research progress reports
- CFD, COMSOL, simulation, and experiment result presentations
- YOLO, ROS2, Jetson, Python, and engineering system decks
- competition, project report, and portfolio presentations
- Beijing Institute of Technology-style academic presentation layouts

The goal is not only to make slides. The goal is to turn source material into a clear story, select credible evidence, organize figures, and produce slides that are easy to present.

## Default Workflow

When asked to work on a deck:

1. Identify the deck type, audience, time limit, expected slide count, tone, source materials, and desired output.
2. Inspect available files before generating content or editing assets.
3. Build or refine the slide logic first.
4. Decide whether the task needs an outline, full slide copy, speaker notes, figure plan, visual plan, or an actual `.pptx`.
5. If a template is provided, inspect and reuse the template structure before creating new layouts.
6. If using papers or external figures, track sources in a manifest, speaker notes, references slide, or footer notes as appropriate.
7. If generating a PowerPoint file, render or inspect previews when possible and check Chinese text, layout consistency, and figure readability before calling the deck finished.

## Template-First Workflow

When the user provides a PPT template:

- Treat the template as the primary design system.
- Identify available slide types such as cover, contents, section divider, body, text + figure, comparison, figure-heavy result, framework diagram, timeline, conclusion, and ending pages.
- Prefer copying and adapting template slides instead of building from blank pages.
- Preserve the template's visual identity, including title hierarchy, color system, footer style, page numbers, and institutional identity areas.
- Do not distort logos, seals, or official marks.
- If the template cannot be reused programmatically, imitate its visual structure based on screenshots, exported slide images, or extracted layout information.

## BIT-Style Academic Layouts

This skill supports BIT-style and Beijing Institute of Technology-style academic presentations as a layout and design direction. It does not distribute or publish any official Beijing Institute of Technology template, logo source file, seal, school image, or proprietary asset.

When the user provides a BIT-style academic template or requests a BIT-style layout:

- Use green and white as the main visual identity when appropriate.
- Use clean cover pages that combine institutional tone with the research topic.
- Use contents pages for decks with clear sections.
- Use section divider pages for major parts.
- Use body pages for standard research content.
- Use text + figure pages for paper-reading, CFD, and result explanation slides.
- Use framework pages for methods, workflows, or technical routes.
- Keep institutional identity areas clean and undistorted.
- Do not imply that the output is an official university template unless the user explicitly provides authorized materials and asks for an internal-use deck.
- Do not mix unrelated beige, dark-blue business, or decorative styles with a BIT-style green academic system unless the user explicitly requests a custom redesign.

For public or reusable outputs, describe the style as "BIT-style presentation layouts" or "Beijing Institute of Technology-style academic presentations", not as an official template release.

## Cover Design For Research PPT

Research covers should communicate both institutional tone and research topic.

Prefer:
- paper-related scientific visuals
- model or system diagrams
- CFD wake fields or simulation visualizations
- velocity cloud maps or result-inspired visuals
- topic-relevant conceptual illustrations labeled as "conceptual illustration / AI-generated" when AI-generated

Avoid:
- generic campus-photo-only covers that do not communicate the research topic
- distorted official marks
- AI-generated imitations of official logos or seals
- decorative imagery that weakens academic credibility

## Contents And Section Divider Pages

Contents and section divider pages may be sparse.

Use whitespace intentionally for hierarchy and pacing. Do not force extra figures into contents or divider pages unless the user asks.

Default:
- contents slide: 3 to 5 sections
- section divider: section number + section title
- no paper figures on section dividers by default
- no AI image generation on contents pages by default

## Research PPT Layout Modes

Choose a layout mode by slide type:

- Cover: institutional tone + topic-related visual
- Contents: clean section overview
- Section divider: large section number and title
- Text + figure: 30-40% text and 60-70% figure
- Figure-heavy result: one-sentence takeaway, large figure, short callouts, small source note
- Comparison / two-figure: aligned captions and equal figure sizes
- Summary card: 3-4 concise takeaways

If a slide is too empty, enlarge figures or text, crop unnecessary figure margins, add a short conclusion, or improve the text-figure ratio. Do not fill space with irrelevant decoration.

If a slide is crowded, split it or reduce content.

## Academic Readability Rules

For formal academic decks:

- Use one main message per slide.
- Prefer conclusion-style slide titles.
- Keep title positions, title sizes, margins, figure captions, footers, and page numbers consistent.
- Avoid title wrapping that looks accidental.
- Avoid splitting English terms across lines, such as Gaussian, Suboff, COMSOL, RANS, CFD, YOLO, ROS2, and Jetson.
- Keep body text generally at least 20 pt when possible.
- Prefer 3 concise bullets per body slide; use 4 only when the layout can support it.
- Use figures as evidence, not decoration.
- For result slides, figures should usually occupy more space than text.
- Captions and source notes should be readable but unobtrusive.

## Paper Reading Workflow

For paper reading, literature reports, and academic group meeting decks:

1. Locate source PDFs and supporting materials.
2. Inspect PDF metadata and page count if tools allow.
3. Build or refine `outline.md`.
4. Build or refine `slide_script.md` or speaker notes.
5. Extract or crop original paper figures when useful.
6. Create or update `figure_manifest.md`.
7. Map slides to suitable layouts.
8. Generate or revise the deck.
9. Render previews or contact sheets if possible.
10. Check readability, Chinese text, source tracking, figure quality, and template consistency.

Default single-paper structure:

1. Title
2. Research background
3. Core problem
4. Main contributions
5. Method overview
6. Key technical detail
7. Experiment or simulation setup
8. Core results
9. Ablation, comparison, or mechanism analysis
10. Limitations
11. Inspiration for the user's work
12. Summary and Q&A

Use conclusion-style titles, not generic titles like "Method", "Experiments", or "Results".

## Figure And Source Rules

For research decks:

- Use original paper figures first when they support the argument.
- Do not hallucinate figures that are not in the paper.
- Preserve axes, legends, labels, units, and captions.
- Crop unnecessary white margins without removing scientific information.
- Prefer one large readable figure over several tiny figures.
- Use annotations or zoom-in crops when they improve explanation.
- Track every external figure with source, page, target slide, purpose, and citation note.
- Do not present published figures as the user's original work.
- Remind the user to check copyright and permissions when public distribution is planned.

Recommended manifest fields:

| Field | Meaning |
|---|---|
| file | extracted or generated asset path |
| source | paper, dataset, screenshot, or generated-image prompt/source |
| page | source page when available |
| figure | source figure number when available |
| target slide | slide where the figure appears |
| purpose | why the figure is used |
| note | citation, copyright, or generation label |

## AI Image Policy

AI-generated images are for atmosphere, explanation, and conceptual support. Original paper figures are for evidence, results, and scientific credibility.

AI-generated images may be used sparingly for:
- cover pages
- abstract or summary pages
- research background
- motivation
- section transitions
- technical route overviews
- conceptual mechanism explanations
- conclusion or ending pages

AI-generated images must not replace:
- experimental data
- simulation cloud maps
- CFD result plots
- validation curves
- comparison tables
- paper result figures

Label AI-generated academic visuals as:

`conceptual illustration / AI-generated`

or, for Chinese decks:

`概念示意 / AI生成`

## Speaker Notes Rule

Do not place long speaker notes or large "talking points" boxes on formal slides unless the user explicitly requests a review-only teaching version.

Default:
- Put speaker notes in PowerPoint speaker notes if supported.
- If speaker notes are not supported by the generation method, write them to `slide_script.md`.
- Keep formal slides concise.
- Remove review-only notes before final delivery.

## Chinese Text Validation

Before claiming a generated deck is finished:

- Render or inspect preview images if possible.
- Check that Chinese text is readable.
- Check that no slide contains repeated `????`.
- Check mixed Chinese-English typography and punctuation.
- Treat garbled Chinese as a build failure that must be repaired.

## Versioning And File Organization

Never overwrite previous deck outputs by default.

Use clear version names, for example:
- `paper-reading-v0.1.pptx`
- `paper-reading-v0.2-template.pptx`
- `paper-reading-v0.3-polished.pptx`

Recommended working structure:

```text
deck_work/
  outline.md
  slide_script.md
  speaker_notes.md
  references.md
  figure_manifest.md
  assets/
    extracted_figures/
    pdf_pages/
    crops/
  output/
  preview/
```

Do not scatter extracted images, generated previews, or output PPT files in the project root.

## Final Review Checklist

Before final output, check:

1. Is the deck story clear?
2. Is the provided template actually used when requested?
3. Are title positions and sizes consistent?
4. Is body text readable?
5. Are figures large enough?
6. Are captions and source notes clear?
7. Are sources tracked?
8. Are speaker notes hidden from formal slides?
9. Is there no Chinese garbling?
10. Does every slide have one main message?
11. Does the deck have a realistic presentation rhythm?
12. Is scientific credibility stronger than decoration?
