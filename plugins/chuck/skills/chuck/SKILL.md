---
name: chuck
description: Creates interactive HTML playgrounds for Chuck — the Claude Code context injection tool. Use when the user wants to configure Chuck visually, build a manifest.json, or log an architectural decision through a form interface.
---

# Chuck Playground Builder

Chuck is a Claude Code tool that injects the right rules and decisions into context automatically. This skill creates two HTML playgrounds that make Chuck setup and decision logging visual and approachable.

## When to use this skill

- User wants to set up Chuck for a new project visually
- User wants to configure their manifest.json without hand-editing JSON
- User wants to log a Decision Ledger entry through a form
- User asks for a "Chuck setup wizard" or "Chuck decision logger"

## Playgrounds

### 1. Chuck Setup Wizard
Load `templates/setup-wizard.md` and build the playground.

Use when: user wants to generate a manifest.json for their project.

Controls:
- Stack checkboxes: React, TypeScript, React Native, Expo, Supabase, Git, Node, Python, Vue, Next.js, Claude API
- Token budget slider: 500–4000 (default 2000)
- Devmode toggle (default off)
- GLOBAL rules textarea (short always-on rules)

Preview: live syntax-highlighted manifest.json that updates on every change.

Prompt output: the complete manifest.json content, ready to paste into `.chuck/manifest.json`.

### 2. Chuck Decision Logger
Load `templates/decision-logger.md` and build the playground.

Use when: user wants to log an architectural decision to the Chuck Decision Ledger.

Controls:
- Decision text input
- Rejected alternatives (tag chips — add/remove)
- Reason textarea
- Constraints (tag chips)
- Tags (tag chips)
- Project name input

Preview: live JSON decision entry + the formatted injection one-liner (what Claude will see).

Prompt output: the pre-filled `chuck decide` command, ready to paste into terminal.

## Core requirements (both playgrounds)

- Single HTML file. Inline all CSS and JS. No external dependencies.
- Live preview. Updates instantly on every control change.
- Copy button with "Copied!" feedback.
- Dark theme (#080810 background, #7C3AED purple accent — Chuck's color palette).
- Sensible defaults. Looks useful on first load.
- After writing the HTML file, run `open <filename>.html` to launch in browser.
