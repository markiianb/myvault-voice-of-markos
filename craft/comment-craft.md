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
depends_on:
  - "voice"
  - "guardrails"
  - "stories"
token_count: ~950
version: "3.0"
last_updated: "2026-06-08"
status: "active"
summary: >-
  The four kudos-first comment frameworks — Agree-and-Add, Share-Experience,
  Question-and-Extend, Another-Angle. v3.0 (MVM-153) supersedes v2.1: it
  RESTORES the four frameworks and gated credential stories that v2.1 removed,
  and adds Markos's own corrections from the 20-post review — engage the actual
  + linked content and lead with the good (never open contrarian); longer
  technical comments allowed; story-gating ("at least part of the topic" +
  no-reuse); an on-point pre-check; a value/ROI-over-privacy topic lens; and a
  marketing-tech-AI no-go. The real defect was the contrarian opener, not the
  credential — so the pathway returns with a gate rather than staying removed.
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
  - Kudos on a specific line ("You nailed it on [X].")
  - What Markos would add, from his experience ("In my experience rolling out AI across [industry], I've seen [specific insight].")
  - Optional: pragmatic caveat or nuance ("One thing worth watching — [edge case].")
- **Length:** 2–4 sentences.
- **Example shape:** "You nailed it on AI-as-component-not-whole-system. In my experience shipping enterprise systems for 25 years, the model is doing maybe 10% of the work — the other 90% is architecture, data plumbing, governance. That's where most orgs underinvest."

### 2. Share-Experience

- **Use when:** Markos has direct firsthand experience on the topic.
- **Structure:**
  - Kudos on the topic ("This is the right conversation to have.")
  - Pivot to specific experience ("When we sold the family software company back in [timeframe], we saw this exact pattern — [specific observation].")
  - Extract the generalisable lesson ("The thing we learned was [insight].")
- **Length:** 3–5 sentences.
- Cross-ref stories in `stories/stories.md`. Story-gating applies — see the 2026-06-04 refinements below.

### 3. Question-and-Extend

- **Use when:** The topic deserves deeper exploration and Markos genuinely wants the poster's take.
- **Structure:**
  - Kudos on the framing ("Interesting way to frame this.")
  - His read ("My read is [Markos's position, one sentence].")
  - Genuine question ("How does this land if we're thinking about [adjacent scenario / specific industry]?")
- **Length:** 2–3 sentences.

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
| 3.0 | 2026-06-08 | **Supersedes v2.1.** Integrated Markos's MVM-153 review (2026-06-04). Restored the four kudos-first frameworks and gated credential stories that v2.1 had removed. Added: engage-the-actual-and-linked-content + lead-with-the-good opening (contrarian opener banned — the real defect); length up to ~8 sentences on technical posts; story-gating ("at least part of the topic" + no-reuse window); on-point pre-check; value/ROI-over-privacy topic lens; marketing-tech-AI no-go. Four provisional decisions held pending Markos's next round (see inline `confirm next round` markers + `_analysis/voice-corrections-log.md`): version 3.0 not "1.1"; daily cap 7–8 not 15; hashtags allowed in Markos's own hand only; launch still gated. | Mark |
| 2.1 | 2026-05-13 | Removed Share-Experience and all credential pathways; stories not loaded; three frameworks (React/Ask/Another angle); cap 15→7–8. *Superseded by 3.0 — the audit mis-diagnosed the defect as credentials; Markos's own review found it was the contrarian opener.* | Mark |
| 2.0 | 2026-05-13 | Inverted v1 default; engage-with-substance principle; demoted Share-Experience. *Superseded.* | Mark |
| 1.0 | 2026-04-14 | Initial chunk replacing v0's "Challenge Respectfully" framework. Kudos-first principle from voice session. | Mark |
