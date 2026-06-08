---
chunk_id: "approval-workflow"
domain: "playbooks"
category: "playbooks"
subcategory: "approvals"
context_tags:
  - "approval"
  - "workflow"
  - "tiers"
  - "monday-rhythm"
  - "slack"
depends_on:
  - "guardrails"
  - "comment-craft"
  - "target-accounts"
token_count: ~720
version: "1.1"
last_updated: "2026-06-08"
status: "active"
summary: >-
  How approvals actually run. Monday rhythm for posts, tiered comment approval, Slack flag comms, one-Linear-task-per-week cap, four-month trust progression.
---

# Approval Workflow

This chunk is the operational contract between Markos, Mark, and Sead. It's the "how" behind the program-level framework.

## Trust progression

The oversight model tightens and relaxes by month. Markos can pull oversight back to a tighter level at any time.

### Month 1 (April–May) — Full oversight

- Every post reviewed and approved before publishing.
- Daily summary of all comments made from Markos's account.
- "Voice check" after the first 10 comments — he flags anything off-voice.
- Update `voice/voice.md` based on feedback.
- **Goal:** establish voice baseline, build Markos's comfort.

### Month 2 (May–June) — Guided engagement

- Posts still require Monday approval.
- Green Zone comments: no individual review, weekly summary instead.
- Yellow Zone comments: pre-approval before posting.
- First monthly analytics report.
- **Goal:** reduce daily review burden, maintain quality.

### Month 3 (June–July) — Conditional autonomy

- Posts approved in weekly batches (3 at once, not 1 at a time).
- Green Zone comments run independently.
- Yellow Zone: "draft and flag" workflow.
- Monthly 15-min voice check call replaces daily summaries.

### Month 4+ (July onward) — Operational trust

- Green Zone posts within established pillars: drafted and published with notification (not pre-approval).
- Yellow Zone + signature content (Privacy Teardowns, stories): still require review.
- Monthly 30-min extraction call to capture new stories, opinions, reactions.
- Quarterly strategy review.
- **Goal:** 1–2 hours/month of Markos's time.

## Override rule

At any point, Markos can pull oversight back to a higher level. If something doesn't feel right, we return to full review. His account, his name, his rules.

## Post approval — the Monday rhythm

1. Sead queues 3 posts by Friday EOD.
2. Markos reviews by Monday EOD.
3. Posts publish Tuesday–Thursday.
4. For time-sensitive newsjacks: draft → schedule → Slack Markos → publish on approval. If no response in 4 hours, hold.

## Comment approval — the tier system

**Tier 1 — Pre-approved (run independently):**

- Replies to comments on Markos's posts (using established voice)
- Green Zone topic engagement on target accounts' posts
- Reactions (likes, celebrates)

**Tier 2 — Draft-and-flag (we draft, Markos approves):**

- Comments on Yellow Zone topics
- First-time engagement with a new high-profile account
- Replies to substantive disagreements on his posts

**Tier 3 — Markos only (we flag, he handles personally):**

- DMs
- Comments from journalists, investors, key partners
- Anything touching Red Zone topics
- Connection request decisions
- Hostile or Yellow-Zone-escalating threads
- Any reply to an exclusion-list account (if one somehow lands — usually just skip)

## Flag comms channel

- **Default: Slack** (confirmed use on the call).
- **Urgent takedowns:** Slack + WhatsApp if no Slack response in 30 min.
- **Format for flags:** "Flag: [Tier 2/3] — [account] on [topic] — [recommended action] — here's the draft."
- **SLA:** Markos responds to flags within 24 hours (Tier 2); urgent takedowns acted on immediately.

## Topic requests — Linear

- **Cap: one Linear task per week.** Markos's explicit ask.
- Task format: short-form topic question, not a long brief. "What's your take on [X] for Thursday's anchor post?"
- Label: `voice-of-markos` or similar.

## When things go wrong

- If a comment or post gets a negative reaction from Markos → delete/edit immediately, no defensiveness.
- Log the learning in `_analysis/voice-corrections-log.md` (create if it doesn't exist).
- Update `voice/voice.md` if it's a voice issue, `guardrails/guardrails.md` if a zone issue.

## Voice-eval gate (Stage 2 — pre-launch)

Markos's open ask before live commenting launches is *another feedback round on the updated voice*. The measurement spine makes that round higher-signal instead of cold.

- **Before his pre-launch round:** run `/myvault:voice-eval --brand voice-of-markos` over the candidate batch (the v3.0 comment drafts + a few posts). It returns, per draft: a blind-lineup blend-in %, the non-blind VoM check (contrarian-opener / on-point / substitution), and voice-stats deltas. Surface the **flagged** drafts to Markos first — he reviews what the instrument doubts, not all of them from scratch.
- **It is a screen, not a gate-keeper.** A low blend-in or a flagged opener routes a draft to a Markos-cadence edit or to Markos himself; it never auto-approves or auto-kills. The Tier system above still governs what publishes.
- **Launch stays gated** regardless of scores — the eval informs the round; it does not end it. (See `_analysis/voice-corrections-log.md` for the gated-launch status and the four provisional MVM-153 points.)

The judge→log→ratify flow (auto-surface, human-ratify, never auto-mutate) is documented in `guide.md` § How the eval feeds corrections and `craft/edit-craft.md` § Voice-eval gate.

## Open items (awaiting confirmation)

- [ ] Password manager — 1Password? Bitwarden? Google Workspace built-in? Pending.
- [ ] Switching LinkedIn from Google Auth to username+password — Markos to action this week.
- [ ] Dedicated mobile device for Sead — agreed in principle, logistics pending (Cyprus shipping).
- [ ] Explicit recording consent at next voice session — process gap to close.
