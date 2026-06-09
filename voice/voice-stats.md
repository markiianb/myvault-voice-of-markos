---
chunk_id: "voice-stats"
domain: "voice"
category: "voice"
subcategory: "measurement"
context_tags: [stylometry, voice-targets, quality-check, directional-prior, ai-tells]
depends_on: ["voice"]
token_count: ~800
version: "1.1"
last_updated: "2026-06-09"
status: "active"
summary: >-
  Directional voice targets for Markos's LinkedIn/blog content — measurable properties where
  his writing tends to differ from generic AI output. A QA instrument and a DIRECTIONAL PRIOR,
  NOT the voice source and NOT derived truth. To be re-grounded from real published posts once
  the edit-log (Loop 1) accumulates data.
---

# Voice Stats — Measurable Targets (Markos)

> **What this is.** A small set of measurable voice properties where Markos tends to diverge from
> generic AI output. Use it as a drift check: *has this draft flattened toward generic AI shape?*
>
> **What this is NOT — read this first.** This is a **directional prior, not derived truth.** The
> numbers were computed from a thin, partly self-authored corpus (see Provenance) — treat them as
> "roughly where his voice sits," not as measured fact. It is **not the voice source**: the curated
> chunks (`voice.md`, `opinions.md`, `stories.md`, `guardrails.md`) define the voice; this only
> flags drift. **Hitting every number while saying nothing only Markos would say is a fail** — the
> substitution test (`craft/antipatterns.md`) is the real bar. Stats never override the pillars or
> the guardrails.
>
> **Provenance (and its limits).** Computed 2026-06-08 by `scripts/voice-stats/voice_stats.py` (the
> shared meter, reused not forked) over Markos's verbatim voice-session speech (1,339 w) and his
> curated written renderings (554 w). Method + caveats: `_research/2026-06-08-voice-stats/`.
> **Two honesty notes the 2026-06-08 audit surfaced:**
> 1. The "written renderings" file is the voice system's *own* after-examples, so any number derived
>    only from it (notably em-dash rate) is **circular** — it measures what we wrote, not what Markos
>    published. Those are dropped as numbers below.
> 2. The earlier "×generic-AI" multipliers compared Markos to a **self-authored strawman baseline**
>    (`generic-baseline.md`) written to lose — so they're retired. What survives independently: the
>    parent A/B ([[RESULTS]]) reproduced the baseline's *specificity* (31.6) using the real
>    production model with full brand chunks loaded, so the **specificity / numerals / low-hedge
>    gaps are real**; only the exact multipliers were theater.
>
> Bottom line: the absolute rates below are a useful **prior**; re-derive from real posts (Loop 1 /
> `markos-edits-log.md` + provenance-tagged posts) before treating any of them as fact.

## The directional targets

Absolute rates (per 1,000 words unless noted) — a prior for where Markos's written voice tends to
sit. The four where he most separates from generic AI (corroborated by the real-model A/B, not just
the strawman) are marked ★.

| Metric | Markos target (directional prior) | What it governs |
|---|---|---|
| ★ Specificity (proper nouns + numerals /1k) | **≈55–65** | Name things. Bedrock, Qwen, the knowledge graph — not "an AI model." |
| ★ Numerals /1k | **≈12–15** | Numbers anchor every big claim. "$100k", "15:1 services", "20× cheaper", "25 years". |
| ★ Hedges /1k (maybe, might, likely, generally…) | **≤3** | Conviction, not cushions. "I don't think" beats "I think"; drop the epistemic softeners. |
| ★ Sentence-length SD | **≥9** (real long-form) | Jagged rhythm — short landings against long winding builds. Low SD = flattened. |
| First-person share of pronouns | **35–45%** | **The VoM inversion.** Parent Product Voice is "we, never I"; Markos is first-person by design. High "I" is correct here, a violation there. |
| Second-person share of pronouns | **~25%** | Addresses the reader ("if you're building with AI…") without relentless "you". |
| Colons /1k | **~9** | Enumeration-in-prose ("you verify: knowledge graph, embeddings, audit logs"). The colon is on-voice for Markos. |
| Sentence-length mean (words) | **12–14** | Mid-length default, varied hard around it. |
| Preach-phrase rate | **0 — hard gate** | "everyone should / you need to / it's obvious / wake up / companies must" → must be zero. The one true numeric *gate*, not a soft signal (encodes the existing hard ban). |
| Em-dashes | **qualitative — on-voice, see note** | His asides and self-corrections render as em-dashes. Don't sand them off. No numeric target (the measured number was circular). |

