# GitHub Profile README Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Create a visually rich, auto-updating GitHub profile README for @GalacticTitan.

**Architecture:** Single `README.md` file using GitHub-flavored Markdown with inline HTML for layout control. External services (github-readme-stats, streak-stats, activity-graph, skillicons.dev, shields.io, komarev) provide auto-updating visual widgets via image URLs. No build step or CI required.

**Tech Stack:** Markdown, HTML (inline), shields.io, github-readme-stats, github-readme-streak-stats, github-readme-activity-graph, skillicons.dev, readme-typing-svg, komarev/github-profile-views-counter

**Spec:** `docs/superpowers/specs/2026-04-01-github-profile-readme-design.md`

---

### Task 1: Create README.md with Hero / Header Section

**Files:**
- Create: `README.md`

- [ ] **Step 1: Create README.md with animated typing header, bio, and social badges**

```markdown
<div align="center">

<!-- Animated Typing Header -->
<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=1000&color=58A6FF&center=true&vCenter=true&multiline=true&repeat=true&width=700&height=100&lines=AI+Commander+%7C+AI+VFX+%7C+AI+Gaming;Building+Open-Source+Flutter+Infrastructure" alt="Typing SVG" /></a>

<!-- Bio -->
<p>
Founder of <a href="https://github.com/Ikolvi"><b>Ikolvi</b></a> — building production-grade open-source Flutter infrastructure.<br/>
9+ years shipping mobile apps (Android, iOS, Web). Co-Founder at <b>KRMR Solutions</b>.<br/>
Creator of <a href="https://www.youtube.com/@DoWonderStudio"><b>DoWonder Studio</b></a> (3D Art / VFX). Previously SDE-3 at Bijak.<br/>
From Kerala, India 🇮🇳
</p>

<!-- Social Badges -->
<p>
<a href="https://github.com/GalacticTitan"><img src="https://img.shields.io/badge/GitHub-GalacticTitan-181717?style=for-the-badge&logo=github" alt="GitHub" /></a>
<a href="https://www.linkedin.com/in/k-b-j/"><img src="https://img.shields.io/badge/LinkedIn-k--b--j-0A66C2?style=for-the-badge&logo=linkedin" alt="LinkedIn" /></a>
<a href="https://medium.com/@kiranbjm"><img src="https://img.shields.io/badge/Medium-@kiranbjm-000000?style=for-the-badge&logo=medium" alt="Medium" /></a>
<a href="https://www.youtube.com/@DoWonderStudio"><img src="https://img.shields.io/badge/YouTube-DoWonderStudio-FF0000?style=for-the-badge&logo=youtube" alt="YouTube" /></a>
<a href="https://www.instagram.com/kiran_bjm/"><img src="https://img.shields.io/badge/Instagram-kiran__bjm-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram" /></a>
<a href="https://buymeacoffee.com/kiranbjm"><img src="https://img.shields.io/badge/Buy_Me_A_Coffee-kiranbjm-FFDD00?style=for-the-badge&logo=buymeacoffee&logoColor=black" alt="Buy Me A Coffee" /></a>
</p>

</div>
```

- [ ] **Step 2: Verify the header renders**

Open the file in VS Code markdown preview (Cmd+Shift+V) and verify:
- Typing SVG URL is well-formed (test by opening the URL in a browser)
- All 6 social badges show correct text/icons
- Everything is centered

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat: add profile README hero section with typing header, bio, and social badges"
```

---

### Task 2: Add Featured Projects Section

**Files:**
- Modify: `README.md` (append after the closing `</div>` of the hero section)

- [ ] **Step 1: Append featured projects section**

Add the following after the hero section's closing `</div>`:

```markdown

---

## ⭐ Featured Projects

