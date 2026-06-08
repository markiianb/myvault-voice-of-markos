---
type: log
status: active
owner: Mark Bobyliak
created: 2026-05-28
updated: 2026-05-28
tags:
  - content-log
  - linkedin
  - markos
  - voice-of-markos
summary: Running log of every short-form LinkedIn post published under Markos Symeonides's personal profile. Full post body inline per entry. Most recent at top.
---

# Markos LinkedIn Posts — Running Log

Running log of short-form LinkedIn posts under Markos's personal profile. Each entry holds the full post body alongside its prep + scheduled dates. Newest entries go at the top.

**Brand system:** Voice of Markos satellite — see [[_manifest|VoM manifest]] and [[guide|VoM guide]]. Parent banned-words + AI-slop rules still apply.

**Tier workflow:** Sead runs Tier 1/2/3 (see [[playbooks/approval-workflow]]). Record tier on every entry.

**Sibling log:** Long-form articles in [[markos-linkedin-articles-log]]. Both logs sit in the same `voice-of-markos/` directory.

## How to add an entry

Paste a new block at the very top of the **Entries** section, above the most recent existing entry. Fill all fields. Keep the post body verbatim.

```
## YYYY-MM-DD — [Hook or working title]

- **Prepared:** YYYY-MM-DD
- **Scheduled:** YYYY-MM-DD
- **Status:** draft | scheduled | shipped
- **Tier:** 1 | 2 | 3
- **URL:** (paste LinkedIn URL once live)
- **Visual:** (Figma node / asset path, or "none")

<!-- Full post body, verbatim, including line breaks and hashtags -->

[Post body]

---
```

## Entries

## 2026-06-12 — Google subscription renewal (designed-in friction)

- **Prepared:** 2026-06-05
- **Scheduled:** 2026-06-12 (Fri)
- **Status:** scheduled
- **Tier:** 1
- **URL:** (paste LinkedIn URL once live)
- **Visual:** none

I got an email from Google reminding me that a subscription was coming up for renewal. First time in my life I have ever seen that.

It was a small thing, but it sent me looking for the rest of them. I'll tell you, there were more than I expected, spread across different cards and accounts I have picked up over the years. So I started cancelling. On Google Play you go into every single one on its own, as if each subscription has its own separate billing account. It is monotonous, and after a while you understand why people just let it run and keep paying. I don't have four hours for it either, and the whole thing is a bit of a cluster.

I spent my career building asset management and service management software. The whole job of that software is to tell an organisation what it owns, what it is running, what each thing costs, and when it comes up for renewal. Retail, logistics, banking, utilities, government, every industry has it. And in my own life I cannot tell you what I am subscribed to without hunting through one account at a time.

The friction is designed in, because leaving is made slow and renewing is automatic, and that is where the money sits. I gather there is even a law coming in Europe that says cancelling should take a click or two. When it takes a law to make cancelling easy, you know the difficulty was on purpose.

Which is part of why we are building MyVault. One private place to show me what I pay for, what renews next, and where I am overpaying, without going through six logins to find it.

When did you last get a straight answer to everything you're paying for?

#ConsumerRights #SubscriptionEconomy

