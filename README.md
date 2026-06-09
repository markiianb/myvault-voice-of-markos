# Voice of Markos System

**Version:** 2.7
**Last updated:** 2026-06-09
**Parent brand:** MyVault
**Owner:** Mark Bobyliak (steward) · Markos Symeonides (voice holder)

---

## What this is

The Voice of Markos system is a **satellite brand-system** that governs how we post and engage from Markos Symeonides's personal LinkedIn account. It is derived from the MyVault parent brand-system but adapted for a personal voice — where "I" is allowed, opinions are held, and the register is authority-educator-challenger rather than product-tool.

It follows the same pattern as the Private by Design Newsletter: self-contained chunks, own manifest, own retrieval rules, explicit conflict-resolution with the parent brand.

## What this is NOT

- **Not MyVault company voice.** MyVault company content continues to use the main brand-system with its Product Voice Rule ("MyVault found," never "I found"). Nothing here overrides that for company content.
- **Not a script.** Markos is a real person with real range. These chunks capture his positions, boundaries, and signature patterns — not a template he must robotically follow.
- **Not a substitute for his judgement.** Everything he wouldn't sign off on stays off. When in doubt, escalate.

## The 16 files

| Domain | File | What it covers |
|---|---|---|
| **voice/** | `voice.md` | How Markos sounds — tone, four qualities, three modes + never-preach, five failure portraits, banned words, rhythm, Final Test |
| **voice/** | `voice-stats.md` | PARKED stub — no numeric voice targets yet (no real Markos posts to derive them from). Judge voice qualitatively; the meter stays dormant. |
| **identity/** | `identity.md` | Who Markos is — bio, positioning, authority claim, audience segments, disclosure rules |
| **opinions/** | `opinions.md` | Quick gate table + eight pillar deep-dives with thesis, sound-bites, story refs, red lines |
| **stories/** | `stories.md` | 12 indexed personal stories with pillar tags, Green/Yellow/Red status, caution flags |
| **guardrails/** | `guardrails.md` | Red/Yellow/Green zones, never-engage exclusion list, personal comfort matrix |
| **audience/** | `audience-linkedin.md` | Five audience segments, content matching, what doesn't land |
| **craft/** | `antipatterns.md` | Before/after casebook for the five failure portraits, self-audit, editing tests |
| **craft/** | `post-craft.md` | How posts get built — anchor, newsjack, build-note |
| **craft/** | `comment-craft.md` | Four kudos-first comment frameworks |
| **craft/** | `newsjack-craft.md` | Reacting to AI/privacy news within 24h |
| **craft/** | `edit-craft.md` | Six-pass editing workflow, flattening tests, checklists |
| **playbooks/** | `approval-workflow.md` | Monday rhythm, three-tier approval, trust progression |
| **playbooks/** | `daily-routine.md` | Volume caps, time-of-day rules, posting schedule |
| **playbooks/** | `target-accounts.md` | Six engagement categories, quality markers, review cadence |

## Output logs

Running logs hold every piece of Markos-bylined content:

- `markos-linkedin-posts-log.md` — short-form LinkedIn posts (anchor / newsjack / build-note). Prep + scheduled dates, full body inline, newest at top. Carries a `provenance` tag.
- `markos-linkedin-articles-log.md` — long-form LinkedIn articles. Same structure plus editorial + SEO titles, reading time, pull-quote markers.
- `markos-edits-log.md` — **the keystone:** every `(system-draft → Markos-final)` edit pair. The highest-signal voice data the program produces — the one habit worth keeping. Read periodically to ratify recurring corrections; never loaded during drafting.

These are records, not retrieval chunks. Load them when answering "what has Markos posted lately?" — not when drafting a new post. The chunks to load for drafting are in the table above.

## Inheritance from MyVault parent brand-system

The parent brand-system at `10-Brand/brand-system/` provides the foundational rules that apply to **all** MyVault-adjacent content, including Markos's LinkedIn. These still apply:

- Banned words (leverage, utilize, seamless, revolutionary, cutting-edge, robust, scalable, ecosystem, journey, magic for AI)
- Banned AI-slop constructions (pseudo-profound two-liners, manufactured punchlines, superficial -ing extenders, copula avoidance, significance inflation)
- Confidence over fear — never fear-monger about security
- Two-Pass Self-Audit after drafting ("What makes this obviously AI?")
- The Final Test (trusted friend / builds confidence / explains AI / passes read-aloud)
- Source quality tiers (A/B/C/D) when citing statistics

## Where Voice of Markos overrides the parent

Where the parent brand-system's rules conflict with how Markos actually communicates, Voice of Markos wins **for Markos's LinkedIn content only**. The parent rules remain unchanged for MyVault company content. Overrides:

| Rule | MyVault parent | Voice of Markos |
|------|----------------|-----------------|
| First-person "I" | Never in product voice | Allowed and expected |
| Taking positions | Product stays neutral | Takes clear positions backed by evidence |
| Register | Product-tool register | Authority-educator-challenger register |
| Personal stories | Product voice doesn't have stories | Story library is core content material |
| Sentence length | Short, declarative | Permitted longer rhythmic sentences that mirror his cadence |
| Tone | Warm, calm, confident | Warm + sharp; occasional dry sarcasm about big tech; never preaching |
| Content topics | MyVault-adjacent | Broader — software architecture, AI implementation, open-source, education, accountability |

All other parent-brand rules apply unchanged.

## Token budget

Consolidated files are larger than the old granular chunks. Approximate loads per task:

- **Anchor post:** ~5,000 tokens (voice + antipatterns + identity + guardrails + post-craft), plus opinions and stories if relevant
- **Comment:** ~3,000 tokens (voice + guardrails + comment-craft), plus opinions and target-accounts if relevant
- **Newsjack:** ~5,200 tokens (voice + antipatterns + opinions + guardrails + newsjack-craft)
- **Edit pass:** ~4,200 tokens (voice + antipatterns + edit-craft + guardrails)

See `_retrieval-rules.yaml` for full task profiles with always_load and load_if_relevant lists.

## How to use

See `CLAUDE.md` in this directory for the operator workflow. The Engagement Framework (`../CEO-LinkedIn-Engagement-Framework.md`) is the program-level document for Markos; this directory is the operational system for the team running the program.

## Evolution

This system is expected to evolve. Every piece of feedback from Markos ("I wouldn't say it this way" / "yes, exactly") refines the chunks. Version-bump on meaningful changes. Major revisions happen after monthly voice-check calls.