<div align="center">
<a href="https://github.com/Ikolvi/Tracelet"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Ikolvi&repo=Tracelet&theme=tokyonight&hide_border=true" alt="Tracelet" /></a>
<a href="https://github.com/Ikolvi/Titan"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Ikolvi&repo=Titan&theme=tokyonight&hide_border=true" alt="Titan" /></a>
<a href="https://github.com/Ikolvi/callbundle"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Ikolvi&repo=callbundle&theme=tokyonight&hide_border=true" alt="CallBundle" /></a>
<a href="https://www.youtube.com/@DoWonderStudio"><img src="https://img.shields.io/badge/🎬_DoWonder_Studio-3D_Art_|_VFX_|_Animation-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="DoWonder Studio" /></a>
</div>

<details>
<summary><b>📌 More Projects</b></summary>
<br/>

| Project | Description |
|---------|-------------|
| [QuicUI](https://github.com/Ikolvi/QuicUI) | Server-driven UI framework for Flutter — JSON-to-native rendering, 70+ widgets |
| [TitanForge](https://github.com/Ikolvi/TitanForge) | VS Code extension bridging AI assistants and running Flutter apps via MCP tools |
| [NodeCo](https://github.com/Ikolvi/NodeCo) | AI-friendly binary programming language built in Rust |
| [xlsxparser](https://github.com/GalacticTitan/xlsxparser) | Android Excel streaming reader library (⭐ 5) |

</details>
```

- [ ] **Step 2: Verify pin cards render**

Open each `github-readme-stats` pin URL in a browser to confirm they return valid SVGs:
- `https://github-readme-stats.vercel.app/api/pin/?username=Ikolvi&repo=Tracelet&theme=tokyonight&hide_border=true`
- `https://github-readme-stats.vercel.app/api/pin/?username=Ikolvi&repo=Titan&theme=tokyonight&hide_border=true`
- `https://github-readme-stats.vercel.app/api/pin/?username=Ikolvi&repo=callbundle&theme=tokyonight&hide_border=true`

Verify the collapsible "More Projects" section expands in markdown preview.

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat: add featured projects section with auto-updating pin cards"
```

---

### Task 3: Add Tech Stack Section

**Files:**
- Modify: `README.md` (append after the featured projects section)

- [ ] **Step 1: Append tech stack section**

Add the following after the featured projects section:

```markdown

---

## 🛠️ Tech Stack

<div align="center">
<img src="https://skillicons.dev/icons?i=dart,flutter,kotlin,swift,java,ts,python,rust,cpp&theme=dark" alt="Languages" /><br/>
<img src="https://skillicons.dev/icons?i=nodejs,firebase,supabase,git,githubactions,vscode,godot,docker,sqlite,postgres&theme=dark" alt="Tools & Platforms" />
</div>
```

- [ ] **Step 2: Verify icons render**

Open the skillicons.dev URLs in a browser to confirm they return icon strips:
- `https://skillicons.dev/icons?i=dart,flutter,kotlin,swift,java,ts,python,rust,cpp&theme=dark`
- `https://skillicons.dev/icons?i=nodejs,firebase,supabase,git,githubactions,vscode,godot,docker,sqlite,postgres&theme=dark`

Any icons that fail to render: check the exact icon ID at https://skillicons.dev and fix.

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat: add tech stack section with skillicons"
```

---

### Task 4: Add GitHub Stats & Graphs Section

**Files:**
- Modify: `README.md` (append after the tech stack section)

- [ ] **Step 1: Append stats and graphs section**

Add the following after the tech stack section:

```markdown

---

## 📊 GitHub Stats

<div align="center">
<img src="https://github-readme-stats.vercel.app/api?username=GalacticTitan&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" alt="GitHub Stats" height="180" />
<img src="https://github-readme-streak-stats.herokuapp.com/?user=GalacticTitan&theme=tokyonight&hide_border=true" alt="GitHub Streak" height="180" />
</div>

<div align="center">
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=GalacticTitan&layout=compact&theme=tokyonight&hide_border=true&langs_count=10&hide=html,css,cmake" alt="Top Languages" height="180" />
</div>

<div align="center">
<img src="https://github-readme-activity-graph.vercel.app/graph?username=GalacticTitan&theme=tokyo-night&hide_border=true&area=true" alt="Contribution Graph" width="100%" />
</div>
```

- [ ] **Step 2: Verify all stats URLs render**

Open each URL in a browser:
- Stats card: `https://github-readme-stats.vercel.app/api?username=GalacticTitan&show_icons=true&theme=tokyonight&hide_border=true&count_private=true`
- Streak: `https://github-readme-streak-stats.herokuapp.com/?user=GalacticTitan&theme=tokyonight&hide_border=true`
- Top langs: `https://github-readme-stats.vercel.app/api/top-langs/?username=GalacticTitan&layout=compact&theme=tokyonight&hide_border=true&langs_count=10&hide=html,css,cmake`
- Activity graph: `https://github-readme-activity-graph.vercel.app/graph?username=GalacticTitan&theme=tokyo-night&hide_border=true&area=true`

All should return SVG images. If any 404 or error, try alternative hosting (e.g., switch `herokuapp.com` to `streak-stats.demolab.com` for streak stats).

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat: add auto-updating GitHub stats, streak, languages, and activity graph"
```

---

### Task 5: Add Career Timeline Section

**Files:**
- Modify: `README.md` (append after the stats section)

- [ ] **Step 1: Append career timeline section**

Add the following after the stats section:

```markdown

---

## 🏢 Career Journey

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
```

- [ ] **Step 2: Verify rendering**

Check in markdown preview that the code block renders correctly with emoji visible and alignment preserved.

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat: add career timeline section"
```

---

### Task 6: Add Achievements & Footer Section

**Files:**
- Modify: `README.md` (append after the career timeline section)

- [ ] **Step 1: Append achievements and footer**

Add the following after the career timeline section:

```markdown

---

## 🏆 GitHub Achievements

<div align="center">

🌟 **Starstruck** · 👥 **Pair Extraordinaire** · 🦈 **Pull Shark x3** · ⚡ **Quickdraw** · 🤠 **YOLO** · 🧊 **Arctic Code Vault Contributor**

</div>

---

<div align="center">

<img src="https://komarev.com/ghpvc/?username=GalacticTitan&style=for-the-badge&color=58A6FF" alt="Profile Views" />

<br/><br/>

<a href="https://buymeacoffee.com/kiranbjm"><img src="https://img.shields.io/badge/☕_Support_My_Work-Buy_Me_A_Coffee-FFDD00?style=for-the-badge&logo=buymeacoffee&logoColor=black" alt="Buy Me A Coffee" /></a>

<br/><br/>

*🤨 One ending game*

</div>
```

- [ ] **Step 2: Verify footer renders**

Open the komarev URL in a browser:
- `https://komarev.com/ghpvc/?username=GalacticTitan&style=for-the-badge&color=58A6FF`

Should return a badge SVG with a view count. Check markdown preview for overall appearance.

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat: add achievements section and footer with profile views counter"
```

---

### Task 7: Final Review & Polish

**Files:**
- Modify: `README.md` (if adjustments needed)

- [ ] **Step 1: Full file review**

Read the complete `README.md` from top to bottom. Check:
1. All sections present in correct order: Hero → Featured Projects → Tech Stack → Stats → Career → Achievements/Footer
2. No broken markdown (unclosed tags, mismatched divs)
3. All URLs are well-formed (no typos in usernames, repo names)
4. Consistent theme across all widgets (`tokyonight` theme, `hide_border=true`)
5. All `<div align="center">` tags are properly closed

- [ ] **Step 2: Test all external service URLs**

Open each external URL in a browser (9 URLs total):
1. Typing SVG
2. Tracelet pin card
3. Titan pin card
4. callbundle pin card
5. skillicons row 1
6. skillicons row 2
7. Stats card
8. Streak stats
9. Activity graph

Fix any that return errors.

- [ ] **Step 3: Final commit**

```bash
git add README.md
git commit -m "chore: final polish and URL verification for profile README"
```

- [ ] **Step 4: Push to GitHub**

The user should push this to their `GalacticTitan/GalacticTitan` repo:

```bash
git push origin main
```

Then visit https://github.com/GalacticTitan to verify the profile README renders correctly on GitHub.