### Em-dash note — relaxed on principle, not on measurement

The parent brand-system bans em-dashes; `craft/edit-craft.md` historically inherited that ban for
Markos. **We relax it for his voice — on principle, not on a number.** His voice is built on asides,
nested thoughts, and self-corrections ("Now it exists — and it's the thing that makes the whole
product work"); on the page those *are* em-dashes, so a hard ban flattens his cadence. The earlier
"≈25/1k" figure is **dropped** — it came only from the system's own after-examples (circular), and
the raw transcript can't show em-dashes at all (Fireflies renders pauses as commas). So:

**Rule:** em-dashes are **on-voice for Markos** — don't strip his asides. There is **no numeric
target** until we can measure his *real published* dash rate (Loop 1). This is a per-voice
qualitative exemption, the same shape the Newsletter satellite uses — not a global ban with a
buried exception, and not a measured rate dressed as evidence.

## How to use at draft time

Lead with the ★ four — the divergences the real-model A/B corroborated:

1. **Be specific** — name the tools, industries, systems. Generic AI stays abstract.
2. **Give numbers** — a Markos draft without one is floating.
3. **Don't hedge** — state it; "I don't think" over "I think".
4. **Vary sentence length hard** — short landings against long builds.

Keep his em-dashes (qualitative). Don't game the numbers — a draft can hit every one and still be
generic; the substitution test and the qualitative review are the real bar. This catches *drift*,
not quality, and never speaks for the pillars.

## How to check after drafting

Run `python3 scripts/voice-stats/voice_stats.py <draft> --json out.json` and compare to the targets;
large misses on the ★ four are the highest-leverage edits. Then `/myvault:voice-eval <draft>
--brand voice-of-markos` — note its **primary** axis is the originality/substitution check, not the
blend-in score. See `craft/edit-craft.md` § Voice-eval gate.

## Per-mode targets (scaffold — mostly pending real data)

The single vector above blends his modes, which is too coarse: his **comment** voice ≠ his
**anchor-post** voice ≠ his **newsjack**. The right structure is per-mode targets — but we honestly
can't fill it from the current thin corpus, so most slots are placeholders. **Do not invent
per-mode numbers.** They fill from `markos-edits-log.md` + provenance-tagged posts (Loop 1), per mode.

| Mode | What we can say now (prior) | Per-mode numeric targets |
|---|---|---|
| **Anchor** | The ★ four apply most cleanly here (long-form, specific, his fullest voice). | *pending real per-mode data* |
| **Newsjack** | Tighter; fewer numerals expected; still no hedging. | *pending real per-mode data* |
| **Build-note** | Short, one story/scene; first-person highest. | *pending real per-mode data* |
| **Comment** | He's the *reader*, not the speaker — lower specificity is fine; the substitution test still governs (a pillar/story when the topic fits). Anchoring is optional (see `craft/comment-craft.md`). | *pending real per-mode data* |

Until those fill, use the single directional vector above as the prior and apply judgement per mode.

## Future instruments (hooks — documented, NOT built)

Two upgrades the 2026-06-08 audit pointed to. Both need data we don't have yet, so they are
**designed, not implemented** — building them now (on thin/absent data) is the exact over-engineering
the audit flagged. Each has an explicit activation threshold:

- **Recognition lineup** (a `/myvault:voice-eval` variant). Instead of "spot the AI," ask **"which of
  these did Markos write?"** with his *real* posts in the lineup — measures *is-it-him*, not just
  *is-it-human* (a far better target). **Activates at ≥10 `provenance: markos-verbatim` (or
  `markos-edited`) posts** — until then there aren't enough real decoys. Hook noted in the
  `/myvault:voice-eval` command.
- **Deterministic style-distance** (a LUAR / STYLEDISTANCE-type content-controlled embedding) as a
  bias-free second opinion to the noisy LLM blind-judge — it survives impersonation and isolates style
  from topic. **Deferred:** needs a real reference corpus (Loop 1 output) **and** a model dependency.
  Do not add the dependency until the corpus exists.

Neither is a backlog promise to build soon — they're hooks so the design is captured and the
thresholds are explicit. The cheap, high-leverage work is Loop 1 (capture real posts/edits); these
become *possible and honest* only after it runs.
