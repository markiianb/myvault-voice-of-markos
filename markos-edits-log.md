---
type: log
status: active
owner: Mark Bobyliak
created: 2026-06-09
updated: 2026-06-09
tags:
  - content-log
  - voice-of-markos
  - ground-truth
  - voice-data
summary: Running log of Markos's edits to drafts — every (system-draft → Markos-final) pair. The highest-signal voice data the program produces. A record, NOT a retrieval chunk; never loaded during drafting.
---

# Markos Edits — Ground-Truth Log

The keystone of the feedback system. Every time Markos rewrites a draft, the **delta between what
the system produced and what he actually published is labeled voice data** — for free. He rewrote
13 of 20 drafts in the MVM-153 comment review; that signal used to be thrown away. This log keeps it.

**Why it matters.** The voice chunks were built from one April voice session + curated renderings —
*zero* validation against real published Markos writing (the 2026-06-08 audit's root finding). These
pairs are the only real written-Markos data the program generates. Once enough accumulate, they're
what any future measurement should be derived from — real numbers from real posts, not guesses. Until
then there are no numeric voice targets (`voice/voice-stats.md` is parked); judge qualitatively.

> [!warning] Not a retrieval chunk; not an exemplar to imitate
> This is a **record**, like the posts/articles logs. It is NOT loaded during drafting and is NOT in
> `_manifest.yaml`'s chunk list (it's an `output_log`). Reading it to *derive corrections or
> re-ground stats* is a deliberate, periodic, human-run analysis step — never an auto-load. Do not
> paste its "before" text into a draft.

## What to capture, and when

Log a pair **whenever Markos changes a draft before it ships** — a full rewrite, a few sentences, or
even one telling word swap. Capture at the approval step (`playbooks/approval-workflow.md`) or in the
end-of-day review (`playbooks/daily-routine.md`). If he accepts a draft verbatim, there's nothing to
log here — record that as `provenance: markos-verbatim` in the posts/articles log instead.

## How to add an entry

Paste a new block at the top of **Entries**, above the most recent. Keep both versions verbatim.

```
## YYYY-MM-DD — [post-id or hook]

- **Post:** [link to posts-log/articles-log entry, or the scheduled post]
- **Format / mode:** anchor | newsjack | build-note | comment | reply | article
- **Scope of edit:** full rewrite | several sentences | one line | word-level
- **What changed (1 line):** [the gist — e.g. "cut the contrarian opener; added the 15:1 services number"]

**Before (system draft):**
> [verbatim]

**After (Markos-final):**
> [verbatim]

**Voice lesson:** [what this teaches the system — the pattern to ratify into a chunk, if any. Link the
chunk: e.g. "→ opinions/opinions.md pillar 7" or "→ candidate for voice.md". Leave blank if one-off.]

---
```

## How this feeds the system (periodic, human-run)

1. **Ratify recurring lessons** — when the same edit-pattern shows up across ≥2–3 pairs, it's a real
   correction: log it in `_analysis/voice-corrections-log.md` and ratify into the relevant chunk
   (version-bump). One-offs stay here as data, not canon.
2. **Derive measurement later — only when it's justified.** Once a real body of `after`
   (Markos-final) text accumulates, voice numbers *could* be derived from it; the dormant meter
   (`scripts/voice-stats/voice_stats.py`) is there for that day. Not before — don't compute targets
   from a handful of pairs. A deliberate human decision, never an automatic step.

## Entries

<!-- Newest at top. No entries yet — the first one lands the next time Markos edits a draft.
     Skeleton above shows the shape. This is expected to be empty until the program runs live;
     that emptiness is the honest state, not a gap to backfill with invented pairs. -->

---

*Created 2026-06-09 (v2.5, ground-truth loops). Sibling logs: `markos-linkedin-posts-log.md`,
`markos-linkedin-articles-log.md`. Governance: `_analysis/voice-corrections-log.md`.*
