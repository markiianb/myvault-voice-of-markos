---
chunk_id: "comment-craft"
domain: "craft"
category: "craft"
subcategory: "comments"
context_tags:
  - "comments"
  - "engagement"
  - "kudos-first"
  - "frameworks"
  - "engage-the-content"
  - "story-gating"
  - "length"
  - "texture"
  - "banned-tells"
  - "batch-diversity"
depends_on:
  - "voice"
  - "guardrails"
  - "stories"
  - "antipatterns"
token_count: ~1900
version: "3.1"
last_updated: "2026-06-10"
status: "active"
summary: >-
  The four kudos-first comment frameworks — Agree-and-Add, Share-Experience,
  Question-and-Extend, Another-Angle — plus, since v3.1, the TEXTURE PACK:
  Markos's real opener bank, credential-phrasing rotation, syntactic
  fingerprint, and batch-level diversity rules, mined verbatim from his 13 own
  comments (2026-06-04). v3.1 fixes the template-echo defect Sead flagged in
  the 2026-06-08 batch (35 drafts, rule-compliant but voice-false: "You
  nailed…", "the line that lands…", "In 25 years building enterprise systems"
  9×). Examples are menus, never templates. v3.0's rules are unchanged: engage
  the actual + linked content, lead with the good (contrarian opener banned),
  longer technical comments allowed, story-gating + no-reuse, on-point
  pre-check, value/ROI-over-privacy topic lens, marketing-tech-AI no-go.
---

# Comment Craft

This chunk replaces v1's "Challenge Respectfully" framework. Markos was explicit on the call: we do not open with disagreement.

## The kudos-first principle

Markos's exact words: *"there's no point pissing off the person that wrote the post, so actually what's better is to find something good in what they wrote… kudos to this post and the topic. Thank you. I just wanted to also, you know, to highlight, from my experience, blah, blah."* And: *"What we don't want to do is disagree with somebody and be in some fight. We'd actually would rather that they then did the same with us on our content."*

Every comment from Markos's account opens with something substantive the poster said. Never "Great post!" or a generic nod. Pick a specific line, observation, or claim — quote or summarise it in 5–10 words. Then add value.

## The four frameworks

### 1. Agree-and-Add *(most common — default mode)*

- **Use when:** The post aligns with Markos's position.
- **Structure:**
  - Kudos on a specific line — name the actual thing he liked, in fresh words. (The *move* is specific praise. "You nailed it on [X]" was one phrasing of it and is now a banned tell — see § The texture pack.)
  - What Markos would add, from his experience — credential phrasing from the rotation bank, or none.
  - Optional: pragmatic caveat or nuance.
- **Length:** 2–4 sentences.
- **Real example (Markos, on Aaron Levie / services & agents):** *"@Aaron, agree on the services scale point. Ratio in enterprise software ran around 10-15x in my last business, and frankly agents-rewiring-process likely makes the tail larger this time given huge certified data needs for agents…"*
- **Real example (Markos, on Helen Toner / Beyond P(doom)):** *"Spent years watching teams argue about a single risk number when the real gap was that nobody agreed on what they were uncertain about. Lohn's split — randomness vs. ignorance, Belief vs. Plausibility — frames that gap precisely."*

### 2. Share-Experience

- **Use when:** Markos has direct firsthand experience on the topic.
- **Structure:**
  - Kudos on the topic ("This is the right conversation to have.")
  - Pivot to specific experience ("When we sold the family software company back in [timeframe], we saw this exact pattern — [specific observation].")
  - Extract the generalisable lesson ("The thing we learned was [insight].")
- **Length:** 3–5 sentences.
- Cross-ref stories in `stories/stories.md`. Story-gating applies — see the 2026-06-04 refinements below.
- **Real example (Markos, on Andy Yen / Proton direct-pay):** *"Twelve years without VC is the proof, not the press cycle. … Can relate - sold a software company we owned outright with zero leverage — Similar value proposition, laser focus on slower yet considered growth focussed around the customer…"*

### 3. Question-and-Extend

