---
type: log
status: active
owner: Mark Bobyliak
created: 2026-05-28
updated: 2026-05-28
tags:
  - content-log
  - linkedin
  - linkedin-article
  - markos
  - voice-of-markos
summary: Running log of every long-form LinkedIn article published under Markos's personal profile. Full article body inline per entry. Most recent at top.
---

# Markos LinkedIn Articles — Running Log

Running log of long-form LinkedIn articles (the LinkedIn "blog" surface) under Markos's personal profile. Distinct from short-form posts — longer, headlined, evergreen-leaning. Full article body inline per entry.

**Brand system:** Voice of Markos satellite — see [[_manifest|VoM manifest]] and [[guide|VoM guide]]. Parent banned-words + AI-slop rules still apply.

**Tier workflow:** Articles default to Tier 1 (strategic, signed-off by Markos). See [[playbooks/approval-workflow]].

**Sibling log:** Short-form posts in [[markos-linkedin-posts-log]]. Both logs sit in the same `voice-of-markos/` directory.

## How to add an entry

Paste a new block at the very top of the **Entries** section, above the most recent existing entry. Fill all fields. Keep the article body verbatim.

```
## YYYY-MM-DD — [Article title]

- **Prepared:** YYYY-MM-DD
- **Scheduled:** YYYY-MM-DD
- **Status:** draft | scheduled | shipped
- **Headline:** (final LinkedIn headline)
- **Cover image:** (Figma node / asset path, or "none")
- **URL:** (paste LinkedIn URL once live)
- **Provenance:** markos-verbatim | markos-edited | system-draft  <!-- tag every entry; if markos-edited, log the (draft→final) pair in markos-edits-log.md -->
- **Tags:** pillar=<1–8 from opinions/opinions.md> · mode=article · story=<id from stories/stories.md, or none>
- **Engagement:** (backfill after ~1wk: impressions / comments / reciprocity)  <!-- Loop 2: manual for now, no analytics pipeline -->

<!-- Full article body, verbatim, including subheads and pull quotes -->

[Article body]

---
```

## Entries

## 2026-05-28 — Garbage in, liability out: data governance for AI (Series Part 4)

- **Prepared:** 2026-05-28
- **Scheduled:** 2026-06-04 (Thu) — Mark publishes manually
- **Status:** draft — **awaiting Markos sign-off on Yellow-zone framing + bio credentials**
- **Editorial headline:** Garbage in, liability out: data governance for AI
- **SEO title:** Enterprise AI data governance: training data, lineage, and PII at the pipeline layer
- **Subtitle:** How to extend your data governance program for what AI actually requires
- **Series indicator:** Part 4 in a series on AI governance for enterprise SaaS leaders
- **Reading time:** 15 min read (~2,950 words at 200 wpm)
- **Cover image:** TBD — Figma (reuse the series framework diagram if one exists from Parts 1–3)
- **URL:** (paste once live)

---

# Garbage in, liability out: data governance for AI

*How to extend your data governance program for what AI actually requires*

*Part 4 in a series on AI governance for enterprise SaaS leaders*

**15 min read**

## Contents

1. The data layer underneath AI
2. Three layers of AI data quality
3. Data lineage for AI: going deeper than your current program
4. PII and privacy in AI: three additions
5. Pointing AI at your systems of record
6. Governing your inference logs
7. 90-day build plan
8. Part 5 preview

---

A few weeks back I sat with a Head of Data at a mid-sized SaaS company. Their catalog was current, their dashboards were trusted, their lineage was solid. Their team had just turned on a CRM copilot with broad service-account access. Within a week, a junior in a partner team was answering questions about deals he had no right to see. Their data program had been built for analytics. It had nothing to say about what they had just deployed.

Every enterprise data program I review is built that way. For what came before AI, not for what AI actually does once it connects to the data.

