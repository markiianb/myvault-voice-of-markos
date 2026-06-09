---
type: guide
status: active
owner: Mark Bobyliak
created: 2026-04-16
updated: 2026-06-09
tags: [linkedin, voice-of-markos, guide, system]
summary: How to use the Voice of Markos system — architecture, workflows, file map, correction loop.
---

# Voice of Markos — System Guide

How the system works, how the pieces connect, and the step-by-step workflow for every task.

---

## How the system is organized

The system has **16 files** across **7 domain folders**, plus 4 orchestration files. Each file does one job.

```
voice-of-markos/
│
│  Orchestration (how to navigate)
├── CLAUDE.md                     ← what to load per task (for AI agents)
├── README.md                     ← architecture, inheritance, overrides
├── _manifest.yaml                ← chunk registry (13 entries)
├── _retrieval-rules.yaml         ← task profiles (7 profiles)
├── guide.md                      ← this file
│
│  The voice (how Markos sounds)
├── voice/voice.md                ← tone, 4 qualities, 3 modes, failure portraits, banned words, Final Test
├── voice/voice-stats.md          ← contrastive measured voice targets (QA instrument) + em-dash target
│
│  The person (who Markos is)
├── identity/identity.md          ← bio, positioning, authority, audience, disclosure rules
│
│  The positions (what he believes)
├── opinions/opinions.md          ← topic gate table + 8 pillars with theses and sound-bites
│
│  The material (what he draws from)
├── stories/stories.md            ← 12 personal stories with status flags and cautions
│
│  The boundaries (what he won't do)
├── guardrails/guardrails.md      ← zones, never-engage list, comfort matrix
│
│  The audience (who reads him)
├── audience/audience-linkedin.md ← 5 segments, content matching
│
│  The craft (how to build content)
├── craft/
│   ├── post-craft.md             ← 3 post formats: anchor, newsjack, build-note
│   ├── comment-craft.md          ← 4 comment frameworks, kudos-first
│   ├── newsjack-craft.md         ← reacting to news within 24h
│   ├── edit-craft.md             ← 6-pass editing workflow, checklists
│   └── antipatterns.md           ← before/after casebook for 5 failure portraits
│
│  The operations (when and how to publish)
└── playbooks/
    ├── approval-workflow.md      ← tiers, Monday rhythm, trust progression
    ├── daily-routine.md          ← volume caps, time-of-day, posting schedule
    └── target-accounts.md        ← engagement categories, quality markers
```

---

## The two layers

**The system files** (inside `voice-of-markos/`) are the source of truth. They hold the complete voice spec, all positions, all stories, all guardrails, all craft patterns. When Markos gives a correction, it gets written here.

**The playbook** (`CEO-LinkedIn-Playbook.md`, one level up) is the daily quick-reference. It has the zone tables, comment frameworks, volume caps, and approval routing — everything Sead needs open while working. It does not duplicate the full voice spec. When Sead needs depth on a topic, mode, or story, the playbook points to the right system file.

**Rule:** If the playbook and a system file disagree, the system file wins.

---

## Workflow: Writing a comment

This is 80% of the daily work. Typical time: 2-5 minutes per comment.

**Step 1 — Check the account.**
Open `guardrails/guardrails.md` § Never Engage. Is the account or anyone in the thread on the exclusion list? If yes, skip. If uncertain, flag in Slack.

**Step 2 — Check the topic.**
Scan the post. What's the topic? Check against the zone table in `guardrails/guardrails.md` or the quick-check in the playbook.
- **Green** → proceed.
- **Yellow** → draft the comment, but do not post. Flag to Markos for sign-off (Tier 2).
- **Red** → do not engage.

**Step 3 — Check topic strength.**
Open `opinions/opinions.md` § Quick Gate Table. Find the topic. Is Markos's position Strong or Mild?
- **Strong** → lead with his position.
- **Mild** → agree-and-add only. Don't overstate.
- **Not listed** → treat as Yellow. Draft and flag.

**Step 4 — Pick a framework.**
Open `craft/comment-craft.md`. Four options:
1. **Agree-and-Add** — default. Use when the post aligns with his position.
2. **Share-Experience** — use when he has a firsthand story. Cross-reference `stories/stories.md`.
3. **Question-and-Extend** — use when the topic deserves deeper exploration.
4. **Another-Angle** — use when he sees it differently. Kudos first, experience-led, never opens with disagreement.

**Step 5 — Write the comment.**
- Open with kudos on something specific the poster said (5-10 words).
- Add value in 2-4 sentences.
- No hashtags. No tagging without reason. No last word.

