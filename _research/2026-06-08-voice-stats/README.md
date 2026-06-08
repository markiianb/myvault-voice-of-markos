# Voice-stats derivation — Markos (2026-06-08)

Reproducible measurement behind `voice/voice-stats.md`. Part of the Spiral-derived
measurement-spine graft ([[Spiral-Style-Engine-Teardown]], [[Content-System-Spiral-Benchmark-and-Improvements]]).

## Method

Contrastive stylometry: measure how Markos's voice deviates from a generic AI-founder
baseline. The meter is the **shared** `scripts/voice-stats/voice_stats.py` (vault root) —
pure-stdlib heuristic stylometry, reused not forked. Ratios (Markos ÷ baseline) are robust
to the meter's heuristic bias because both sides run the identical script.

**Corpus firewall:** the meter only reads text to compute statistics. None of these files is
ever an exemplar to imitate or loaded into a drafting context. They measure; they don't teach.

## Why two Markos corpora

- `markos-spoken.md` (1,339 w) — verbatim 2026-04-10 voice-session speech + story quotes.
  The deep voice signal: first-person rate, specificity, hedging, jagged rhythm (sentence-SD).
  **Not** the source for punctuation — Fireflies renders pauses as commas/periods, so em-dash
  reads a false ~1.5/1k.
- `markos-written.md` (554 w) — the hand-curated "✅ real Markos" renderings + LinkedIn
  projections from the voice system. The correct source for **punctuation + written rhythm**:
  his asides and self-corrections become em-dashes on the page (25/1k).

Deliberately **excluded**: `markos-linkedin-posts-log.md` / `…-articles-log.md` — mostly
system/Sead-drafted; the parent A/B ([[RESULTS]]) proved shipped corpus carries the
gravitas-fragment AI tell. Measuring them would baseline the system's *approximation* of Markos.

`generic-baseline.md` (432 w) — three vanilla-AI "founder on LinkedIn" posts on his topics
(pragmatic AI, open source, privacy), no VoM chunks loaded. The contrast set.

## Headline results (per 1,000 words unless noted)

| Metric | Markos written | Markos spoken | Generic AI | Written ÷ AI | Read |
|---|---|---|---|---|---|
| Specificity (proper nouns + numerals) | 63.2 | 34.4 | 30.1 | **2.10×** | ★ name things |
| Numerals | 14.4 | 11.2 | **0.0** | **∞** | ★ numbers anchor claims |
| Em-dashes | **25.3** | 1.5 (artifact) | 13.9 | **1.82×** | ★ his cadence, not a tell |
| Hedges (maybe/might/likely…) | 5.4 | 2.2 | 11.6 | **0.47×** | ★ conviction, not cushions |
| First-person share of pronouns | 38.1% | 44.8% | 29.4% | 1.30× | VoM inversion (HIGH "I/we") |
| Second-person share | 23.8% | 16.8% | 11.8% | 2.02× | addresses the reader |
| Sentence-length SD | 6.9 | **9.6** | 6.1 | 1.13× (1.58× spoken) | jagged rhythm (strongest in real long-form) |
| Colons | 9.0 | 1.5 | 4.6 | 1.95× | enumeration-in-prose ("verify: a, b, c") |
| Comparatives | 3.6 | 7.5 | 6.9 | 0.52× | not a strong written signal |
| MTLD (lexical diversity) | 194.8 | 68.6 | 161.0 | 1.21× | rich (small-sample inflated) |

## Caveats (treat the vector as directional, v1.0)

- **Small corpora** (554 w / 432 w) — MTLD and some per-1k rates are noisy/inflated. Ratios on
  the ★ four are large enough to be load-bearing; treat the rest as directional.
- **Spoken ≠ written.** Speech over-indexes discourse markers ("you know", "right?") the meter
  doesn't count as hedges; written tightens. Lead the target with transfer-robust metrics
  (specificity, numerals, low-hedge, first-person) + the written em-dash signal.
- **Em-dash number is curated-sample-high** (the ✅ examples over-represent his cadence). The
  *direction* is certain (em-dash is on-voice for Markos); the exact rate is a ceiling-ish
  signature, not a floor to hit. Re-derive when genuine published Markos posts accumulate.

## Files
`markos-spoken.md`, `markos-written.md`, `generic-baseline.md` (inputs) ·
`metrics_spoken.json`, `metrics_written.json`, `metrics_baseline.json` (meter output).
Re-run: `python3 scripts/voice-stats/voice_stats.py <file> --json <out> --label <name>`.
