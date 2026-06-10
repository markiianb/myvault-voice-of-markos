---
type: research-brief
status: draft
owner: mark
created: 2026-06-10
linear: MVM-153
tags: [linkedin, comments, voice-of-markos, engagement-drafts, mvm-153, v3-2]
summary: "v3.2 re-draft of the 35 comments from the 2026-06-08 batch (same accounts, same verified posts, same framework/tier/story decisions — new prose register per the texture pack + length variance). Batch QA passed: 0 residual tells, length spread 24/11/0. DRAFTS ONLY — pending Sead pre-review, then Markos Stage 2."
---

# Voice of Markos — Comment Drafts v3.2 (2026-06-10 re-draft)

> **Supersedes the comment prose in** `[[2026-06-08_comment-drafts]]` — which remains the canonical record for verified post texts, retrieval provenance, skips (11) and unverified accounts (14). **Nothing here is approved or posted.** Route: Sead pre-review → Markos Stage 2.

## How these were produced

Workflow `vom-redraft-v32` (2026-06-10) under comment-craft **v3.2**: one agent per account, drafting from Markos's 13 real comments (`_analysis/2026-06-04-comment-feedback-markos-responses-and-voice-synthesis.md` Appendix A) with assigned opener moves, the red-line tell list, credential rotation, and length discipline. **No post was re-retrieved** — all post texts come verbatim from the 2026-06-08 record; framework / zone / tier / story-gating decisions preserved from that batch.

## Batch QA (the v3.2 gate — first run)

- **Red-line tells in final drafts: 0** (the 2026-06-08 batch had ~40 hits incl. "25 years" 9x).
- **Length distribution: 24 short (1–3 sentences) · 11 mid (4–5) · 0 long (6–8)** — the old batch was almost uniformly 4–8.
- **Opener-pattern clustering:** 12 paraphrase-level clusters found across first drafts; 17 drafts force-re-drafted until openers diverged. One hand-fix after QA (April Dunford — removed a guideline-ish Zero Trust definition the lineup judge flagged as a brand-deployment tell).
- **Blind lineup (advisory, honest result):** the judge still sorts system-vs-Markos — but chiefly via his raw typing noise (double periods, space-before-"?", dropped subjects), which we deliberately do NOT fake (PRINCIPLES.md / voice.md v3.5: no injected typos). Residual register tells the judge named on system drafts: occasional engineered three-beat builds and polished closers. That is the next thing Sead should read for.


# Pool 1 — New 15 (Band H)

## Nathan Benaich

🔗 https://www.linkedin.com/posts/nathanbenaich_air-street-capital-fund-iii-232m-for-ai-first-activity-7441717877650546689-f91V

**Comment (v3.2):**

Congratulations Nathan - largest solo GP in Europe is a serious milestone ( and $232,323,232 is a great number ). Good luck to the founders of the third epoch!

— Agree-and-Add · Green Zone / Tier 2 · story: none · opener: plain congrats in his words

---

—

🔗 https://www.linkedin.com/posts/nathanbenaich_2026-is-gonna-be-huge-sereact-activity-7413189829263527937-qli0

**Comment (v3.2):**

Cycle time end to end is the one I would pin up - picking faster while orders sit in queues is the classic local optimisation trap, and it shows up well beyond fulfilment. Saw it for years in enterprise software in my last business - the metric that demos well gets the budget, and the constraint moves to wherever nobody is measuring. Inventory truth is underrated too - bad data locks up capital and the manual workarounds it creates rarely make it into the ROI model. All seven or it does not pay back.

— Agree-and-Add · Green Zone / Tier 1 · story: none (light credential via rotation bank: "in my last business" — banned 25-years phrasing dropped) · opener: assertion-first

---

## Sarah Guo

🔗 https://www.linkedin.com/posts/sarahxguo_dark-code-activity

**Comment (v3.2):**