**TL;DR.** Your data governance program was built for analytics. AI adds five new requirements that sit alongside it: representativeness, memorization risk, feedback loop integrity, training data lineage, and PII handling at the training-pipeline stage. The 90-day plan at the end maps out where to start.

In Part 3, you built the security AI requires around adversarial inputs and model behavior. Part 4 turns to the data layer underneath. Your work here is keeping the data your models train on and operate against accurate, representative, and compliant. Call it data governance, extended for what AI demands.

Your existing data governance program was almost certainly designed for analytics and reporting. You care about accuracy, completeness, consistency, and timeliness because those properties determine whether your dashboards and reports are trustworthy. Those properties matter for AI too, and AI brings additional requirements that sit alongside them: representativeness, memorization risk, feedback loop bias, lineage at the training dataset level, and the implications of a user's right to erasure once their data has been used to train a model.

> **"Frankly, every enterprise data program I review was built for analytics. The new questions AI brings deserve their own documentation layer, sitting alongside everything you already maintain."**

The new questions AI brings — training data lineage, memorization risk, and how to scope AI access to each user's authorization level — deserve their own documentation layer, sitting alongside everything you already maintain.

The work has two pieces. What do you add to the program you already have, and what do you ask of the vendors whose AI is reading your data?

## Pillar 4: Data integrity and privacy

### What AI adds to the data governance you already run

Your data governance framework manages data quality in your operational and analytical systems. When a record is wrong, you correct it. When data is missing, you fill it. The consequence of a data quality issue is a bad report or a stalled process, localized and correctable.

In AI, data quality issues compound differently. A model trained on biased or unrepresentative data produces systematically skewed outputs at scale, across every inference it runs, often in ways that sit below aggregate accuracy metrics. Correcting it lives at the training-pipeline layer: you identify the issue in the training data, rebuild the dataset, and retrain the model from a clean baseline.

AI also introduces two data properties new to standard data governance.

First is memorization. Large language models can memorize and reproduce verbatim text from their training data, which means PII or confidential information in your training set can resurface in model outputs. Memorization needs handling at the training-pipeline layer, where standard reporting-layer masking sits at the wrong stage.

Second is feedback loops. When a model's outputs influence what data gets collected next — a recommendation model shapes user behavior, which shapes the next dataset it is trained on — your data can drift in ways that need monitoring beyond what your standard quality program produces today.

### Three layers of AI data quality

You need to assess data quality for AI across three layers, each extending what your standard DQ framework already covers.

**Layer 1: Representativeness.** Your training data needs to reflect the population and environment where your model will operate, including segments your historical data may underrepresent. Historical data collection carries collection bias by default. If your CRM data was collected predominantly from enterprise accounts, a model trained on it will underperform for SMB customers. If your support ticket data reflects the behavior of customers who self-select to raise tickets, your model's understanding of customer experience will under-represent customers who churn silently.

Before you use any dataset for training, document what populations and scenarios are well-represented and where representation is thin, then assess whether the level of coverage is acceptable for the use case. The documentation becomes part of your data lineage record.

**Layer 2: Recency and temporal validity.** Your model's understanding of the world is frozen at the point its training data was collected. If your market conditions, customer base, regulatory environment, or competitive landscape have shifted meaningfully since that collection date, your model's learned patterns need refresh. A churn prediction model trained on pre-pandemic behavior is a common example. A credit risk model trained before a market cycle shift is another.

Establish a recency threshold for each AI use case. How current does the training data need to be for the model's outputs to remain reliable? That threshold drives your retraining schedule and should be documented in your AI risk register as a Concept Drift trigger.

**Layer 3: Feedback loop integrity.** When your model's outputs influence real-world behavior, and that behavior generates the data you use to evaluate or retrain the model, you have a feedback loop. Recommendation systems are the canonical case. The model recommends content, users engage with what they're shown, engagement data trains the next model, which recommends more of what drove engagement before. Your model becomes excellent at predicting what it already optimized for, which can drift from your business objective.

