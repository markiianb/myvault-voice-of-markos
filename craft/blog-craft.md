---
chunk_id: "blog-craft"
domain: "craft"
category: "craft"
subcategory: "blog"
context_tags:
  - "blog-format"
  - "long-form"
  - "reader-path"
  - "distribution"
  - "series"
depends_on:
  - "voice"
  - "opinions"
  - "stories"
  - "edit-craft"
token_count: ~700
version: "1.0"
last_updated: "2026-04-20"
status: "active"
summary: >-
  How Markos's blog posts are shaped — length, pull quotes, reading time, TOC,
  heading hierarchy, series identity, dual titles, internal linking, lead
  capture, bio format. Load when the draft is a blog post, not a LinkedIn post.
---

# Markos — Blog Craft

Load when the draft is a blog post under Markos's byline.

The voice, opinion, guardrail, and edit rules from the other chunks apply unchanged. This chunk covers what's different about the long-form container.

---

## Length

| Format | Target | Hard cap |
|---|---|---|
| Standard blog | 1,500–2,500 words | 3,000 |
| Series post (pillar) | 2,500–3,500 words | 4,000 |
| Founder-log update | 600–1,200 words | 1,500 |

Past the hard cap, split into two posts. Markos's audience skims; long posts without navigation lose them.

---

## Reader path: reading time, TOC, pull quotes

- **Reading time** at the top of every post. Calculate at 200 wpm, round up.
- **Anchor-link TOC** above the first H2 for every post over 2,000 words.
- **Pull quotes** — 1–2 per post, visually broken out. Anchored to specific claims, not punchlines. Screenshotable on a phone. These are the shareable units.

---

## Heading hierarchy

- H1: post title (one)
- H2: major sections
- H3: subsections within a major section
- **No H4 or deeper.** If the draft needs H4, the section is a separate post.
- Hierarchy stays consistent across every post in a series.

---

## Series identity

When a post is part of a series:

- **One visual framework diagram** designed once, reused unchanged in every post. Treat it as the series identity element.
- **Hub-and-spoke linking** — every series post links back to a pillar page and forward to the next post. Every post links to every other post in the series at least once.
- **Series indicator** in the subtitle ("Part N in a series on X").
- **Preview the next post** at the end with substance, not a placeholder.

---

## Titles: editorial vs SEO

Every blog post needs two titles:

- **Editorial title** — voice-led; appears as H1 and in social shares ("The guardrails are gone. Now what?")
- **SEO title** — searchable; appears in the `<title>` tag ("Enterprise AI governance framework: when vendor safeguards aren't enough")

Most CMSes accept both separately. If only one is allowed, use the SEO title in the `<title>` tag and the editorial title as H1.

**Why two:** the editorial title earns the click from social and repeat readers; the SEO title earns the click from search. The same phrase rarely does both jobs well.

---

## Internal linking

Every blog post links to at least:

- **2 other MyVault pages** — company blog posts, product pages, feature explainers
- **1 related Markos post** if one exists
- **1 external authoritative source per 500 words** — academic paper, government source, legal text, respected trade publication

No links to vendor marketing pages. No "as I wrote about X" links without a real linked target.

---

## Lead capture and CTAs

Markos-bylined blogs route to:

- **Founder-log newsletter** (Markos's build log) — default for reflective or opinionated posts
- **Next post in the series** — for framework series posts
- **A downloadable artefact** (framework PDF, 90-day plan, checklist) — if one is ready and built

Never ship with an unresolved placeholder. `[CTA: Link]`, `[TODO]`, `[placeholder]`, `XXX` must be resolved or removed before publishing.

**Why founder-log over company newsletter:** Markos-bylined content attracts readers who want *him*, not the product. Route them where the relationship continues. Company newsletter sign-ups from Markos's blog convert worse and erode both lists.

---

## Bio block

- Third person throughout. No first-person slip inside the bio.
- Cleared credentials only. Every claim cross-checked against `identity/identity.md`.
- Company-sale credentials — fully held, profitable, no debt — are the only money details cleared for public use.
- If a claim isn't in `identity.md`, flag for Markos sign-off before publishing. Do not infer credentials from track record.

---

## What carries over unchanged from LinkedIn

All of the following apply identically:

- The four voice qualities (systems-thinker, evidence-led, diagnostic, warm expertise)
- The five failure portraits (Agency, Preacher, Lecture Hall, LinkedIn Lottery, Hot Take)
- Banned words, cringe list, preach phrases
- Mode selection (Explain / Challenge-from-evidence / Educate — never Preach)
- Guardrails with their reasoning categories
- Opinion activation (see `opinions/opinions.md`)
- Story activation (see `stories/stories.md`)

**Genre note:** blogs are prescriptive by format (how-to, framework). Moderate prescriptive density is allowed where LinkedIn would flag it — *as long as* the core diagnostic arc holds: open with a scene, earn the framework, land on an implication (not a summary).

---

## Blog-specific failure patterns

Add these to the Pass 4 failure scan when editing a blog:

- **Framework-first open.** Post announces the framework before any scene. Fix: move a Tuesday-style scene to the top.
- **Closed-box conclusion.** "By day 90, you have a functioning X." Fix: close on an implication or the open question the next post will answer.
- **Uncaught placeholders.** `[CTA: Link]`, `[TODO]`, etc. Fix: resolve or remove.
- **Missing pull quotes.** No visually broken-out quotes. Fix: extract 1–2 anchored to specifics.
- **Heading hierarchy drift.** Inconsistent # and ## use, or H4+. Fix: rebuild to H1/H2/H3 only.
- **Teaser mismatch.** LinkedIn teaser promises content the blog doesn't deliver. Fix: align teaser, or add the section to the blog.
- **Label-vs-content mismatch.** Tier/label names contradict the examples (e.g. labelled "Prohibited" but example requires sign-off). Fix: rename the label or change the example.
- **Count mismatch.** Post promises N items and delivers M. Fix before publishing; AI drafts often miscount.

---

## Pre-publish checklist (blog-specific)

Run after the six-pass edit:

- [ ] Reading time at top, calculated at 200 wpm
- [ ] TOC present if post > 2,000 words
- [ ] 1–2 pull quotes marked, anchored to specifics
- [ ] H1/H2/H3 only, consistent within series
- [ ] Two titles set (editorial + SEO) where CMS supports it
- [ ] Internal links: ≥2 MyVault pages, ≥1 Markos post (if applicable), ≥1 external per 500 words
- [ ] CTA resolved — no placeholders
- [ ] Lead capture routes to founder-log unless artefact download is ready
- [ ] Bio third person; every claim in `identity/identity.md`
- [ ] Series linking present (back + forward + pillar page)
- [ ] Framework diagram attached if series post