"Dark code" is going to stick - I have sat through enough incident calls where every service stayed inside its permissions and still nobody could say what actually ran. Your example turns on the agent being gone before anyone went looking, so whatever trail the agent kept went with it - the audit has to live platform-side, outside the agent's lifetime. In practice that means a small set of pre-declared actions an agent can invoke ( each one logged with the trigger, the data touched, where the results landed ) and runtime caches treated as owned surfaces, since a shared cache is exactly where this one leaked. Get that plumbing in early and "who did this" becomes a query instead of a four day reconstruction - the difference between a bad afternoon and a CEO glued to the incident channel.

— Agree-and-Add · Green Zone / Tier 2 · story: Story 2 (enterprise career) deployed lightly via experience-implicit rotation phrasing ('I have sat through enough incident calls') — banned 25-years line dropped; pillar 1 (AI-as-one-component) + pillar 6 (governance/auditability as a build concern) carried in the platform-side-audit take · opener: experience-implicit

---

## Harrison Chase

🔗 https://www.linkedin.com/posts/harrison-chase-961287118_announcing-langchain-and-langgraph-10-activity-7386795886137434114--AC0

**Comment (v3.2):**

Middleware in the agent loop is the right call - that is the obvious home for permissioning and for keeping a record of what an agent actually did, whatever model sits underneath. Pairs well with the standard content blocks too: swap the model, keep the controls. Congrats on 1.0 - and well done leading with the docs, that is half the adoption battle!

— Agree-and-Add · Green Zone / Tier 2 · story: none (build-level take; no credential deployed — preserved from original decision) · opener: take-first

---

—

🔗 https://www.linkedin.com/posts/harrison-chase-961287118_today-were-excited-to-announce-new-funding-activity-7386446903250608128-vWzN

**Comment (v3.2):**

If I had to bet which product closes the Cisco and Workday end of that customer list, it is LangSmith, not the agent builder. I have been through security-control audits in some of the most restrictive environments I have worked in, and they always start with evidence - what controls exist, and proof of what the system actually did. Put an agent in the middle and that evidence requirement grows fast ( every tool call, every decision it made on its own ). Traces are exactly that proof - without them an agent stays in pilot, and pilots do not carry enterprise budgets.

— Agree-and-Add · Yellow Zone / Tier 2 · story: Story 8 — Official Secrets Act / classified-agency security-control audits, deployed abstractly (no agency/client names) per the original gating decision; not reused on post 1 · opener: prediction · re-drafted in batch QA

---

## Jerry Liu

🔗 https://www.linkedin.com/posts/jerry-liu-64390071_im-excited-to-announce-that-llamaindex-is-activity-7457447965922734080-UVnC

**Comment (v3.2):**

The agents part of the mission is the less forgiving one - a person spots a garbled scan and works around it, an agent takes the output at face value and acts. Well deserved, Jerry - no shortage of PDFs left.

— Agree-and-Add · Green Zone / Tier 2 · story: none · opener: plain congrats + one specific · re-drafted in batch QA

---

—

🔗 https://www.linkedin.com/posts/jerry-liu-64390071_parsebench-doc-ocr-for-ai-agents-leaderboard-activity-7454956913911459840-8VsK

**Comment (v3.2):**

This propagation problem is the same one we have always had with bad data at the bottom of a stack - it compounds, and by the time the wrong answer surfaces nobody is looking back at the parse that caused it. Scoring semantic faithfulness over character-level accuracy is the right yardstick for agents too. We went hard on this layer ourselves - I put a hierarchical knowledge graph under the whole system and took real pushback for it at the time ( overkill, why not just feed the model the files ? ) - and it is the call I would defend hardest now, because the agent works from typed, checked structure rather than whatever the OCR thought it saw. Off to see how the frontier VLMs stack up against the dedicated OCR tools on the leaderboard.

— Share-Experience · Green Zone / Tier 2 · story: Story 12 — Knowledge Graph / Architecture 'Hardest Decision' (Green) · opener: pattern-naming

