# Voice of Markos — Operator Guide

The operational system for Markos Symeonides's LinkedIn presence and personal blog. Eighteen chunks across seven domain folders.

> **Before changing the system, read `PRINCIPLES.md`** — the constitution: why the system is shaped this way, what it deliberately refuses, and the Spiral learnings that govern the measurement spine (instruments are a directional prior until Markos's real edits make them trustworthy; originality is the moat; capture real edits).

## What to load

**Every task:** `voice/voice.md` + `guardrails/guardrails.md`

**Writing a LinkedIn post:** add `craft/post-craft.md` + `opinions/opinions.md` + `stories/stories.md`

**Writing a newsjack:** add `craft/newsjack-craft.md` + `opinions/opinions.md`

**Writing a comment:** add `craft/comment-craft.md` + `opinions/opinions.md` (check topic strength before engaging). Before drafting a *batch*, read Markos's 13 real comments (`_analysis/2026-06-04-comment-feedback-markos-responses-and-voice-synthesis.md` Appendix A, vault-side) — the imitation source is his corpus, never the chunk examples. After drafting a batch, run the Batch QA step below.

**Writing a blog post:** add `craft/blog-craft.md` + `craft/post-craft.md` (for anchor patterns) + `opinions/opinions.md` + `stories/stories.md`

**Editing a LinkedIn draft:** add `craft/edit-craft.md` + `craft/antipatterns.md` (Pass 0 preservation scan, then Quick Scan, then Final Test). For a measured check, add `voice/voice-stats.md` and run the Voice-eval gate (`craft/edit-craft.md` § Voice-eval gate) — blind-lineup + contrarian-opener/on-point/substitution + voice-stats deltas. Soft signal; surfaces candidates to the corrections log, never auto-edits.

**Editing a blog draft:** add `craft/edit-craft.md` + `craft/antipatterns.md` + `craft/blog-craft.md` (blog-specific failure patterns and pre-publish checklist apply)

**Checking who Markos is:** `identity/identity.md`

**Checking audience fit:** `audience/audience-linkedin.md`

**Checking approval / cadence / accounts:** `playbooks/approval-workflow.md` + `playbooks/daily-routine.md` + `playbooks/target-accounts.md`

**Checking what's been posted recently:** `markos-linkedin-posts-log.md` for short-form (anchor / newsjack / build-note) + `markos-linkedin-articles-log.md` for long-form. Newest at top. Both now carry a `provenance` tag (markos-verbatim | markos-edited | system-draft) + pillar/mode/story/engagement tags. **`markos-edits-log.md`** holds every `(system-draft → Markos-final)` edit pair — the ground-truth voice data (Loop 1). These are records, not retrieval chunks — load when triaging past activity or re-grounding voice-stats, not when drafting.

## Two scans run before every review

Before Pass 1 of any edit, run these in order:

1. **Preservation scan** (from `craft/edit-craft.md` Pass 0) — name 3–5 things working, with the mechanism. Mark as do-not-edit.
2. **Opinion + Story activation scan** (from `opinions/opinions.md` and `stories/stories.md`) — list every on-topic pillar and Green story; mark activation status (Activated / Mentioned / Absent or Deployed / Referenced / Absent).

Absent-but-on-topic pillars and stories are the highest-leverage rewrite opportunity. Flag before voice or copy issues.

## Batch QA for comment drafts (v3.1 — mandatory before any batch ships to review)

Per-draft rules don't survive parallel generation: the 2026-06-08 batch passed every v3.0 rule per-draft and came out collectively monotone (Sead: "standard AI speech" — "25 years" 9×, "the line that lands" ~10× across 35 drafts). So every multi-comment batch runs two checks before a reviewer sees it:

1. **Cross-batch repetition scan (mechanical).** Grep the batch for the red-line tells (`craft/antipatterns.md` § The Template Echo) and build an opener-pattern + credential-phrasing frequency table across all drafts, plus a **length distribution** (sentence count per draft). Any red-line hit, any opener pattern recurring (at paraphrase level), any credential phrasing appearing >2×, or a batch where most drafts run 5+ sentences (length echo — long is earned, not default) → the offending drafts go back with explicit "these N phrasings are already used in this batch — vary / re-cut to the shortest version that lands" context.
2. **Blind-lineup spot check (judgement).** Sample ~5 drafts; line each against 2–3 of Markos's real comments (same synthesis doc). If a reviewer-agent can reliably sort system-vs-Markos on register alone, the batch fails — fix is re-drafting from his corpus, not word-swapping tells.

Both checks *flag*; agents re-draft; humans ratify (PRINCIPLES.md — the loop never auto-mutates). Frequencies are reported indicators, never targets (`voice/voice-stats.md` § Tell-frequency report).

## The sixteen files

| Domain | File | What it covers |
|---|---|---|
| **voice/** | `voice.md` | How Markos sounds — tone, four qualities, three modes + never-preach, five failure portraits, banned words, rhythm, length, Final Test |
| **voice/** | `voice-stats.md` | Measured, contrastive voice targets (specificity, numerals, em-dash rate, hedges, first-person, sentence SD) vs a generic-AI baseline. The per-voice em-dash target. A QA instrument, never the voice source. |
| **identity/** | `identity.md` | Who Markos is — bio, positioning, authority claim, audience segments, disclosure rules |
| **opinions/** | `opinions.md` | What he believes — activation scan, quick gate table, 8 pillars with thesis + sound-bites + red lines |
| **stories/** | `stories.md` | 12 indexed stories with activation scan, Green/Yellow/Red status, pillar tags, cautions |
| **guardrails/** | `guardrails.md` | Red/Yellow/Green zones with reasoning categories, never-engage exclusion list, personal comfort matrix |
| **audience/** | `audience-linkedin.md` | Five audience segments, content-to-audience matching, what doesn't land |
| **craft/** | `antipatterns.md` | Before/after casebook for the failure portraits (incl. The Template Echo + red-line tell list), self-audit, editing tests |
| **craft/** | `post-craft.md` | How to build LinkedIn posts — anchor, newsjack, build-note formats |
| **craft/** | `comment-craft.md` | Four kudos-first comment frameworks + the texture pack (real opener bank, credential rotation, batch diversity rules) |
| **craft/** | `newsjack-craft.md` | Reacting to news within 24h without preaching |
| **craft/** | `blog-craft.md` | Blog format — length, pull quotes, TOC, heading hierarchy, series identity, dual titles, internal linking, lead capture, bio |
| **craft/** | `edit-craft.md` | Pass 0 preservation + six critique passes, flattening tests, pre-write and self-review checklists |
| **playbooks/** | `approval-workflow.md` | Monday rhythm, three-tier approval, trust progression month 1-4+ |
| **playbooks/** | `daily-routine.md` | Volume caps, time-of-day rules, posting schedule |
| **playbooks/** | `target-accounts.md` | Six engagement categories, quality markers, review cadence |

## Hard constraints (inherited from parent brand, non-negotiable)

- Never fear-monger about security. Confidence, not fear.
- Banned words and AI-slop constructions from the parent apply — see `voice/voice.md` for the consolidated list.
- **Zero Trust, not zero-knowledge.** Always.

## Voice of Markos overrides (for his content only)

- First-person "I" is allowed and expected.
- Opinions are held and defended with evidence.
- Register is authority-educator-challenger.
- Personal stories are core material.

When Markos's voice rules conflict with the parent brand-system, Voice of Markos wins for his LinkedIn content. For MyVault company content, the parent rules apply unchanged.

## Parent brand-system

Lives at `10-Brand/brand-system/`. When Markos talks about MyVault the product, also read the product chunks from the parent.

## Evolution

Every correction from Markos ("wouldn't say it this way" / "yes, exactly") updates the relevant file. Version-bump on material changes.
