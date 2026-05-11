---
chunk_id: "daily-routine"
domain: "playbooks"
category: "playbooks"
subcategory: "cadence"
context_tags:
  - "daily"
  - "cadence"
  - "volume"
  - "time-of-day"
depends_on:
  - "comment-craft"
  - "target-accounts"
  - "guardrails"
token_count: ~450
version: "1.0"
last_updated: "2026-04-14"
status: "active"
summary: >-
  What good engagement looks like on a typical day from Markos's account. Volume caps, time-of-day rules, posting schedule, end-of-day voice consistency check.
---

# Daily Routine

The goal is engagement that looks human, not industrial. Volume caps exist because over-posting trips LinkedIn's automation filters and — more importantly — trips Markos's readers' "this isn't really him" detector.

## Daily volume caps

- **Comments on target accounts' posts:** 5–10/day max.
- **Reactions (likes, celebrates):** 10–15/day.
- **Replies to comments on Markos's own posts:** all comments within 24 hours; within 30 minutes when feasible (first-hour replies boost algorithmic reach ~64%).
- **Hard cap:** 15 comments total/day. Over 15 signals automation.
- **Hashtags in comments:** never.
- **Tagging people:** only with genuine reason (they're the person being quoted, e.g.).

## Time-of-day rules

- **Morning (08:00–10:00 Markos's audience TZ):** primary commenting window. Most CIOs/execs check LinkedIn first thing.
- **Mid-day (12:00–14:00):** reactions and light comments.
- **Evening (17:00–19:00):** replies to comments on his posts; minor new engagement.
- **Never:** overnight engagement from his account (looks bot-like).

## Posting schedule

Three posts per week (per Q2 plan):

- **Anchor post:** Tuesday or Wednesday
- **Newsjack:** day of the news item, ideally morning of his audience
- **Build-note:** Thursday
- **Never:** weekends (his audience doesn't engage; posting then risks looking automated)

## Voice consistency checks (end of day)

Every day, one last-10-comments review:

- Do all 5–10 read like Markos?
- Would he wince at any?
- Any that drift toward preach / binary / generic?
- If any drift → pull the comment, log the learning in `_analysis/voice-corrections-log.md`, update `voice/voice.md` if it's a pattern.

## Engagement loop

The point of the routine is mutual engagement, not one-sided broadcast:

1. Comment on target account's post →
2. They engage back on Markos's post (or DM) →
3. Markos replies personally (Tier 3) →
4. Pattern established: reciprocal conversation.

If a target account never reciprocates after three substantive comments, drop them from the monthly list.

## Analytics to track daily

- Comments made (count, by framework used)
- Reactions given
- Replies received on Markos's posts (response time)
- Any escalations (journalists, Yellow Zone, flagged exclusions)

## End-of-week review

Every Friday:

- Which 3 comments drove the most substantive conversation?
- Which target accounts reciprocated?
- Which accounts went silent? (Review for monthly pruning.)
- Any voice corrections to push upstream into `voice/voice.md`?