**Step 6 — Quick scan before posting.**
- Any banned phrases? (preach phrases, parent bans, cringe list — see `voice/voice.md` § Banned Words or the playbook § 9)
- Does it sound like Markos or like an agency?
- Would he wince?

Post if Green Zone + Tier 1. Flag if Yellow Zone or Tier 2/3.

---

## Workflow: Writing a post

Three posts per week. Drafted by Friday, reviewed by Monday, published Tuesday-Thursday.

**Step 1 — Pick the format.**
- **Anchor** (1/week, Tue or Wed): 250-600 words, opinion-led, pairs with a pillar and a story.
- **Newsjack** (1/week, day of news): 100-250 words, reacting to AI/privacy news.
- **Build-note** (1/week, Thu): 80-200 words, personal scene to generalisable lesson.

**Step 2 — Pick the mode.**
Open `voice/voice.md` § Three Modes.
- **Explain** — teaching how something works.
- **Challenge-from-evidence** — newsjacks and contrarian takes. Evidence before challenge.
- **Educate** — making capability accessible.
- **Never-preach** — spot and eliminate. If you find "everyone should," "you need to," or exclamation marks, you've drifted here.

**Step 3 — Load the content.**
- Open `opinions/opinions.md` — find the relevant pillar. Use the thesis and sound-bites as raw material, not as copy-paste.
- Open `stories/stories.md` — find a deployable story. Check status (Green = use, Yellow = sign-off needed, Red = abstract only).
- Check `guardrails/guardrails.md` — any Red or Yellow flags on the topic?

**Step 4 — Draft.**
Follow the structure in `craft/post-craft.md`:
- Open with a specific scene, diagnosis, or reframe.
- Body: peel-the-onion, step-through, or story-to-principle.
- Close with an implication or substance-inviting question. Never a CTA.
- Product mentions: MyVault in ~1 of 4 posts, as context not pitch.

For newsjacks, use the 5-part arc in `craft/newsjack-craft.md`.

**Step 5 — Edit.**
Open `craft/edit-craft.md`. Run the six passes:
1. **Structure** — diagnosis → evidence → lesson, in that order?
2. **Mode** — is it Explain/Challenge/Educate, or has it drifted to Preach?
3. **Voice qualities** — systems-thinker? Evidence-led? Diagnostic? Warm?
4. **Failure portrait scan** — any of the five? Check `craft/antipatterns.md` for before/afters.
5. **Mechanical** — banned words, preach phrases, "zero-knowledge," exclamation marks.
6. **Two-pass self-audit + read aloud** — "What makes this obviously AI?" Fix 3-5 tells.

**Step 6 — Final Test.**
Four questions (from `voice/voice.md` § Final Test):
1. Would Markos wince?
2. Every big claim anchored?
3. Turn after the evidence?
4. Thinking, or performance?

**Step 7 — Queue for approval.**
Queue by Friday EOD. Markos reviews by Monday. Publish Tuesday-Thursday.
For newsjacks: draft → Slack Markos → publish on approval. No response in 4h → hold.

---

## Workflow: Editing someone else's draft

When reviewing a draft Sead or an AI agent produced.

**Load:** `voice/voice.md` + `craft/antipatterns.md` + `craft/edit-craft.md` + `guardrails/guardrails.md`

**Run the six passes** from `craft/edit-craft.md`. The most common issues (from the writer review of batch 1):

1. **"Challenge Respectfully" openers** — dead framework. All disagreement uses Another-Angle. Cut any "I'd push back," "I disagree," "Actually."
2. **No tools named** — Bedrock should appear in most AI-architecture comments. Claude, Qwen, knowledge graph are all deployable proof points.
3. **Fabricated credentials** — every bio claim must trace to `identity/identity.md`. If it's not there, it doesn't go in.
4. **Pseudo-profound closings** — "X is the secret sauce" / "That changes everything." Cut these.
5. **No first-person scenes** — "I have seen this across dozens of deployments" is generic. "When we rolled out Eloqua in 2003..." is Markos.
6. **No confidence markers** — zero uses of "frankly," "honestly though," "look," "back to basics." A Markos comment should carry one most of the time.

After the six passes, run the Final Test. If the draft passes, it's ready for Markos (or for publishing if Green Zone + Tier 1).

---

## Workflow: Brainstorming post ideas

When generating angles for the next week's posts.

**Load:** `identity/identity.md` + `opinions/opinions.md` + `guardrails/guardrails.md`

**Optionally load:** `stories/stories.md` (for story-led angles) + `audience/audience-linkedin.md` (for segment targeting)

