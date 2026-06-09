# Improvement-loop — Run 1 (2026-06-09)

First real run of the round-over-round improvement loop (`playbooks/improvement-loop.md`). Seed: the
"Frontier-model commoditization" system-drafted post. Workflow: discrimination test → 3 loop rounds →
synthesis. Run via 19 agents (rounds sequential, 3 measures parallel per round).

> [!warning] The hard limit
> **No real Markos was in this loop.** Every originality / only-Markos / blind-catch judgment came from
> LLM judges grading against the encoded chunks — not from Markos. This run shows the **mechanism
> works** and surfaces **candidate** fixes. It does **not** validate the system. Real validation waits
> for Loop 1 (`markos-edits-log.md`) to accrue Markos's own edits. The 5 candidates below are
> **hypotheses for ratification, not settled corrections.**

## 1. Discrimination test — the instrument ranks correctly

On the primary (originality) axis the eval produced the right strict order:

| Item | substitution_pass | only_markos | reading |
|---|---|---|---|
| **Gold** (verbatim Markos) | ✅ true | yes | deploys a pillar + credential + named specifics |
| **System-draft** (frontier post) | ❌ false | no | on-topic but deploys no pillar thesis; borrowed authority (Evans/Huang); "liftable by any founder" |
| **Anti** (strawman) | ❌ false | no | generic-analyst slop, zero specifics, banned opener |

The gap between gold and system-draft is exactly the gap the loop then tried to close.
**Honest caveat:** graded by the same LLM-judge family that runs the loop — confirms the judge is
internally consistent and sensitive to the right signal; does **not** prove it agrees with Markos.

## 2. Round-over-round deltas

**Originality (primary gate):** passed from R1 and held (R2 dipped to `partial`, R3 restored `yes`,
`substitution_pass=true` throughout). The voice was *found* early; the rounds were about removing
machine tells, not finding it.

**Blind-lineup (advisory):** caught the draft at **high confidence in ALL three rounds.** R1/R2 — a
leaked meta-reasoning preamble pasted into the draft body. R3 (preamble gone) — register/cadence:
too-smooth written register, stacked two-beat mic-drops, an aphoristic closer, no spoken
self-correction. **This standing catch is the run's most important honest signal.**

**Voice-stats — did NOT converge** (targets: spec 55–65, numerals 12–15, 1st-person 35–45%, hedges ≤3, SD ≥9):

| Axis | R1 | R2 | R3 | Target | Trend |
|---|---|---|---|---|---|
| specificity/1k | 29.9 | 44.7 | 34.9 | 55–65 | peaked then fell — **never hit** |
| numerals/1k | 9.0 | 11.2 | 11.6 | 12–15 | climbed, just under |
| first-person % | 36.8 | 30.0 | 55.6 | 35–45 | oscillated, **overshot** |
| em-dash/1k | 18.0 | 16.8 | 19.4 | on-voice | fine |
| hedges/1k | 3.0 | 2.8 | 3.9 | ≤3 | **drifted over** |
| sentence SD | 9.2 | 11.3 | 8.9 | ≥9 | **dropped below** at stop |

The loop **stopped on the originality gate (R3, `stop=true`) while human-likeness was still failing by
design** (the blind-lineup is advisory/noisy and does not block). The stats wander — there's no
controller pulling them toward target.

## 3. System-fix candidates → see `_analysis/voice-corrections-log.md` (UNRATIFIED)

Five surfaced; the two sharpest: (1) the generator leaked its own working-reasoning into the draft
body (R1+R2 — the blind judge's #1 catch); (2) no mechanism injects spoken texture, the residual R3
tell. Full list in the corrections log. **None ratified** — most are generator/system-wiring fixes
(the writer agent, not a VoM chunk), and nothing here is real-Markos-validated.

## 4. The final draft (system-curation, NOT Markos)

The loop's best output — a genuinely Markos-shaped rewrite of the seed (opens on a scene, deploys
Pillar 1 + Pillar 2, the Qwen-at-a-twentieth specific, the Bedrock no-training clause, 25-years
credential, swappable-engine landing). Labelled **system-curation**: it is our best curation, not
Markos. If it ever ships, it logs to the posts log as `provenance: system-draft` (or `markos-edited`
if he revises it).

> A founder showed me his architecture last month. Every call wired to a single frontier lab. No fallback, no second path, nothing underneath if the price moved or the terms changed.
>
> I asked him what happens when it does. He didn't have an answer.
>
> Here's what most people miss. The model is about 10% of the work. The other 90% is the unglamorous part — retrieval, data plumbing, guardrails, the knowledge graph that actually knows your business. The model is a swappable engine. We had Qwen 3 match Claude Opus end-to-end on a multi-file refactor recently. Not thirteen percent cheaper. A twentieth.
>
> So if the engine is swappable, why is everyone betting the company on one supplier?
>
> The banks and payments firms we work with didn't pick Bedrock because it was cheapest — the raw API is cheaper. They picked it for one clause: their data is never trained on. Compliance doesn't care how clever your model is. It cares what happens to the data after the call.
>
> That's the part nobody's selling you, because the platforms with the budget to shape the conversation have no commercial reason to point you at the open-source engine sitting right there. Twenty-five years in enterprise software taught me that being first isn't the same as being right.
>
> Build the 90% so the 10% can be swapped out underneath a loan-underwriting workflow without anyone noticing. That's the architecture that survives the next price move.

## 5. Bottom line

The loop works as an instrument — ranks correctly, converges originality, surfaces real recurring
system gaps. But it stopped on the moat (only-Markos) while human-likeness was caught every round, and
**no real Markos validated any of it.** Ship the 5 fixes to the log as hypotheses; the real next step
is Loop 1 data, not another synthetic loop run.

*Run: workflow `wf_b784c01c-bdd`, 2026-06-09. Reproducible via the script in the session workflow dir.*
