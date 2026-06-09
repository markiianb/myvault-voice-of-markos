---
chunk_id: "improvement-loop"
domain: "playbooks"
category: "playbooks"
subcategory: "evaluation"
context_tags: [evaluation, improvement-loop, measurement, governance, discrimination-test]
depends_on: ["voice-stats", "edit-craft", "antipatterns"]
token_count: ~750
version: "1.0"
last_updated: "2026-06-09"
status: "active"
summary: >-
  How we evaluate and improve the Voice of Markos system: the discrimination test (does the
  eval instrument rank known-quality drafts correctly?) and the round-over-round improvement loop
  (draft → measure → diagnose → revise + surface system-fix candidates → re-measure). A process
  record, NOT a retrieval chunk. Carries the hard honesty limits.
---

# Improvement Loop — how we evaluate and improve the system

This is the standing process for making the voice system better over time — the round-over-round
loop the parent prototyped (`80-Documents/Research/Competitive/Spiral/Improvement-Loop-Log.md` + the
vault-vs-gdrive A/B). A **process record**, not a retrieval chunk — never loaded during drafting.

> [!warning] The hard limit — state it in every run
> **No real Markos is in this loop.** Drafts are system-generated; the "improved" version is our best
> *curation*, not actual Markos. The loop can (a) demonstrate the mechanism, (b) raise the system's
> *self-consistency* against its own targets, and (c) surface **system-fix candidates**. It **cannot**
> prove the system is good or validate it against real Markos — that waits for Loop 1
> (`markos-edits-log.md`) to accrue real edits. An improvement loop with no ground truth risks
> measuring its own reflection; the rules below are what keep it honest.

## Two non-negotiable rules

1. **Originality is the target; never optimize blend-in.** The loop revises toward *deploying a pillar
   + a story + a named-specific* (the substitution test — `craft/antipatterns.md` § The Substitution
   Test). Blend-in is a noisy secondary signal; optimizing it just games human-likeness (the audit's
   flagged theater).
2. **Never auto-mutate canon.** Draft revisions happen in-loop. Chunk edits do not. System-fix
   candidates append to `_analysis/voice-corrections-log.md` *unratified*; a human ratifies (version-bump).

---

## Part 1 — The discrimination test (validate the instrument)

Before trusting the eval to steer the loop, check it can tell good from bad. Reuse the labeled corpus
we already have — **build no new fixtures**:

- **Gold** (should pass / rank high): verbatim Markos — `_research/2026-06-08-voice-stats/markos-spoken.md`, `markos-written.md`.
- **System-draft** (should rank middle): a real generated post (e.g. the frontier-model post).
- **Anti** (should fail / rank low): the retired strawman — `_research/2026-06-08-voice-stats/generic-baseline.md`.

Run the eval axes on each and check the ranking is **gold > system-draft > anti** on the primary
(originality) axis, ideally on blend-in too. **A muddy result is a finding, not a failure to hide** —
it means the instrument needs work (→ a candidate to improve the eval), and you record it plainly.

---

## Part 2 — The round-over-round loop

Seed with a real artifact (ideally one with a known baseline). Each round:

1. **Revise toward Markos voice** — deploy a pillar (`opinions/opinions.md`) + a story
   (`stories/stories.md`) + named-specifics + his cadence (asides, first-person, a number); cut
   generic-analyst framing and contrarian openers.
2. **Measure (3 axes, originality first):**
   - **PRIMARY — originality / substitution** (non-blind): does it deploy a pillar/story/named-specific?
     Could only Markos have written it?
   - **secondary — blind-lineup blend-in** (advisory, noisy): `/myvault:voice-eval` + `blind-judge` vs verbatim decoys.
   - **tertiary — voice-stats deltas**: `scripts/voice-stats/voice_stats.py` vs the directional targets.
3. **Diagnose** — name the top 2–3 failures, and tag each: **DRAFT problem** (fix in-loop) or
   **SYSTEM problem** (a chunk/generator gap → a candidate, logged, not applied).
4. **Stop** at the round cap (default 3) or when originality passes and the deltas flatten. Don't
   manufacture a delta — a non-improving round is recorded honestly and ends the loop.

Run it as a Workflow when orchestrating: **rounds sequential, the 3 measures a small parallel batch
per round** (a gentle burst, not a wide one — avoids rate limits).

---

## Part 3 — How the output feeds the system

- **DRAFT improvements** stay with the artifact (and, if it ships, feed the posts log).
- **SYSTEM-fix candidates** → `_analysis/voice-corrections-log.md` as an *unratified* block. A human
  ratifies recurring, clear wins into the relevant chunk (version-bump + changelog). Default to
  leaving them for review; ratify only the obvious ones.
- **The run-up** (rounds, deltas, candidates, the honesty caveat) → `_research/<date>-improvement-loop/`.
- **The trend** → one line in `playbooks/approval-workflow.md` § Voice-eval gate trend block
  (substitution-pass % is the headline; the KPI is the *direction* over runs, not any single score).
- **The real unlock is still Loop 1** — once `markos-edits-log.md` has real edits, re-derive
  `voice/voice-stats.md` from them and re-run this loop against *real* Markos data. Until then, this
  loop improves self-consistency and surfaces candidates; it does not validate.
