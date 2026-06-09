---
chunk_id: "principles"
domain: "constitution"
category: "constitution"
context_tags: [principles, constitution, governance, spiral-learnings, measurement, ground-truth]
token_count: ~700
version: "1.0"
last_updated: "2026-06-09"
status: "active"
summary: >-
  The constitution of the Voice of Markos system — WHY it's shaped this way, the governing
  principles, and what it deliberately refuses. Read this before changing the system. Carries the
  Spiral learnings as the principle that governs the measurement spine.
---

# Voice of Markos — Principles (the constitution)

Read this before changing the system. The chunks say *how Markos sounds*; the playbooks say *how we
run*; **this says *why the system is shaped this way* — and what we refuse.** It exists because the
system has, more than once, been over-built and then over-cut; these principles are the stable spine
that should survive both impulses.

## The six principles

1. **Curated substance, not averaged samples.** Voice comes from hand-curated pillars, stories, and
   red lines drawn from a real source (the voice session) — not from statistically averaging past
   output. We are deliberately **not** the mean of what we've written. (That is Spiral's model; it
   regresses toward generic — see the teardown.) The curation is the moat.

2. **Originality is the moat; human-likeness is table stakes.** Any competent model sounds human.
   Only Markos says what *only Markos* would. The primary check is always the substitution test
   (`craft/antipatterns.md`): *could only he have written this?* Optimize the half a competitor's
   engine structurally cannot copy — his opinions and lived stories.

3. **Measure only against real ground truth.** The measurement spine — `voice/voice-stats.md`, the
   `/myvault:voice-eval` blind-lineup, the `playbooks/improvement-loop.md` loop — is real and kept
   wired. But until Markos's *real edits* accrue, **its numbers are a directional prior, not truth.**
   Do not optimize to them (a target you can game stops measuring anything — write to an em-dash rate
   and you've corrupted the voice). Do not present them as validated. Blend-in is advisory; originality
   gates.

4. **Capture real edits — the only thing that compounds.** `markos-edits-log.md` is the keystone.
   Every `(system-draft → Markos-final)` pair is the ground truth that, over time, lets the spine
   measure for real instead of guessing. One real edit is worth more than any synthetic loop run.

5. **The loop never auto-mutates canon.** Instruments *surface* candidates; humans *ratify* them into
   chunks (version-bump + changelog). The system improves by human-ratified compounding, not by
   grading itself and self-refining. This is the deliberate difference from Spiral, which lets its
   judge auto-tune — and is why our voice can't drift toward the judge's biases.

6. **Keep the instruments ready, but honest — don't over-build on absent data.** We built the spine
   (v2.4–2.6), cut it as over-built (v2.7), and restored it under this constitution (v2.8). The
   resolution: the spine is valuable *and* provisional. Keep it wired so it's exercised and ready —
   but governed by principles 2–4, so it never masquerades as validated truth. When real edits make
   the numbers trustworthy, this principle relaxes; until then, it holds.

## What we learned from Spiral (the source of principles 1–3, 5)

Spiral (by Every) is an agent-native writing tool. We reverse-engineered it (no theft — convergent
evolution; if anything our content was fed *into* it). Its engine = a short prose voice guide + a
contrastive stylometry vector + a conditionally-loaded principle-file library + an LLM-as-judge loop.
**The one genuinely good idea worth borrowing was the *measurement spine*** — quantify how a voice
deviates from generic AI, and close a feedback loop. **The one fatal flaw for us:** Spiral *is* the
average of its samples (regression to the mean), and a measurement loop with no real ground truth
just grades the system against its own assumptions. So we keep the spine and reject the
sample-averaging soul — curation stays canonical; the instruments stay subordinate and provisional.

Full research (do not duplicate here):
- `80-Documents/Strategy/Spiral-Style-Engine-Teardown.md` — how the engine works, the verdict.
- `80-Documents/Strategy/Content-System-Spiral-Benchmark-and-Improvements.md` — us vs Spiral.
- `_research/2026-06-08-voice-stats/` + `_research/2026-06-09-improvement-loop/` — our build + first loop run.

## The standing test before adding machinery

Before building another instrument, ask: **does it have real ground truth to work against?** If no —
park it (don't delete it; keep it ready) and capture more real edits instead. Precision on absent
data is noise. The unlock is always Loop 1, never more apparatus.