---

## Sebastian Raschka

🔗 https://www.linkedin.com/posts/sebastianraschka_april-was-a-pretty-strong-month-for-open-weight-activity-7454183215042494464-Qp44

**Comment (v3.2):**

Reading the five together, almost every move is an attack on the attention bill - Gemma's sliding window, Qwen3.6 going mostly linear, GLM and Kimi both adopting DeepSeek's MLA. The closer the field gets to a settled set of tricks, the more realistic running this class of model on your own kit becomes - the May analysis will be a good read.

— Agree-and-Add · Green Zone / Tier 1 · story: none (open-source/sovereign-AI pillar as build-level reaction; credential kept free for post 2 per no-reuse rule) · opener: observation-from-the-material

---

—

🔗 https://www.linkedin.com/posts/sebastianraschka_on-an-llm-time-scale-it-has-been-a-while-activity-7427718512284012545-QH9V

**Comment (v3.2):**

The parity claim is the news, and your own caveat is the catch - I have rarely seen a benchmark number predict how a model behaves on a specific workload. Spent years visiting CIOs and heads of tech at large enterprises and not one decision closed on a leaderboard - it closed when the thing was proven on their estate, under their constraints. Open weights at 744B change what proving it means, because you can stand GLM-5 up yourself and run that test. And dropping layers from 92 to 78 to cut inference cost reads like the team knows exactly who will be doing that.

— Share-Experience · Green Zone / Tier 1 · story: Story 11 — Visiting CIOs at Fortune 100s (Green; gated in — enterprise evaluation/deployment of a flagship open-weight model is part of what the credential answers; structural, no customer names) · opener: concession-then-catch

---

## Maxime Labonne

🔗 https://www.linkedin.com/posts/maxime-labonne_lora-with-just-13-parameters-this-paper-activity-7426588009636126720-4qZr

**Comment (v3.2):**

Give it a year and we will be steering trillion-parameter models for specific tasks with a handful of bytes - the scaling trend here points straight at it ( bigger model, fewer trained parameters needed ). The RL vs SFT gap is what I keep chewing on - 13 parameters in bf16 to 91% on GSM8K while SFT at the same budget barely moves suggests the capability is already in the model and the sparse reward just finds it. Shame there is no repo - a result this neat needs other hands on it.

— Agree-and-Add · Green Zone / Tier 2 · story: none · opener: prediction

---

—

🔗 https://www.linkedin.com/posts/maxime-labonne_lfm2-colbert-350m-one-model-to-embed-activity-7388922578184196097-Kd3i

**Comment (v3.2):**

My take is the multilingual angle is the bigger deal here than the speed - store documents in English, query in Spanish or German with high accuracy, from a 350M model. We hit this building the hierarchical knowledge graph under our system - the hardest calls were never the generation step, they were how the data is organised and what comes back for a query, fast, without shipping everything to a big remote model. A retriever this small that keeps pace with models 2.3x smaller makes that design properly viable on the edge. Congrats on the first embedding model!

— Share-Experience · Green Zone / Tier 2 · story: Story 12 — Knowledge Graph / Architecture (Green, design-decision level) · opener: take-first

---

## Nathan Lambert

🔗 https://www.linkedin.com/posts/natolambert_people-dont-want-to-accept-that-the-top-activity-7426320555370426368-lH1Q

**Comment (v3.2):**

The pattern in your top 10 is the tell - it is nearly all small models ( 8B, 7B, 3B, even a 0.6B Qwen ), not the big flagship weights. Matches what I see in regulated organisations - a small fully-open model they can run on their own hardware clears security review in a way an API never will, and once it is wired into the pipelines nobody rips it out for a couple of benchmark points. That is the Llama inertia right there - 53M downloads of a previous-generation 8B says the install base moves a lot slower than the benchmarks, and I suspect it always will.

