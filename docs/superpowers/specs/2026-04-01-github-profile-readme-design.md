# GitHub Profile README — Design Spec

**Date:** 2026-04-01
**Author:** Kiran Benny Joseph (@GalacticTitan)
**Status:** Approved

## Goal

Build a visually rich, auto-updating GitHub profile README for github.com/GalacticTitan. The file lives in a `GalacticTitan/GalacticTitan` special repo as `README.md`. It should showcase professional identity, featured projects, tech stack, career history, and GitHub activity — with minimal ongoing maintenance.

## Design Principles

- **Balanced mix:** Professional structure with creative flair (emoji, badges, graphs).
- **Auto-updating where possible:** 7 of 11 visual elements use third-party services that pull live data from the GitHub API. No manual updates needed for stats, stars, streaks, languages, or contribution graphs.
- **No blog section:** Medium link included in social badges; no dedicated posts section.
- **Accurate data only:** All information verified against GitHub, LinkedIn, and Buy Me a Coffee profiles.

## Profile Data (Verified)

- **Name:** Kiran Benny Joseph
- **GitHub:** @GalacticTitan
- **Location:** Kerala, India
- **Tagline:** AI Commander | AI VFX | AI Gaming
- **Bio status:** 🤨 One ending game
- **Contributions (last year):** 3,340
- **GitHub Achievements:** Starstruck, Pair Extraordinaire, Pull Shark x3, Quickdraw, YOLO, Arctic Code Vault Contributor
- **Organizations:** Ikolvi, OpenHomePlanet

### Social Links

| Platform | URL |
|----------|-----|
| GitHub | https://github.com/GalacticTitan |
| LinkedIn | https://www.linkedin.com/in/k-b-j/ |
| Medium | https://medium.com/@kiranbjm |
| YouTube | https://www.youtube.com/@DoWonderStudio |
| Instagram | https://www.instagram.com/kiran_bjm/ |
| Buy Me a Coffee | https://buymeacoffee.com/kiranbjm |

### Career Timeline

| Period | Role | Company | Notes |
|--------|------|---------|-------|
| 2025–Present | Founder | Ikolvi | Tracelet, Titan, QuicUI, CallBundle |
| 2024–Present | Co-Founder | KRMR Solutions | Part-time, remote |
| 2023–Present | Founder | DoWonder Studio | 3D Art, VFX, Animation |
| Aug–Oct 2024 | SDE-3 | Bijak | Payment gateways, API integration |
| Nov 2021–Jul 2024 | SDE-2 | Bijak | Flutter, cross-platform mobile |
| Dec 2020–Nov 2021 | Flutter/Android/Node.js Dev | Inmenzo Technologies | Cross-platform apps, backend |
| Nov 2018–Nov 2020 | Flutter/Android Dev | Feathersoft | Thrissur, Kerala |
| Jan 2016–Nov 2018 | Android Developer | Inmenzo Technologies | First role |
| Education | B.E. Electronics & Communication | — | — |

### Featured Projects (4 primary)

| Project | Org | Description | Stars | Language |
|---------|-----|-------------|-------|----------|
| Tracelet | Ikolvi | Production-grade background geolocation for Flutter — motion detection, geofencing, SQLite persistence, HTTP sync, headless Dart. Fully open-source (Apache 2.0). 9 releases, native SDKs for Android & iOS. | 20 | Dart, Kotlin, Swift |
| Titan | Ikolvi | Signal-based reactive state management for Dart & Flutter. Zero boilerplate, surgical rebuilds, 25M allocations/sec. Includes Atlas routing, Colossus perf monitoring, Basalt infrastructure. Published on pub.dev. | 1 | Dart |
| CallBundle | Ikolvi | Native incoming/outgoing call UI for Flutter. CallKit (iOS) + TelecomManager + OEM-adaptive notifications (Android). Federated plugin architecture. | 3 | Kotlin, Dart, Swift |
| DoWonder Studio | — | 3D Art, VFX & Animation. YouTube channel @DoWonderStudio. | — | — |

### Secondary Projects (mentioned briefly)

| Project | Description |
|---------|-------------|
| QuicUI | Server-driven UI framework for Flutter — JSON-to-native rendering, 70+ widgets, pub.dev package |
| TitanForge | VS Code extension bridging AI assistants and running Flutter apps via MCP tools |
| NodeCo | AI-friendly binary programming language built in Rust |
| xlsxparser | Android Excel streaming reader library (5 stars, JitPack) |

### Tech Stack

**Languages:** Dart, Kotlin, Swift, Java, TypeScript, Python, Rust, GDScript, C++
**Frameworks:** Flutter, Node.js, Flask
**Tools & Platforms:** Firebase, Supabase, Git, GitHub Actions, VS Code, Godot, Docker
**Databases:** SQLite, ObjectBox, PostgreSQL

## README Structure

### Section 1: Hero / Header

- **Animated typing SVG** via `readme-typing-svg` (github.com/DenverCoder1/readme-typing-svg)
  - Text: `AI Commander | AI VFX | AI Gaming`
  - Centered, theme-aware colors
