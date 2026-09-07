# PPT Basic Deduction

A reusable **Skill** for AI Agents (Kimi, Claude Code, Workbuddy, etc.): **learn from a PPT and produce a Markdown note that re-expresses the knowledge rather than transcribing the slides page by page.**

Transform PPT / slide-deck content into a **comprehension-oriented** Markdown note. Use this skill whenever a user hands you a PPT, PPTX, PDF handout, slide screenshots, or exported lecture notes and asks you to take notes, organize, summarize, digest, review, convert to Markdown, or output study notes.

The deliverable is **not** a mirror summary of the PPT—it is a reconstructed note written by a smart learner *after* studying the material: a third party (human or AI) should be able to deliver a complete, accurate presentation of every key point and logical thread in the original PPT based solely on this note.

The methodology blends the **Feynman Technique**, **Progressive Summarization**, and **knowledge deconstruction & reconstruction**. Images, frameworks, topology diagrams, and logic diagrams from the PPT are restored natively with Mermaid, tables, ASCII art, or structured text. Page numbers, file names, "slide / page X", or any other provenance metadata are strictly forbidden.

## Core Features

- **Comprehension-oriented reconstruction, no transcription** — Dismantle the original page order and reorganize by cognitive logic. Write with the Feynman Technique: explain jargon in plain language on the spot; every causal claim must answer "why"; expose and eliminate comprehension blind spots as you write.
- **Progressive Summarization** — One-sentence overview → bullet-point quick view → layered expanded body → optional appendix. Readers can stop at any level.
- **Native diagram restoration** — Flowcharts, architecture diagrams, topology diagrams, and logic diagrams are restored with Mermaid / Markdown tables / ASCII art / structured text. No image references or screenshots allowed.
- **Zero metadata** — No page numbers, file names, "slide", "page X", or any provenance markers appear in the note.
- **Critical closing chapter** — The final chapter, *"The Author's Design and Shortcomings"*, restores the original author's design logic (target audience, narrative strategy, trade-off logic) and systematically audits shortcomings: objective constraints, cognitive blind spots, and intentional omissions (each judgment carries evidence; speculation is explicitly labeled).

## Methodology

Feynman Technique (explain concepts in plain language and self-test for blind spots) × Progressive Summarization (layered distillation from detailed to concise) × Knowledge Deconstruction & Reconstruction (break the original structure and reorganize by understanding).

## Installation

### Option 1: Install as a Kimi Work / Claude Code compatible Skill

Copy the `ppt-basic-deduction/` directory into your Skills directory:

- **Kimi Work**: `%APPDATA%\kimi-desktop\daimon-share\daimon\skills\`
- **Claude Code (user-level)**: `~/.claude/skills/` or `~/.config/agents/skills/`
- **Project-level**: `<project>/.agents/skills/`

### Option 2: Import the `.skill` distribution package

`ppt-basic-deduction.skill` is a zip-format distribution package (see Releases). Unzip and place it as described in Option 1.

## Usage

Hand the Agent a PPT / PPTX / PDF handout / slide screenshot and say **"use PPT Basic Deduction to organize this into notes"** to trigger it. Output is a single self-contained `.md` file.

## Directory Structure

```
ppt-basic-deduction/
├── SKILL.md                    # Main skill file: ironclad rules, six-step workflow, diagram-reconstruction rules, self-checklist
└── references/
    └── output-template.md      # Output structure template + good/bad writing examples + closing chapter examples
```

## License

MIT