- **Use when:** The topic deserves deeper exploration and Markos genuinely wants the poster's take.
- **Structure:**
  - Kudos on the framing ("Interesting way to frame this.")
  - His read ("My read is [Markos's position, one sentence].")
  - Genuine question ("How does this land if we're thinking about [adjacent scenario / specific industry]?")
- **Length:** 2–3 sentences.
- **Real example (Markos, on Konrad Hippius / knowledge graph):** *"…Although I am curious about whether they use Graph search exclusively or Hybrid Search techniques leveraging advanced semantic search (VectorDB)… It would be interesting to know how the testing and evals are setup as well."* — his questions are build-level and specific, never "curious to hear your thoughts."

### 4. Another-Angle *(replaces v1's Challenge-Respectfully)*

- **Use when:** Markos disagrees or sees it differently. This is the only safe way to surface that on LinkedIn.
- **Structure:**
  - Kudos on the topic or a specific line ("Great topic to raise. [Line you liked].")
  - Thank-you or acknowledgement ("Thank you for putting this out there — we need more of this conversation.")
  - Another angle, framed as experience-led ("One angle I'd add, from my own time in [context] — [alternative view, framed as observation not correction].")
- **Length:** 3–4 sentences.
- **Forbidden openings:** "I disagree", "Actually", "I'd push back", "I don't think that's right." All read as fight-starters.
- **The test:** after writing, would the original poster feel they could reply and continue the conversation? If no — rewrite softer.

## 2026-06-04 refinements (MVM-153)

From the 20-post comment-feedback review (full analysis: `_analysis/2026-06-04_Comment-Feedback_Markos-Responses_and_Voice-Synthesis.md`). Markos ran the 20 posts himself. Only 4 of 20 system drafts were accepted as-is; on 13 of 20 he wrote his own. The four frameworks above were already right — the generators drifted from them. These refinements make the drift explicit.

> **Why v3.0 reverses v2.1.** The 2026-05-13 audit concluded the defect was credential-dropping and removed the pathway: it deleted Share-Experience, stopped loading `stories`/`identity` for comments, and cut to three frameworks. Markos's own review found the real defect was the **contrarian opener** — every system, including v2.1, argued *against* the post instead of engaging it. Credentials were a smaller, *gateable* problem. So v3.0 restores the four frameworks and gated stories, and bans the contrarian opener.

**Engage the actual content — and lead with the good.** The single biggest correction. The generated comments opened contrarian ("the harder question is…", "but", a reframe) and reacted to the post's headline. Markos: *"they were contrarian and steered to an argument against. Vs calling out something good then giving my own take or lasering in on a specific point to expand on."* So: read the post **and whatever sits behind its link**, name something specific that's genuinely good, then add the take or laser on one point. A harder question is fine *after* genuine engagement — never as the opener.

**Length — let technical comments run.** The 2–4 / 3–5 sentence guides above hold for quick reactions and humour. On in-wheelhouse technical posts where Markos has a real build-level take, allow up to ~8 sentences. His actual comments reach for concrete hooks (hybrid vector+graph search and caching, evals, LLM councils and model-mixing, scoped/auditable agent primitives, shared-memory edge hardware). Do not truncate them to hit a short-length rule.

**Story-gating.** Deploy a credential story (the family software company, father on the Visa system, 100%-family-held, services 10–15×) only when the post topic is *at least part* of what the story answers — Markos's exact rule. And never reuse the same credential within a short window. Evidence: he kept the story where the topic fit (direct-pay, services scale) and declined it where it only loosely fit (cadence) or where he'd already used it (the 15× twice). The `stories` and `identity` chunks are loaded *conditionally* for comments under this gate (`_retrieval-rules.yaml` v2.3) — not removed (v2.1), not always-on (v1).

**On-point pre-check.** Before drafting, ask: is our angle about *this* post's actual substance? On a post about organizational change he flagged our tool-focused comment as "off point." If the angle doesn't fit the post's real subject, skip.

**Topic lens.** Lead with utility, value, ROI and AI-readiness ahead of privacy/security. Markos: *"a bit too much on privacy and security vs utility, value, ROI and readiness for AI."* Privacy is still true — he's over-indexed on it.

