![ckw-skills — a Claude Code plugin marketplace of human-in-the-loop studios, deterministic design tooling, and MCP servers by Conner K. Ward](https://raw.githubusercontent.com/connerkward/ckw-skills/main/docs/banner.png)

# ckw-skills

A Claude Code **plugin marketplace** of skills **and MCP servers** by Conner K. Ward,
built around three ideas: **human-in-the-loop** generative studios, **determinism over
AI randomness**, and **traversing your own mass of data**.

This repo is an *index*, not the skills themselves — it ships a single
[`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json) manifest that
the `/plugin marketplace add` command reads to resolve and install each one from
its own repo (linked below).

## Install

```
/plugin marketplace add connerkward/ckw-skills
/plugin install lookdev@connerkward
```

The marketplace name stays `connerkward`, so installs are `<name>@connerkward`.

## Skills & servers

| Name | What it is | Repo |
|---|---|---|
| **lookdev** | Human-in-the-loop web studio to tune AI output by eye | [lookdev-studio-skill](https://github.com/connerkward/lookdev-studio-skill) |
| **deterministic-design** | Render + *measure* your UI (layout audit + vision-judged usability) | [deterministic-design-skill](https://github.com/connerkward/deterministic-design-skill) |
| **screenstudio-alternative** | Open-source headless Screen Studio alternative | [screenstudio-alternative-skill](https://github.com/connerkward/screenstudio-alternative-skill) |
| **ckw-design** | Frontend design: direction, system, philosophy | [ckw-design-skill](https://github.com/connerkward/ckw-design-skill) |
| **web-media-getter** | One query across free image/video/GIF APIs | [web-media-getter-skill](https://github.com/connerkward/web-media-getter-skill) |
| **macos-screen-recorder** | macOS screen recording with system audio (CLI) | [macos-screen-recorder-system-audio](https://github.com/connerkward/macos-screen-recorder-system-audio) |
| **lookdev-auto** | Automated vision-judged tuning loop | [lookdev-auto-skill](https://github.com/connerkward/lookdev-auto-skill) |
| **apple-notes** | MCP server: semantic search + connection-discovery across your own Apple Notes | [mcp-apple-notes](https://github.com/connerkward/mcp-apple-notes) |
| **muser** | Local-first semantic image search by description — on-device CLIP/SigLIP + LanceDB; CLI + MCP gallery | [Muser](https://github.com/connerkward/Muser) |
| **skeuo** | MCP server: turn a sentence into a real, *working* skeuomorphic music-player skin — switches flip, knobs turn, faders slide. Bundles the skill + an inline Create/preview ext-app | [skeuo-mcp](https://github.com/connerkward/skeuo-mcp) |

## Previews

Each image lives in its own skill repo's `docs/` and is linked here.

### lookdev — tune AI output by eye in a live studio
A real studio instance: a depth map extruded into a machinable XPS bas-relief, with live
controls for plaque size, board thickness, depth remap, material, lighting, and a sheet-layout
visualizer. You drag, it re-renders — you never guess a number. [repo](https://github.com/connerkward/lookdev-studio-skill)

![lookdev: bas-relief XPS extrusion studio rendering a depth map into a 3D relief, with a full control panel and ViewCube](https://raw.githubusercontent.com/connerkward/lookdev-studio-skill/main/docs/lookdev.png)

### deterministic-design — render the UI and *measure* it
The thesis, animated: balance is a measurable quantity. A layout's ink-weighted centroid must land on
the optical center — so the model *measures* the moment and self-balances (grow the heading, settle the
image) instead of asking an LLM to eyeball it. The demo itself is audited by the skill's own `layout-audit.js`. [repo](https://github.com/connerkward/deterministic-design-skill)

![deterministic-design: an animated layout self-balancing — the measured centroid sliding onto the optical center as the heading grows and the image settles](https://raw.githubusercontent.com/connerkward/deterministic-design-skill/main/docs/demo.gif)

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

### apple-notes — search and connect your own corpus of notes
An MCP server that turns your Apple Notes into a searchable, traversable corpus: hybrid
semantic + keyword search, Swanson-ABC **bridges** (non-obvious A↔C links via a shared note),
entity threads, related-notes, and cited **synthesis** over everything you've written. Search,
embeddings, and bridges run on-device; only synthesis calls an LLM (local or cloud). Installs as
a plugin *and* registers the MCP server in one step. [repo](https://github.com/connerkward/mcp-apple-notes)

![mcp-apple-notes: semantic search over Apple Notes with hybrid ranking and connection-discovery](https://raw.githubusercontent.com/connerkward/mcp-apple-notes/main/images/demo.png)

### muser — find images by describing them
Local-first semantic image search: index folders of images, then query them in natural language ("sunset over water", "a login screen with a blue button"). On-device SigLIP/CLIP embeddings + LanceDB — fully offline, no API keys. Ships as a CLI, an MCP server with an interactive results gallery, and a skill. [repo](https://github.com/connerkward/Muser)

![muser: live demo — typing "sunset over water" then "iridescent abstract gradient", each returning a ranked on-device semantic-search grid](https://raw.githubusercontent.com/connerkward/Muser/main/docs/demo.gif)

### skeuo — a sentence becomes a real, working skeuomorphic skin
Say *"a fanged anglerfish jaw"* and get back a finished music-player: a body shaped like that jaw,
with genuinely working hardware — switches that flip, knobs that turn, faders that slide — composited
live over a WebAudio engine. The prompt is the device's *silhouette*; the controls come from a chosen
variant, aligned true by construction (drawn inside the painted mask, never detected or repaired).
Installs as a plugin *and* registers the MCP server, bundling the `skeuo-skin-generator` skill and an
inline Create/preview ext-app. [repo](https://github.com/connerkward/skeuo-mcp) · [live demo](https://skeuo-ui.pages.dev)

![skeuo: skeuomorphic music-player skins with working switches, knobs, and faders generated from one-sentence prompts](https://raw.githubusercontent.com/connerkward/skeuo-ui/main/docs/skeuo-card.png)

MIT © Conner K Ward
