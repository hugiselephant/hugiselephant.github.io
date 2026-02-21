# Hugi's Elephant — Site Roadmap

> Last updated: February 2026

---

## Current State

### Strengths
- Logseq → Hugo publishing pipeline with bidirectional backlinks (rare and valuable)
- Custom shortcodes preserving Logseq callout formatting
- Clean PaperMod theme, fast static site, solid GitHub Actions CI/CD
- 42 pages of personal writing across tech, philosophy, and travel
- Social presence: GitHub, YouTube, Twitter, LinkedIn, RSS

### Gaps to Address
- No About / Start Here page — visitors have no context on who you are or why to stay
- No clear site identity — hard to answer "what is this site for?"
- Contact form is broken (no backend)
- No newsletter or email capture
- Large unoptimized images (11 MB JPEG)
- Missing `date` / `description` frontmatter on several pages
- No book log, no mental models section

---

## Phase 1 — Fix the Foundation
*Target: 1–2 weeks, low effort, high leverage*

These small changes have outsized impact on first impressions and discoverability.

| Task | Why |
|------|-----|
| Add an **About / Start Here** page | First thing every serious visitor looks for |
| Fix or remove the broken contact form | A broken form signals neglect |
| Add a **newsletter signup** (Buttondown, Beehiiv, or Substack) | Email is the #1 channel for building loyal readers |
| Compress images — especially the 11 MB JPEG | Page speed affects both UX and SEO |
| Fill missing `date` and `description` frontmatter on all pages | Fixes archive ordering, sharing previews, and SEO |
| Add a `/now` page (Derek Sivers style) | Low maintenance, high signal — tells readers what you're currently focused on |

---

## Phase 2 — The Two Core Features
*Target: 2–4 weeks each*

### Book Log — `/books/`

A dedicated Hugo section where each book gets its own page. More valuable than Goodreads because it captures *your* thinking, not just ratings.

**Frontmatter structure per book:**
```yaml
title: "Thinking, Fast and Slow"
author: "Daniel Kahneman"
status: read          # options: want-to-read / reading / read
date_finished: 2024-03-15
rating: 5             # out of 5
tags: [mental-models, psychology, decision-making]
```

**What each book page contains:**
- Why you read it
- Key ideas and highlights
- How it changed your thinking
- Cross-links to related essays and mental models via backlinks

**Listing page features:**
- Sortable by date finished, rating, or tag
- Filter by status (read / reading / want to read)
- Shows rating, author, and your one-line summary

---

### Mental Models — `/models/`

A section dedicated to the mental models you've collected, created, and actively use.

**Implementation options:**

1. **Canvas embeds (Excalidraw / Miro)** — draw the model, export an embed snippet, drop it in via the existing `<iframe>` shortcode support
2. **SVG illustrations** — draw in Figma or Excalidraw, export as SVG, store in `/content/assets/`, embed inline — no external dependency, loads faster
3. **Text + diagram hybrid** — describe the model in prose, illustrate with a simple ASCII or SVG diagram

**Frontmatter structure per model:**
```yaml
title: "Von Hammerstein Matrix"
tags: [decision-making, leadership, productivity]
date: 2024-01-10
origin: collected     # options: collected / created / adapted
```

**Each model page contains:**
- What the model is
- When to use it
- A visual canvas or diagram
- Your personal examples and applications
- Cross-links to books and essays where it appears

---

## Phase 3 — Engagement and Readers
*Target: ongoing*

The sites that build real followings share a pattern: **a consistent format people can expect**.

### Publishing Cadence

- **Short notes** (5–10 min) published frequently — lower the bar, increase surface area
- **Long essays** polished and evergreen — the anchors of the site
- **Newsletter** — even monthly compounds over time; email is your most valuable asset

### Content Maturity Tags (Digital Garden Model)

Tag posts by maturity to signal what's polished vs. raw thinking. Reduces pressure to "finish" everything before publishing.

| Tag | Meaning |
|-----|---------|
| Seedling | Early idea, rough draft |
| Growing | Being actively developed |
| Evergreen | Polished, stable, worth reading |

### Cross-posting Strategy

Your essays are long enough to slice into Twitter/LinkedIn threads. Each thread drives readers back to the full post on the site. Use the existing social accounts (YouTube, Twitter, LinkedIn) intentionally.

---

## Phase 4 — Big Vision
*Target: 3–6 months*

### Ideal Site Structure

```
hugiselephant.com/
├── /essays          ← polished, long-form writing
├── /notes           ← short, frequent, raw thinking
├── /books           ← reading log with annotations and takeaways
├── /models          ← mental models with visual canvases
├── /now             ← what you're currently focused on (Derek Sivers)
└── newsletter       ← email list — your most valuable long-term asset
```

### Graph View

Your Logseq workflow and existing backlinks system puts you 80% of the way to a full knowledge graph view. [Quartz](https://quartz.jzhao.xyz/) is a Hugo-compatible static site generator built specifically for this — it adds an interactive graph visualization of how all notes connect.

Migrating to Quartz (or adding a graph view to the current setup) would be the most distinctive feature for a site of this type, making the interconnected nature of the thinking visible to readers.

### Community / Engagement Features

| Feature | Tool / Approach |
|---------|----------------|
| Comments | Giscus (GitHub Discussions-backed, free, no ads) |
| Newsletter | Beehiiv or Buttondown (both have free tiers, support embeds) |
| Reader Q&A | A dedicated page or Substack Notes-style short posts |
| Webmentions | Webmention.io — surfaces when others link to your posts |

---

## Priority Order

1. **About page + newsletter signup** — this week, affects every new visitor
2. **Book log section** — concrete, achievable, immediately useful for you and readers
3. **Mental models section** — start with 3–5 models you already use; add canvases over time
4. **Content maturity tags** — reduces friction to publish more frequently
5. **Newsletter cadence** — even once a month builds a compounding audience
6. **Graph view / Quartz migration** — bigger lift, but the most distinctive long-term feature

---

## Reference Sites

Sites worth studying for inspiration:

- [Maggie Appleton](https://maggieappleton.com) — digital garden with original SVG illustrations, mental models, essays
- [Simon Willison](https://simonwillison.net) — high-frequency short notes + long essays, excellent tagging
- [Derek Sivers](https://sive.rs) — books section, /now page, simple and personal
- [Andy Matuschak](https://andymatuschak.org) — evergreen notes, interconnected thinking
- [James Clear](https://jamesclear.com) — 3-2-1 newsletter format, consistent publishing cadence
