---
chunk_id: "edit-craft"
domain: "craft"
category: "craft"
subcategory: "editing"
context_tags:
  - "editing-workflow"
  - "anti-ai-slop"
  - "self-audit"
  - "flattening-tests"
  - "review"
depends_on:
  - "voice"
  - "antipatterns"
token_count: ~900
version: "1.0"
last_updated: "2026-04-15"
status: "active"
summary: >-
  Edit workflow for Markos drafts. Pass 0 preservation scan + six critique passes.
  Two-Pass Self-Audit, Markos-specific flattening tests, Conversation Test, pre-write
  and self-review checklists. The anti-AI editor. Adapted from parent brand-system
  editing-process.md.
---

# Markos — Edit Craft

The editing discipline for any draft that goes near his account. Mirrors the parent brand-system's editing process, tightened for Markos. Load this after a draft exists — use it to catch what the writer missed.

The goal is not polish. Markos has rough edges; keep them. The goal is **to catch the places where an AI wrote for him instead of as him.**

Pass 0 identifies what to preserve. Passes 1–6 identify what to change.

---

## The Edit Workflow (run in order)

### Pass 0 — Preservation scan

Run this before critique. Read the draft once. Write down 3–5 things that are working, each with its *mechanism*.

- Not "the opening is strong" — "the opening anchors urgency in two specific events with dates; that's why it lands."
- Not "good line" — "this line is earned because the parallelism is backed by specificity in both halves."

Mark every preserved element as **do not edit** for Passes 1–6. Subsequent passes rewrite *around* preserved content, never through it.

**Why:** Markos reviews this way. He names what's working before naming what to change. Without this pass, editors over-correct and cut the parts carrying the piece. It also changes the review's register from audit to editorial partnership.

### Pass 1 — Structure

Does the post go **diagnosis → evidence → lesson**, in that order?

- ❌ If the lesson arrives before the evidence → Lecture Hall drift. Rewrite to scene-first.
- ❌ If there's no scene / number / named tool anchoring the claim → add one or cut the claim.
- ❌ If the close restates the thesis → cut the close; end on an implication instead.

### Pass 2 — Mode

Is this clearly **Explain / Challenge-from-evidence / Educate**? Any drift toward **Preach**?

Preach tells to check for:
- "everyone should" / "you need to" / "it's obvious" / "people don't realise" / "wake up" / "companies must"
- Exclamation marks in posts
- Binary right-wrong declaratives
- Moral urgency about a commercial issue

If any tell → replace the instruction with an observation. Replace moral urgency with pragmatic consequence.

### Pass 3 — Voice Qualities

Run the draft against the four qualities from `voice/voice.md`:

- **Systems-thinker, not hype-pundit?** Are Bedrock / Qwen / knowledge graph / specific tools named? If the draft talks about "AI" without specificity, tighten.
- **Evidence-led, not opinion-led?** Is the opinion the landing, not the takeoff?
- **Diagnostic, not prescriptive?** Does it show, or does it tell?
- **Warm expertise, not cold authority?** Does it sound lived, or résumé-read?

### Pass 4 — Failure Portrait Scan

Run against all five failure portraits from `craft/antipatterns.md`. Flag every instance:

1. **Agency Wearing His Face** — pseudo-profound two-liners, rhythmic parallelism, manufactured punchlines, over-polished list dumps, sanitised openers, tagline closes.
2. **Preacher** — see Pass 2.
3. **Lecture Hall** — see Pass 1.
4. **LinkedIn Lottery** — CTA close, hashtag wall, emoji string, symmetric 3-bullet list, formulaic opener ("For anyone building in 2026…").
5. **Hot Take Machine** — binary declaratives, two-sentence hot takes, named-competitor pin, anything misinterpretable in 2 sentences.

For each hit, apply the "after" rewrite pattern from the casebook.

### Pass 5 — Mechanical / Word-level

- Parent banned words: leverage, utilize, seamless, revolutionary, cutting-edge, robust, scalable, ecosystem, journey, magic. **Cut all.**
- Markos's cringe list: circle back, touch base, loop in, synergise, game changer. **Cut all.**
- "Right?" in a post → cut. Max once in a comment.
- "You know" → compress out.
- "Zero-knowledge" → replace with "Zero Trust" (load-bearing correction).
- Straight quotes, not curly. No em-dashes (the parent rule holds for Markos posts too).
- Contractions always: don't, can't, won't — not do not, cannot, will not.
- No hashtag walls (2–3 relevant max, inline).
- No emoji in posts.
- Length within the range for the post type (see `voice/voice.md` § Length).

### Pass 6 — Two-Pass Self-Audit + Read-Aloud

**Two-Pass Self-Audit.** Re-read the draft. Ask: *"What makes this obviously AI-generated?"* Write 3–5 specific tells. Fix them. Repeat. This catches patterns that survive every checklist because checklists never cover everything.

**Read aloud.** If it sounds robotic — every sentence the same length, every transition smooth, every insight landing in the same shape — the AI has flattened his voice. Reintroduce variation:
- Combine two short sentences into one winding one that earns its length.
- Break a long sentence in half where the thought actually turns.
- Add one self-correcting aside if the draft has zero ("I mean — not exactly that — but the pattern around that").
- Let a sentence end on a preposition or a mid-word reconsideration if that's how he'd say it.

Finally, run the **Markos Final Test** from `voice/voice.md`:
1. Would Markos wince reading this with his name attached?
2. Is every big claim anchored by a number, named tool, industry, or date?
3. Is the turn AFTER the evidence?
4. Does it sound like thinking or like a performance?