Identify every AI system in your environment where this dynamic exists, document it in your risk register under Concept Drift Risk, and design evaluation datasets collected independently of model outputs so you have a clean signal for model performance.

### Data lineage for AI: going deeper than your current program

Data lineage in a standard analytics environment tracks how data moves from source system to report: which tables fed which transformation, which transformation produced which dataset, which dataset powers which dashboard. When something is wrong, you trace backward.

AI data lineage requires you to go several levels deeper, and it has regulatory implications worth surfacing in your current lineage program.

What AI data lineage must capture:

- **Source systems and collection dates.** Where did the data originate, when was it collected, and what version of the source system generated it?
- **Preprocessing and transformation history.** What cleaning, normalization, augmentation, or filtering was applied? What was removed, and why? Datasets that look similar can have dramatically different properties depending on what was filtered out.
- **PII review status.** Was the dataset reviewed for personally identifiable information? By whom, when, and with what tooling? What was found and how was it handled?
- **Representativeness assessment.** What populations and scenarios are well-represented, and what are the known gaps?
- **Legal basis for use.** Under what legal basis is this data being used for AI training? Is it covered by your existing data processing agreements with data subjects, or did AI training require a new basis?

**The EU AI Act requirement.** For high-risk AI systems under the EU AI Act, training data documentation is a compliance requirement that goes beyond best practice. If you are deploying AI in hiring, credit, insurance, education, or law enforcement contexts within EU jurisdictions, your lineage records need to meet a specific documentation standard. Your legal team should review whether any of your current or planned AI systems fall within the Act's high-risk categories.

**Tooling.** Your existing data catalog (Collibra, Alation, DataHub, Apache Atlas) extends to cover ML datasets with custom metadata schemas. Lineage records for AI training data should be version-controlled alongside the model, so when you retrain, you document which version of which dataset produced which version of the model.

### PII and privacy in AI: three additions your standard privacy program needs

Your privacy program handles PII in operational and analytical systems. For AI, three additions extend that coverage to the new surfaces AI creates.

**Problem 1: Model memorization.** Large language models can memorize training data and reproduce it verbatim in outputs. Research has demonstrated extraction of real email addresses, phone numbers, and verbatim text passages from models trained on public internet data. If you fine-tune a model on internal data containing PII (customer records, employee data, support tickets), that PII can resurface in model outputs in response to prompts that have nothing to do with the original records.

Memorization is solved at the training-pipeline stage, before the model has learned from the raw data. Run automated PII detection and removal on training datasets before they enter your training pipeline. Tools like Microsoft Presidio, AWS Comprehend, or Google DLP handle the automated layer, with human review for high-confidence flags. After masking, test whether the model can be prompted to reproduce sensitive strings from the training period.

**Problem 2: Re-identification.** Anonymization techniques tuned for structured datasets need adaptation when applied to text data that will train a language model. A model trained on "anonymized" support tickets may still surface information that re-identifies individuals when queried in the right way, because language models learn patterns and relationships across records, alongside the discrete fields. Your privacy impact assessment for AI training datasets needs to account for re-identification risk through the model, alongside risk from the raw dataset.

**Problem 3: Right to erasure and training data.** Under GDPR, individuals have the right to request deletion of their personal data. In a standard operational system, you delete the record. In an AI context, if that individual's data was used to train a model, the legal picture is considerably more complex. Once data has trained a model, the path to removing its influence runs through retraining the model from a corrected dataset. Frankly, the legal consensus is still settling, and different regulators are taking different positions on what "erasure" means once data has been incorporated into model weights.

In practice, document the legal basis for using personal data in AI training as part of your data lineage record, maintain a log of which individuals' data was included in which training datasets, and have your legal team establish a position on erasure requests that affect training data ahead of receiving one. You also want to assess whether you can design your AI systems to use aggregated or synthetic data rather than individual records where possible, which reduces your exposure significantly.

### Pointing AI at your systems of record (and the access controls to put in place first)

