---
chunk_id: "voice-stats"
domain: "voice"
category: "voice"
subcategory: "measurement"
context_tags: [stylometry, voice-targets, quality-check, contrastive, ai-tells, em-dash]
depends_on: ["voice"]
token_count: ~750
version: "1.0"
last_updated: "2026-06-08"
status: "active"
summary: >-
  Quantified, contrastive voice targets for Markos's LinkedIn/blog content — how his
  writing measurably differs from a generic AI-founder voice. A QA instrument, NOT the
  voice source. Carries the per-voice em-dash target that supersedes the parent ban.
---

# Voice Stats — Measurable Targets (Markos)

> **What this is.** A small vector of measurable voice properties, computed from Markos's
> real verbatim speech and his curated written renderings, expressed **contrastively** — as a
> ratio against a generic AI-founder-LinkedIn baseline (how a vanilla assistant writes the same
> kind of post). It answers one question: *is this draft measurably Markos, or has it drifted
> toward generic AI shape?*
>
> **What this is NOT.** Not the voice source, and not a target to write *to*. The curated chunks
> — `voice/voice.md`, `opinions/opinions.md`, `stories/stories.md`, `guardrails/guardrails.md`
> — define the voice; this only *measures* adherence. **Hitting the vector while saying nothing
> only Markos would say is a fail** (the substitution test still governs). A number can flag
> flattening; it can never supply an opinion, a story, or a red line. Stats never override the
> pillars or the guardrails.
>
> **Provenance.** Computed 2026-06-08 by `scripts/voice-stats/voice_stats.py` (the shared meter,
> reused not forked) over Markos's verbatim voice-session speech (1,339 w) and his curated written
> renderings (554 w) vs a generic-AI baseline (432 w). Full method + caveats:
> `_research/2026-06-08-voice-stats/`. Heuristic stylometry on small corpora — **v1.0 directional**.
> Re-derive when genuine published Markos posts accumulate.

## The contrastive fingerprint

Each target is Markos's value with the **ratio vs the generic-AI baseline** and what it governs.
The load-bearing four — where he separates hardest from generic AI — are marked ★.

| Metric | Markos target | vs generic-AI | What it governs |
|---|---|---|---|
| ★ Specificity (proper nouns + numerals /1k) | **≈55–65** | **2.1× more** | Name things. Bedrock, Qwen, the knowledge graph — not "an AI model." |
| ★ Numerals /1k | **≈12–15** | **generic AI ≈ 0** | Numbers anchor every big claim. "$100k", "15:1 services", "20× cheaper", "25 years". |
| ★ Em-dashes /1k | **≈20–25** (do not strip below ~15) | **1.8× more** | His thinking-aloud cadence — asides and self-corrections render as em-dashes. A signature, **not** a tell. Supersedes the parent ban (see note). |
| ★ Hedges /1k (maybe, might, likely, generally…) | **≤3** | **0.5× (half)** | Conviction, not cushions. "I don't think" beats "I think"; drop the epistemic softeners. |
| First-person share of pronouns | **35–45%** | 1.3–1.5× | **The VoM inversion.** Parent Product Voice is "we, never I"; Markos is first-person by design. High "I" is correct here, a violation there. |
| Second-person share of pronouns | **~25%** | ~2× | He addresses the reader ("if you're building with AI…") without relentless "you". |
| Sentence-length SD | **≥9** (real long-form) | up to 1.6× | Jagged rhythm — short landings against long winding builds. Low SD = flattened. |
| Colons /1k | **~9** | ~2× | Enumeration-in-prose ("you verify: knowledge graph, embeddings, audit logs"). Unlike the parent, the colon is on-voice for Markos. |
| Sentence-length mean (words) | **12–14** | ~same | Mid-length default, varied hard around it. |
| Preach-phrase rate | **0 — hard gate** | — | "everyone should / you need to / it's obvious / wake up / companies must" → must be zero. The one numeric *gate*, not a soft signal (encodes the existing hard ban). |

### Em-dash note — the per-voice target that supersedes the parent ban

The parent brand-system bans em-dashes; `craft/edit-craft.md` historically inherited that ban for
Markos. **The data overturns it.** His curated written renderings run **≈25 em-dashes/1k** — 1.8×
the generic-AI baseline (13.9) and ~5× the parent corpus (4.9). His voice is built on asides,
nested thoughts, and self-corrections ("Now it exists — and it's the thing that makes the whole
product work"); on the page those *are* em-dashes. (The raw speech transcript reads ~1.5/1k only
because Fireflies renders pauses as commas — a transcription artifact, not his voice.)

**Rule:** em-dashes are **on-voice for Markos**. Do not ban them; do not strip a draft below
~15/1k — that flattens his cadence. The ~20–25/1k figure is a ceiling-ish signature (the curated
sample over-represents it), not a floor to hit. This is a per-voice *rate that governs*, the same
mechanism the Newsletter satellite uses — not a global ban with a buried exception.

## How to use at draft time

Lead with the ★ four — they're where Markos most separates from generic AI:

1. **Be specific** — name the tools, the industries, the systems. Generic AI stays abstract.
2. **Give numbers** — the baseline used *zero* numerals; a Markos draft without one is floating.
3. **Keep the em-dashes** — his asides are the voice; don't sand them off.
4. **Don't hedge** — half the baseline's hedging. State it.

Don't game it. A draft can hit every number and still be generic — the qualitative review
(`craft/edit-craft.md`, the activation scans in `opinions/`+`stories/`) and the substitution test
are the real bar. This vector catches *drift*, not quality, and never speaks for the pillars.

## How to check after drafting

Run `python3 scripts/voice-stats/voice_stats.py <draft> --json out.json` and compare to the targets;
large misses on the ★ four are the highest-leverage edits. Then `/myvault:voice-eval <draft>
--brand voice-of-markos` for the blind-lineup blend-in score + the non-blind VoM check
(contrarian-opener, on-point, substitution). See `craft/edit-craft.md` § Voice-eval gate.
