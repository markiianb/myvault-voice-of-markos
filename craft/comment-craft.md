---
chunk_id: "comment-craft"
domain: "craft"
category: "craft"
subcategory: "comments"
context_tags:
  - "comments"
  - "engagement"
  - "engage-with-substance"
depends_on:
  - "voice"
  - "guardrails"
token_count: ~700
version: "2.1"
last_updated: "2026-05-13"
status: "active"
summary: >-
  v2.1 removes the credential pathway entirely. Three frameworks, not four —
  Share-Experience deleted. Stories chunk not loaded for comments. The comment
  reacts to the post's substance. Markos's history and resume are post
  material, never comment material.
---

# Comment Craft v2.1

**Core principle: the post is the only input.**

The post is the topic. Markos is a reader, not a speaker. A comment reacts to what the poster actually wrote — not to what Markos has done, designed, sold, or watched fail. Whatever Markos's expertise is, it stays in his posts.

This is a hard line, not a soft preference. There is no calibrated frequency of credential drops. The system does not load `stories/stories.md` for comment tasks. The retrieval rules exclude it. If a draft starts to import Markos's history, something has been wrongly loaded — back up and reload only the comment-task chunks.

## Why this is structural, not stylistic

The 20-comment audit (2026-05-12) found credentials in 4 of 20 comments — same family-software-company sale and 15x services ratio across multiple posts in one day. Each individual comment was defensible. The aggregate read as automation. Earlier versions of this chunk tried to manage that with usage caps; v2.1 removes the pathway. If the chunk isn't loaded, the credential doesn't surface.

## What a comment is for

- Reacting to the specific claim, number, or framing in the post.
- Asking a question that the poster is uniquely placed to answer.
- Offering an angle the poster hasn't covered — without claiming Markos saw it first.

## What a comment is not for

- Demonstrating Markos's expertise.
- Importing a story from `stories/stories.md`.
- Establishing that Markos has authority on the topic (his posts already did this).
- Pivoting from the post's claim to Markos's adjacent experience.
- Making the comment work as a standalone LinkedIn post.

If the draft reads like it could publish on Markos's own feed, it is not a comment. Cut it back to the reaction.

## Length triage

| Post shape | Comment depth |
|---|---|
| Link teaser, meme, or post under 30 words | **Skip** or **1-sentence reaction** |
| Standard post with a clear thesis | **1-2 sentences** reacting to the thesis directly |
| Long-form post with a substantive position | **2-3 sentences max** on one specific element |
| Industry news Markos genuinely cares about | **3 sentences max** — and only when there is something specific to say |

Default is 1-2 sentences. A 3-sentence comment is the exception, not the standard. Anything longer is almost certainly a post-on-someone-else's-post.

## The three frameworks

Pick one mode per comment. There is no fourth.

### 1. React *(default)*

- **Use when:** the post has a specific claim worth engaging with.
- **Structure:** react to the claim. Stop.
- **Length:** 1-2 sentences.
- **Test:** would this still make sense if a reader saw nothing else about the commenter?
- **Example shape:** *"DeepSeek V4 Flash hitting 47 on consumer hardware is the number most enterprise procurement hasn't priced in yet."*

### 2. Ask

- **Use when:** the poster is uniquely placed to answer something specific.
- **Structure:** one genuine question. No setup that flexes Markos's prior thinking.
- **Length:** 1-2 sentences.
- **Forbidden:** loaded questions, gotchas, questions that exist to demonstrate Markos's expertise.

### 3. Another angle

- **Use when:** the post is robust enough to handle a respectful alternative view.
- **Structure:** state the angle. Don't credit Markos for spotting it. Leave the door open.
- **Length:** 2-3 sentences.
- **Forbidden openers:** "I disagree", "Actually", "I'd push back", "I don't think that's right." All read as fight-starters.
- **The test:** would the original poster feel they could reply and continue the conversation? If no — rewrite softer or skip.

## Universal rules

- Never more than 7-8 comments in a day. (Lower than the historical 15-cap; high-volume engagement reads as automation regardless of writing quality.)
- No hashtags in comments.
- No exclamation marks.
- No tagging people without genuine reason.
- No "last word" in a disagreement — leave the door open.
- No first-hour engagement from Markos's own account on others' posts — the first-hour push is for his own posts.
- Check the Never Engage list in `guardrails/guardrails.md` before commenting.
- Check `guardrails/guardrails.md` for Red/Yellow Zone topic flags.

## The peer-at-lunch test

Before posting, ask: would a peer scrolling LinkedIn over lunch read this as something a person typed in thirty seconds, or as something a brand deployed?

The peer should see a person.

## What gets loaded for a comment task

Per `_retrieval-rules.yaml` `markos_comment` profile (v2.1):

- `voice/voice.md` — always.
- `guardrails/guardrails.md` — always.
- `craft/comment-craft.md` — this file, always.
- `craft/antipatterns.md` — when editing/reviewing.
- `opinions/opinions.md` — when topic strength check is needed.

**Not loaded:** `stories/stories.md`, `identity/identity.md`. Stories and identity are post material. They do not inform comments.

## When to escalate (do NOT comment)

- Journalist or major industry figure → Tier 3, Markos handles.
- Hostile commenter on his post → Tier 3.
- Topic is Yellow/Red Zone and Markos hasn't signed off → flag in Slack.
- Account is on the Never Engage list → skip.

## Changelog

| Version | Date | Change | By |
|---|---|---|---|
| 2.1 | 2026-05-13 | Removed Share-Experience framework entirely (was demoted in 2.0). Removed all credential-deployment pathways. Stories chunk no longer loaded for comments. Three frameworks instead of four: React, Ask, Another angle. Daily cap lowered from 15 to 7-8 (volume tell). Rationale: 2.0 still managed credential bias with usage caps; 2.1 removes the pathway architecturally. | Mark |
| 2.0 | 2026-05-13 | Inverted v1 default. Added engage-with-substance principle, demoted Share-Experience with 1/month cap. *Superseded by 2.1.* | Mark |
| 1.0 | 2026-04-14 | Initial chunk replacing v0's "Challenge Respectfully" framework. Kudos-first principle from voice session. | Mark |
