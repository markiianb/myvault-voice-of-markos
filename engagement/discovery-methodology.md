---
type: playbook
status: draft
owner: mark
created: 2026-05-11
updated: 2026-05-11
tags: [linkedin, engagement, voice-of-markos, methodology, playbook, q2-2026]
summary: "How the May 2026 LinkedIn target-account list was built, what tools to use (and avoid) to extend it, and the TOS-safe engagement workflow for Markos's personal + MyVault company page commenting."
---

# Discovery Methodology — LinkedIn Target Accounts for Voice of Markos

> **Companion doc:** [[target-accounts-v1]] — the 50-person v1 list this playbook describes how to build and extend.
>
> **Status:** v1 May 2026. Refresh after Q2 retrospective ([[70-Reviews/Plans/2026-Q2-Plan]]).

---

## Why this exists

The [[target-accounts-v1]] list will go stale. People stop posting. New voices emerge. We will want to find another 50 — or 100, or a fresh 50 for a different segment (B2B2C advisors, enterprise privacy decision-makers, etc.).

This doc captures how the v1 list was built so:

1. **The work is reproducible** — Sead or a new teammate can run it cold.
2. **The tool calls and trade-offs are explicit** — we don't relitigate "should we buy Phantombuster" every quarter.
3. **The TOS landmines are mapped** — Markos's personal account is a load-bearing distribution asset; one Tier-3 ban destroys the playbook entirely.

---

## TL;DR