**Editor's notes (2026-06-05):** Logged verbatim per Mark — body is Markos's draft, not edited. Replaces the earlier Samsung→wealth-advisory draft. Pillar 4 (Big Tech Accountability) + Pillar 7 (Simplicity) activated; Green Zone. **Open before Markos approves in Planable:** (1) confirm "asset management and service management software" as cleared career framing — consistent with documented ITSM background but not yet verbatim in `identity/identity.md` cleared list; clear it there if approved. (2) Verify the EU "click to cancel" law claim (the famous click-to-cancel rule is the US FTC's; hedged "I gather" keeps it safe).

---

## 2026-06-10 — Frontier-model commoditization (Benedict Evans deck)

- **Prepared:** 2026-06-05
- **Scheduled:** 2026-06-10 (Wed)
- **Status:** scheduled
- **Tier:** 1
- **URL:** (paste LinkedIn URL once live)
- **Visual:** TBD — convergence chart ref (Benedict Evans deck)
- **Source:** https://www.ben-evans.com/presentations

Frontier model prices today reflect a temporary supply and demand condition. Wiring your product to a single frontier lab right now guarantees you pay a premium, and that kind of premium rarely holds for long in technology markets.

Every frontier model from every major lab now scores within a few points of every other one on the public benchmarks. Benedict Evans's "AI eats the world" deck this month maps this convergence on a single chart.

Look at the telecom parallel for a minute. Mobile networks moved trillions of bits a year through the 2010s, but the actual value capture happened entirely above the network layer, driven by people building products on top. The core infrastructure layer commoditized within a decade.

I think a parallel commoditization wave is hitting frontier models right now, just on a faster clock. Claude Opus 4.7 still leads the public coding benchmarks at 87.6% on SWE-bench Verified, against Qwen3-Coder-Next at 74.8%. Qwen runs roughly thirteen times cheaper across input and output. For a growing share of production work, the price gap no longer justifies sticking with the premium option.

Teams making infrastructure choices right now have to decide whether to wire to one lab, or build resilient routing that lets you swap an LLM out instantly when prices move, and run an evaluation pass before shipping.

Jensen Huang calls this framework sovereign AI when he is pitching governments. Founders building a product face an identical architecture choice. A single vendor's pricing model and roadmap should never dictate your underlying unit economics.

A frontier reasoning model remains the wrong tool for pulling a simple birthday out of a database anyway.

#AIInfrastructure #BuildingInPublic

**Editor's notes (2026-06-05):** Logged verbatim per Mark — not edited. Pillar 2 (Open-Source & Sovereign AI) activated; strongest pillar fit of the batch. **`[integrity]` — verify before Markos approves in Planable:** (1) benchmark figures + model names — "Claude Opus 4.7" (latest is 4.8), "87.6% SWE-bench Verified", "Qwen3-Coder-Next 74.8%", "thirteen times cheaper"; (2) Benedict Evans deck exact title + "this month" timing + that the convergence chart exists. If unverifiable, genericize ("within a few points… a fraction of the cost") — the thesis survives without staking his name on a precise number.

---

## 2026-06-09 — Simplicity is hard to build

- **Prepared:** 2026-06-05
- **Scheduled:** 2026-06-09 (Tue)
- **Status:** scheduled
- **Tier:** 1
- **URL:** (paste LinkedIn URL once live)
- **Visual:** Carousel (5 slides) — see below

Simplicity is hard to build.

When you're building software, the temptation is to keep adding — another feature, another setting, another option. Each one makes sense on its own. People asking are usually right that a feature would be useful.

With MyVault, I keep making the same call. How much can we do in the backend so the user never has to think about it? The connecting, the security, the structured parts of the knowledge graph — all of it lives underneath. The experience on top stays clean and fast.

Yes, it would have shipped faster with more complexity left in the user's hands. I didn't go that way, because that's not the product I want to ship.

#ProductDesign #MyVault #BuildingInPublic

**Carousel:**

Cover: Finding your own information should be easy.

Slide 1 — The temptation when you're building
Every feature added makes sense on its own — another setting, another option, another control.
People asking are usually right
Each call sounds reasonable in isolation
Simplicity is the hardest design decision to defend

Slide 2 — What I keep choosing
With every product decision, the same instinct comes back.
Simple surface, deep engineering
User's job is what they came to do
Clean surfaces don't need a tutorial

Slide 3 — The question we keep asking
When we want to add something to MyVault, the first question is whether the user actually needs to see it.
Complicated part runs in the backend
Security stays invisible to the user
Knowledge graph does the connecting
What you'll see is your information, fast and searchable.

Slide 4 — What we're designing for
When you open MyVault, you'll find what you need without reading a manual, watching a tutorial, or configuring anything.
Find your insurance policy in seconds
Records sorted as they come in
Files that connect across the vault

Closing:
We do the complicated part so you don't have to think about it.
myvaultai.com

**Editor's notes (2026-06-05):** Logged verbatim per Mark — not edited. Pillar 7 (Simplicity) activated. Note for future iteration (not applied here): the strongest unused anchor is the 15× services-ratio story (Story 10) — "complexity is the business model" — which would ground the post in lived specifics if Markos wants a punchier v2.

---

## 2026-06-03 — Blog Part 4 teaser (data governance for AI)

- **Prepared:** 2026-05-28
- **Scheduled:** 2026-06-03 (Wed, one day before Part 4 blog)
- **Status:** scheduled
- **Tier:** 1
- **URL:** (paste LinkedIn URL once live)
- **Visual:** TBD — Figma

Every enterprise SaaS data program I review has the same gap.

The catalog is current, the dashboards are trusted, the lineage is solid. None of it is designed for what happens when an AI agent runs on a service account with broad data access and answers questions for users who shouldn't see half of what it can read.

Part 4 is on the five additions that close that gap: training-pipeline PII, user-scoped data access, vendor data terms, inference-log governance, and training data lineage built for ML.

Part 4 lands tomorrow.

#AIGovernance

**Editor's notes (2026-05-28):**
- Converted symmetric 5-bullet list with `→` arrows to inline prose (LinkedIn Lottery pattern avoidance per `craft/antipatterns.md`).
- Tightened "Live tomorrow." → "Part 4 lands tomorrow." for less CTA energy.
- Pillar 6 (Accountability — "AI governance vs work practices") activated.
- No Red / Yellow zone hits.

---

## 2026-06-02 — The Sophist and the Skeptic (architecture as reliability)

- **Prepared:** 2026-05-28
- **Scheduled:** 2026-06-02 (Tue)
- **Status:** scheduled
- **Tier:** 1
- **URL:** (paste LinkedIn URL once live)
- **Visual:** TBD — Figma

When we were stress-testing MyVault's retrieval, I saw the same model fail in two completely different ways on the same question. Every one of those failures turned out to be an architecture problem with a clean fix once you looked at the stack around the model.

On one question, the model delivered an articulate, confident answer that was wrong on the exact piece I needed. I've been calling that one the Sophist.

On a near-identical question, the same model qualified everything and walked straight around a perfectly good answer sitting there in the source documents. I've been calling that one the Skeptic.

Think about what changes between those two runs. Put the same model over a structured knowledge graph and you get one behavior. Point it at a folder of PDFs and you get another. Tightening retrieval alone changes the behavior more than swapping to a different model would.

Layer a schema on top of the output, drop temperature to zero on factual work, and the "AI is unreliable" story collapses into something you can engineer against.

When someone tells you AI is unreliable, they usually mean the unconstrained version they tried once. Wrap a model inside a tight architecture and you get predictable, traceable, repeatable behavior. You solve reliability in the architecture around the core technology, then you ship and improve it on a normal release cadence.

The Greeks had archetypes for these behaviors centuries before we had models. Give a Geometer a problem and they work through it the way Euclid worked a proof, checking every step. Give an Empiricist the same question and they run an external check before committing to an answer. Tighten the architecture and the model behaves more like the second.

#AIArchitecture #KnowledgeGraph #MyVault

**Editor's notes (2026-05-28):**
- Two contractions applied: "I have been" → "I've been" (×2). Edit-craft mandates contractions for Markos posts.
- Count integrity fix: original opened the closing section with *"Six Greek thinkers pinned down these behaviors centuries ago"* but only named two (Geometer, Empiricist). Reframed to *"The Greeks had archetypes for these behaviors centuries before we had models"* — removes the promise to enumerate six. If Markos wants to keep "six" as a teaser for a follow-up post, swap back and add an explicit tee-up.
- Trimmed AI-tell triplet: "design, ship, and improve" → "ship and improve".
- Added closing landing sentence: *"Tighten the architecture and the model behaves more like the second."* Threads the Greek archetypes back to the architecture point so the closing section earns its place rather than dangling.
- Pillar 1 (Pragmatic AI Implementation) fully activated. Structured-output + temperature sub-positions activated.
- Story 12 (knowledge graph "hardest decision") remains **Referenced** rather than **Deployed** — adding the lived design-with-pushback frame would push the post past the 600-word anchor cap. Reserve for a dedicated future post if Markos wants that angle.
- Hashtags at the maximum allowed (3). `#MyVault` is brand-mention; canonical category tag per `identity/identity.md` is `#KnowledgeVault` — consider swap.
- No Red / Yellow zone hits.

---

## 2026-06-01 — The 30-year-old sketch (MyVault origin story)

- **Prepared:** 2026-05-28
- **Scheduled:** 2026-06-01 (Mon)
- **Status:** scheduled
- **Tier:** 1
- **URL:** (paste LinkedIn URL once live)
- **Visual:** TBD — Figma

About 30 years ago, during the early days of the dot-com era, I sketched out the initial vision for MyVault on a single sheet of paper. Ambition was right back then, but tools were thirty years away. AI is what finally makes the original drawing buildable.

This would have been around 1995. I had one piece of paper, a product spec written across it, and I was trying to map every dimension of a person's life onto a single page. Finances and assets, investments and bills, travel and health, home and family, education, even philanthropy. The whole map of where a person's information actually sits. I think I still have a copy of it in storage somewhere, and the funny thing is, it's not all that different from what we're building today.

Long before that sketch, I was in a bookshop with my father walking through generations of programming languages, and I asked him which generation it would be when we could just speak to the computer and have it program. He didn't have a number. We agreed it would be an inflection point. I'm telling my son the same thing now.

The obvious problem in 1995 was that you could draw the system but nobody could build it. Compute wasn't there, storage wasn't there, and models capable of reading something, understanding what's actually in it, and figuring out how it connects to everything else in a person's life didn't exist yet. So the page went into a drawer, and it sat there for the next two decades while I went off and ran a software company.

Around 2023 I pulled it back out, had a look at it, and realized something fundamental had shifted. The cost of inference had collapsed. Open source models were catching up with the frontier labs on real tasks. Privacy infrastructure (Amazon Bedrock, VPC isolation, sovereign AI patterns) was sitting there off the shelf. And the right partners showed up at the right time, which is often the variable nobody gives credit to.

So the page came out of the drawer for good, and it's the exact infrastructure we're building at MyVault.

The original sketch has stayed with me my whole career. The tools are unrecognizable now compared to 1995, and the shape of the problem on that page hasn't moved at all.

And if you've been carrying a sketch of your own around with you for thirty years, the gap to buildable has finally closed.

What's in that drawer of yours?

**Editor's notes (2026-05-28):**
- Contractions applied: *"what we are building today"* → *"what we're building today"*; *"is the exact infrastructure we are building"* → *"it's the exact infrastructure we're building"*.
- **Story 3 (Bookshop with father) deployed** as new paragraph 3 — the canonical inflection-point conversation threading three generations (father → Markos → son). Was the largest activation gap in the original draft. The bookshop story is in `stories/stories.md` as Green status, no caution required.
- Cut filler "you know" from paragraph 2 per Pass-5 rule. Reads slightly more formal; revert if Markos prefers the spoken-cadence beat.
- Reframed closing line from prescriptive *"this is probably the right time to take it out of the drawer"* → observational *"the gap to buildable has finally closed."* Avoids the mild Preacher drift flagged in the review.
- Pillar 1 (Pragmatic AI Implementation) activated via the named-infrastructure stack (inference cost, open source, Bedrock, VPC, sovereign AI). Pillar 3 (Democratising AI / education) lightly activated via the household-mapping angle + the son thread.
- Closing substantive question — *"What's in that drawer of yours?"* — preserved. Functions as the post-craft "substantive question" closing pattern, not a CTA.
- No Red / Yellow zone hits.

---

> **Note (2026-05-28 back-log):** Entries below this date imported from Planable scheduled-publish history. Tier field marked "unknown — backfill" for all imported entries; live LinkedIn URLs also pending backfill. Bodies are verbatim from Planable plainText.

## 2026-05-27 — Buy-in from the top decides whether AI rollouts ship

- **Prepared:** 2026-05-25
- **Scheduled:** 2026-05-27
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

A fifteen-minute meeting can approve what twelve months of committee couldn't. Buy-in from the top is the only thing that changed.

Pattern is the same across maybe a hundred enterprise rollouts I've been near. When the CIO is genuinely bought in, decisions get made, owners get named, blockers get unblocked, and the rollout ships. Without that backing, the same decision sits in a working group, then a steering committee, then an executive review, and six months later somebody asks if anyone has heard from the vendor lately.

At the end of the day, somebody at the top has to make the decision. Committees can advise, working groups can map out the options, executive reviews can stress-test the assumptions, but someone has to be the one who actually makes the call. When nobody plays that role, the project stalls, and the status quo wins by attrition.

That year in committee shows up later as lost competitor advantage, piled-up opportunity cost, and senior engineers leaving for companies where things actually move.

Direction from the top is the variable nobody puts on the slide. Stack, vendor, architecture, all of that makes the cut. The person willing to actually decide doesn't fit on a slide, and they're the difference between a rollout that ships and one that floats.

---

## 2026-05-26 — The model is doing maybe a tenth of the work

- **Prepared:** 2026-05-21
- **Scheduled:** 2026-05-26
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** multiple images

In any real AI product, the model is doing maybe a tenth of the work. The other nine-tenths is the system around it, and that's where the cost, the time, and the failure modes all live.

Benedict Evans's new "AI eats the world" deck this month puts both sides of the same dynamic on adjacent pages. Mark Zuckerberg saying one or two people are building in a week what used to take dozens of people months. Two pages later, Uber's CTO is back to the drawing board because his full-year AI budget for 2026 got blown a few months in.

I've been writing software for thirty-odd years. Project hours go into the system around the model, and that share keeps growing as the typing gets cheaper. Models behind a product change every six months and yesterday's prompts drift. Retrieval breaks when embeddings get re-indexed. A user hands the system messy data, asks a question nobody wrote a test for, and the answers start sounding confident and wrong.

Every product I've built that lasted had the same call made early. Spend the months on the plumbing first, even when people are asking for the front end yesterday. A beautiful UI sitting on top of hallucinated answers is worse than no product at all, because the first time a user sees the system get something wrong with confidence, the trust is gone and you don't get it back. So the plumbing goes in first.

People get fixated like AI is the whole thing. It's a software application that happens to have AI as one of its critical components, but only one of many. Without the others, it wouldn't be accurate, it wouldn't be safe, it wouldn't be private, it wouldn't be fast.


#AIInfrastructure #BuildingInPublic

---

## 2026-05-21 — Wealth managers automating data gaps with AI

- **Prepared:** 2026-05-15
- **Scheduled:** 2026-05-21
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** none

Wealth managers who deploy AI without auditing their client data first end up automating the same gaps they already had.

BCG studied over 1,000 executives across 59 countries to find what the companies doing well with AI have in common. When Salesforce launched Agentforce and Microsoft deepened Copilot into agentic workflows, the companies that got it working did the same thing first:

→ Audited what data they had and where it lived
→ Fixed the gaps, the silos, the schemas nobody had touched in years
→ Then deployed the AI on top of it

Success followed the same pattern whether it was a customer service agent, a financial copilot, or an internal knowledge tool.

Your clients are dealing with the same thing. Before you can deliver proactive advice, you need a complete picture of their financial life. What you usually have is:

- a portfolio you manage
- some tax documents from last year
- a vague awareness that insurance policies exist somewhere
- no real visibility into what their estate plan says

Capgemini reports that nearly 30% of firms take over three months to fully onboard ultra-wealthy clients.

Give your clients a secure vault on day one. Ask them to populate it with their tax returns, insurance policies, property deeds, and estate documents before the engagement properly begins.

---

## 2026-05-20 — Recursive self-improvement vs the personal data layer

- **Prepared:** 2026-05-15
- **Scheduled:** 2026-05-20
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

Another team is chasing recursive self-improvement. Socher, Norvig, and a handful of OpenAI and Meta alumni raised over $650M at a $4B valuation to build AI that improves itself. "A.I. is code. And now, A.I. can code," Socher told the Times. 

"The ingredients are there."

The layer I keep coming back to sits underneath all of this. There's a problem the frontier-model race doesn't touch, and it's been unsolved for years. People don't have working access to, or ownership of, their own personal information.

It lives across paper, email inboxes, cloud drives, mobile devices, pcs and apps that don't talk to each other, held by platforms that won't return it in a form anyone can use. The hunt for a three-year-old appliance warranty, an insurance schedule, or a vaccination record runs through four or five services that don't coordinate. That's the daily texture of how scattered household data is.

In building MyVault, that's the problem we're working on. We're designing it so the household owns its data and controls who gets to see it.

Recursive AI that improves itself is interesting research. The personal data layer one floor down decides what the AI on top can actually do for a household. $650M and a $4B valuation are going into the top of the stack. 

What gets built at the bottom of it is what the AI on top has to work with.

---

## 2026-05-19 — Inflection point: standing in a bookstore 35 years ago

- **Prepared:** 2026-05-15
- **Scheduled:** 2026-05-19
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

We're at an inflection point with technology right now, and I mean that in the most literal sense.

About 35 years ago I was in a bookstore with my father, looking through hundreds of computer science books because that's how you did research back then, and I remember asking him a question that had been sitting in my head for a while. 

What generation of programming language will it be when we can just speak to the computer and it programs itself? 

He didn't have an answer. Nobody did at the time. But I knew it was coming, and I knew when it arrived it would be one of those moments where everything before it and everything after it would feel like two completely different worlds. 

Last month I told my son the same story. He's about the same age I was then, and I told him: we're there now. You can use natural language, a bit of structure, the right architecture around it, and you can get computers to automate, connect, build, communicate and reason in ways that would have been genuinely unimaginable when I was standing in that bookstore.

And you know, the thing I keep thinking about is that every generation has had one of these moments, Windows, the web, the smartphone, cloud, and each time the people who understood what was actually happening early had an enormous advantage over the people who waited to see how it played out. And each time, more people got left behind than needed to.

We're at one of those moments right now, so which person are you going to be?

#AI #TechLeadership #Founders

---

## 2026-05-18 — Architecture order decides whether privacy claims hold up

- **Prepared:** 2026-05-08
- **Scheduled:** 2026-05-18
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** multiple images

I made one decision before MyVault wrote its first line of code: architecture order is the variable that decides whether a privacy claim holds up later. Encryption boundaries, key separation, data flows, and the AI's read access all settle into very different products depending on when in the build they get designed.

For MyVault, that meant choosing Amazon Bedrock because the data-handling agreement is legally binding, not aspirational.

Full reasoning behind the architecture, and what "private by design" means in practice, in the new post on MyVault's blog.

Link in the first comment.

---

## 2026-05-13 — AI security Part 3: extending your existing program

- **Prepared:** 2026-05-08
- **Scheduled:** 2026-05-13
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

I have spent a lot of time with security teams who are good at what they do, running penetration tests, SDLC gates, SIEM management, and vulnerability disclosure programs built and maintained with care.

AI systems introduce inputs you cannot fully validate, outputs that vary run to run, and agents that can act in your environment. Part 3 of this series walks through how to extend your existing security program with controls designed for the way AI actually behaves.

Part 3 covers:
→ The seven OWASP Top 10 LLM vulnerabilities most relevant to enterprise SaaS, with specific controls for each
→ How to run an AI threat model across six components your standard STRIDE session doesn't reach
→ How to structure an AI red team engagement with specific harm scenarios and clear success conditions
→ ML bill of materials and what to track across every layer of your AI supply chain
→ How to monitor AI workloads with telemetry, anomaly detection, and kill switches for risks you cannot close
→ Six vendor security questions to put in your standard review before any third-party AI deployment
→ Where AI security plugs into your SDLC, stage by stage
→ A 90-day build plan to get it all operational

Read the full framework in the LinkedIn article tomorrow.
#AIGovernance

---

## 2026-05-12 — 58 minutes looking for a laptop invoice

- **Prepared:** 2026-05-08
- **Scheduled:** 2026-05-12
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

Last month I spent 58 minutes looking for a laptop invoice.

I got the request while deep in another task and had to divert time and focus to it as it was time-sensitive.

For 20 years I built SaaS Service Delivery and Asset Management solutions for the largest and leading businesses and governments. Those provided governance, process automation, and audit trails that ensure end-to-end tracking of assets from request, to procurement, delivery, implementation, and support. All while retaining the connection to the supplier, finance information, and service level agreements. These can tell an organization exactly where every asset and related information lives within seconds. My company was the first BS 15000 (now ISO/IEC 20000) certified firm in the world, and I spent two decades watching enterprises prioritize projects to solve a problem I couldn't solve for my own personal files.

I needed the invoice, the exact make and model, and a CEE certificate to courier a laptop from Dubai to Europe, and I found it eventually after systematically searching through three email accounts, two Google Drive accounts, Dropbox, two phones, and my workstation.

What individuals have available for managing their own assets and supporting documentation is a search bar, a downloads folder, and their own memory of when they saved something and what they called it, which is roughly where enterprise IT was in the early 1990s before classification and intelligent retrieval became standard.

Those 58 minutes came out of time I should have been spending on my business or with my kids. Enough of those afternoons is what made me start building MyVault.

How do you find your important documents when you actually need them?

---

## 2026-05-08 — Everyone blames the model; the cause sits in the system around it

- **Prepared:** 2026-05-01
- **Scheduled:** 2026-05-08
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** multiple images

When something goes wrong in an AI application, everyone blames the model. But the cause usually sits in the system around it.

When people ask which AI MyVaultAI is built on, I tell them: I'm not giving you an AI. I'm giving you a software application that happens to have AI as one of its components. The interesting work happens in everything around the model, and that's what shapes whether the answer is accurate, safe, fast, and private. 

Five things shape whether AI gets the answer right:
→ Context. What data, in what shape, gets sent to the model on each call.
→ Memory. What the system remembers across the session and what it forgets, and where that line gets drawn.
→ Prompts. The instructions and constraints the model is operating under.
→ Tool calling. When the model is allowed to reach for an external tool, and how the system handles whatever the tool returns.
→ Evals and testing. Whether you can measure if the agent is improving or regressing on the cases you care about. 

When the model hallucinates, the cause usually traces back to one of those. Context was thin, memory pulled the wrong thread, the prompt left room for ambiguity, the tool returned junk, or the eval framework was thin.

Choosing Amazon Bedrock for MyVault was about the contractual layer behind the model. Your data isn't used for training. It isn't stored by the model provider. It stays inside the contracted region for the inference at hand, and that's the full scope. Reduce the temperature, structure the output, verify against the source document, and you head off the failure modes everyone talks about.

Which model, which version, is it Claude, is it GPT, is it Gemini, Qwen, or Kimi. And I get why, that's what gets talked about everywhere. But it's a bit like asking which engine brand is in a car when what you want to know is whether the brakes work, and whether it'll get you where you're going.

So when someone asks me what AI powers MyVault, I tell them they're asking about the part doing the least interesting work.

---

## 2026-05-06 — When did you last speak with your client's adult children?

- **Prepared:** 2026-05-01
- **Scheduled:** 2026-05-06
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** multiple images

When was the last time you had a conversation with your client's adult children?
Cerulli Associates found that over 70% of heirs fire their parents' advisor after the wealth transfer, and Harris Poll found 43% of younger Americans plan to switch advisors after receiving an inheritance, with another 16% still undecided.
Advisory relationships that outlast a single generation look different from the inside. The advisor knew the whole family, had conversations with the children before anything was at stake, and became the person everyone called when something happened.

Think about your own client relationships:
- How many of your clients' adult children know your name?
- How many have ever had a conversation with you?
- How many would call you first if something happened to their parents tomorrow?

$84 trillion in wealth is changing hands right now, and every transfer is an opportunity for an advisor who already knows the family.

When the family's documents, policies, and wishes are organized in one place and shared with the people you trust, the next generation isn't meeting you for the first time at the worst moment of their lives. You're already the person who knew their family.

Has anyone gone deeper than the primary account holder?

#WealthManagement

---
## 2026-05-05 — Descope: what I learned in an attic in Scotland

- **Prepared:** 2026-05-01
- **Scheduled:** 2026-05-05
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

If there's one thing I learned from building a business with my father, it's to descope.

He didn't start the company in a garage. It was an attic in Scotland, which I think actually suits the story better than any California origin myth.

Character-based systems, dial-up, acetate slides on the projector, that was the full setup, and I used to wander up there as a kid just to see what he was working on. One day it was Windows 1.0 alpha, another day he sat me down and said (I must have been nine at this point) "that's called Unix, son, let me just show you a few things." The next thing I know, he's got me building his presentations. He'd scribble something out on paper, I'd put it together on whatever package we had at the time, he'd print it onto acetate sheets and take it to clients. I mean, I was better at it than him, which helped, and he had other things to do anyway, so we made it work.

He had this instinct that when a project was sprawling, going nowhere, trying to do everything at once, the first move was always to descope. Someone would bring him something that had been failing for years and he'd look at it and say: you're trying to do too much here, a lot of this is nice-to-have and not actually needed, so let's make it workable and get it done. And they got it done.

I've watched that exact same thing go wrong for my entire career, in enterprise software, in AI projects, in startups with serious funding behind them, and the frustrating part is that decades pass, the tools change completely, and the mistake stays the same. Scope creep destroys more projects than bad technology ever has, and it's almost always avoidable.

Four or five years ago I sold that company (family-owned, privately held, profitable, and we never borrowed a penny to build it, which I'm proud of). It took the better part of a decade to grow it properly, and now I'm building again with MyVault. 

And if I'm honest, I think about those conversations in the attic more than most things I picked up in a boardroom over the years, because some things genuinely don't change, the tools do, the fundamentals don't.

🔗Follow along at myvaultai.com

---

## 2026-04-30 — The silent map of your data, in 6 categories

- **Prepared:** 2026-02-23
- **Scheduled:** 2026-04-30
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

Every account you've created, purchase you've made, location you've shared, photo you've uploaded has built a silent map of your data  distributed across hundreds of platforms.

Some of it was handed over intentionally. A larger portion was collected indirectly through tracking pixels, ad networks, data brokers, and aggregators you may have never interacted with.

Here is an infographic that breaks down this personal data into 6 categories showing where each one typically ends up. 

If you want to take control of your digital life, start with this simple exercise:
Count your footprint from the infographic.

---

## 2026-04-28 — Risk frameworks weren't built for AI (Part 2 teaser)

- **Prepared:** 2026-04-24
- **Scheduled:** 2026-04-28
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

"We have frameworks for everything, we just didn't build them for this." That was the most common thing risk committees told me across financial services, healthcare, and enterprise SaaS in 2025.

Enterprise risk frameworks were designed for risks that behave predictably, where you identify them, score them, assign a treatment, and review them quarterly, which works well for regulatory exposure, financial risk, and operational categories where risk profiles stay stable between reviews.

AI systems change after you deploy them. A model accurate at launch can produce different outputs six months later as data flowing into it changes, and because that happens incrementally, your quarterly review cycle will not catch it. 

When multiple models share data pipelines or feed outputs into each other, a single point of failure can move across your entire stack before anyone notices it on a dashboard. And if you are running OpenAI, Anthropic, or Google APIs for anything mission-critical, that third-party dependency almost certainly is not in your vendor risk register at the right severity.

Part 2 of this framework covers how to extend your risk program to see all of it:
→ NIST AI RMF four-function cycle and how to run it continuously
→ A complete AI risk register template with every field your ERM platform can't do without
→ Nine risk categories standard taxonomy doesn't cover, including third-party dependency and concentration risk
→ Velocity scoring as the dimension your existing 5x5 matrix can't capture
→ How traditional and AI-specific risk differ across behavior and failure modes
→ SR 11-7 guidance and why it doesn't stop at banking
→ How to write an AI risk appetite statement your board can stand behind
→ A 90-day build plan is included

The full framework will be published as a LinkedIn article tomorrow.

#AIGovernance

---

## 2026-04-23 — Vendor governance assumption no longer safe (Part 1)

- **Prepared:** 2026-04-16
- **Scheduled:** 2026-04-23
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

Multiple frontier AI labs revised their usage policies in the last six months, expanding what their models can be used for and walking back constraints that were previously non-negotiable. The Pentagon started deploying AI without governance layers that used to be standard. 

The assumption that your vendors own the governance layer is no longer safe to make.

Enterprise AI strategy assumes OpenAI, Anthropic, Google, Microsoft have guardrails covered so you don't need to build your own. You deploy their tools and governance becomes their responsibility.

Your head of sales wants an AI forecasting tool that reads Salesforce data.
→ IT sees it as business strategy
→ Finance sees it as IT infrastructure
→ Legal reviews the contract
→ Data security gets informed after
→ Your head of sales has a board meeting in three weeks and subscribes on a corporate card

When a vendor changes safety commitments, ownership becomes yours. When your CRM-embedded AI makes a recommendation that misses something important, your vendor's safety team stays in the lab. You end up in the boardroom with your general counsel answering for it.

Building governance infrastructure now means you control the outcome instead of discovering gaps after deployment. I wrote Part 1 covering everything you need to launch in 90 days.

The full piece covers seven things:
→ How to build a governance committee that actually makes decisions
→ Risk tiering framework for each deployment tier
→ What your AI policy must contain to be enforceable
→ A RACI matrix for your AI lifecycle
→ How to audit the shadow AI already running
→ A 60-day amnesty window to surface undisclosed tools
→ Your 90-day launch sequence

Read the full framework in the LinkedIn article tomorrow.

#AIGovernance #EnterpriseAI #CISO

---

## 2026-04-22 — Where MyVault maps to OpenAI's privacy-preserving fellowship

- **Prepared:** 2026-04-16
- **Scheduled:** 2026-04-22
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** multiple images

OpenAI funded a six-month fellowship on four things it knows AI hasn't solved. Evaluation, agentic oversight, robustness, and privacy-preserving methods.

That last one is where we've been building since day one.

We designed around zero-trust architecture and a per-user knowledge graph from the start, with nothing leaving the vault to train anything, ours or anyone else's.

Swipe through to see where MyVault's architecture maps to each of the fellowship's priority areas.

#DataPrivacy #AIPrivacy #PrivateByDesign

---

## 2026-04-21 — Privacy is a fundamental human right (rarely in AI talk)

- **Prepared:** 2026-04-16
- **Scheduled:** 2026-04-21
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** video

You either hand over your data to get access to something useful, or you opt out and fall behind.

A trade-off that's been accepted, whether people realise it or not.

Privacy is recognised as a fundamental human right, and I find it interesting how rarely that comes up in conversations about AI and data.

What we've ended up with is a situation where getting any genuinely private, convenient digital tool is nearly impossible. And I think it's been normalised to the point where people don't even question it anymore.

Think about what you're agreeing to when you use most consumer apps. There's a privacy policy somewhere, probably updated a few times since you signed up, and somewhere in it there's a paragraph that says something like "we may use your data to improve our products and services." 

What does that mean exactly? 

It means they can do more or less anything with your data as long as it benefits them. Meta updated their terms last year to explicitly include AI training, and their policy runs to more than forty pages. You'd have to be checking it regularly to even know it changed, which nobody does, and frankly they know nobody does.

And the argument I hear is that people don't really care, that they're happy to trade data for convenience, and maybe that's true for some people. But I think a lot of the time people aren't making that trade consciously, they're just not being given the full picture of what they're agreeing to.

What I believe is that you should be able to have both, privacy and convenience, and the reason you can't get both right now as a consumer is that the business model of most platforms depends on you not having both. If users had real control over their data, a lot of those models would break.

That's the gap we're building MyVault to fill, and it's not a small gap.

#DataPrivacy #DigitalRights #PrivacyFirst

---

## 2026-04-16 — Infrastructure scaling vs access cheapening: eight numbers

- **Prepared:** 2026-04-10
- **Scheduled:** 2026-04-16
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** multiple images

Two things are happening in AI at the same time and they (usually) don't usually go together.

Infrastructure is scaling at a speed that requires nuclear energy contracts and nine-figure hardware orders.

Access to that same capability, the models, the compute, the APIs, is getting cheaper fast.

As someone building a product on top of these models, it changes the calculations on what's worth building and when.

These eight numbers from January and February are the ones that changed how I see it.

Swipe through.

---

## 2026-04-15 — Five pillars of AI governance designed from the ground up

- **Prepared:** 2026-04-10
- **Scheduled:** 2026-04-15
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

How do you know if your AI governance program is working, or producing the appearance of oversight?

Plenty of organizations have structures that technically apply to AI:

→ IT policies
→ Data governance frameworks
→ Security controls and reviews
→ Vendor management

A lot of thought and care went into building these frameworks, but AI wasn't on anyone's mind during the process, and that's why we now have the surface covered while everything underneath is still left exposed. 

So I decided to share with you my perspective on what a governance framework looks like when it's designed for AI from the ground up, drawing on work across financial services, healthcare, and enterprise SaaS environments where the stakes of getting it wrong are high. What I built comes down to five pillars: 

→ who is in charge,
→ what you are governing
→ how you close the security gaps AI creates
→ what data integrity looks like when AI is in the stack
→ how you keep visibility into what your models are doing after you deploy them

During the next 5 weeks I'll be posting each part. If you work in risk, security, or lead AI deployment in your organisation, follow along. 

All five pillars are mapped out in the infographic below.

#AIGovernance #EnterpriseAI #RiskManagement #CISO #CRO #EnterpriseSaaS #NIST #AIRisk

---

## 2026-04-14 — Use case first, then model size answers itself

- **Prepared:** 2026-04-10
- **Scheduled:** 2026-04-14
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** multiple images

For much of the past year, the answer to which model to use was "it depends," which is true but not particularly helpful.

What helps is forcing the use case question first. When you're specific about what the model needs to do, the size question almost answers itself.

→ On-device or cloud. 
→ Narrow task or broad reasoning. 
→ Batch processing or live queries at scale.

Diabetica-7B outperforming leading frontier models on diabetes-specific benchmarks isn't a surprise if you think about it that way.

Swipe through the five questions.

Then drop a comment: which camp does your main workload land in? I will reply to every one.

---

## 2026-04-09 — AI agents need structured, connected data

- **Prepared:** 2026-03-03
- **Scheduled:** 2026-04-09
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

AI agents are only as useful as what they have to work from. Structured, connected data is what separates a useful answer from a file you still have to open yourself.

We have been thinking about this from the personal side. Your insurance policies, medical records, warranties, receipts, registrations, all of it exists somewhere but none of it is connected in a way that makes it queryable. (And if it is not queryable, an agent can't do much with it either.)

Built the infographic below to show what three layers of structure look like and what becomes possible when your context is finally in order.

---
## 2026-04-08 — Anthropic's Project Glasswing and what it means for your data

- **Prepared:** 2026-04-08
- **Scheduled:** 2026-04-08
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** multiple images

Anthropic announced Project Glasswing this week, bringing together AWS, Apple, Cisco, CrowdStrike, Google, JPMorganChase, Microsoft, NVIDIA, and Palo Alto Networks around a frontier model called Claude Mythos Preview. 

Working autonomously and without human steering, the model found thousands of zero-day vulnerabilities across every major operating system and every major browser, including:

→ 27-year-old flaw in OpenBSD
→ 16-year-old bug in FFmpeg that survived five million automated test runs
→ chain of Linux kernel vulnerabilities that escalate from ordinary user access to full root control

Anthropic's $100M commitment and the depth of the coalition tell you how seriously this is being treated, with the stated focus on banking systems, power grids, healthcare networks, and government agencies. But what it means for the data individuals hold about themselves is what I have been thinking about since I read it.

Swipe through. 

#AI #Cybersecurity #DataPrivacy #ZeroTrust #PrivateByDesign

---

## 2026-04-07 — Claude Mythos leaked through the kind of lapse it's designed for

- **Prepared:** 2026-04-02
- **Scheduled:** 2026-04-07
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** multiple images

Nothing quite captures the gap between capability and operational discipline like a company building frontier AI, known for safety and guardrails, yet accidentally leaking its own announcement through the kind of security lapse their models are designed for.

Anthropic confirmed Claude Mythos after Fortune found draft blog posts sitting in an unsecured public data store. A model tier above Opus, significantly ahead of Claude Opus 4.6 on coding, reasoning, and cybersecurity benchmarks, described internally as presaging a wave of AI-driven exploits that outpace existing defenses. Early access goes to cybersecurity defenders first, which is the right sequencing decision under the circumstances.

Organisations building the most capable AI are also the ones whose operational decisions, release sequencing, access controls, and transparency choices will set the standard everyone else follows. When those decisions are good, they're worth recognising. When they fall short, that's worth recognising too.

Following this closely at MyVault as we build architectures and products that handle your most sensitive personal records, communincations and files to give you the confidence in intelligence that understands your context over time. 

The reality with any attack vector in life, work and the wider world. To be secure requires investment in education and technology. The more AI capabiltities exist that create risk, the more AI ( and human ) capabilities need deployed in defence.  

#Anthropic #AIGovernance #DataPrivacy #AISecurity #PrivateByDesign #EnterpriseAI #AIRisk

---

## 2026-03-24 — 66% use AI, only 46% trust it (KPMG 47-country study)

- **Prepared:** 2026-02-26
- **Scheduled:** 2026-03-24
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** multiple images

66% of people use AI regularly → Only 46% trust it.

KPMG surveyed 48,000 people across 47 countries and found that adoption keeps climbing while confidence is falling. Every year since ChatGPT launched, trust has dropped.

But the same data shows exactly what people will pay for. Around 76% of users said they would switch to an AI product that proves where their data goes, and half would even pay more for that transparency.

You don't have to wait for better tech to build a reliable system. If you start with clear choices for data training and let people see how their information moves, you can give users a way to verify the results from the start.

I broke down the numbers in the carousel.

#AI #DataPrivacy #ProductDesign #TrustInTech

---

## 2026-03-03 — How Anthropic teams actually use Claude Code internally

- **Prepared:** 2026-02-23
- **Scheduled:** 2026-03-03
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** multiple images

As a power user of Claude for work automation I thought to share : 

Anthropic published how their teams actually use Claude Code internally. Not marketing fluff. Real workflows.

One non-technical marketer at Anthropic cut ad creation from two hours to 15 minutes.

Growth marketing team built a Figma plugin that generates 100 ad variations per batch. One person doing the work of a full creative team.

Data infrastructure team sped up onboarding, simplified automation and leverage claude code to diagnose and fix issues autonomously, that traditionally involves bringing multiple expert teams together  

Product development built 70% of a major feature by letting Claude Code work autonomously while engineers reviewed checkpoints.

While a lot of discussion is ongoing about "will AI replace jobs." Smaller teams are already doing work that used to require entire departments and a lot more time.

#ClaudeCode #AI

---

## 2026-02-26 — IBM falls 13%, AI agents need your data, Citrini selloff

- **Prepared:** 2026-02-26
- **Scheduled:** 2026-02-26
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

IBM fell 13% in a single session after Anthropic announced Claude could work with COBOL. Citrini Research published a speculative scenario about AI agents, assigned it a 10% probability, and moved billions in capital within 48 hours.

Every analyst and portfolio manager talks about which companies are exposed. (Fair enough, that is their job.) But there is a parallel question that gets much less attention.

If AI agents will eventually:
--> re-shop your insurance
--> flag unused subscriptions
--> surface insights from your financial records

...those agents need your data to work from. Right now that data lives across a dozen platforms that do not talk to each other, each with its own terms of service and its own reasons for holding onto what you shared.

What Citrini describes creates real opportunity for you if you get your data infrastructure in order first.

Wrote about what that looks like and why it matters now. 

Interested to know what those in AI and or Wealth Management think about this 

Read here: https://www.myvaultai.com/blog/the-citrini-selloff

#AIagents #DataInfrastructure #FinancialInsights #InsuranceAutomation #SubscriptionManagement #CapitalMovement #TechSpeculation #FutureOfFinance #DataPrivacyConcerns

---

## 2026-02-13 — OpenClaw, prompt injection, and 42,900 exposed instances

- **Prepared:** 2026-02-12
- **Scheduled:** 2026-02-13
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** multiple images

We wrote recently about OpenClaw's explosive rise and what it signals for personal AI. In that piece, we noted that security researchers found issues and the community patched them quickly. Open source working as intended.
Turns out that was only the beginning. Since then, OpenClaw partnered with Google-owned VirusTotal to scan marketplace skills for malware, which was a smart move, but one that only catches known threats. Prompt injection, which OWASP ranks as the number one security risk for large language models, doesn't show up in any threat database because it isn't malware in the traditional sense. 

Researchers have already shown:
--> How a single email can trick an agent into leaking private keys
--> How a WhatsApp message can grab credential files
--> How a web page can plant a persistent backdoor in the agent's memory

All without the user ever knowing, and all while the agent behaves exactly as designed.

Meanwhile, SecurityScorecard found 42,900 exposed OpenClaw instances across 82 countries, and 78% are still running unpatched versions. Many of these belong to people who installed it during the buzz, played with it for a few minutes, and left it running with default settings wide open.

Our blog covers what OpenClaw's rise means for personal AI, and while the demand was never in question, the security conversation is just getting started and we plan to stay close to it.

Read here: https://www.myvaultai.com/blog/openclaw-the-moment-ai-got-something-to-grab-with

---

## 2026-01-22 — Prompt injection and giving AI more responsibility

- **Prepared:** 2026-01-19
- **Scheduled:** 2026-01-22
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

We are giving AI more responsibility every week. It reads emails, summarizes documents, and prepares actions we used to handle ourselves. We assume it is working for us. But a recent update from OpenAI shows how easily that can go wrong.

Experts warn that prompt injection is a problem that may never go away. A few hidden words on a website or in an email can trick an AI into following a stranger's orders instead of yours. When a machine has the ability to send messages or handle payments, a hidden sentence in the wrong place can cause serious damage. 

Some AI systems are now being tested with automated safeguards to find these weaknesses before attackers do. It is a game of cat and mouse. For now, the safest approach is still close human oversight.

If you use AI agents, three rules still hold: 

--> Request a human confirmation before the AI acts
--> Keep sensitive data where access is granted, not assumed
--> Give specific instructions rather than broad access

Saving five minutes shouldn't come at the cost of security. Attention remains the best safety feature, and a vault that stays locked. 

#AISecurity #DataPrivacy #MyVault #PromptInjection

---

## 2026-01-20 — Context engineering, Manus, and the agent bottleneck

- **Prepared:** 2026-01-05
- **Scheduled:** 2026-01-20
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

One of the more interesting problems in agent design right now is where the main engineering bottleneck seems to sit.

--> Early LLM systems struggled mainly with prompt sensitivity
--> RAG systems moved much of that pain into retrieval quality
--> With agents, it increasingly looks like the problem might be context itself

Lance Martin and Yichao "Peak" Ji recently discussed how Manus approaches agent architecture. What stood out was the focus on context engineering rather than simply expanding prompt length.

Manus agents can run dozens of tool calls per task. If every result accumulates in the prompt, the model's attention can fragment and reasoning quality may degrade over time. Managing that state starts to look less like prompting and more like an operating system problem.

Their approach appears to rely on three ideas:

--> Context reduction: Full tool outputs are replaced with compact references. The system keeps pointers instead of tokens, with the option to recover details when needed.

--> Context offloading: Moving the action space to a sandbox using a small set of primitives like Bash or a file system. This may reduce prompt clutter and help the model focus on decisions rather than mechanics.

--> Context isolation: Sub-agents are given separate windows so parallel tasks do not interfere with each other's working memory.

--> There is also tension here with the Bitter Lesson. Systems that rely heavily on human designed structure often get overtaken as compute and models improve. Peak mentioned Manus has been rebuilt multiple times in a short period, which suggests any architecture that becomes rigid could eventually limit the agent rather than support it.

In the smartphone era, control largely lived in the app store. In the agent era, the advantage might belong to whoever manages working memory most effectively.

TLDR: The most capable agents may not be the ones with the largest models, but the ones with architectures that can reduce, offload, and isolate context as tasks grow more complex.

---

## 2026-01-16 — Karpathy's jagged AI and the thick app layer

- **Prepared:** 2026-01-05
- **Scheduled:** 2026-01-16
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

Andrej Karpathy's reflection on 2025 points to a real tension in AI progress. Models are becoming more capable, but also more jagged. Exceptional at logic in some moments, unpredictable in others.

At MyVault, we see a clear way through that tension. If LLMs are "summoning ghosts," then those ghosts need a private, controlled place to work.

Here is what that means for document management:

1. The right precedence for agents
AI agents work best when they have structured access to the right context. MyVault follows this logic. When you upload data, our backend derives a unique encryption key and secures your information server-side. Your AI agents work on your documents within this secure environment. Your data remains private. No one else sees it, including us.

2. Verified reasoning over vague chat
As AI moves toward verified reasoning, correctness matters more than tone. You do not need a chatbot that vibes with your taxes. You need answers verified against your actual PDFs, records, and receipts.

3. The "thick" app layer
Karpathy argues that base models are generalists, while real value comes from apps that turn them into professionals. MyVault is that layer for personal and professional documents, adding structure, permissions, and feedback loops around the model.

AI agents are getting closer to real data and real decisions. When these ghosts start handling your most sensitive information, they should only ever work inside your secure vault.

#AI #LLM #ResponsibleAI #AIAgents #MyVault #DataPrivacy

---

## 2026-01-15 — State of AI: workload-model fit and the Cinderella effect

- **Prepared:** 2026-01-05
- **Scheduled:** 2026-01-15
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

If you are building, investing in, or just thinking seriously about AI, you might be focused on the wrong things.

We all assume AI is mostly for work tasks. But a new "State of AI" report from OpenRouter and Andreessen Horowitz (known as "a16z"  ) looked at over 100 trillion tokens about how people actually use proprietary and open-source models.

Here are three key findings that might change your strategy:

--> Creative and technical needs drive the most use. Two areas dominate the workload. Creative roleplay accounts for 58% of use. Programming and debugging represent the highest value. Builders must solve specific technical friction or deep creative needs. There is no middle ground.

--> The end of the single prompt: The report confirms that users are moving toward multi-step problem solving. This changed after the o1 reasoning model arrived in late 2024. Users stay when the AI finishes a task instead of just providing an answer.

--> Solving the problem creates retention: The study found a "Cinderella effect" where early user groups stayed active longer than those who joined later. These users found a "Workload-Model Fit." They remain because the model solved a specific, recurring problem.

Growth comes from products that use multi-step capabilities to handle complex, personal tasks.

Where do you see users with unsolved problems right now?

#AI #LLMs #StateOfAI #TechStrategy #MyVault

---
## 2026-01-06 — Decision latency is the least measured waste in business

- **Prepared:** 2025-12-15
- **Scheduled:** 2026-01-06
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

Decision latency is likely the least measured waste in business. Teams gather data, schedule meetings, and wait for approvals. But work stalls because of hesitation, not effort.

Most leaders think you trade speed for quality. But the data says the opposite. Research from McKinsey & Company shows fast-moving organizations are twice as likely to make high-quality decisions than slow ones. Slow decisions rely on stale data. In this market, a "perfect" decision two weeks late is already wrong.

AI can finally cut this cost. It condenses massive data, compares historical patterns, and simulates outcomes to show you only the tradeoffs that matter.
When you shorten the time between insight and action, performance changes. 

--> Projects move faster
--> Coordination improves
--> Uncertainty decreases

Taking all that into account, it is reasonable to conclude that the companies that gain a competitive advantage in the next decade will be those that act faster on the data they already possess.

Where's the highest decision latency in your organization right now?

---

## 2025-12-31 — People care about whether the task gets completed

- **Prepared:** 2025-12-09
- **Scheduled:** 2025-12-31
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

People no longer care much about features. They care about whether the task is actually completed.

For a decade, consumer apps focused on feature lists and intricate design. But that approach may be becoming irrelevant if the user's only goal is to get a complex task done with the least effort possible.

Intelligent agents remove the need for screen navigation, setting searches, or app management. You just say what you want, and the system completes the work. 

This results focused approach is highly likely to disrupt sectors like finance, travel, healthcare, education, and daily administration faster than many businesses expect.

Overloaded interfaces will not reliably protect any product. And companies will find it difficult to stand out just by adding new features. Their success is more probable if they focus on these four pillars:

--> Outcomes that are consistently correct
--> Reasoning that holds up
--> Memory that actually helps the user
--> Trust that people are willing to give (foundation for everything else)

Agents represent the layer that understands the person and manages the work. The digital experience seems to be shifting from using apps to achieving results.

What is the first non trivial task in your daily life you would comfortably hand over to a capable, private and secure intelligent agent?

---

## 2025-12-25 — Your brain wasn't built for modern information volume

- **Prepared:** 2025-12-15
- **Scheduled:** 2025-12-25
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** video

Your brain was simply not built to manage the volume of information modern life carries. You are storing passwords, policies, invoices, subscriptions, medical files, financial documents, and random notes across scattered apps and inboxes that were never meant to work together.

So you already offload. Everyone does. The issue is that we offload into scattered systems, not a real memory.

What people need is truly a system that actually remembers for them. One place that is structured, searchable, and smart enough to surface the right information at the right moment. When you stop spending mental energy on constant tracking, it is widely accepted that you will:

--> think more clearly
--> make better decisions
and finally have space for real work

Personal digital infrastructure is becoming as important as any professional skill you invest in.

If you could hand off one category of mental load to a reliable system, what would it be?

---

## 2025-12-24 — Boardrooms hit a wall: AI as a strategic counterpoint

- **Prepared:** 2025-12-09
- **Scheduled:** 2025-12-24
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

Large organizations are hitting a wall. Markets move too fast. Data volumes exceed what humans can process. Risk multiplies. Experience and intuition alone are probably insufficient for the current competitive reality.

AI can already handle work that no human team can match:

--> Simulate scenarios at scale
--> Test thousands of strategic possibilities
--> Spot second-order effects
--> Quantify operational risk

But this technology is not expected to replace human judgment. It challenges and scrutinizes it. It catches blind spots. It runs scenarios without emotion, ego, or internal politics. Its only incentive is accuracy.

Companies combining human intuition with machine precision are positioned to achieve better results than those depending on one alone.

This suggests that AI's greatest contribution is giving directors a massive upgrade in strategic oversight and risk management. It forces better, faster discussion by providing a constant, data driven counterpoint to human assumptions.

Which board responsibility do you think AI could strengthen most?

---

## 2025-12-24 — Consumer AI vs enterprise AI and model drift

- **Prepared:** 2025-12-09
- **Scheduled:** 2025-12-24
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

Consumer AI wants speed, ease, and creativity. It works when it removes friction. Enterprise AI goes in the opposite direction. It needs to be explainable, verifiable, and stable. It succeeds when it reduces risk and supports serious decisions. It is highly improbable that one system can meet both sets of expectations for long.

The requirements and safety limits pull away from each other. 

Consumer AI failure typically means poor personalization or user frustration
In enterprise AI, failure means millions in regulatory fines, critical system malfunction Enterprise AI failure could mean millions in regulatory fines, critical system malfunction (like predictive maintenance), or a data breach violating HIPAA/GDPR

The most insidious threat in enterprise AI may be model drift (AI is confused, not lying). Unlike hallucination, where the AI invents facts, drift occurs when the AI finds a document or policy that is factually correct but no longer valid in the current regulatory context. Because enterprises rely on "living documents" (policies, clinical guidelines), this simple version error can translate directly into compliance violations and serious liability.

Companies that recognize this conflict early are positioned to build tools that fit their highly regulated environment. Companies that ignore it will likely deal with rising complexity and regulatory pressure they cannot manage.

Do you think general models stay relevant, or do industry or domain specific ones take over?

---

## 2025-12-18 — Benedict Evans's platform shift map is missing data custody

- **Prepared:** 2025-12-09
- **Scheduled:** 2025-12-18
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

Benedict Evans maps GenAI as the next platform shift: Mainframes → PCs → Web → Smartphones → now this. It's a common and useful tech analyst framing, but it may be missing a critical variable.

Every platform event also restructured where data lives and who controls it:

--> Mainframes: Data often remained locked in corporate IT systems
--> PCs: Data moved to personal hard drives (mostly user-owned)
--> Web: Data moved to servers you don't control (early centralization)
--> Smartphones: You leak location, contacts, and behavior 24/7 (ambient leakage)
--> GenAI: The strategic question of data custody is entirely open

Evans asks "how will the new thing work?" and lists browsers, agents, voice, MCP, wearables. These are interface questions. He potentially skips the deeper architectural problem: centralized inference vs. local models.

This distinction matters because platform events create new gatekeepers through whatever becomes the bottleneck. In mobile, it was app stores and attention. In the cloud, it was infra scale. In GenAI, the bottleneck candidates could be:

--> Compute: Favors hyper scalers 
--> Data moats: Favors incumbents with massive user graphs
--> Model quality: Currently shows no durable advantage
--> Trust and context: Favors... who?

The trust angle is interesting. LLMs store your documents. But they understand them. They extract relationships, intent, patterns. 

While it's true that early leaders often disappear (e.g., Apple in early PCs, Netscape in browsers), and the incumbents largely seem to assume centralized inference, there is a strong strategic question to consider:

What if the winning architecture is the one that doesn't require uploading your life to someone else's servers?

TLDR: Evans's mapping of the GenAI platform event focuses on interface and value capture. It is very likely that this view misses that each new era also fundamentally restructured data custody, and that is the critical, open strategic question for GenAI.

The link to the full presentation;
https://www.linkedin.com/posts/benedictevans_presentations-benedict-evans-activity-7396903363956744192-ffwp/

---

## 2025-12-17 — $400B AI infrastructure bet and the case for local inference

- **Prepared:** 2025-12-12
- **Scheduled:** 2025-12-17
- **Status:** shipped
- **Tier:** unknown — backfill
- **URL:** (backfill)
- **Visual:** single image

Benedict Evans notes that the big four are spending roughly $400 billion annually on AI infrastructure. This investment is larger than the global telecom industry's spending. Data centers are now competing fiercely with commercial real estate for construction resources.

The implicit bet: success in AI is presumed to mean building massive, centralized inference capabilities at unprecedented scale.

But there are accelerating constraints on this centralized model that demand critical attention:

@Nvidia's supply chain is reportedly unable to meet demand for their high end accelerators, leading to bottlenecks. Centralized scale is limited by one vendor's capacity

The US power grid adds 2% capacity yearly while AI wants 1% more (multi-year backlogs)

Hyperscaler cash flow is enormous, but capex is eating it (capital leases and debt keep creeping up)

This entire spending spree operates on the core assumption that centralized inference is the only viable path. And what if this assumption is flawed? If AI models continue to become significantly more efficient (they are), and if users start to prioritize and demand control over where their data lives (which is very likely due to privacy and security concerns), then maybe the optimal architecture is not about who can build the most data center capacity.

Local inference (running models on device or at the edge) largely avoids the massive strain on the centralized power grid

It offers lower latency, offline functionality, and enhanced data privacy because sensitive data is processed locally

The hyperscalers are investing hundreds of billions in an architecture of scale. This is a business model choice designed to consolidate control. And given the physical and financial constraints they face, that choice could age poorly.

TLDR: The roughly $400B/year AI investment assumes centralized inference will succeed. It is highly strategic to scrutinize that assumption, as physical resource constraints and the compelling advantages of local, efficient models very likely point to an alternative, decentralized path.

---
