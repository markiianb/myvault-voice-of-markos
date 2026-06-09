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
token_count: ~820
version: "1.2"
last_updated: "2026-06-09"
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
5. **Capture his edits (Loop 1 — ground truth).** When Markos changes a draft before it ships, log the `(system-draft → Markos-final)` pair in [[markos-edits-log]] and tag the post `provenance: markos-edited`. If he accepts it verbatim, tag `provenance: markos-verbatim` (nothing to capture). His edits are the highest-signal voice data the program produces — this is the 30 seconds that re-grounds the whole system over time.

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

## Voice-eval gate (Stage 2 — pre-launch) — REQUIRED to run

Markos's open ask before live commenting launches is *another feedback round on the updated voice*. The measurement spine makes that round higher-signal instead of cold — but only if it actually runs. The 2026-06-08 audit's #1 fix: an opt-in eval is decorative. So running it is now a **required, ticked precondition** of requesting his round (the *result* stays advisory — see below).

**Required before you request Markos's pre-launch round** (don't open the round until all are ticked):

- [ ] Ran `/myvault:voice-eval --brand voice-of-markos` over the candidate batch (the v3.0 comment drafts + a few posts).
- [ ] **Attached the flagged-drafts list** — the drafts that failed the PRIMARY originality check (substitution / contrarian-opener / on-point) or that the secondary blend-in doubted. Markos reviews these first, not all of them cold.
- [ ] Logged the batch line in the trend block below.

**Advisory in verdict, never auto-kill.** A failed substitution or a flagged opener routes a draft to a cadence edit or to Markos himself; the eval never auto-approves or auto-kills, and the Tier system still governs what publishes. Required to *run*; advisory in *outcome*.

**Launch stays gated** regardless of scores — the eval informs the round, it does not end it. (See `_analysis/voice-corrections-log.md` for gated-launch status and the four provisional MVM-153 points.)

### Eval trend (the KPI is the trend, not any single score)

Append one line per batch. The headline metric is **substitution-pass %** (the primary gate — originality, the moat); blend-in is secondary and noisy. Watch the direction over batches: drifting toward or away from his voice.

```
| date | n drafts | substitution-pass % | median blend-in % | top recurring tell |
|------|----------|---------------------|-------------------|--------------------|
|      |          |                     |                   |                    |
```

The judge→log→ratify flow (auto-surface, human-ratify, never auto-mutate) is documented in `guide.md` § How the eval feeds corrections and `craft/edit-craft.md` § Voice-eval gate. Markos's own edits from the round feed [[markos-edits-log]] (Loop 1).

## Open items (awaiting confirmation)

- [ ] Password manager — 1Password? Bitwarden? Google Workspace built-in? Pending.
- [ ] Switching LinkedIn from Google Auth to username+password — Markos to action this week.
- [ ] Dedicated mobile device for Sead — agreed in principle, logistics pending (Cyprus shipping).
- [ ] Explicit recording consent at next voice session — process gap to close.
