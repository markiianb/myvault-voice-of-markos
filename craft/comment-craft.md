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
depends_on:
  - "voice"
  - "guardrails"
  - "stories"
token_count: ~650
version: "1.0"
last_updated: "2026-04-14"
status: "active"
summary: >-
  The four comment frameworks — Agree-and-Add, Share-Experience, Question-and-Extend, Another-Angle — all opened kudos-first. Replaces v1's "Challenge Respectfully" framework, which Markos vetoed.
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
- Cross-ref stories in `stories/stories.md`.

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

## Universal rules

- Never more than 15 comments in a day (over-commenting signals automation).
- No hashtags in comments.
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