**Skipping is a valid outcome.** Thin teasers and off-point posts are legitimate non-comments. Don't force a comment to hit volume.

## The texture pack (v3.1) — how Markos actually writes

> **Why this exists.** The 2026-06-08 batch (35 drafts) followed every v3.0 rule and still read as "standard AI speech" (Sead's review, 2026-06-10). Cause: this chunk carried ONE example sentence, and parallel drafting agents stamped it across the batch — "You nailed" 5×, "the line that lands" ~10×, "In 25 years building enterprise systems" 9×. The example became the voice. Source for everything below: Markos's 13 real comments, `_analysis/2026-06-04-comment-feedback-markos-responses-and-voice-synthesis.md` Appendix A. Read them before drafting a batch.

**Examples are menus, never templates.** Every example in this chunk illustrates a *move*, not wording. Reusing an example's phrasing in a draft is a defect (the Template Echo, `antipatterns.md`). If a phrase from this chunk — or from another draft in the same batch — appears in your draft, rewrite it.

### Real opener bank (verbatim Markos — one per move, vary across a batch)

| Move | His actual opener |
|---|---|
| Assertion-first | "Twelve years without VC is the proof, not the press cycle." |
| Take-first | "My take is that Knowledge Graph traversal is certainly part of it - design of the ontology, hierarchy, schema… is absolutely critical.." |
| @-mention + agree | "@Aaron, agree on the services scale point." |
| Direct action | "Adding this to my list, @Andrew." |
| Experience-implicit | "Spent years watching teams argue about a single risk number when the real gap was that nobody agreed on what they were uncertain about." |
| Pattern-naming | "The pattern across all three is the same gap solved at a different point in the stack…" |
| Concession-then-catch | "The Asimov example is the right one, and it is also the catch…" |
| Easy-half pivot | "Exposing the data layer is the easy half. The harder question is what customer outcomes… are firms trying to achieve" *(his line — the pivot comes after engagement, never as a contrarian opener)* |
| Prediction | "By the Autumn there will be desktops with 128Gb shared memory for GPU/CPU…" |
| Observation-from-the-material | "What jumps out from the map is that nearly every 'Not built / Manual' row is blocked on the same thing…" |

"What lands for me is…" appears ONCE in his corpus. Single occurrences are seasoning, not signatures — nothing from this bank repeats within a batch.

### Credential phrasing rotation

The credential is real; the fossilized phrasing is not. **Banned verbatim: "In 25 years building enterprise systems" and close variants** ("In 25 years of shipping/building…", "25 years of enterprise delivery"). He said it once, speaking, in an interview — he never writes it. His real written credential lines:

- "in my last business" / "Ratio in enterprise software ran around 10-15x in my last business"
- "sold a software company we owned outright with zero leverage"
- "Speaking as someone who already runs most of my stack through agents"
- "Spent years watching…"
- "It is the dirty little secret of Enterprise Software…"

Rotate; or use none — most of his 13 comments carry no credential at all, the authority is in the technical specifics.

### Syntactic fingerprint (descriptive guidance, not targets)

His comments read typed-in-the-moment, not edited: spaced " - " dashes alongside em-dashes; parentheticals with inner spaces "( like AI context for my data beyond RAG )"; doubled-dot ellipses "criticial.."; mid-comment rhetorical questions ("I wonder if it will be the same way with tokens ?"); trailing forward energy ("lets see how we get there!", "Its coming quicker than we think."); UK spellings. **Do not sand this texture off into clean parallel prose — and do not fake it either** (no injected typos, no performed quirks). The instruction is negative: stop polishing, stop balancing every sentence, let a thought trail.

### Density norm

His comments carry 2–4 concrete technical specifics each (named tech: Neo4j Aura, GRPO, LangSmith-class specifics; numbers: 10-15x, 128Gb; mechanisms: caching happy-path traversals, evals setup) — not one abstract thesis elegantly restated. If a draft has zero named mechanisms, it isn't his.

### Batch-level diversity rules (hard)

The no-reuse rule was per-account; these are per-batch:

- No opener pattern recurs within a batch — at paraphrase level, not just verbatim ("The line that lands for me" = "The line that jumps out" = same pattern).
- No credential phrasing appears more than twice per batch.
- No banned tell appears at all (`antipatterns.md` § The Template Echo).
- Before a batch ships to review, run the batch QA step (`CLAUDE.md` § Batch QA for comment drafts).

## Universal rules

- Never more than 7–8 comments in a day (over-commenting signals automation regardless of writing quality). <!-- confirm next round: Markos's MVM-153 chunk reverted to 15; the 2026-05-12 volume-tell finding kept 7–8. Holding 7–8 pending Markos's confirmation. -->
- No hashtags added by the generator. An occasional topical hashtag in Markos's *own hand* is acceptable (he used `#Humanintheloop` in his own post-9 draft); the system never adds one. <!-- confirm next round: the flat "no hashtags in comments" rule vs Markos's own usage — confirm the his-hand-only carve-out. -->
- No tagging people without genuine reason.
- No "last word" in a disagreement — we leave the door open.
- First-hour engagement on Markos's own posts matters (team comments on his post in the first hour to boost algorithmic reach).
- Check the Never Engage list in `guardrails/guardrails.md` before commenting on any account.
- Check `guardrails/guardrails.md` for Red/Yellow Zone topic flags.

## When to escalate (do NOT comment)

- Journalist or major industry figure → Tier 3, Markos handles.
- Hostile commenter on his post → Tier 3.
- Topic is Yellow/Red Zone and Markos hasn't signed off → flag in Slack.
- Account is on the Never Engage list in `guardrails/guardrails.md` → skip.
- Marketing-tech AI posts (HubSpot and similar) → skip. What MyVault does there is a competitor moat — keep it to ourselves. (MVM-153)
- The post's real subject isn't our angle (e.g. it's about org change and we'd talk tools) → skip. (MVM-153)

## Changelog

| Version | Date | Change | By |
|---|---|---|---|
| 3.1 | 2026-06-10 | **Texture reconciliation (Sead's review of the 2026-06-08 batch: "standard AI speech").** Added the texture pack: real opener bank, credential-phrasing rotation (verbatim "25 years building enterprise systems" banned — he never writes it), syntactic fingerprint, density norm, batch-level diversity rules. Replaced the single Agree-and-Add example shape (the template-echo source: stamped across all 35 drafts) with verbatim real-Markos examples per framework + the menus-not-templates rule. Cross-refs `antipatterns.md` § The Template Echo and `CLAUDE.md` § Batch QA. Rules from v3.0 unchanged. Plan: `_analysis/2026-06-10-comment-system-v3.1-texture-plan.md`. | Mark |
| 3.0 | 2026-06-08 | **Supersedes v2.1.** Integrated Markos's MVM-153 review (2026-06-04). Restored the four kudos-first frameworks and gated credential stories that v2.1 had removed. Added: engage-the-actual-and-linked-content + lead-with-the-good opening (contrarian opener banned — the real defect); length up to ~8 sentences on technical posts; story-gating ("at least part of the topic" + no-reuse window); on-point pre-check; value/ROI-over-privacy topic lens; marketing-tech-AI no-go. Four provisional decisions held pending Markos's next round (see inline `confirm next round` markers + `_analysis/voice-corrections-log.md`): version 3.0 not "1.1"; daily cap 7–8 not 15; hashtags allowed in Markos's own hand only; launch still gated. | Mark |
| 2.1 | 2026-05-13 | Removed Share-Experience and all credential pathways; stories not loaded; three frameworks (React/Ask/Another angle); cap 15→7–8. *Superseded by 3.0 — the audit mis-diagnosed the defect as credentials; Markos's own review found it was the contrarian opener.* | Mark |
| 2.0 | 2026-05-13 | Inverted v1 default; engage-with-substance principle; demoted Share-Experience. *Superseded.* | Mark |
| 1.0 | 2026-04-14 | Initial chunk replacing v0's "Challenge Respectfully" framework. Kudos-first principle from voice session. | Mark |