**Process:**
1. Scan the week's AI/privacy news. Any newsjack-worthy items?
2. Review the 8 pillars in `opinions/opinions.md`. Which hasn't been covered recently?
3. Check `stories/stories.md` for an unused Green story that pairs with that pillar.
4. Draft 3-5 one-line angles. For each: which format (anchor/newsjack/build-note)? Which mode?
5. Check each angle against `guardrails/guardrails.md`. Any Yellow/Red flags?
6. Pick the 3 strongest. Queue for drafting.

---

## How corrections flow back into the system

When Markos says "I wouldn't say it this way" or "yes, exactly":

1. **Log it** in `_analysis/voice-corrections-log.md`.
2. **Identify which file** the correction applies to:
   - Voice/tone/phrasing issue → update `voice/voice.md`
   - Zone boundary shift → update `guardrails/guardrails.md`
   - New opinion or position change → update `opinions/opinions.md`
   - New story or story status change → update `stories/stories.md`
   - Craft pattern issue → update the relevant `craft/` file
3. **Update the file.** Bump the version in frontmatter. Add a line to the manifest changelog if it's a material change.
4. **Tell Sead** what changed and why, so the same mistake doesn't repeat.

The system gets better with every correction. That's the point.

### How the eval feeds corrections (the measurement spine)

`/myvault:voice-eval --brand voice-of-markos` adds an *automated* feeder to the loop above — without changing who decides. The flow is **auto-surface, human-ratify, never auto-mutate**:

1. The eval runs **originality-first** (v2.5): the substitution / pillar-activation check is PRIMARY, the blind-lineup blend-in is secondary/advisory, voice-stats deltas tertiary — see `craft/edit-craft.md` § Voice-eval gate. It is now a *required* step before Markos's pre-launch round, with a trend block (substitution-pass % over batches) in `playbooks/approval-workflow.md`.
2. Its deduped tells and gate flags append to `_analysis/voice-corrections-log.md` under a clearly-marked **`voice-eval candidates (unratified)`** block.
3. A human reads the candidates and ratifies the real ones into chunk edits — exactly the 4-step flow above (log → identify file → update + version-bump → tell Sead). Unratified candidates are never applied automatically.

The round-over-round version of this — how we *improve the system*, not just gate one draft — is `playbooks/improvement-loop.md` (the discrimination test + the loop procedure + the honesty limits). Its first run is logged at `_research/2026-06-09-improvement-loop/run-1.md`.

**The keystone feeder is Loop 1 (`markos-edits-log.md`):** every time Markos edits a draft, the `(draft → final)` pair is captured. Those pairs are the only real written-Markos data the program generates — once they accumulate they re-ground `voice/voice-stats.md` (replacing today's directional prior with real, per-mode numbers) and seed the recognition lineup. The whole spine was built with **zero ground truth**; this is how it earns some.

So the machine *surfaces* what looks off; the human still *decides* what's canon. This is the deliberate difference from Spiral, which lets its judge auto-refine — our canon stays hand-ratified and version-controlled. The voice targets it scores against live in `voice/voice-stats.md` — a QA instrument and a **directional prior**, never the voice source.

---

## Who uses what

| Person | Primary document | Goes deeper when... |
|---|---|---|
| **Sead** (writer) | `CEO-LinkedIn-Playbook.md` — open while working | Needs a story → `stories/stories.md`. Needs a position → `opinions/opinions.md`. Needs the editing workflow → `craft/edit-craft.md`. |
| **Mark** (steward) | This guide + the system files directly | Reviewing Sead's work, updating the system after corrections, onboarding a new writer. |
| **Markos** (voice holder) | `CEO-LinkedIn-Engagement-Framework.md` | Reviewing the trust progression, understanding how his voice is captured. He doesn't need the system files. |
| **AI agent** | `CLAUDE.md` + `_retrieval-rules.yaml` | Loads the right files per task profile. Uses the manifest for discovery. |

---

## The relationship between documents

```
CEO-LinkedIn-Engagement-Framework.md    ← program-level: what we do and why (for Markos)
        │
CEO-LinkedIn-Playbook.md               ← daily reference: quick-checks and routing (for Sead)
        │
voice-of-markos/                        ← source of truth: the full voice system
├── CLAUDE.md                           ← AI routing: what to load per task
├── guide.md                            ← this file: how to use the system
└── [16 content files]                  ← the actual voice, positions, stories, craft, guardrails
```

The Framework explains the program. The Playbook runs the daily work. The system files hold the truth. This guide explains how they connect.

---

*v1.0 · 2026-04-16.*