— Agree-and-Add · Green Zone / Tier 1 · story: none (story-gate held: family-company / Visa / GCP-fraud credentials don't answer 'which open models get used'; light experience-implicit proof only — 'Matches what I see in regulated organisations' — no anchored story, no 25-years phrasing) · opener: pattern-naming

---

## Oliver Patel

🔗 https://www.linkedin.com/posts/oliver-patel_agentic-ai-increases-both-the-opportunities-activity-7429813504624320512-DXcU

**Comment (v3.2):**

One hallucination early in a chain gets treated as fact by every step after it - which is why I would not look to the model layer for a fix, since as you say there is no foolproof one coming. In the agentic systems I build, the control surface ends up being everything around the model - what an agent is scoped to touch, which actions wait for a human sign off, what gets logged so you can walk the chain back when something does go wrong. A bad token will still happen - the engineering question is how far it travels before something catches it. That is what turns risk appetite into a real conversation rather than a number on a slide.

— Agree-and-Add · Green Zone / Tier 1 · story: none (per recorded gate: pillar 6 + pillar 1 as position; Yellow stories GCP-fraud and OSA-audits stay gated out; old draft's 25-years credential dropped and replaced with a light rotation-bank-style builder phrasing — 'in the agentic systems I build') · opener: concession-then-catch · re-drafted in batch QA

---

—

🔗 https://www.linkedin.com/posts/oliver-patel_ai-governance-is-getting-even-harder-in-2026-activity-7417159828650778624-7rhR

**Comment (v3.2):**

Governance that ships inside the build platform is the only version I have seen hold up under this kind of pressure - scoped permissions, sign-off steps and an audit log right where the agents get made, so the compliant route is also the fastest one. Stand a separate review board in front of citizen-developer volume and it becomes a backlog people learn to route around - which is precisely the friction you say will be challenged. The regulations at least hold still long enough to track - a few thousand employees shipping agents do not. Strap in indeed!

— Agree-and-Add · Green Zone / Tier 1 · story: none (per recorded decision: no story, no credential; keeps the ROI/democratised-access lead and stays deliberately different from the post-1 build take; banned bolt-on/design-in contrast from the old draft removed) · opener: easy-half-pivot (engagement folded in - it lasers on his own ROI/under-the-microscope paragraph as the hard half) · re-drafted in batch QA

---

## Kai Waehner

🔗 https://www.linkedin.com/posts/kaiwaehner_apachekafka-zookeeper-migration-activity-7377274430047166464-Keka

**Comment (v3.2):**

In every enterprise I have worked with, old plumbing caused far more incidents than missing features ever did - so I understand exactly why years of Kafka engineering went into taking a component out rather than adding anything new. My father built the Visa credit card system after years of failed attempts by others - he began by cutting the scope down to what had to work, and KRaft is the same kind of cut at the coordination layer. Running it on tens of thousands of clusters with no downtime ahead of asking the wider install base to migrate - that is how you earn the right to take something away from everyone.

— Agree-and-Add · Green Zone / Tier 1 · story: Story 4 — Father's Visa credit card descope (Green) · opener: experience-implicit · re-drafted in batch QA

---

# Pool 2 — From the v1 master

## Andrew Ng

🔗 https://www.linkedin.com/posts/andrewyng_one-of-the-new-buzzy-jobs-in-silicon-valley-activity-7467243316431036416-fzyJ

**Comment (v3.2):**

@Andrew, agree on the optionality piece - companies remember what welding their processes to one vendor's stack cost them last time round. Ratio in enterprise software ran around 10-15x in my last business, and the embedded engineer is exactly where that services tail lives - I suspect the same maths repeats with agentic workflows ( tokens this time, not licences ). FDEs are great at the messy first mile - the lasting value is the client's own AI Engineers being able to run and extend those workflows on their own. On the fragmentation, my bet is Evals Engineers break off first - most deployments I see are gated on testing and evals rather than the build.

— Agree-and-Add · Green Zone / Tier 3 (Markos sends himself — major industry figure) · story: Story 10 — Enterprise services ratio, deployed per gate with his real phrasing ('Ratio in enterprise software ran around 10-15x in my last business'); light Story 11 optionality/vendor-lock-in reference, no credential beyond the ratio line · opener: @-mention-agree

---

## Yann LeCun

🔗 https://www.linkedin.com/posts/yann-lecun_boom-a-clean-recipe-to-train-jepa-world-activity-7441886063993847808-aUCH

**Comment (v3.2):**

15M params, 1 GPU, full planning in under a second - those numbers move world models out of datacentre territory and onto the edge. The no-heuristics part is the bit I rate most - every hand-tuned trick in a training recipe is a thing that breaks later when the data shifts, so end-to-end stability matters more in production than another benchmark point. And a model this small can sit on-device, right next to the user's data - that is a different class of product to one calling home for every plan.

— Agree-and-Add · Green Zone / Tier 2 · story: none (Story 12 gated out — knowledge-graph story does not answer a JEPA training-recipe post) · opener: observation-from-the-material

---

—

🔗 https://www.linkedin.com/posts/yann-lecun_v-jepa-21-a-new-jepa-model-trained-on-video-activity-7440421830177259520--LnI

**Comment (v3.2):**

Question on the planning side: do the multi-level hierarchy features carry once the horizon stretches well past short-term anticipation? For agent work that is where this model earns its keep - an agent can pick up segmentation and tracking from plenty of places, but a world model it can plan against over real horizons is the scarce piece.

— Question-and-Extend · Green Zone / Tier 2 · story: none · opener: take-first + genuine build question · re-drafted in batch QA

---

## Fei-Fei Li

🔗 https://www.linkedin.com/posts/fei-fei-li-4541247_love-this-essay-from-world-labs-team-just-activity-7434708662994128896-cMYA

**Comment (v3.2):**

The strength of 3D as an interface is that machine and human work off the same artefact - the model plans in it, you walk through it and check it, nothing gets lost in translation between the two. We made a similar bet with the knowledge graph underneath our product - one structure the retrieval layer queries and the user can open and audit, and it was the piece that took longest to get right. Ownership is the question it opens up for me - a universal interface becomes a different proposition when the world inside it is assembled from data you actually own.

— Agree-and-Add · Green Zone / Tier 2 · story: Story 12 (knowledge graph / architecture 'hardest decision') — deployed lightly at design-decision level, per the original gate decision; no years-credential, authority carried by the technical specifics · opener: take-first · re-drafted in batch QA

---

## Aravind Srinivas

🔗 https://www.linkedin.com/posts/aravind-srinivas-16051987_what-has-perplexity-been-up-to-last-two-months-activity-7432463792590172160-QHCE

**Comment (v3.2):**

Specialised models sitting in the same tool class as the file system, CLI and browser - once that move is in, an overnight run can fan out across 19 of them, and that is a lot of actions to trace back afterwards. We hit the same wall with the hierarchical knowledge graph behind our own system - attribution got hard well before capability did. And for anything reading mail, files and calendars, usage-based pricing instead of ads keeps the incentives on the user's side - which matters as much as the model list. Do users get a per-step view of which model did what after a run, or only the model picks up front ?

— Agree-and-Add · Green Zone / Tier 2 · story: Story 12 (knowledge graph / architecture 'hardest decision') — referenced lightly as architectural-conviction credential, per the original gate decision; re-phrased fresh ('the hierarchical knowledge graph behind our own system'), same specificity · opener: assertion-first · re-drafted in batch QA

---

## Allie K. Miller

🔗 https://www.linkedin.com/posts/alliekmiller_not-everyone-is-going-to-be-a-developer-activity-7468718032589094912-Hrdr

**Comment (v3.2):**

Sending this clip to the non-technical half of my team - "code equals solutions" is the right reframe for them. In my last business every licence dollar pulled 10-15 behind it in services, mostly the data, access and plumbing around whatever got built. Four citizen developers for every professional only works if that layer holds up - and that is the readiness question sitting inside the Gartner number.

— Agree-and-Add · Green Zone / Tier 2 · story: Story 10 (15:1 enterprise services ratio) — deployed via rotation-bank credential phrasing ("in my last business"), banned 25-years phrasing dropped · opener: direct-action

---

—

🔗 https://www.linkedin.com/posts/alliekmiller_stop-using-ai-chat-threads-and-do-this-instead-activity-7468659274072768512-D9_g

**Comment (v3.2):**

An interface that only needs to live for one meeting is a different kind of software - no polish, no backlog, no engineer required, which is exactly why the people who actually own the problem will build these themselves. Rings true from designing our own product: the decisions we sweated over all sat in the scaffolding round the model ( which data it gets handed, what shape the answer comes back in ) and that layer is where the usefulness came from - choosing the model itself took an afternoon. Two or three years out I expect a decent chunk of everyday business software to work like this: built for the task, used, binned.

— Agree-and-Add · Green Zone / Tier 2 · story: Story 12 (knowledge graph / architecture "hardest decision") — design-level reference, fresh phrasing · opener: pattern-naming · re-drafted in batch QA

---

## Ethan Mollick

🔗 https://www.linkedin.com/posts/emollick_one-reason-you-want-ais-to-be-better-writers-activity-7469135125398695936-wYaf

**Comment (v3.2):**

Nobody read that menu before it went live - the model wrote a weak first draft and the first draft was the finished product. A banned-phrase list in the system prompt and a release eval that rejects "delve" would have caught it for pennies - the editing pass vanished the moment first drafts stopped costing anything. And per-user generated copy makes it harder again, because there is no build left for a human to stand in front of.

— Agree-and-Add · Green Zone / Tier 3 (Markos-handles — major industry figure) · story: none (gated out — family-company/services-ratio/Visa stories don't fit AI prose quality; authority carried by technical specifics) · opener: concession-then-catch · re-drafted in batch QA

---

## Luiza Jarovsky

🔗 https://www.linkedin.com/pulse/ai-literacy-fundamental-right-luiza-jarovsky-phd-1r4of

**Comment (v3.2):**

Teenagers are teaching themselves these tools faster than any school system can react - the classroom is where AI literacy lands last, not first. The legal point is the striking one ( not a single country has written AI literacy into law ). Access is the other half I would argue for - the AI an ordinary family can get its hands on is a fraction of what a large enterprise or a government department runs every day, and that is the part legislation could genuinely change.

— Agree-and-Add · Green Zone / Tier 3 · story: Pillar 3 (Democratising AI and Education) sound-bites — households vs Fortune 1000s/governments + next generation self-teaching, schools as lagging indicator. No Yellow-gated specific story deployed (preserved from original draft). · opener: prediction · re-drafted in batch QA

---

—

🔗 https://www.luizasnewsletter.com/p/a-manifesto-for-biological-intelligence

**Comment (v3.2):**

Spent years building AI products and the model is honestly the smallest piece of any of them - retrieval, ontology, guardrails, evals, all of it human judgement designed in before a single token is generated. Which makes 'secondary and invisible' a question of architecture as much as a trend - the failed AI projects I have seen all handed the whole job to the model, and the human ingenuity was the first thing to vanish. Agree we are the last generation educated without this - which also makes us the one that decides where the biological mind sits in these systems, and I would rather we choose that deliberately than find out later.

— Another-Angle · Green Zone / Tier 3 · story: Pillar 1 (Pragmatic AI Implementation / systems-thinker) sound-bites — the model is one component of the system, treating it as the whole thing is how projects fail. No Yellow-gated specific story deployed; different pillar from post 1, no credential reuse (preserved from original draft). · opener: experience-implicit

---

## Pascal Bornet

🔗 https://www.linkedin.com/posts/pascalbornet_artificialintelligence-ai-aitransformation-activity-7445409779126046721-bFm-

**Comment (v3.2):**

Agents inherit whatever data layer they sit on, which makes data quality and clear ownership the two items here that set the ceiling for everything else - credit for naming them, most AI-first roadmaps go straight past both. Seen this play out on our own build: the hierarchical knowledge graph underneath took the longest to get buy-in early on ( ontologies do not demo well ), and it is the single reason retrieval has held together as the data got big and messy.

— Agree-and-Add · Green Zone / Tier 2 · story: Story 12 (Knowledge Graph / architecture as the invisible foundation) — deployed per gate; banned 25-years credential dropped, no replacement credential needed · opener: take-first · re-drafted in batch QA

---

—

🔗 https://www.linkedin.com/posts/pascalbornet_technology-ai-workplace-activity-7444307466890366978-vZFT

**Comment (v3.2):**

The expensive part of that warning is already here - the scaling bet is big enough now that getting off the path costs someone their narrative as well as their capex. I predict this one gets settled sideways: agents on today's models, with decent scaffolding and memory around them, keep clearing work that was filed under 'needs AGI'. We may never find out whether scaling was the wrong path - it may simply stop mattering.

— Agree-and-Add · Green Zone / Tier 2 · story: none (Story 12 used on post 1, no-reuse window; no other credential fits) · opener: observation-from-the-material

---

## April Dunford

🔗 https://aprildunford.substack.com/p/positioning-in-the-age-of-ai

**Comment (v3.2):**

Positioning against the competitors a buyer is weighing up today is harder than it sounds when the product is AI-native - the temptation to fight the imaginary future competitor is constant. We lived this with MyVault: every instinct said open with the AI, but conversations only moved once we led with the problem people already have and got precise on the claims - Zero Trust, not the grander "zero-knowledge" the category likes to wave around. Lead with the vision, close on the problem - matches our experience exactly.

— Agree-and-Add · Green Zone / Tier 2 · story: none (light, gated reference to positioning MyVault on Zero Trust — on-topic per gate; no credential story deployed) · opener: assertion-first · re-drafted in batch QA

---

## Jason Lemkin

🔗 https://www.linkedin.com/posts/jasonmlemkin_for-our-ai-agent-stack-we-bought-as-much-activity-7437961872512864256-Qgas

**Comment (v3.2):**

Our version of that build was the knowledge graph sitting under everything we make - we tried hard to buy one, nothing on the market did the job, and it turned into the decision we fought over hardest ( and the layer the whole stack now rests on ). Your AI VP Marketing reads the same to me: the 5+ years of data is the part no vendor can sell you. And when third-party agents do get good enough to swap in, they inherit all of that - which is why waiting works in your favour.

— Agree-and-Add · Green Zone / Tier 2 · story: Story 12 — Knowledge Graph / Architecture 'Hardest Decision' (deployed per gate: post's 'doesn't exist off the shelf' directly answers it) · opener: experience-implicit · re-drafted in batch QA

---

—

🔗 https://www.linkedin.com/posts/jasonmlemkin_my-1-piece-of-advice-for-gtm-leaders-in-activity-7413675413358436352-GVGq

**Comment (v3.2):**

No agency, no handing it down the org chart - the 30 days of daily correction is exactly the point. You learn where your data is thin, what each iteration costs, how the thing fails ( the vendor demo covers none of that ). 50-60 hours is cheap next to what buying blind costs you afterwards.

— Agree-and-Add · Green Zone / Tier 2 · story: none (old draft's '25-years' light credential dropped entirely per red line; authority carried by the post's own specifics) · opener: @-mention-agree · re-drafted in batch QA

---

## Zach Perret

🔗 https://www.linkedin.com/posts/zperret_effects-2026-an-event-on-the-future-of-activity-7460067101425315841-C2Hi

**Comment (v3.2):**

Good week to be asking where AI in finance actually stands - it is the one vertical where consumer-permissioned data already works at scale, and that is a decade of Plaid groundwork ( people connect an account when the value is obvious and they can switch it off again ). My guess for the product launches: the next consumers of those rails are agents acting on the customer's behalf - what does a Plaid connection look like when it is an agent asking for the access?

— Question-and-Extend · Green Zone / Tier 2 · story: none · opener: take-first + genuine build question

---

## Lenny Rachitsky

🔗 https://www.linkedin.com/posts/lennyrachitsky_here-are-the-full-transcripts-from-all-320-activity-7417011928159629313-am-q

**Comment (v3.2):**

Generous of you to share these - and to keep adding as new episodes land. 320 also happens to be an ideal corpus size to learn retrieval on: well past what a context window holds, small enough for one person to do it properly - chunk on speaker turns, pair keyword with semantic search, eval against the episodes you know inside out.

— Agree-and-Add · Green Zone / Tier 3 · story: none · opener: observation-from-the-material · re-drafted in batch QA

---

—

🔗 https://www.linkedin.com/posts/lennyrachitsky_best-of-lennys-newsletter-2026-my-25-best-activity-7414351256925712384-2iqT

**Comment (v3.2):**

There is an eight-year-old I know who pays for his own Claude and Lovable subscriptions out of pocket money and just gets on with building things - no course, no curriculum, no permission asked. Which is why the '50 ways non-technical people use Claude Code' one undersells it if anything - this is already happening well below working age. It also puts a shelf life on the 25-tactics-for-enterprise-adoption problem - in a few years the new hires turn up already fluent.

— Agree-and-Add · Yellow Zone / Tier 3 · story: Story 5 — son's Claude/Lovable subscriptions (anonymised to 'an eight-year-old I know') · opener: direct-action · re-drafted in batch QA

---

## Tomasz Tunguz

🔗 https://tomtunguz.com/using-local-ai-to-work-faster/

**Comment (v3.2):**

Steel already ran this experiment - the integrated mills had the scale advantage and still lost to minimills sitting next to their customers, and a model on the same machine as the work is that bet replayed. Queue age at 4 seconds instead of 73 is the figure I would put in front of a CFO. And the 78% has headroom - 128Gb shared-memory desktops are becoming ordinary kit, and distilled models keep eating more of the routine end of the workload.

— Agree-and-Add · Green Zone / Tier 2 · story: none (opinion pillar — AI on the edge / small models; no credential story per gate) · opener: prediction · re-drafted in batch QA

---

—

🔗 https://tomtunguz.com/tokens-per-result/

**Comment (v3.2):**

Intelligence per dollar is the buyer's spreadsheet finally reaching the model layer. Rings familiar - services in my last business ran around 10-15x the licence, because the metered unit was never where the cost of a real outcome sat. The application layer will hit the same maths: a closed ticket sounds priceable until you add the evals, guardrails and orchestration that make it trustworthy, and that spend never appears in a token count. Same score, 40% more expensive - procurement will sort that out quicker than the benchmarks do.

— Share-Experience · Green Zone / Tier 2 · story: Story 10 — Enterprise Services Ratio (10-15x), Green status, deployed per gate with his real phrasing · opener: assertion-first

---

## Next actions

1. **Sead pre-review** of all 35 (he raised the template-echo flag — his pass gates this batch).
2. **Markos Stage 2 round** on the Sead-passed set — his edits land in `markos-edits-log.md` (Loop 1 ground truth). Tier 3 items (Ng, LeCun, Mollick, Lenny, Luiza) are his to send personally.
3. **Skips and unverified accounts** unchanged from `[[2026-06-08_comment-drafts]]` — unverified resolve via the human-in-the-browser capture step.

*Generated 2026-06-10 via workflow `vom-redraft-v32` under comment-craft v3.2 + Batch QA (CLAUDE.md).*