1. **Sales Navigator Core ($100/mo)** is the single best investment in this playbook. Use it.
2. **Phantombuster and the dripify/expandi/waalaxy class of cloud-based LinkedIn automation tools** are off-limits. Documented 31% restriction rate in 2025. Will not be used on Markos's account or the company page.
3. **The proposed workflow** (Sead drafts in voice → Markos reviews → Markos posts manually) is fully TOS-safe. No part of drafting with AI and posting manually violates LinkedIn's terms.
4. **Monitoring is the hardest problem.** LinkedIn has no native "alert me when this person posts." Solve with manual weekly scan + Taplio Engage Lists on the company page (only after confirming Taplio's post-April-2025 authentication is OAuth-based).
5. **Discovery is multi-source.** No single tool finds the right 50. The sequence is: conference speaker lists → Sales Nav posted-recently filter → LinkedIn Top Voices lists → podcast guest mining → X cross-mapping → manual verification. Free sources do 70% of the work.

---

## 1. Discovery Sources — strengths / weaknesses / cost / yield

For each source: what it is, current pricing, when to use, when to skip.

### 1.1 LinkedIn native search + filters (FREE)

**What it is:** Standard LinkedIn search across People and Posts.

**Strengths for this task:** Good for one-shot lookups by name or keyword. The Posts tab surfaces recent content in a topic — searching "AI privacy" or "personal data" finds actively-talking voices. People results bias toward your network (1st/2nd), creating warm-path discovery.

**Weaknesses:** Heavy rate limits for free accounts (80–100 profile views/day before restrictions). No "recently active" filter. No bulk list export.

**Recommendation:** **Use for initial orientation.** Find 5–10 anchor accounts. Not sufficient for systematic 50-account building.

### 1.2 LinkedIn Sales Navigator (Core $99.99/mo monthly, ~$80/mo annual)

**Pricing (2026):**
- Core: $99.99/mo or $959.88/year
- Advanced: $179.99/mo ($135/mo annual)
- Advanced Plus: enterprise

**The filter that matters:** **"Posted on LinkedIn in the past 30 days"** (Spotlight filter). Improves engagement response rates 40–60% by narrowing to actually-active people. Combined with Seniority Level (CXO/Owner/Partner) + Industry (Software, AI, Financial Services) + Keywords (founder, privacy, AI, fintech), produces a clean list of LinkedIn-active executives.

**For mega-influencers:** Mega-names (Altman, Huang, Benioff) appear but often post infrequently on LinkedIn vs X. Sales Nav better surfaces the *tier below* — the 50K–500K follower founders who are genuinely LinkedIn-native. **This is the right target** — mega-accounts have low comment engagement per follower; mid-tier accounts have higher relative engagement and smaller comment communities where a strong reply gets noticed.

**Recommendation:** **Use. Core plan sufficient.** Advanced adds TeamLink and CRM sync — unnecessary for a 2-person workflow.

### 1.3 Phantombuster (~$56–$352/mo)

**Status 2025/2026:** **Off-limits.** April 2025 LinkedIn crackdown hit Phantombuster users. Cookie-based auth is specifically flagged by LinkedIn's detection layer. Cloud IP ranges are known. Cited 31% restriction risk for cloud-based tools (vs 8% for browser-native). HeyReach API access was revoked Feb 2025 — LinkedIn is going after data-extraction at the API-partner level too.

**TOS:** Explicitly prohibited. Not a gray area.

**Recommendation:** **Do not use on Markos's personal account. Period.** The distribution strategy depends on his account being healthy. A Tier 2 restriction (3–14 day lockout) or Tier 3 ban destroys the comment-section playbook. Also do not use on the company page — losing the company-page outbound capability is also bad.

### 1.4 Clay.com ($0 / $185 / $495 per month, post Mar 2026 update)

**What it is:** Data enrichment and workflow orchestration. NOT a discovery tool — it enriches a list you bring. Imports LinkedIn URLs or names, calls 50+ data providers in a "waterfall" to fill in job titles, emails, recent posts, company info.

**For this task:** Strong at the *enrichment* stage, not discovery. Workflow: (1) take 50-account list from Sales Nav, (2) pull each person's recent posts via Clay's LinkedIn waterfall, (3) auto-generate a hook/first-comment draft with Claygent (their AI agent), (4) output to Sheet/Notion.

**Recommendation:** **Situational.** Useful if running this workflow repeatedly at scale. Overkill for one-time 50-account build. $185/mo Launch plan is entry tier.

### 1.5 Apollo.io ($59–$99/user/mo)

**What it is:** B2B contact database (275M+ contacts) + sales engagement.

**2025 event:** Apollo's LinkedIn company page was removed in early 2025 due to data policy violations. Ongoing friction with LinkedIn.

**For this task:** Useful for *confirming* someone matches expected professional profile + retrieving emails if outreach escalates beyond LinkedIn comments. Apollo's own filters are SDR-built (industry + title + company size) — useful for finding *companies* in fintech/AI, then manually checking LinkedIn activity of founders.

**Not good for:** Finding LinkedIn-active creators. No "posted recently" equivalent.

**Recommendation:** **Situational.** Use for confirmation and email enrichment only.

### 1.6 Hunter.io ($49/mo Starter; free tier 25 searches/mo)

**Recommendation:** **Use only if outreach escalates to email.** Verification tool, not discovery.

### 1.7 X → LinkedIn cross-mapping (FREE, manual)

**Why it works:** Many tech-CEO and founder types are more active on X than LinkedIn, but also maintain LinkedIn. X's search is more open — find debates on AI privacy, fintech regulation, data ownership without Sales Nav. Cross-reference to LinkedIn.

**Execution:** Search X for "personal data AI", "digital privacy founder", "data ownership" with `filter:verified` or `sort:top`. Note handles. Search each name on LinkedIn. Check profile for recent posts manually.

**Limitations:** Time-intensive (3–4 hours for 50). No automation. X search quality variable post-2023 API restrictions.

**Recommendation:** **Use for anchor-account seeding.** Excellent for 10–15 high-quality seeds. Not for bulk.

### 1.8 Substack Discover + Substack Notes (FREE)

**Yield for this audience:** Good for journalist + newsletter-writer voices, mid-tier. Less good for pure CEO/operator profiles.

**Recommendation:** **Supplementary.** Particularly strong for the journalist + newsletter creator slice.

### 1.9 Podcast guest mining — Listen Notes, Podchaser, podscan.fm (FREE / $99/mo Pro)

**Why it works:** Podcast guests are comfortable with public discourse and tend to be LinkedIn-active. A CEO on a16z Future, 20VC, or Lex Fridman is almost certainly LinkedIn-present. High-quality targets with confirmed willingness to engage publicly.

**Execution:** On Listen Notes, search "personal data AI" or "digital privacy vault". Grab 20–30 guest names. Cross-map to LinkedIn. Filter by "posted recently" check (manual).

**Recommendation:** **Use.** One of the highest-yield discovery paths for this audience. Listen Notes free tier sufficient for initial exploration; Podchaser Pro ($99/mo) adds guest-specific search if going deeper.

### 1.10 Crunchbase Pro ($99/mo, $588/year)

**For this task:** Excellent for finding *founders of AI/fintech/privacy companies* funded in last 1–3 years. Filter: Industry (Privacy Technology, Personal Finance Technology, AI), Funding Stage (Seed–Series B), Founded Date (2020–2024), Location (US/EU). Each company links to founder LinkedIn profiles.

**Key limitation:** Tells you *who founded a company*, not who is LinkedIn-active. A funded fintech founder may not post at all. Cross-reference manually or via Sales Nav's "posted recently" filter.

**Recommendation:** **Situational.** Useful for the CEO/founder segment specifically. Skip for creator/journalist/podcaster discovery.

### 1.11 LinkedIn Top Voices lists + Creator badge (FREE)

**What's available:** Engati's "40 LinkedIn Top Voices in Tech 2025", Ordinal's "30 Influential AI Leaders on LinkedIn 2025", Contentworks' "Fintech Influencers to Follow on LinkedIn in 2025" — all publicly available. LinkedIn itself publishes Top Voices lists annually.

**Creator badge filter:** **LinkedIn search does not allow filtering by Creator badge.** Sales Nav doesn't expose Creator as a filter either. The badge shows on profiles for manual inspection only.

**Recommendation:** **Use as a starting point.** These lists give the top tier quickly. Mega-influencer bias means higher comment-section competition — use as anchors from which to discover adjacent mid-tier voices.

### 1.12 Conference speaker lists (FREE)

**Relevant for this audience:** Web Summit, SaaStr Annual + SaaStr AI Summit, AI Engineer Summit, World Summit AI, Money 20/20, TechCrunch Disrupt, Sifted Summit.

**Why it works:** Conference speakers are paid/selected to speak publicly — comfortable with positioning, almost universally LinkedIn-active during/after conference season.

**Recommendation:** **Use. One of the highest-quality discovery paths for CEO/founder/executive segment.** Completely free. Time engagement to conference season when speakers are in "sharing my talk" posting mode (high-activity window).

### 1.13 Newsletter directory mining — beehiiv Discover, Substack Discover, Refind

**Recommendation:** **Supplementary.** Good for journalist/writer voices who are LinkedIn-active. Use to diversify beyond pure founder/executive profiles.

### 1.14 AI tools for discovery (Perplexity / ChatGPT / Claude)

**What they can do:** Asking "find me 20 fintech CEOs who post regularly on LinkedIn" produces a plausible-sounding list. **In 2025/2026, all three major AI assistants hallucinate LinkedIn activity data** — they can name real people but cannot verify recency of posting or engagement rates. Knowledge cutoff is especially acute.

**What they're actually good for:** Seeding anchor lists with well-known names you then verify manually. Better-constrained queries ("which CEOs spoke at [conference] about AI privacy") produce more reliable results.

**Recommendation:** **Use for seed-list generation, never as verification source.** Treat AI lists as hypotheses to confirm in Sales Nav or manual inspection. **This is exactly how the v1 list was built — agents seeded, manual cross-source verification confirmed.**

### 1.15 Taplio, AuthoredUp, Shield

| Tool | Price | What it does | Safe? |
|---|---|---|---|
| **Taplio** | $39–199/mo | Engage Lists (target-account post monitoring); content creation; analytics | **Risk-qualified.** April 2025 enforcement event: LinkedIn blocked Taplio's cookie auth, Taplio's own company page was restricted. Status post-April 2025 unclear — verify current auth method before activating on Markos's personal account. |
| **AuthoredUp** | $15–20/mo | LinkedIn editor enhancement, formatting | **Fully safe.** Browser extension that only enhances the LinkedIn editor. |
| **Shield** | $12–24/mo | Analytics on your *own* LinkedIn performance | **Fully safe.** Read-only on your account. |

**Recommendation:**
- AuthoredUp and Shield: **safe to activate immediately** on Markos's account.
- Taplio Engage Lists: **most useful target-monitoring feature available**. Test on the company page first. Only activate on Markos's personal account after confirming current authentication is OAuth-compliant.

### 1.16 Engagement-graph / pod tools

**Lempod:** Shut down. Removed from Chrome Web Store.

**Current alternatives (Podawaa, HyperClapper, LinkBoost, LinkHub):** Same TOS-gray zone as Lempod. LinkedIn's Professional Community Policies explicitly prohibit pod activity — accounts face shadow bans and reduced reach.

**Recommendation:** **Do not use.** Both TOS-risky and **off-strategy** — pod-generated engagement contradicts MyVault's brand positioning around authenticity. The whole point of Markos commenting is to demonstrate genuine expertise.

---

## 2. Playbook — finding 50 more accounts in segment X

### Step 1: Define the segment (1 line + anchors)

Write one sentence: who you're targeting and why their audience matters for MyVault.

Example definitions:

- **A. AI/Privacy Founders.** CEOs/founders of AI-native companies touching personal data. LinkedIn-active, 10K–200K followers. Anchors: pull current Top Voices lists for AI + fintech.
- **B. Fintech Thought Leaders.** Senior figures at banks/neobanks/fintechs with personal LinkedIn voice. Anchors: Chris Skinner, Theodora Lau.
- **C. Business/Tech Podcasters/Journalists.** Top-50 tech or business podcast hosts who post on LinkedIn. Anchors: Listen Notes top shows.
- **D. LinkedIn-Native Business Creators.** 50K–500K-follower daily posters on business/productivity/leadership/wealth. Anchors: LinkedIn Top Voices 2024/2025.

### Step 2: 5 anchor accounts you already know

Before opening any tool, write 5 names you know are LinkedIn-active in the segment. These are seed nodes. (For A: search X for "AI personal data CEO", surface 5 names, confirm LinkedIn-active.) These 5 drive Steps 3–4.

### Step 3: Discovery sequence (run in order — each layer adds names not surfaced by previous)

**Layer 1 — Conference speaker lists (free, 30 min).** Pull speaker pages for the 2–3 most relevant recent conferences. Paste names into a working spreadsheet. Expect 50–100 raw candidates.

**Layer 2 — Sales Nav "posted recently" filter (Core plan, ~45 min).** Lead search → Seniority CXO + Owner/Partner → Industry per segment → Keywords per segment → Spotlight "Posted on LinkedIn in past 30 days" ON. Export to CSV. Expect 200–500 results for broad segments.

**Layer 3 — LinkedIn Top Voices lists (free, 20 min).** Google "LinkedIn Top Voices AI 2025", "LinkedIn Top Voices Fintech 2025". Add names to candidate spreadsheet.

**Layer 4 — Podcast guest mining (Listen Notes free, 30 min).** Search segment keyword. Filter by episode date last 12 months. Pull guest names from top 20–30 episodes. Cross-map to LinkedIn manually.

**Layer 5 — X cross-mapping (free, 30–60 min manual).** Search X for segment keywords with `sort:top`. Identify 10–15 active voices. Search each on LinkedIn.

**Layer 6 — Substack/beehiiv Discover (free, 20 min, journalist/writer segment).** Browse by category. Pull newsletter writer names.

**Surfacing LinkedIn-active vs platform-dormant:** Cannot fully automate. Sales Nav's "posted recently" filter + manual 10-second profile scroll is the most efficient.

### Step 4: Verification (right person / recently active / audience fit)

For each candidate, answer three questions:

1. **Right person?** Current title, current company, profile photo match.
2. **Recently active?** Posts in last 30 days? Generating 50+ comments?
3. **Audience fit?** Scan last 3 posts. Are their commenters professionals/tech-adjacent/high earners? Or just bots and motivational quotes?

### Step 5: Enrichment

For each verified account (after reducing to 60–80 before cutting to 50):

- **Recent post snapshot.** First line of their most engaging recent post by comment count → hook for Markos's first comment.
- **Engagement rate estimate.** Comments / Followers × 100. Target >0.1%. A 100K-follower account with 200 comments/post (0.2%) > 500K-follower with 100 comments/post (0.02%).
- **Topic-fit score (1–3).** 3 = AI/privacy/personal data/wealth/digital life directly. 2 = tech/business with occasional overlap. 1 = leadership/motivation with rare overlap.
- **Email (optional).** Hunter.io / Apollo if email outreach is also planned.

### Step 6: Prioritisation

```
Priority Score = (Comment Engagement Rate × 10) + (Topic-Fit Score × 3) + (Follower Tier Score)
```

**Follower Tier Score** (inverse — smaller comment communities reward strong replies more):

- 50K–200K = 3 points
- 200K–500K = 2 points
- 500K+ = 1 point
- <50K = 1 point

**Replyability gate (qualitative).** Confirm the person's post style invites replies — they ask questions, share opinions that create disagreement, post personal takes (not press releases). Skip pure-corporate-announcement posters.

Rank by score. Cut to 50. Bottom 10 = bench.

### Step 7: Loading into engagement workflow

**Recommended system:** Notion database (free tier sufficient). MyVault is otherwise a Markdown/Obsidian shop, but Notion is the best option for a shared live view Sead and Markos both update during draft → review → post cycles. Alternative: an Obsidian Base (.base file) inside this engagement folder works for solo-Sead workflow if Markos approves via review docs.

**Recommended schema:**

| Field | Type | Notes |
|---|---|---|
| Account Name | Title | LinkedIn display name |
| LinkedIn URL | URL | Direct link |
| Segment | Select | A/B/C/D/etc |
| Follower Count | Number | Approximate; refresh quarterly |
| Avg Comments/Post | Number | From last 5 posts |
| Topic-Fit Score | Select | 1/2/3 |
| Priority Score | Number | Per Step 6 formula |
| Last Post Date | Date | Updated weekly by Sead |
| Last Post Topic | Text | One-line summary |
| Last Comment by Markos | Date | When last engaged |
| Comment Draft | Text | Sead's draft for review |
| Status | Select | Queue / Drafting / Reviewed / Posted / Cooling Off |
| Notes | Text | Context, history |

**Cooling Off rule:** After Markos comments on an account, set a 7–14 day cooling-off before commenting on the same account again. Over-commenting on one creator looks spammy.

---

## 3. Engagement workflow + automation risk assessment

### 3.1 LinkedIn enforcement reality (2024–2026)

LinkedIn's enforcement escalated sharply in 2024–2025. Known facts:

- **April 2025 crackdown.** Coordinated enforcement action — LinkedIn blocked several major automation tools, restricted accounts connected to them. Taplio's company page was restricted during this period.
- **HeyReach API revocation (Feb 2025).** LinkedIn revoked HeyReach's partner API access. Enforcement at the API-partner level, not just individual accounts.
- **Restriction tiers:**
  - **Tier 1:** Temporary feature disable, 1–24 hrs. Trigger: sudden activity spike.
  - **Tier 2:** Account lockout 3–14 days, requires ID verification. Trigger: detected automation patterns, IP changes, cookie-tool use.
  - **Tier 3:** Permanent ban. <15% recovery rate via appeals. Trigger: repeated violations, severe scraping, ToS violations at scale.
- **Detection methods.** Machine learning on behavioural patterns (action timing, scroll behaviour, keystroke cadence). IP consistency checks (cloud-tool data-center IPs don't match residential patterns). Extension fingerprinting. Cookie-auth flagging.

### 3.2 What does NOT trigger restrictions (documented safe behaviours)

- Posting manually from LinkedIn web or native mobile app
- LinkedIn's native scheduler (built-in)
- Commenting manually (any volume — LinkedIn does not rate-limit manual human commenting)
- Viewing profiles manually (up to ~100/day free, ~500/day Sales Nav)
- Using AI to draft content a human then posts manually

**The Sead-drafts → Markos-reviews → Markos-posts-manually workflow is fully safe.** LinkedIn cannot detect how content was drafted; only how it was posted.

### 3.3 TOS-safe automations

- **Scheduling** — LinkedIn native scheduler (zero risk); Buffer ($6/mo/channel, official API partner); Hootsuite (official partner).
- **Draft generation** — Any AI tool. Zero TOS risk.

### 3.4 Monitoring — the hard problem

LinkedIn has **no native "alert me when [person] posts."** This is a real gap. Options:

1. **Manual weekly scan (fully safe).** Sead maintains the 50-account Notion DB. Once per week, visits each profile, updates Last Post Date + Topic fields. ~45–60 min/week for 50 accounts.

2. **Taplio Engage Lists (risk-qualified).** Most useful target-monitoring feature available. April 2025 enforcement around their cookie auth is documented risk. If they migrated to OAuth post-April 2025, risk drops significantly. **Verify current auth method before activating on Markos's personal account.** Test on company page first.

3. **RSS.app LinkedIn feeds (gray area).** Effectiveness unreliable — LinkedIn fights scrapers. Workarounds break without notice. **Not recommended on Markos's account.**

4. **Google Alerts `[Name] site:linkedin.com`.** Often doesn't work — LinkedIn blocks Google crawling of most profile content. Low reliability.

5. **Brand24 / social listening.** Tracks public mentions for keywords ("MyVault"). Doesn't do per-profile post monitoring. **Useful for brand mentions, not for target-account monitoring.**

**Practical recommendation:** Manual weekly scan + Taplio Engage Lists as secondary dashboard on company page. Once Taplio's current auth is confirmed OAuth-compliant, consider activating on Markos's personal account at lowest plan tier.

### 3.5 TOS-risky automations — risk assessment

| Tool | Risk | Mechanism | Real-world consequence |
|---|---|---|---|
| Phantombuster | HIGH | Cloud, cookie auth | 31% restriction rate; April 2025 crackdown confirmed |
| Dripify | HIGH | Cookie, cloud proxy | Extension fingerprinting detected |
| Expandi | HIGH | Cloud | Flagged by multiple enforcement reports |
| Waalaxy | HIGH | Cloud | Same architecture as Expandi/Dripify |
| We-Connect | MEDIUM-HIGH | Cloud | Less documented but same class |
| MeetAlfred | MEDIUM | Browser-extension hybrid | Lower cloud exposure, still TOS violation |
| LinkedIn Helper | MEDIUM | Browser-based | Claims safer detection evasion; still ToS-prohibited |
| Taplio (automation features) | MEDIUM | Cookie auth pre-April 2025 | Company page restricted April 2025 |
| Dux-Soup | MEDIUM | Browser extension | Claims no known bans in 300K+ users since 2021; still ToS-prohibited |
| Engagement pods (Podawaa, HyperClapper) | MEDIUM | Artificial engagement | Shadow banning documented; off-strategy |

### 3.6 LinkedIn API access (2025/2026)

**Marketing Developer Platform (MDP).** Two tiers — Development (up to 5 ad accounts, POST operations) and Standard (production). Requires application + approval. Endpoints cover ad campaign management, lead gen forms, analytics. **Not content monitoring or profile scraping.**

**What the API does NOT allow:** Individual member posts without explicit OAuth authorisation; profile scraping; monitoring third-party account activity. Connections API largely locked down since 2015.

**Practical conclusion:** LinkedIn's API is useful for ad operations and managing your own page. Not a path to monitoring target accounts or automating content interactions. Any tool claiming "the LinkedIn API" for competitor monitoring is using a deprecated endpoint or operating outside permitted use.

### 3.7 Recommendation for MyVault's stage

MyVault is early-stage, brand-sensitive, with a CEO whose LinkedIn is a core distribution asset. The calculus is clear:

✅ **Workflow architecture is right.** Sead drafts → Markos reviews → Markos posts manually. Fully TOS-safe. No part violates LinkedIn's terms.

✅ **Use Sales Navigator Core ($100/mo).** LinkedIn's own product. Zero TOS risk. Single best investment in this playbook.

✅ **Use Buffer or LinkedIn native scheduler** for company page posts. Official partners. Avoid third-party schedulers that require LinkedIn login credentials.

✅ **AuthoredUp + Shield** safe to activate on Markos's account immediately.

⚠️ **Taplio Engage Lists** — evaluate. Activate on company page first as lower-risk test. If post-April-2025 auth is OAuth-compliant, consider activating on Markos's personal account at lowest tier. Don't activate without confirming auth method.

🚫 **Do not touch Phantombuster, Dripify, Expandi, Waalaxy, engagement pods** on either Markos's personal account or the company page. The risk of Tier 2–3 restriction is real, documented, existential for the playbook. Explicit ToS violation territory, not gray area.

✅ **Company-page commenting (12+/mo per [[70-Reviews/Plans/2026-05-Plan]]).** Manual commenting on public posts has no documented rate limit. Safe.

---

## 4. How the v1 list was built (for retrospective)

The [[target-accounts-v1]] list was built using:

- **9 parallel research sub-agents.** Each owned a slice (AI/privacy, digital legacy, consumer-trust founders, fintech CEOs, journalists/podcasters, LinkedIn top voices, community builders, plus methodology) and over-recruited 12+ candidates per slice.
- **Hard URL-verification rule.** No URL constructed from a name. Each candidate's LinkedIn URL had to appear in ≥2 public sources (search snippets, articles, podcast bios, personal websites) before inclusion.
- **2025/2026 activity check.** Each candidate had to have evidence of public activity in 2025 or 2026 (podcast appearance, conference, article byline, post mention).
- **Namesake disambiguation.** When multiple LinkedIn profiles exist for similar names, the active profile was confirmed by cross-checking topic/affiliation against the person's public bio.
- **Competitor exclusion.** Direct-overlap products (AI personal knowledge vault / second brain / personal data wallet / AI life-OS / digital-vault probate tools) were stripped at agent level and confirmed at compile.
- **Mid-task scope pivot.** Initial brief was tightly Sarah-anchored (UK family manager, AI privacy, family preparedness). Mid-task Mark clarified: go broad — tech/AI/fintech CEOs, famous LinkedIn voices, mega-creators welcome. The 5 narrow agents kept their best picks; 5 broader-scope agents added tech/AI/CEO breadth. The final 50 mixes both bands.

**What worked best for this audience:**
1. AI-agent seeding + manual cross-source verification of LinkedIn URLs — fastest path to a 50-name pool, but verification is everything.
2. LinkedIn Top Voices lists (already exist publicly, free, high-signal).
3. Cross-referencing podcast guests + journalists to LinkedIn (Kashmir Hill, Madhumita Murgia, Casey Newton, Parmy Olson — all surfaced quickly because they post their pieces with framing to LinkedIn).
4. Conference speaker lists (not heavily used in v1 build but called out as best free path for v2).

**What didn't work / didn't get tried:**
1. **No Sales Navigator access** during v1 build. Almost certainly the biggest gap — would have surfaced LinkedIn-active executives Sales Nav can find that web search can't.
2. **No Clay enrichment.** Done at the next stage if v1 succeeds.
3. **No live "posted in last 30 days" verification** per account at agent level. The brief required ≥30/50 posted in last 30 days; the agents confirmed 2025/2026 activity but most evidence was from the last 60 days, not strictly the last 30. **Action item:** before W1 engagement, Sead spends 30 minutes manually clicking through the 50 to confirm last-30-days posts. Any failing the check moves to bench; bench promotes up.

---

## 5. Repeatable playbook — for v2 build

Once we want another 50 (or a v2 for a new segment), Sead runs:

1. **30 min — define segment + 5 anchors** (Step 1–2 above).
2. **30 min — pull conference speaker lists** for 2–3 relevant conferences in segment.
3. **45 min — Sales Nav "posted recently" filter** with segment-specific filters. Export CSV.
4. **20 min — pull LinkedIn Top Voices lists** for segment.
5. **30 min — podcast guest mining** on Listen Notes.
6. **30–60 min — X cross-mapping** for the segment.
7. **2–3 hours — manual verification** (Step 4 above) on the consolidated ~150-candidate list. Reduce to 60–80.
8. **1–2 hours — enrichment** (recent post, engagement rate, topic-fit score). Reduce to 50.
9. **30 min — prioritisation + loading** to Notion DB.

**Total: 8–10 hours of Sead's time for a fresh 50.** Most of that is manual verification — there is no clean shortcut.

---

## 6. Open questions / decisions to revisit

- **Sales Navigator subscription.** Approve $100/mo before next list build? Strongly recommended.
- **Taplio Engage Lists on the company page.** Test in W2/W3 May after confirming current auth method. If safe, this is the single highest-leverage tool for monitoring 50 targets.
- **Notion vs Obsidian Base for the DB.** Notion recommended for shared editability. If Markos prefers all data in vault, an Obsidian Base in this engagement folder works for solo Sead operation.
- **First-hour engagement on Markos's own posts.** The May plan calls for "team first-hour engagement on every Markos post" — coordinating that across Sead/Mark/team needs its own micro-playbook. **Out of scope of this doc; flag for a separate one.**
- **Company-page engagement targets.** This doc covers Markos's personal-account targets. The May plan calls for 12+/mo outbound comments from the MyVault company page as well — those targets may overlap with this 50 but may also need their own narrower list (industry posts, partner accounts). **Flag for a v1 company-page target list.**

---

## Changelog

| Date | Change | By |
|---|---|---|
| 2026-05-11 | v1 playbook. Written from methodology research agent + integration with v1 target-accounts list. | Mark / Claude |
