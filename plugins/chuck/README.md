# Chuck Plugin — Visual Configurator for Claude Code

> Interactive HTML playgrounds for [chuck-core](https://www.npmjs.com/package/chuck-core) — the smart context injection tool for Claude Code.

This plugin adds two visual tools to Claude Code via the Playground plugin system:

---

## Playgrounds

### Chuck Setup Wizard
Visually configure your Chuck setup and generate a `manifest.json` — no JSON hand-editing required.

- Select your tech stack (React, TypeScript, React Native, Expo, Supabase, Git, and more)
- Adjust token budget and settings
- Live syntax-highlighted manifest.json preview
- Copy button — paste directly into `.chuck/manifest.json`
- Presets: React Native App, Web Full-Stack, Python API

### Chuck Decision Logger
Log architectural decisions to Chuck's Decision Ledger through a visual form.

- Fill in decision, rejected alternatives, reason, constraints, tags
- Live preview: decision JSON + the formatted one-liner Claude will see
- Copy button — outputs the pre-filled `chuck decide` command
- Auto-generates the decision ID from your decision text

---

## Installation

Install [chuck-core](https://www.npmjs.com/package/chuck-core) first:

```bash
npm install -g chuck-core
chuck init
chuck install-hook
```

Then add this plugin to your Claude Code configuration.

---

## What is Chuck?

Chuck is a Claude Code hook that injects only the rules Claude needs for each prompt — React rules when building components, Git rules when committing. It also maintains a Decision Ledger so Claude never re-suggests what you already rejected.

- **chuck-core on npm** — `npm install -g chuck-core`
- **GitHub** — https://github.com/cssmith615/chuck

---

## License

Apache 2.0