If any fails, rewrite that specific line — not the whole piece.

---

## Markos-Specific Flattening Tests

AI flattens distinctive rough edges. For Markos, flattening usually shows up as:

**The Uniform Paragraph Shape.** Every paragraph is 2–3 sentences, same rhythm, same landing. Markos's paragraphs range from 1 sentence to 200+ words depending on the thought. If all your paragraphs are the same size, the AI flattened him.

**The Too-Smooth Transition.** "Moreover," "Furthermore," "In addition," "Additionally," "That said," — these connect ideas the AI thinks belong together. Markos connects with "and", "anyway", "look,", "frankly", or just a line break. Cut the formal transitions.

**The Hedged Everything.** Every opinion softened with "might," "perhaps," "some argue." Markos doesn't hedge conviction — "I don't think" is stronger than "I think." If every claim is cushioned, drop half the cushions.

**The Resolved Conclusion.** A conclusion that neatly ties up everything above. Markos often lands on an implication that widens the scope or invites the reader to extend it. Closed-box conclusions are AI tells.

**The Missing "I."** Markos is a first-person voice. If a paragraph reads like it could have come from a company page, rewrite with "I" and a specific experience.

**The Generic Number.** "Many companies," "most orgs," "a lot of people." Real Markos: "The fintechs and the banks." "For every million in license, fifteen million in services." "25 years." Numbers and named groups.

**The Summary That Restates.** Bad close: "So remember: AI is one part of a bigger system." Good close: "If you're building with AI in 2026, this is the conversation to be having." — extends, not restates.

---

## The Conversation Test

Ask: *Is this explaining something to a colleague, or performing to an audience?*

| Performing (rewrite) | Explaining (keep) |
|---|---|
| "In today's rapidly evolving AI landscape, architecture is paramount." | "The model's doing maybe 10% of the work. The rest is the system around it." |
| "Organizations must adopt a Zero Trust posture." | "Zero Trust is a methodology — every layer protects the data. That's the difference." |
| "For anyone building on foundation models in 2026…" | "If you're building with AI this year, the question worth a week of thought is what the system around the model looks like." |

If any paragraph sounds like a TED slide, rewrite it as if he were talking to a peer at a dinner.

---

## The LA Story Test (adapted)

Skim the finished piece quickly. Whatever phrase, sentence, or paragraph jumps out but doesn't actually advance the argument — that's the extra earring. **Cut it.** Markos doesn't decorate; he diagnoses.

---

## The Blurry Eyes Test

If you find your eyes skipping over a sentence while editing, that's a cut candidate. Markos doesn't pad.

---

## Pre-Write Checklist

Before drafting anything from his account:

- [ ] Post type identified (anchor / newsjack / build-note / comment / reply)
- [ ] Mode chosen (Explain / Challenge-from-evidence / Educate — never Preach)
- [ ] Relevant pillar(s) from `opinions/opinions.md` loaded
- [ ] At least one deployable story from `stories/stories.md` identified
- [ ] Red / Yellow Zone flags from `guardrails/guardrails.md` checked
- [ ] For comments: Never Engage list in `guardrails/guardrails.md` verified
- [ ] For anchor posts: target length 250–600 words noted

---

## Self-Review Checklist (run before flagging for Markos)

- [ ] Pass 0 complete — 3–5 preserved elements named with mechanism
- [ ] Preserved elements still intact after Passes 1–6
- [ ] Scene, number, or diagnosis in first line — not a generic opener
- [ ] Every big claim anchored by a number / named tool / named industry / date
- [ ] Diagnosis before prescription throughout
- [ ] No pseudo-profound two-liners ("[X] isn't [Y]. It's [Z].")
- [ ] No rhythmic parallelism ("That's where X. That's where Y.")
- [ ] No manufactured punchlines as standalone paragraphs
- [ ] No signature phrase dropped as a final-line tagline
- [ ] No hashtag wall, no emoji, no CTA close
- [ ] No binary right-wrong declaratives
- [ ] Preach phrases cut ("everyone should / you need to / it's obvious / wake up / companies must")
- [ ] Parent banned words cut (leverage, utilize, seamless, etc.)
- [ ] "Right?" removed from posts (max once in comments)
- [ ] "You know" compressed out
- [ ] Zero Trust, not zero-knowledge
- [ ] Paragraph sizes vary; sentence lengths vary
- [ ] At least one self-correcting aside OR at least one winding sentence that earns its length
- [ ] At least one signature move used (peel-onion / step-through / story→principle / case→pattern / history→present / technical→human / contrast / incentive-callout)
- [ ] Close lands on implication or substance-inviting question — never CTA
- [ ] Read aloud sounds like a practitioner, not an agency
- [ ] Two-Pass Self-Audit run: 3–5 AI tells identified and fixed
- [ ] Markos Final Test passed

If any unchecked box remains, fix before sending.

---

## Working with AI on Markos content

- **Never forward raw AI output to Markos.** Line-by-line review always. Read aloud before sending.
- **Replace every AI-generated example with a real one.** If the draft mentions a number, a company, a scenario — verify it's real, not plausible-sounding. AI invents plausible examples; Markos uses real ones.
- **Watch the flattening effect.** AI smooths distinctive rough edges. Mark a passage as AI-flattened if: uniform paragraph shape, formal transitions, hedged conviction, neat conclusion, missing "I", generic numbers, restating summary close.
- **Own the byline.** If a paragraph doesn't sound like something Markos would say to a peer at dinner, rewrite it.