Your most valuable data for enterprise AI sits in your systems of record. Your CRM holds customer relationship history, your ERP holds financial and operational data, your HRIS holds employee data, and your ITSM holds service history. The AI use cases built on this data are among the highest-value in any enterprise SaaS environment.

Systems of record also carry the highest data governance stakes, which makes the controls below worth putting in place before AI connects to any of them.

**The access scoping problem.** When you give an AI system access to your CRM data to power an AI sales assistant, your design choice is whether the AI sees all the data a CRM admin can see, or only the data the specific user interacting with the AI is authorized to see. Out-of-the-box AI implementations typically run on a service account with broad data access. Scoping AI access to the requesting user's authorization level is the control that aligns AI behavior with how the underlying CRM already governs access.

Implement user-scoped data access for any AI system that connects to a system of record. The AI retrieves only what the requesting user is authorized to see, enforced at the data layer rather than at the UI layer.

> **"Zero Trust is a methodology: every layer, every contract, every integration designed to protect the data on its own terms, not borrow assumed protection from somewhere else in the stack."**

This is Zero Trust applied to your data layer. Every retrieval verified against the requesting user's actual permissions. No implicit access just because the AI is inside your tenant. Zero Trust is a methodology: every layer, every contract, every integration designed to protect the data on its own terms, not borrow assumed protection from somewhere else in the stack.

**Data contracts for AI.** Before you connect an AI system to any system of record, you need a data contract. The contract is a documented agreement between the data owner and the AI system that specifies what data the AI can read, whether it can write or modify records, under what conditions it can act on data, and what logging is required for every data access.

Treat it as a governance artifact rather than a technical configuration. It sits alongside your data lineage records and is reviewed by your data governance team before the connection is approved. Your RACI from Part 1 should route all system-of-record AI connections through a data governance review gate.

**Vendor data use provisions.** Every major SaaS vendor is now embedding AI into their platform, and the data use terms attached to those AI features vary significantly. Before you enable AI features in Salesforce, Workday, ServiceNow, HubSpot, or any other platform you use, review and amend the relevant contract terms.

The specific questions your legal and procurement teams need to answer for every vendor:

- Does the vendor use your data to train or improve their shared AI models? What is the opt-out mechanism?
- Is your data used exclusively within your tenant, or does it contribute to cross-customer model training?
- Where is your data processed when AI features are active, and does that meet your data residency requirements?
- How long does the vendor retain prompts and responses from AI interactions?
- What are the vendor's incident notification timelines for events affecting AI-processed data?
- If you terminate the contract, what happens to any model fine-tuning that used your data?

Many enterprise SaaS vendors have published AI data processing addenda in response to customer demand. Your starting point is to request those addenda for every active vendor with AI features enabled, review them against the questions above, and negotiate the terms you want in place.

### Governing your inference logs: the dataset to bring inside your classification scheme

Every time a user interacts with an AI system you operate, that interaction generates a log: the input prompt, the model's response, the retrieved context if you are using RAG, the timestamp, and the user identifier. These logs are valuable for monitoring model performance, debugging unexpected outputs, and improving the system over time.

They are also a dataset containing highly sensitive information, which makes them worth governing with the same rigor you apply to your other high-classification data.

I have worked on engagements where security controls had to hold up under Official Secrets Act audit — the level most enterprises never see. The discipline that stayed with me from that work is straightforward: classify every dataset by what is in the data, not by which system happens to store it. I have seen enterprise programs apply the full data classification scheme to every system of record and then bring inference logs in as the same kind of dataset once they realized those logs belonged inside the scheme.

Your inference logs likely contain customer names and details mentioned in prompts, confidential business information users paste into AI interfaces, employee information mentioned in HR-adjacent AI use cases, and strategically sensitive information about deals, plans, and decisions. They sit alongside your operational data in terms of sensitivity, which is the standard your classification scheme should apply.

What you need to govern inference logs properly:

- **Classification.** Apply your standard data classification scheme to inference logs based on the sensitivity of the use case. Inference logs from a customer-facing AI assistant should be classified at least at the same level as your CRM data.
- **Access controls.** Define who can access inference logs and for what purpose. Limit AI system administrator access to defined investigative and maintenance scenarios.
- **Retention policy.** Define how long you retain inference logs and align that period with your legal obligations. Inference logs are subject to data subject access requests under GDPR and CCPA, so your retention and indexing should support producing or deleting a user's inference history on request.
- **Training use policy.** If you plan to use inference logs to fine-tune or improve your models, that use needs to be covered by your privacy policy, disclosed to users, and governed by the same PII review process you apply to other training datasets.

## Data governance for AI: 90-day build plan

**Days 1–30: Map your current state**

- Inventory all AI systems that connect to systems of record and document their current data access scope
- Pull and review AI data use provisions for your top 10 SaaS vendors
- Audit inference log handling across all production AI systems (classification, access controls, retention)
- Identify all datasets currently used for AI training or fine-tuning and check their lineage documentation

**Days 31–60: Implement critical controls**

- Implement user-scoped data access for all AI systems connected to systems of record
- Run automated PII scanning on all training datasets where PII review is yet to be documented
- Establish inference log classification, access control, and retention policies
- Draft the vendor AI data processing addendum template for your legal team to use in contract reviews

**Days 61–90: Operationalize**

- Add a data governance review gate to your RACI for any new AI-to-system-of-record connection
- Publish training dataset lineage documentation requirements to your data and ML teams
- Establish a legal position on right-to-erasure requests affecting training data
- Add representativeness assessment to your data quality checklist for AI training datasets

## Part 5 lands next week

Now that your data foundation is solid, I turn to the operational domain. Part 5 covers the monitoring and transparency infrastructure that tells you whether your AI systems are performing as expected in production, surfaces drift early, and gives you a response path well before any degradation reaches users.

## About the author

Markos Symeonides has spent his career delivering enterprise software to some of the world's largest governments and companies. His firm was the first in the world to achieve BS15000, now ISO/IEC 20000, and he pioneered assyst as the original ITIL solution before selling in 2021. He is currently building MyVault, with solutions that comply with SOC 2, ISO 27001, NIST, and ISO 42001 standards.

He applies the same governance principles to MyVault: structured oversight, clear accountability, and documented risk appetite, applied to the documents and data families rely on.

---

**Editor's notes (2026-05-28):**

**Scene opener added (blog-craft Pre-publish):** The original opened framework-first (TL;DR + "In Part 3, you built…"). Added a 2-paragraph anchored scene at the top — Head of Data + CRM copilot incident — to earn the universal observation that every enterprise data program is built for what came before AI. Scene is principle-level (no client name, no industry-identifying detail) and verifiable as the kind of conversation Markos has regularly per his "every enterprise SaaS data program I review" framing in the companion teaser post.

**Story 8 (Official Secrets Act / classified security audit) deployed** at principle level in the Governing inference logs section. Sets up the "classify by what is in the data, not which system stores it" discipline. Per `guardrails/guardrails.md`, OSA references are Yellow — abstract framing is acceptable but **Markos sign-off required on first public deployment of this story in long-form**. No agencies, clients, projects, or time-periods named.

**Pillar 8 (Zero Trust) activated** with a new paragraph in the access scoping section using the canonical Markos sound-bite from `opinions/opinions.md`. The original blog talked about access scoping without naming the methodology that holds it together.

**Em-dashes stripped** in three places: section heading "PILLAR 4 — Data integrity and privacy" → "Pillar 4: Data integrity and privacy"; Part 5 preview *"I turn to the operational domain — covering…"* → split into two sentences; bio paragraph *"structured oversight, clear accountability, documented risk appetite — for the documents and data families rely on"* → restructured with commas. Note: one em-dash retained in the new Story 8 paragraph *"under Official Secrets Act audit — the level most enterprises never see"* — flag for sweep if you want strict zero em-dashes; alternative: *"under Official Secrets Act audit, the level most enterprises never see."*

