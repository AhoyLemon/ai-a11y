# Can AI Pass Your Accessibility Audit? Yes. Also No.

[![RevealJS](https://img.shields.io/badge/reveal.js-000?style=for-the-badge&labelColor=F2E142&logo=reveal.js&logoColor=111&color=222)](https://revealjs.com/)
[![Pug](https://img.shields.io/badge/Pug-000?style=for-the-badge&labelColor=A86454&logo=pug&logoColor=white&color=222)](https://pugjs.org/)
[![Sass](https://img.shields.io/badge/Sass-000?style=for-the-badge&labelColor=CD6799&logo=sass&logoColor=white&color=222)](https://sass-lang.com/)

## The talk

You've already had this argument. Someone dropped an AI accessibility scanner's report into Slack and said "See? we're basically done." and somebody else in the room aged five years in real time. Nobody misread the findings. They misread how final they were.

Good news first: some of this is easier than you think. Claude and Codex know the WCAG spec by heart. They know to scour for missing labels, busted focus states, and contrast that never should have shipped. That doesn't replace you. It just narrows down where you're actually needed. That's the part that never actually finishes: Accessibility isn't a state you reach and walk away from, it's a habit of making things a little better than you found them, forever.

In this high-energy session, Lemon walks through the actual system he built to put that split into practice, one that hands you a clean verdict on every accessibility check: pass, fail, or needs a human to look. That's the actual bar, not a marketing one. You'll leave with an actual workflow, not just the philosophy behind it.

| Event | When | Where |
|---|---|---|
| [Build Stuff](https://buildstuff.events/) | Wed 2 Dec 2026, 12:15 | Vilnius, room Alpha |
| [NDC London](https://ndclondon.com/) | Wed 27 Jan 2027, 15:00 | Queen Elizabeth II Centre, Room 1 |

The deck lives at [ahoylemon.github.io/ai-a11y](https://ahoylemon.github.io/ai-a11y/). The planning docs are in [`docs/`](docs/), starting with [`docs/TIMELINE.md`](docs/TIMELINE.md).

## About this repo

A [reveal.js](https://revealjs.com/) presentation template with Pug, Sass, and modern build tools. Every deck starts on the Lemon deck system: a 1280×720 canvas, Syne, Yrsa and Share Tech Mono, statements hung high and flush left, and one dissolve between slides. Retune it per talk from `scss/talk.scss`.

## Prerequisites

You'll need both [Node.js](https://nodejs.org/) and [Bun](https://bun.sh/). The build scripts run on Node (through `tsx`, and some chain `npm run`), and the demo TypeScript build shells out to `bun build`.

## Getting Started

1. Click [Use This Template](https://github.com/AhoyLemon/new-talk/generate) to use this repo as a project template.
1. Clone your new repository locally
1. Run `bun install`[^1] to install dependencies. It also warns you if the deck's three fonts aren't installed locally (they load from Google Fonts, but a local copy keeps the deck right offline).
1. Run `bun run setup` to configure your talk's title, URL, handle and description
1. Run `bun run dev` to start the development server
1. On GitHub, set Settings → Pages → Source to **GitHub Actions** so pushes to `main` deploy

[^1]: Any bun command works with npm as well, eg `npm install`, `npm run setup`, `npm run dev`, etc. Use `bun run test`, not `bun test`: the latter is bun's own test runner and ignores the script.

## Commands

```bash
bun run dev             # Start the dev server with live reload
bun run build           # Build all Pug, Sass and demo TypeScript
bun run test            # Check Sass compiles, TypeScript typechecks, the script tests pass, and every Pug page renders
bun run update:reveal   # Copy reveal.js from node_modules into the vendored reveal/ folder
bun run check:fonts     # Warn if Yrsa, Syne or Share Tech Mono aren't installed locally
```

## How do I edit the deck?

- A fresh talk starts with the catalogue of every slide template ([`pug/examples/_example-slides.pug`](pug/examples/_example-slides.pug)) between the shared intro and outro. Browse it, copy what you need into your own files in `pug/sections/`, then swap its include in [`pug/index.pug`](pug/index.pug) for yours.
  - [`pug/partials/_mixins.pug`](pug/partials/_mixins.pug) has the mixins, like `+demo`, `+image`, `+iframe` and `+gag`.
- The look lives in [`scss/lemon/`](scss/lemon/), and [`docs/LEMON-DECK.md`](docs/LEMON-DECK.md) explains it. Put this talk's own styles, and any colour retuning, in [`scss/talk.scss`](scss/talk.scss).
- **Need help with demos?** See [`demos/demos.md`](demos/demos.md)
- Edit [`js/reveal-config.js`](js/reveal-config.js) for reveal.js settings, but leave the canvas, `display`, `center` and `transition` alone unless you've read why they're set.
- Working with an AI tool? [`docs/REPO.md`](docs/REPO.md) is the repo guide it reads.
- Need additional reveal.js help? Check out the [reveal.js documentation](https://revealjs.com/).

## Updating reveal.js

When you want to update to the latest version of reveal.js:

1. Update the reveal.js dependency: `bun update reveal.js`
2. Copy the new files: `bun run update:reveal`
3. Walk the deck, then commit the updated `reveal/` folder

## License

[CC-BY-4.0](LICENSE) - Creative Commons Attribution 4.0 International License