- **One-paragraph bio** (plain markdown, centered):
  > Founder of **Ikolvi** — building production-grade open-source Flutter infrastructure. 9+ years shipping mobile apps (Android, iOS, Web). Co-Founder at KRMR Solutions. Creator of **DoWonder Studio** (3D Art / VFX). Previously SDE-3 at Bijak. From Kerala, India 🇮🇳
- **Social badges row** (shields.io, centered):
  - GitHub, LinkedIn, Medium, YouTube, Instagram, Buy Me a Coffee
  - Style: `for-the-badge` (consistent across all badges)

**Update frequency:** Static. Only changes if tagline or bio changes.

### Section 2: Featured Projects

- **4 GitHub Readme Stats pin cards** via `github-readme-stats` (github.com/anuraghazra/github-readme-stats)
  - `Ikolvi/Tracelet`, `Ikolvi/Titan`, `Ikolvi/callbundle` — auto-pull stars, forks, language from API
  - DoWonder Studio — custom badge/link to YouTube (not a GitHub repo card)
- **Secondary projects** in a compact list below:
  - QuicUI, TitanForge, NodeCo, xlsxparser — one-liner each with link

**Update frequency:** Auto for GitHub repos (stars, forks update on page load). DoWonder Studio link is static.

### Section 3: Tech Stack

- **Single icon strip** via `skillicons.dev` URL:
  - `https://skillicons.dev/icons?i=dart,flutter,kotlin,swift,java,ts,python,rust,cpp,nodejs,firebase,supabase,git,githubactions,vscode,godot,docker,sqlite,postgres`
- Centered, one or two rows

**Update frequency:** Static. Only changes if new tech is added.

### Section 4: GitHub Stats & Graphs

Three widgets in a row (or stacked on narrow screens), all centered:

1. **GitHub Stats Card** — `github-readme-stats` api
   - Shows: stars, commits, PRs, issues, contributions
   - Theme: matching the README aesthetic
2. **Streak Stats** — `github-readme-streak-stats` (github.com/DenverCoder1/github-readme-streak-stats)
   - Shows: current streak, longest streak, total contributions
3. **Top Languages** — `github-readme-stats` top-langs card
   - Layout: `compact` or `donut`
   - Exclude: HTML, CSS, CMake (noise from forked repos)

4. **Contribution Activity Graph** — `github-readme-activity-graph` (github.com/Ashutosh00710/github-readme-activity-graph)
   - Full-width, themed to match

**Update frequency:** All auto-update on every page view (cached by the services, typically 30-min to 4-hour TTL).

### Section 5: Career Timeline

Compact markdown using emoji prefixes:

```
🏛️ 2025–Present   Founder @ Ikolvi — Tracelet, Titan, QuicUI, CallBundle
🎬 2023–Present   Founder @ DoWonder Studio — 3D Art, VFX, Animation
🤝 2024–Present   Co-Founder @ KRMR Solutions
💼 2024            SDE-3 @ Bijak
💼 2021–2024      SDE-2 @ Bijak
📱 2020–2021      Flutter / Android / Node.js Dev @ Inmenzo Technologies
📱 2018–2020      Flutter / Android Dev @ Feathersoft
📱 2016–2018      Android Developer @ Inmenzo Technologies
🎓                B.E. Electronics & Communication
```

**Update frequency:** Static. Only changes on job change.

### Section 6: Achievements & Footer

- **GitHub Achievements** listed as text with emoji (Starstruck, Pull Shark x3, Arctic Code Vault Contributor, etc.)
- **Profile views counter** via `komarev/github-profile-views-counter` — auto-updating badge
- **Buy Me a Coffee** link/badge
- **Sign-off** with the bio status: 🤨 One ending game

**Update frequency:** Views counter is auto. Achievements are static (update on new achievement).

## Third-Party Services Used

| Service | Purpose | Auto-updates? |
|---------|---------|---------------|
| readme-typing-svg | Animated header text | No (static config) |
| shields.io | Social link badges, custom badges | No (static config) |
| github-readme-stats | Stats card, top languages, repo pin cards | Yes (GitHub API) |
| github-readme-streak-stats | Contribution streak | Yes (GitHub API) |
| github-readme-activity-graph | Full-width activity chart | Yes (GitHub API) |
| skillicons.dev | Tech stack icon strip | No (static config) |
| komarev/github-profile-views-counter | Profile view count badge | Yes (on page view) |

## File Deliverable

A single `README.md` file to be placed in the `GalacticTitan/GalacticTitan` repository (GitHub special profile repo). The file uses standard GitHub-flavored Markdown with inline HTML for layout (centering, tables, image sizing).

## Out of Scope

- GitHub Actions workflows for auto-updating blog posts (no blog section)
- Custom CSS/themes (GitHub strips CSS from READMEs)
- Animated GIF/SVG snake contribution graph (adds complexity, fragile GitHub Action dependency)
- Detailed project descriptions beyond one-liners for secondary projects
