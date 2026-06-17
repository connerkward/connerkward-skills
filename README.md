![ckw-skills — a Claude Code plugin marketplace of human-in-the-loop studios and deterministic design tooling by Conner K. Ward](https://raw.githubusercontent.com/connerkward/ckw-skills/main/docs/banner.png)

# ckw-skills

A Claude Code **plugin marketplace** of skills by Conner K. Ward, built around two
ideas: **human-in-the-loop** generative studios and **determinism over AI
randomness**.

This repo is an *index*, not the skills themselves — it ships a single
[`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json) manifest that
the `/plugin marketplace add` command reads to resolve and install each skill from
its own repo (linked below).

## Install

```
/plugin marketplace add connerkward/ckw-skills
/plugin install lookdev@connerkward
```

The marketplace name stays `connerkward`, so installs are `<skill>@connerkward`.

## Skills

| Skill | What it is | Repo |
|---|---|---|
| **lookdev** | Human-in-the-loop web studio to tune AI output by eye | [lookdev-studio-skill](https://github.com/connerkward/lookdev-studio-skill) |
| **deterministic-design** | Render + *measure* your UI (layout audit + vision-judged usability) | [deterministic-design-skill](https://github.com/connerkward/deterministic-design-skill) |
| **screenstudio-alternative** | Open-source headless Screen Studio alternative | [screenstudio-alternative-skill](https://github.com/connerkward/screenstudio-alternative-skill) |
| **ckw-design** | Frontend design: direction, system, philosophy | [ckw-design-skill](https://github.com/connerkward/ckw-design-skill) |
| **web-media-getter** | One query across free image/video/GIF APIs | [web-media-getter-skill](https://github.com/connerkward/web-media-getter-skill) |
| **macos-screen-recorder** | macOS screen recording with system audio (CLI) | [macos-screen-recorder-system-audio](https://github.com/connerkward/macos-screen-recorder-system-audio) |
| **lookdev-auto** | Automated vision-judged tuning loop | [lookdev-auto-skill](https://github.com/connerkward/lookdev-auto-skill) |

## Previews

Each image lives in its own skill repo's `docs/` and is linked here.

### lookdev — tune AI output by eye in a live studio
A real studio instance: a depth map extruded into a machinable XPS bas-relief, with live
controls for plaque size, board thickness, depth remap, material, lighting, and a sheet-layout
visualizer. You drag, it re-renders — you never guess a number. [repo](https://github.com/connerkward/lookdev-studio-skill)

![lookdev: bas-relief XPS extrusion studio rendering a depth map into a 3D relief, with a full control panel and ViewCube](https://raw.githubusercontent.com/connerkward/lookdev-studio-skill/main/docs/lookdev.png)

### deterministic-design — render the UI and *measure* it
The thesis: balance is a measurable quantity, not a vibe. A layout balances like a see-saw — ink
weight × distance from center — so the model can *measure* the moment instead of asking an LLM to
eyeball it. (Preview placeholder; an animated example is in review.) [repo](https://github.com/connerkward/deterministic-design-skill)

![deterministic-design: a see-saw showing layout balance as a physical moment — a portrait and a text column balanced on a fulcrum](https://raw.githubusercontent.com/connerkward/deterministic-design-skill/main/docs/balance-explorable.png)

### screenstudio-alternative — headless Screen Studio pipeline
Auto speed-up of idle, auto-zoom on click clusters, keystroke overlays, a smoothed synthetic
cursor, and 9:16 vertical export — all from the CLI, no GUI, no subscription. [repo](https://github.com/connerkward/screenstudio-alternative-skill)

![screenstudio-alternative pipeline demo](https://raw.githubusercontent.com/connerkward/screenstudio-alternative-skill/main/docs/demo.gif)

### lookdev-auto — a vision model rates rendered variants in a loop
N labeled variants render into one contact sheet (params burned on each cell), a vision model
scores them and suggests new values, and the best is applied — the eye is automated, you run the
loop. [repo](https://github.com/connerkward/lookdev-auto-skill)

![lookdev-auto labeled variant contact sheet](https://raw.githubusercontent.com/connerkward/lookdev-auto-skill/main/docs/contact-sheet.png)

### macos-screen-recorder — CLI capture with system audio, no driver
Records the main display plus system audio via ScreenCaptureKit — the one gap QuickTime and
`screencapture -v` can't fill without a loopback driver. No BlackHole, no sudo, one Swift binary. [repo](https://github.com/connerkward/macos-screen-recorder-system-audio)

![macos-screen-recorder CLI usage](https://raw.githubusercontent.com/connerkward/macos-screen-recorder-system-audio/main/docs/usage.png)

### web-media-getter — one query, fanned out across free media sources
Searches free **images, videos, and GIFs** in one query — openverse, wikimedia, internet archive,
the Library of Congress, NASA (and, with free keys, Pexels / Pixabay / GIF engines) in parallel —
returning a normalized, license-tagged result list with attribution. The retrieval peer to local
search and generation. [repo](https://github.com/connerkward/web-media-getter-skill)

![web-media-getter: one apollo-moon-landing query returning results badged by source — internet archive, openverse, wikimedia, loc, nasa](https://raw.githubusercontent.com/connerkward/web-media-getter-skill/main/docs/example-output.png)

MIT © Conner K Ward
