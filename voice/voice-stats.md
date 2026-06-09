---
chunk_id: "voice-stats"
domain: "voice"
category: "voice"
subcategory: "measurement"
token_count: ~150
version: "2.0"
last_updated: "2026-06-09"
status: "parked"
summary: >-
  PARKED. There are no trustworthy numeric voice targets yet — we have no real published Markos
  posts to derive them from. This file is a placeholder that explains the parking so nobody
  re-adds invented numbers. Not loaded by any task profile.
---

# Voice Stats — parked until we have real data

There are **no numeric voice targets** here, on purpose.

Earlier versions carried a vector of targets (specificity, em-dash rate, first-person %, etc.)
computed from a thin, partly self-authored corpus. They were guesses dressed as measurements, so
they were removed. **Do not write to invented numbers, and do not re-add a target vector until it
comes from real data.**

**The honest state:** the only trustworthy source of "how Markos actually writes" is his real
published posts and his edits. We don't have enough yet. The capture mechanism is
[[markos-edits-log]] (Loop 1) — once it accrues real `(draft → final)` pairs, re-derive targets from
*those*, not from the system's own renderings.

Until then, judge voice **qualitatively**: the four qualities and the Final Test in `voice/voice.md`,
the failure portraits + the substitution test in `craft/antipatterns.md`. Those are the bar.

The stylometry meter (`scripts/voice-stats/voice_stats.py`) stays on disk, dormant — a tool to run
*when* real data exists, not a routine step.