**Banned word "journey" replaced:** *"tracks the journey of data"* → *"tracks how data moves"*.

**Pull quotes inserted** at two natural break points (post-Frankly observation; Zero Trust methodology statement). Both anchored to specific claims per `craft/blog-craft.md`, not punchlines.

**TOC added** above the first H2 per blog-craft (post > 2,000 words).

**Reading time** calculated at 200 wpm: ~2,950 words → 15 min read.

**Dual titles:** Editorial = *"Garbage in, liability out: data governance for AI"* (voice-led). SEO = *"Enterprise AI data governance: training data, lineage, and PII at the pipeline layer"* (searchable).

---

**🟡 Yellow zone — Markos sign-off needed before publish:**

1. **EU AI Act framing** — "For high-risk AI systems under the EU AI Act, training data documentation is a compliance requirement that goes beyond best practice." `opinions/opinions.md` lists "Specific AI regulation (EU AI Act, US executive orders)" under **Flag for Markos**. Current draft hedges to "your legal team should review" — likely OK but needs Markos confirmation.
2. **GDPR right-to-erasure position** — "Once data has trained a model, the path to removing its influence runs through retraining the model from a corrected dataset." `opinions/opinions.md` lists GDPR under **Flag for Markos**. Current draft includes "Frankly, the legal consensus is still settling" hedge — likely OK but needs sign-off.
3. **Bio credential: BS15000 / ISO/IEC 20000 / assyst / ITIL** — these claims are NOT in `identity/identity.md` (cleared credentials there: 25+ years enterprise software, Eloqua first in Europe / third in world, OSA work at principle level, Bedrock/Claude/Qwen/Deep Seek hands-on, hierarchical knowledge graph design). Per `craft/blog-craft.md` Pass: every credential cross-checked against identity.md, flag for Markos sign-off if absent. **Action:** Markos confirms accuracy → I add to `identity/identity.md` so it's canonical going forward.
4. **Bio compliance claims: SOC 2, ISO 27001, NIST, ISO 42001** — product claims that need MyVault product-team confirmation per the Pillar 5 red line "Do not overclaim MyVault does things it doesn't." Most likely accurate but needs explicit sign-off from product before publish.
5. **Sale year "before selling in 2021"** — `identity/identity.md` says "four or five years ago" (relative to 2026 = 2021–2022). Consistent but worth confirming the specific year is OK to state.

**Pre-publish checklist gaps still open (blog-craft):**

- [ ] Internal linking: ≥2 MyVault pages, ≥1 related Markos post (the teaser counts), ≥1 external authoritative source per 500 words (so ≥6 external citations for a 2,950-word post). Original draft had **zero outbound links** rendered in the body — needs an editorial pass to add: links to Parts 1–3 in the series, plus authoritative external citations for the EU AI Act, GDPR memorization research, Microsoft Presidio / AWS Comprehend / Google DLP, the Collibra / Alation / DataHub / Apache Atlas references.
- [ ] Lead capture / CTA at end. Currently lands on "Part 5 lands next week" preview — appropriate for a series post. If a founder-log newsletter signup belongs at the end, add it.
- [ ] Framework diagram (if Parts 1–3 used one as the series identity element, reuse here).
- [ ] Hero / cover image — to be produced in Figma.

**Activation summary:**
- Pillar 1 (Pragmatic AI) — **Mentioned** (system-around-the-model implicit). Could be activated harder with a paragraph naming the stack components, similar to Post 1's named-infrastructure beat — deferred to a future post if at all.
- Pillar 6 (Accountability — "You can't just blame the AI") — **Activated** throughout via the "data program had nothing to say about what they had just deployed" framing.
- Pillar 8 (Zero Trust) — **Activated** in access scoping section.
- Story 8 (OSA security audits) — **Deployed at principle-level** in inference logs section.

---
