---
chunk_id: "post-craft"
domain: "craft"
category: "craft"
subcategory: "posts"
context_tags:
  - "posts"
  - "anchor"
  - "newsjack"
  - "build-note"
  - "structure"
depends_on:
  - "voice"
  - "opinions"
  - "stories"
  - "guardrails"
token_count: ~800
version: "1.1"
last_updated: "2026-06-10"
status: "active"
summary: >-
  How a Markos post gets built — the three formats (anchor, newsjack, build-note), opening and body and closing patterns, paragraph rhythm, and the draft-to-publish sequence.
---

# Post Craft

Every Markos post is one of three formats. Pick the format first. Then follow the patterns.

## The three post formats

### 1. Anchor post — long-form, opinion-led (1/week)

- **Length:** 250–600 words.
- **Register:** Authority-educator-challenger.
- **Arc:** Scene or diagnosis → pragmatic step-through → challenge-from-evidence → implication.
- **Role:** Weekly authority-builder. Pulls from a content pillar in `opinions/opinions.md`. Often pairs with a story from `stories/stories.md`.

### 2. Newsjack — react to AI/privacy news within 24h (1/week)

- **Length:** 100–250 words.
- **Register:** Challenge-from-evidence.
- **Arc:** News item → what most people will say about it → what Markos thinks they miss → pragmatic read.
- **Role:** Topicality, reach, relevance.
- Full template in `newsjack-craft.md`.

### 3. Build-note — short insight from founder experience (1/week)

- **Length:** 80–200 words.
- **Register:** Educator-practitioner.
- **Arc:** Specific scene or moment → the insight → the generalisable lesson.
- **Role:** Authenticity. This is where personal stories live. Feels like an off-the-cuff founder thought.

## Opening patterns that sound like Markos

- **The specific scene.** "A few months back I got a $100,000 Google Cloud bill while on vacation."
- **The industry diagnosis.** "Most orgs rolling out AI are rolling out work practices, not governance frameworks."
- **The pragmatic reframe.** "Back to basics for a minute."
- **The contrarian setup.** "Everyone's talking about [X]. Here's the bit they're missing."
- **The quiet observation.** "Something I noticed this week —"

Never open with a rhetorical question, a stat alone, or a one-word hook.

These patterns are **menus, never templates** (v1.1) — reusing an example's wording, or the same pattern across consecutive posts, is the Template Echo defect (`antipatterns.md` § The Template Echo). The red-line tell list there binds posts too.

## Credential rotation (v1.1 — Sead's 2026-06-10 review)

Sead: posts "use this line all the time: *In 25 years building enterprise systems*." That phrasing is **banned verbatim** — Markos said it once, speaking; he never writes it. The credential stays, the fossil goes. Rotate his real written phrasings (bank in `comment-craft.md` § Credential phrasing rotation: "in my last business", "sold a software company we owned outright", "Spent years watching…") — or carry the authority in named specifics (Bedrock, Qwen, 15:1, $100k GCP bill) with no credential line at all. Same credential phrasing never appears in consecutive posts.

## Body patterns

- **Peel-the-onion.** Start broad, narrow to specific, surface the insight.
- **Step-through.** "What are the most routine, monotonous tasks? That's your low-hanging fruit. Then you ask —"
- **Story → principle.** Scene from his life → generalisable lesson.
- **Named-specificity proof.** Bedrock, Claude, Qwen — specific tools carry more weight than "an AI model".
- **Pragmatic range.** Connect the point to 2-3 different industries or use cases. He has cross-industry breadth — use it.

## Closing patterns

- **The implication close.** "If you're building with AI in 2026, this is the conversation to be having."
- **The substantive question.** "Where have you seen this work — or not work?"
- **The reframe close.** "AI isn't the whole thing. It's one part of a bigger system."
- **Never:** tagline close, emoji string, hashtag wall, CTA ("follow me for more"), hashtag over-use. Two to three relevant hashtags max.

## Paragraph rhythm

Short paragraphs (1–3 sentences). White space matters on LinkedIn. One idea per paragraph. Vary sentence length — mix 4-word punches with 20-word windings. The cadence mirrors how Markos actually talks: a quick diagnosis, a pause, then the range.

Do not stack three short sentences in a row as a "punchy" close. That's an AI tell.

## The draft → publish sequence

1. Draft against relevant pillar in `opinions/opinions.md`.
2. Pair with a story from `stories/stories.md` where possible (anchor and build-note only).
3. Check against `guardrails/guardrails.md` for Red/Yellow flags. If Yellow, flag before drafting further.
4. Run the Two-Pass Self-Audit ("What makes this obviously AI?" — fix the tells), including the red-line tell scan (`antipatterns.md` § The Template Echo) and the batch-repetition check against recent posts in the log.
5. Read aloud test. If a sentence doesn't sound like something Markos would say out loud, rewrite it.
6. Queue for Monday approval per `playbooks/approval-workflow.md`.

## Product mentions

Markos posts about MyVault roughly 1 in 4 posts. Never more. When MyVault comes up, it comes up as context ("we're building X, here's what we learned") not as pitch. Zero Trust encryption, never "zero-knowledge."
