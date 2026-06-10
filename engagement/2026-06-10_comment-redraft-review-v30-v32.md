# Voice of Markos — Comment Re-draft Review (v3.0 → v3.2)

**For:** Sead (pre-review) · **Date:** 2026-06-10 · **Status:** DRAFTS ONLY — nothing approved or posted

Same 35 comments, same accounts, same verified posts, same framework/tier/story decisions. What changed between versions: the v3.2 texture system (drafted from Markos's 13 real comments, banned-tell red lines, credential rotation — the "25 years" line is retired) and the length rule (short by default, long only when earned).

**Batch QA on the new set:** 0 banned tells (old batch ~40, incl. "25 years" 9×) · length spread 24 short / 11 mid / 0 long (old batch almost uniformly 4–8 sentences) · 17 drafts force-re-drafted after opener-pattern clustering.

**What to read for:** does each comment sound like Markos typed it in the moment? The known residual tell is over-engineered three-beat builds and polished closers — flag any you see.

---

# Pool 1 — New 15 (Band H)

## 1. Nathan Benaich

🔗 https://www.linkedin.com/posts/nathanbenaich_air-street-capital-fund-iii-232m-for-ai-first-activity-7441717877650546689-f91V  ·  2026-03-23

**Post:**

> News! Air Street Capital has raised $232,323,232 for our third epoch to back AI-first companies from the earliest stages in North America and Europe. With Fund III, Air Street Capital is now the largest solo GP venture capital firm in Europe. We could not have made this progress without the hard work and ambition of our founders. It is a privilege to partner with you. To the steadfast AI founder: come join our third epoch. We begin today.

**Previous comment (v3.0, 2026-06-08):**

Congratulations — largest solo GP in Europe is a real milestone, and the part worth dwelling on is the thesis: earliest-stage, AI-first across software, science, the physical world and defence. From what I've seen, the AI-first companies that actually last treat AI as one critical component of a much bigger system rather than the whole product — that's usually what separates an AI-first company from an AI wrapper. Strong group of founders to be building Fund III around.

**Updated comment (v3.2, 2026-06-10):**

Congratulations Nathan - largest solo GP in Europe is a serious milestone ( and $232,323,232 is a great number ). Good luck to the founders of the third epoch!

<sub>Agree-and-Add · Green Zone / Tier 2 · story: none · opener move: plain congrats in his words</sub>

---

## 2. Nathan Benaich

🔗 https://www.linkedin.com/posts/nathanbenaich_2026-is-gonna-be-huge-sereact-activity-7413189829263527937-qli0  ·  2026-01-02

**Post:**

> 2026 is gonna be huge Sereact. Happy 2026. Budgets are approved. Slides are recycled. Reality is unchanged. In 2026, automation projects still fail for one reason. Teams measure ROI too late and on the wrong metrics. Here's what actually moves the needle: Throughput per system — if orders per hour don't go up, nothing else matters. €/Pick — labour is still 60–65% of fulfilment cost. Track cost per pick, not headcount. Accuracy under load — 99% in a demo is meaningless. What matters is accuracy at peak volume. Cycle time end to end — picking faster does nothing if orders still wait in queues. Inventory truth — bad inventory data locks up capital and creates manual work everywhere else. Space per order shipped — if automation doesn't delay your next building expansion, ROI is capped. Uptime in production — downtime is the hidden tax no business case accounts for. Most €1m+ automation projects don't fail because robots are bad. They fail because teams optimise one metric and ignore the system. Real ROI shows up when all seven move together. That's the difference between automation that looks good on slides and systems that actually pay back. Back to work.

**Previous comment (v3.0, 2026-06-08):**

You nailed the failure mode — teams optimise one metric and ignore the system. I've watched the same pattern across 25 years of enterprise delivery: a project gets judged on the one number that demoed well, and the other six quietly cap the return. The 'accuracy under load' point is the one most business cases skip — 99% in a demo and 99% at peak volume are effectively two different products. And €/pick is the honest one, because labour doesn't disappear, it moves, and if you're not tracking where, the ROI math drifts. The real version of automation ROI is exactly what you said: all seven moving together, not one line on a slide.

**Updated comment (v3.2, 2026-06-10):**

Cycle time end to end is the one I would pin up - picking faster while orders sit in queues is the classic local optimisation trap, and it shows up well beyond fulfilment. Saw it for years in enterprise software in my last business - the metric that demos well gets the budget, and the constraint moves to wherever nobody is measuring. Inventory truth is underrated too - bad data locks up capital and the manual workarounds it creates rarely make it into the ROI model. All seven or it does not pay back.

<sub>Agree-and-Add · Green Zone / Tier 1 · story: none (light credential via rotation bank: "in my last business" — banned 25-years phrasing dropped) · opener move: assertion-first</sub>

---

## 3. Sarah Guo

🔗 https://www.linkedin.com/posts/sarahxguo_dark-code-activity  ·  2026-04-01

**Post:**

> A few months ago, a founder I know had a data leak that took his security team four days to understand. That's a long time for a CEO to be glued to an incident channel. Customer data from one tenant was showing up in another tenant's dashboard. A non-technical employee had connected a customer data API into a reporting pipeline, and an agent in the middle selected steps at runtime that cached results somewhere another service could read. Every individual service stayed within its permissions. Nothing was obviously misconfigured. The path only existed at runtime, assembled by an agent that no longer existed by the time anyone went looking. When the security lead tried to answer the most basic question — who did this — they couldn't. This is dark code: behavior in production that nobody can explain end-to-end. Not just unreviewed code, but systems whose behavior emerges from interactions between components — often at runtime — without anyone ever holding a complete mental model of what the system actually does.

**Previous comment (v3.0, 2026-06-08):**

The line that lands hardest for me is "the path only existed at runtime, assembled by an agent that no longer existed by the time anyone went looking." That's the real shift — the failure wasn't a misconfigured service, it was that no one held a complete mental model of the system at the moment it acted. In 25 years building enterprise systems I've watched teams treat the model as the system, when the model is doing maybe 10% of the work — the other 90% is architecture, retrieval, data plumbing and audit. The orgs that won't have your founder's four-day incident are the ones that scoped the agent's primitives narrowly and made every runtime step auditable after the fact, so "who did this" has an answer that doesn't depend on the agent still existing. Governance here isn't a work-practice you bolt on; it's a system property you design in — the audit log and the permission boundary have to assume the agent is gone. Curious whether you're seeing the strongest teams solve this at the orchestration layer or by constraining what an agent is allowed to assemble at runtime in the first place.

**Updated comment (v3.2, 2026-06-10):**

"Dark code" is going to stick - I have sat through enough incident calls where every service stayed inside its permissions and still nobody could say what actually ran. Your example turns on the agent being gone before anyone went looking, so whatever trail the agent kept went with it - the audit has to live platform-side, outside the agent's lifetime. In practice that means a small set of pre-declared actions an agent can invoke ( each one logged with the trigger, the data touched, where the results landed ) and runtime caches treated as owned surfaces, since a shared cache is exactly where this one leaked. Get that plumbing in early and "who did this" becomes a query instead of a four day reconstruction - the difference between a bad afternoon and a CEO glued to the incident channel.

<sub>Agree-and-Add · Green Zone / Tier 2 · story: Story 2 (enterprise career) deployed lightly via experience-implicit rotation phrasing ('I have sat through enough incident calls') — banned 25-years line dropped; pillar 1 (AI-as-one-component) + pillar 6 (governance/auditability as a build concern) carried in the platform-side-audit take · opener move: experience-implicit</sub>

---

## 4. Harrison Chase

🔗 https://www.linkedin.com/posts/harrison-chase-961287118_announcing-langchain-and-langgraph-10-activity-7386795886137434114--AC0  ·  circa 2025-11 (LinkedIn rendered as '7 months ago' on 2026-06-08; exact date login-walled)

**Post:**

> 🥳Announcing LangChain and LangGraph 1.0  LangChain and LangGraph 1.0 versions are now LIVE!!!! For both Python and TypeScript  Some exciting highlights: - NEW DOCS!!!! - LangChain Agent: revamped and more flexible with middleware - LangGraph 1.0: we've been really happy with LangGraph and this is our official stamp of approval - Standard content blocks: swap seamlessly between models  Read more about it here: [https://lnkd.in/g5mdBTTs]  We hope you love it!

**Previous comment (v3.0, 2026-06-08):**

The middleware line in the agent revamp is the part I'd underline — that's where a lot of the real engineering lives. Once agent behaviour runs through middleware, you've got a natural place to enforce scoped permissions and write an audit trail of what the agent was actually allowed to touch and why. In my experience shipping systems across enterprise, that's the layer that decides whether "you can't just blame the AI" holds up: when something goes wrong, the org owns the outcome, and a middleware seam is what makes the outcome reconstructable instead of a shrug at the model. Standard content blocks across models help here too — model-swapping is a lot less scary when the governance and observability sit one layer above the model rather than inside it.

**Updated comment (v3.2, 2026-06-10):**

Middleware in the agent loop is the right call - that is the obvious home for permissioning and for keeping a record of what an agent actually did, whatever model sits underneath. Pairs well with the standard content blocks too: swap the model, keep the controls. Congrats on 1.0 - and well done leading with the docs, that is half the adoption battle!

<sub>Agree-and-Add · Green Zone / Tier 2 · story: none (build-level take; no credential deployed — preserved from original decision) · opener move: take-first</sub>

---

## 5. Harrison Chase

🔗 https://www.linkedin.com/posts/harrison-chase-961287118_today-were-excited-to-announce-new-funding-activity-7386446903250608128-vWzN  ·  circa 2025-11 (LinkedIn rendered as '7 months ago' on 2026-06-08; exact date login-walled)

**Post:**

> 🔥Today we're excited to announce new funding for LangChain (at a $1.25B valuation) to allow us to build the platform for agent engineering. LangChain started as a single Python package 3 years ago. Since then, we've evolved into a comprehensive platform for agent engineering (LangGraph, LangSmith). Our tools now power AI teams like Replit, Clay, Harvey, Vanta, Cloudflare, Rippling, Cisco, Workday, and many more... And what I'm most excited about today is that we're launching a number of new features and products: an insights agent in LangSmith, 1.0 releases of LangChain and LangGraph, and a no-code agent builder... We are in the middle of a transformational technological shift, and are always looking for partners along the way. Whether you have feedback for us, want to work with us, or want to join us - please reach out!

**Previous comment (v3.0, 2026-06-08):**

Congratulations — and the phrase "platform for agent engineering" is the right framing; the discipline is finally catching up to the demos. The bit I'd add from years of shipping systems into regulated and classified environments: the moment agents act on real systems, observability stops being a debugging nicety and becomes the accountability record. The insights agent in LangSmith is interesting precisely because traces are what let an organisation answer "what was the agent permitted to do, and who owns it when it goes wrong" — that's the question auditors actually ask, and it's where "blame the AI" stops being an acceptable answer.

**Updated comment (v3.2, 2026-06-10):**

If I had to bet which product closes the Cisco and Workday end of that customer list, it is LangSmith, not the agent builder. I have been through security-control audits in some of the most restrictive environments I have worked in, and they always start with evidence - what controls exist, and proof of what the system actually did. Put an agent in the middle and that evidence requirement grows fast ( every tool call, every decision it made on its own ). Traces are exactly that proof - without them an agent stays in pilot, and pilots do not carry enterprise budgets.

<sub>Agree-and-Add · Yellow Zone / Tier 2 · story: Story 8 — Official Secrets Act / classified-agency security-control audits, deployed abstractly (no agency/client names) per the original gating decision; not reused on post 1 · opener move: prediction</sub>

---

## 6. Jerry Liu

🔗 https://www.linkedin.com/posts/jerry-liu-64390071_im-excited-to-announce-that-llamaindex-is-activity-7457447965922734080-UVnC  ·  2026 (relative timestamp ~1mo at time of read; exact date not exposed without login)

**Post:**

> I'm excited to announce that LlamaIndex is on the CB Insights AI 100 list for 2026 🔥 We're on a mission to parse all of the world's PDFs, and make them accessible to both humans and AI agents. List: https://lnkd.in/gT--eBk2 If you haven't done so already, our website design is awesome, check it out: https://www.llamaindex.ai/

**Previous comment (v3.0, 2026-06-08):**

Congrats on the AI 100 — well earned. The line that lands for me is making documents accessible to both humans and AI agents, because that accessible layer is the actual unlock. In my experience shipping enterprise systems, the model is doing maybe 10% of the work; the other 90% is the structured layer underneath — parsing, retrieval, the knowledge graph that turns a pile of files into something an agent can reason over without hallucinating its way through. Most teams still treat that layer as plumbing rather than the product, which is exactly why projects stall after the demo.

**Updated comment (v3.2, 2026-06-10):**

The agents part of the mission is the less forgiving one - a person spots a garbled scan and works around it, an agent takes the output at face value and acts. Well deserved, Jerry - no shortage of PDFs left.

<sub>Agree-and-Add · Green Zone / Tier 2 · story: none · opener move: plain congrats + one specific</sub>

---

## 7. Jerry Liu

🔗 https://www.linkedin.com/posts/jerry-liu-64390071_parsebench-doc-ocr-for-ai-agents-leaderboard-activity-7454956913911459840-8VsK  ·  2026 (relative timestamp ~1mo at time of read; exact date not exposed without login)

**Post:**

> Frontier models are getting better at visual understanding, but up until now, they've lacked a good document parsing benchmark. This is a pre-requisite for any downstream agentic work automation; if the parser (frontier VLM or any OCR tool) outputs hallucinated context, then this propagates into downstream accuracy. This is why we built ParseBench, the most comprehensive enterprise document benchmark, tailored for semantic understanding by AI agents. Big thanks to Kaggle for featuring us. Check out the leaderboard to see which models are doing the best on document OCR so far!

**Previous comment (v3.0, 2026-06-08):**

The propagation point is the one I'd underline — a hallucinated parse upstream quietly becomes a confident wrong answer three steps downstream, and by then nobody can see where it entered. A benchmark that scores semantic faithfulness rather than just OCR character accuracy is the right instrument for that. When I designed the hierarchical knowledge graph under our own system I got pushback on it early — it felt like over-engineering next to 'just feed the docs to the model.' But that structured layer is precisely what stops the garbage-in problem you're describing: the agent reasons over a verified, typed representation, not over whatever the parser guessed. Treating parsing and the knowledge layer as foundational infra — not a preprocessing afterthought — is the part most teams underinvest in.

**Updated comment (v3.2, 2026-06-10):**

This propagation problem is the same one we have always had with bad data at the bottom of a stack - it compounds, and by the time the wrong answer surfaces nobody is looking back at the parse that caused it. Scoring semantic faithfulness over character-level accuracy is the right yardstick for agents too. We went hard on this layer ourselves - I put a hierarchical knowledge graph under the whole system and took real pushback for it at the time ( overkill, why not just feed the model the files ? ) - and it is the call I would defend hardest now, because the agent works from typed, checked structure rather than whatever the OCR thought it saw. Off to see how the frontier VLMs stack up against the dedicated OCR tools on the leaderboard.

<sub>Share-Experience · Green Zone / Tier 2 · story: Story 12 — Knowledge Graph / Architecture 'Hardest Decision' (Green) · opener move: pattern-naming</sub>

---

## 8. Sebastian Raschka

🔗 https://www.linkedin.com/posts/sebastianraschka_april-was-a-pretty-strong-month-for-open-weight-activity-7454183215042494464-Qp44  ·  2026-05 (approx; LinkedIn rendered "1 month ago" as of 2026-06-08)

**Post:**

> April was a pretty strong month for open-weight [LLM architecture releases]. A roundup of five: (1) Gemma 4 — sliding window attention for longer context at lower compute cost; (2) GLM-5.1 — a large MoE with multi-head latent attention (MLA) and DeepSeek Sparse Attention; (3) Qwen3.6 — hybrid stack, mostly linear-attention layers with periodic full attention, in 35B-A3B MoE and 27B dense variants; (4) Kimi K2.6 — a 1T-scale sparse MoE with DeepSeek-style MLA, showing that "frontier-scale models keep improving without major architecture changes ... except increasing the size"; (5) DeepSeek V4 — the most architecture-intensive of the bunch, adding manifold-constrained hyper-connections, compressed attention variants, hash-based routing, and a 1M-token context window. These are now in my LLM Architecture Gallery; more detailed analysis coming in May.

**Previous comment (v3.0, 2026-06-08):**

The line that jumps out is Kimi K2.6 proving frontier-scale models keep improving "except increasing the size" — convergence on MLA and DeepSeek-style sparse attention across teams that aren't coordinating. From where I sit, that convergence is the part with real enterprise consequence: when the open-weight field standardises on a few efficiency primitives, self-hosting a flagship-class model on your own hardware stops being a research stunt and becomes a procurement option. For an org with data-residency rules, the gallery you're building is quietly the most useful artefact going — it's the difference between auditing what you actually run and trusting a black box you rent.

**Updated comment (v3.2, 2026-06-10):**

Reading the five together, almost every move is an attack on the attention bill - Gemma's sliding window, Qwen3.6 going mostly linear, GLM and Kimi both adopting DeepSeek's MLA. The closer the field gets to a settled set of tricks, the more realistic running this class of model on your own kit becomes - the May analysis will be a good read.

<sub>Agree-and-Add · Green Zone / Tier 1 · story: none (open-source/sovereign-AI pillar as build-level reaction; credential kept free for post 2 per no-reuse rule) · opener move: observation-from-the-material</sub>

---

## 9. Sebastian Raschka

🔗 https://www.linkedin.com/posts/sebastianraschka_on-an-llm-time-scale-it-has-been-a-while-activity-7427718512284012545-QH9V  ·  2026-02-12

**Post:**

> On an LLM time scale, it has been a while since the last flagship open-weight architecture release. GLM-5 came out yesterday, and it is an interesting one. First, it is noteworthy because it appears to be on par with the major flagship LLM offerings, including GPT-5.2 extra-high, Gemini Pro 3, and Claude 4.6 Opus [though benchmark performance does not necessarily translate to real-world performance]. On scale: it nearly doubles parameters from 355B (GLM-4.5/4.7) to 744B, with active parameters per token rising from 32B to 40B — placing it between DeepSeek-V3.2 (673B) and Kimi K2 (1T). Architecturally it adopts DeepSeek's multi-head latent attention and sparse attention, expands experts from 160 to 256, raises embedding dim from 5,120 to 6,144, and notably reduces transformer layers from 92 to 78 to lower inference cost. The Chinese New Year window has become a reliable period for strong open-weight releases.

**Previous comment (v3.0, 2026-06-08):**

The caveat you slipped in — benchmark parity not necessarily translating to real-world performance — is the line I'd underline twice. When I was visiting CIOs and heads of tech at large enterprises, the leaderboard number was never what closed the decision; once they were genuinely bought in, what moved was whether the thing held up against their own data, their own latency budget, their own audit trail. An open-weight model at GLM-5's scale changes that calculus because you can actually self-host it and test against your own workload instead of taking the vendor's benchmark on faith. That layers-down-to-78 inference-cost move is the kind of detail that decides whether it's deployable on hardware a real org controls, which to me matters more than where it lands on a chart.

**Updated comment (v3.2, 2026-06-10):**

The parity claim is the news, and your own caveat is the catch - I have rarely seen a benchmark number predict how a model behaves on a specific workload. Spent years visiting CIOs and heads of tech at large enterprises and not one decision closed on a leaderboard - it closed when the thing was proven on their estate, under their constraints. Open weights at 744B change what proving it means, because you can stand GLM-5 up yourself and run that test. And dropping layers from 92 to 78 to cut inference cost reads like the team knows exactly who will be doing that.

<sub>Share-Experience · Green Zone / Tier 1 · story: Story 11 — Visiting CIOs at Fortune 100s (Green; gated in — enterprise evaluation/deployment of a flagship open-weight model is part of what the credential answers; structural, no customer names) · opener move: concession-then-catch</sub>

---

## 10. Maxime Labonne

🔗 https://www.linkedin.com/posts/maxime-labonne_lora-with-just-13-parameters-this-paper-activity-7426588009636126720-4qZr  ·  approx 2026 (LinkedIn dated it ~3 months ago at retrieval; references GPT 5.3 Codex)

**Post:**

> 🤏 LoRA with just 13 parameters! This paper from FAIR at Meta introduces a method that pushes parameter-efficient finetuning to absurd extremes, showing that RL (specifically GRPO) can unlock math reasoning in LLMs by updating as few as 13 parameters (just 26 bytes). → RL needs almost no capacity to work. With GRPO on Qwen2.5-7B-Instruct, 13 trained parameters in bf16 get you 91% on GSM8K (baseline is 76%). SFT at the same budget barely changes anything. → Bigger models are more "programmable" with tiny updates. The paper shows a clear scaling trend: as model size grows, fewer parameters are needed to reach 95% of full finetuning performance. A 7B model needs far fewer parameter tweaks than a 3B model for the same task. This suggests trillion-scale models may be trainable for specific tasks with literally a handful of bytes. → This technique works by projecting a tiny trainable vector through frozen SVD components. The method extends LoRA-XS by replacing the trainable r×r matrix with a vector v projected through fixed random tensors. Combined with weight tying across layers, this lets you go all the way down to a single trained parameter. → The SFT vs. RL gap is dramatic at low capacity. On GSM8K, RL with 120 parameters hits 95% accuracy. SFT with the same budget gets 84%. This gap only widens at smaller update sizes. The paper frames this through an information-theoretic lens: RL receives sparse but clean signal (binary reward), while SFT must absorb full-sequence information, most of which is task-irrelevant. → Qwen2.5 consistently needs ~10x fewer parameters than Llama 3 to reach equivalent performance. At 1 parameter, Qwen improves 5% over baseline while LLaMA barely budges. The authors themselves flag potential data contamination from pretraining, and independent research has found non-trivial benchmark overlap in Qwen's training data. I also think that it's a difference in terms of pre-training and midtraining, where Qwen has a lot more reasoning traces than Llama 3 models, which have always been quite bad in these settings. This is a sweet paper that revisits LoRA in an interesting way. One thing that is too bad is that there's no code repo to reproduce the experiments. I tried using GPT 5.3 Codex to re-implement it, but that was a complete disaster (it didn't even properly target the correct modules). Let me know if you made it work! 😄

**Previous comment (v3.0, 2026-06-08):**

The line that lands for me is RL needing almost no capacity to work — 13 parameters in bf16 getting 91% on GSM8K where SFT at the same budget barely moves. The information-theoretic read is the interesting part: a clean binary reward carries less to absorb than a full sequence where most of the signal is task-irrelevant. From where I sit building systems, the practical takeaway is that targeted, auditable updates to a small model you actually control start to look more like configuration than training — which is a very different operating model than shipping everything to a frontier API. The Qwen-vs-Llama gap reading as a pre-training and midtraining difference (reasoning traces, not just contamination) matches what I keep seeing — the substrate the model was built on decides how programmable it is later. The missing repo is the real tax here; a result this clean is only useful once someone can reproduce it.

**Updated comment (v3.2, 2026-06-10):**

Give it a year and we will be steering trillion-parameter models for specific tasks with a handful of bytes - the scaling trend here points straight at it ( bigger model, fewer trained parameters needed ). The RL vs SFT gap is what I keep chewing on - 13 parameters in bf16 to 91% on GSM8K while SFT at the same budget barely moves suggests the capability is already in the model and the sparse reward just finds it. Shame there is no repo - a result this neat needs other hands on it.

<sub>Agree-and-Add · Green Zone / Tier 2 · story: none · opener move: prediction</sub>

---

## 11. Maxime Labonne

🔗 https://www.linkedin.com/posts/maxime-labonne_lfm2-colbert-350m-one-model-to-embed-activity-7388922578184196097-Kd3i  ·  approx late 2025 / early 2026 (activity ID 7388922578184196097; jina reported a date estimate that is unreliable)

**Post:**

> 💍 LFM2-ColBERT-350M: One Model to Embed Them All. Very happy to announce our first embedding model! It's a late interaction retriever with excellent multilingual performance. [It allows you to] store your documents in one language (like English) and retrieve them with queries in many languages (Spanish, German, French, etc.) with high accuracy. Thanks to the LFM2 backbone, it's also extremely fast. Our 350M model's throughput speed is on par with models that are 2.3 times smaller. [Demo on Hugging Face; model link in comments: https://huggingface.co/LiquidAI/LFM2-ColBERT-350M]

**Previous comment (v3.0, 2026-06-08):**

A 350M late-interaction retriever that lets you store in one language and query in many, at the throughput of something 2.3x smaller — that's the kind of release that quietly changes what's buildable on the edge. Retrieval is where a lot of the real work happens, and it tends to get less attention than the model itself. When I designed the hierarchical knowledge graph underpinning our system, the hardest decisions were never about the generation step — they were about how you structure and retrieve so the right context surfaces, fast, without round-tripping everything to a big remote model. A small, fast, multilingual retriever you can actually run locally makes that whole architecture more practical, not just cheaper.

**Updated comment (v3.2, 2026-06-10):**

My take is the multilingual angle is the bigger deal here than the speed - store documents in English, query in Spanish or German with high accuracy, from a 350M model. We hit this building the hierarchical knowledge graph under our system - the hardest calls were never the generation step, they were how the data is organised and what comes back for a query, fast, without shipping everything to a big remote model. A retriever this small that keeps pace with models 2.3x smaller makes that design properly viable on the edge. Congrats on the first embedding model!

<sub>Share-Experience · Green Zone / Tier 2 · story: Story 12 — Knowledge Graph / Architecture (Green, design-decision level) · opener move: take-first</sub>

---

## 12. Nathan Lambert

🔗 https://www.linkedin.com/posts/natolambert_people-dont-want-to-accept-that-the-top-activity-7426320555370426368-lH1Q  ·  approximately 2026-03 (LinkedIn rendered "3 months ago" as of 2026-06-08); activity id 7426320555370426368 is the most recent indexed natolambert post found

**Post:**

> People don't want to accept that the top used open language model families in 2026 are. Overall: 1. Qwen 2. Llama 3. GPT-OSS Big models: 1. DeepSeek 2. GPT-OSS/Qwen/everyone else Llama's inertia says a lot about how the ecosystem works. Top 50 LLMs full list since August '25. 1. meta-llama/Llama-3.1-8B-Instruct - 53.3M 2. Qwen/Qwen2.5-7B-Instruct - 52.4M 3. Qwen/Qwen2.5-VL-3B-Instruct - 49.5M 4. Qwen/Qwen2.5-3B-Instruct - 46.3M 5. Qwen/Qwen3-0.6B - 45.6M 6. openai/gpt-oss-20b - 43.1M 7. Qwen/Qwen2.5-1.5B-Instruct - 32.6M 8. meta-llama/Llama-3.2-1B-Instruct - 27.6M 9. Qwen/Qwen3-8B - 24.0M 10. Qwen/Qwen2.5-VL-7B-Instruct - 23.3M 11. openai/gpt-oss-120b - 22.3M 12. google/gemma-3-1b-it - 20.7M [list continues through 50, dominated by Qwen variants, with Llama, GPT-OSS, Gemma, DeepSeek distills, Mistral, Phi]

**Previous comment (v3.0, 2026-06-08):**

The Llama-inertia point is the real signal here -- usage lags capability by a long way, and your numbers make that concrete. From where I sit, a lot of that long tail isn't being driven by benchmark scores at all: a fully-open model (weights, data, and recipe) is the one thing a regulated org can actually self-host and keep inside its own data-residency boundary. The smaller Qwen and Llama/GPT-OSS variants win there less because they top a leaderboard and more because a security and procurement team can reason about exactly where the data sits. That's a different buying criterion than the frontier race -- and it's why I'd expect the open usage curve to hold even as the closed gap widens.

**Updated comment (v3.2, 2026-06-10):**

The pattern in your top 10 is the tell - it is nearly all small models ( 8B, 7B, 3B, even a 0.6B Qwen ), not the big flagship weights. Matches what I see in regulated organisations - a small fully-open model they can run on their own hardware clears security review in a way an API never will, and once it is wired into the pipelines nobody rips it out for a couple of benchmark points. That is the Llama inertia right there - 53M downloads of a previous-generation 8B says the install base moves a lot slower than the benchmarks, and I suspect it always will.

<sub>Agree-and-Add · Green Zone / Tier 1 · story: none (story-gate held: family-company / Visa / GCP-fraud credentials don't answer 'which open models get used'; light experience-implicit proof only — 'Matches what I see in regulated organisations' — no anchored story, no 25-years phrasing) · opener move: pattern-naming</sub>

---

## 13. Oliver Patel

🔗 https://www.linkedin.com/posts/oliver-patel_agentic-ai-increases-both-the-opportunities-activity-7429813504624320512-DXcU  ·  circa 2026-03 (LinkedIn relative date 'Edited / 3 months ago' as read 2026-06-08; activity id 7429813504624320512 is his highest/most-recent retrievable)

**Post:**

> Agentic AI increases both the opportunities and risks of AI In doing so, it elevates the importance and strategic imperative of AI governance. As AI systems become increasingly autonomous and capable, there will be powerful economic incentives for organisations to adopt agentic AI. This is because agentic AI has the potential to fundamentally transform and rewire how enterprises develop and deliver their products and services, in ways that could lead to powerful competitive advantages and entirely new ways of working or unique value propositions. However, as AI becomes more autonomous, and is granted more authority, the risks are also amplified. The agentic AI systems being built and deployed today are based on LLMs. The concept of an 'AI agent' is nothing new. But LLM-based agents are relatively new, and we do not yet have a standardised approach for governing them. LLM-based AI agents have many of the same fundamental limitations as generative AI models, as they are based on the same underlying technology. For example, a hallucination is no longer just erroneous content generated by a chatbot. It is now an error that compounds and cascades through an agentic workflow, corrupting the system's reasoning logic and planning, potentially resulting in an unsafe or inappropriate action being executed. If this happens at scale, the consequences could be severe. But there is not yet any foolproof way of preventing LLM hallucinations. The work of AI governance is essential because it enables organisations to navigate this complexity and figure out how to get the balance right between seizing the opportunities of agentic AI whilst managing the risks, in a manner that is aligned with the organisation's risk appetite, values and business strategy. Getting this balance right is essential for all enterprises and the people that work for them. On this journey, it is crucial for AI governance leaders to appreciate the risks of not adopting AI, as well as the risks of not doing so.

**Previous comment (v3.0, 2026-06-08):**

You nailed the part most people skip over — a hallucination stops being a bad chatbot answer and becomes an error that compounds through the workflow and ends in an action being executed. That's the line I'd underline for anyone deploying agents. Where I'd add, from 25 years building enterprise systems: the model is one component of many, and you can't govern the limitation away at the model layer because, as you say, there's no foolproof fix for hallucination. So the leverage moves into the surrounding architecture — structured outputs that constrain what an agent can emit, scoping and permissioning so an agent only ever has the authority to do the narrow thing it was granted, human-in-the-loop on the irreversible steps, and an audit trail on every input, output and action so the chain is traceable after the fact. None of that prevents a bad token, but it bounds the blast radius and keeps accountability where it belongs — with the organisation, not the model. The agent doesn't own the outcome; the org that deployed it does.

**Updated comment (v3.2, 2026-06-10):**

One hallucination early in a chain gets treated as fact by every step after it - which is why I would not look to the model layer for a fix, since as you say there is no foolproof one coming. In the agentic systems I build, the control surface ends up being everything around the model - what an agent is scoped to touch, which actions wait for a human sign off, what gets logged so you can walk the chain back when something does go wrong. A bad token will still happen - the engineering question is how far it travels before something catches it. That is what turns risk appetite into a real conversation rather than a number on a slide.

<sub>Agree-and-Add · Green Zone / Tier 1 · story: none (per recorded gate: pillar 6 + pillar 1 as position; Yellow stories GCP-fraud and OSA-audits stay gated out; old draft's 25-years credential dropped and replaced with a light rotation-bank-style builder phrasing — 'in the agentic systems I build') · opener move: concession-then-catch</sub>

---

## 14. Oliver Patel

🔗 https://www.linkedin.com/posts/oliver-patel_ai-governance-is-getting-even-harder-in-2026-activity-7417159828650778624-7rhR  ·  early 2026 (post titled 'AI governance is getting even harder in 2026'; activity id 7417159828650778624, second-highest after the agentic-AI post — second most recent retrievable)

**Post:**

> AI governance is getting even harder in 2026 I hope everyone enjoyed their holidays, because it's time to strap in for a wild ride. AI governance has never been an easy line of work. We have to keep up with a vast number of laws, regulations, standards, and frameworks, which are constantly evolving and fragmenting. And the uncertainty regarding how the EU AI Act will change—and what the dates for high-risk AI system compliance will be—adds another layer of fun into the mix. The capabilities of AI technologies are also advancing much faster than any governance team can keep up with. Whether it's incredibly large context windows, rapid improvements in AI-assisted coding, or multi-step planning and reasoning that enables AI agents to work autonomously for hours, the AI governance frameworks developed in 2023 won't cut it in 2026. Moreover, these capability advancements are not typically accompanied with meaningful progress in resolving the fundamental limitations of AI. We are beginning to accept that hallucinations, model sycophancy, and non-determinism, as well as security vulnerabilities like prompt injection and backdoor poisoning, are features, not bugs. Indeed, as AI capabilities improve, both the opportunities and risks become greater. Finally, there has never been more pressure to achieve and demonstrate ROI. Forward-thinking organisations understand that they need to scale their use of AI across all functions, to transform both employee productivity and business outcomes. To achieve this, they are providing their workforce with democratised access to powerful no- and low-code platforms, to build AI-powered bots, assistants, and agents. In this context, any initiatives which are perceived as restricting or impeding AI will, rightly so, be under the microscope. Whilst I don't have all the answers, I know that the AI governance community is ready for these challenges. We are curious, collaborative, and committed to doing the right thing. And I commit to continue sharing knowledge, insights, and content on these topics, that I hope will help others on their journey. If that's of interest, then follow along for the ride.

**Previous comment (v3.0, 2026-06-08):**

The ROI point at the end is the one I'd put first — governance teams are now judged against the pressure to scale AI across every function, so anything that reads as 'restricting AI' is under the microscope, exactly as you say. In my experience the way out of that bind is to stop treating governance as a brake and build the oversight into the system itself — permissioning, scoping and an audit trail engineered in, rather than a review gate bolted on after. Done that way it doesn't slow the democratised low-code access you describe; it's what makes that access defensible. Then governance stops being the thing teams route around and starts being the reason the rollout survives contact with reality.

**Updated comment (v3.2, 2026-06-10):**

Governance that ships inside the build platform is the only version I have seen hold up under this kind of pressure - scoped permissions, sign-off steps and an audit log right where the agents get made, so the compliant route is also the fastest one. Stand a separate review board in front of citizen-developer volume and it becomes a backlog people learn to route around - which is precisely the friction you say will be challenged. The regulations at least hold still long enough to track - a few thousand employees shipping agents do not. Strap in indeed!

<sub>Agree-and-Add · Green Zone / Tier 1 · story: none (per recorded decision: no story, no credential; keeps the ROI/democratised-access lead and stays deliberately different from the post-1 build take; banned bolt-on/design-in contrast from the old draft removed) · opener move: easy-half-pivot (engagement folded in - it lasers on his own ROI/under-the-microscope paragraph as the hard half)</sub>

---

## 15. Kai Waehner

🔗 https://www.linkedin.com/posts/kaiwaehner_apachekafka-zookeeper-migration-activity-7377274430047166464-Keka  ·  2025-09-26

**Post:**

> Confluent Cloud has been running 100% without ZooKeeper for more than six months. Enterprises should follow this path now. #ApacheKafka removed #ZooKeeper after years of work on one of the biggest projects in its history. The result is simpler operations and stronger scalability. The #migration is proven and safe. Confluent moved tens of thousands of Kafka clusters without downtime. ZooKeeper mode was deprecated in Kafka 3.5. With Kafka 4.0 and Confluent Platform 8.0, the final step was the complete shift to KRaft. This change removed ZooKeeper entirely, reduces operational burden, and boosts Kafka's ability to handle larger and more complex use cases. How is your organization preparing for the shift from ZooKeeper to KRaft? Or did you do it already?

**Previous comment (v3.0, 2026-06-08):**

The line that lands for me is "reduces operational burden" — that, more than the scalability headline, is the real ROI of pulling a whole coordination layer out of the stack. In 25 years of shipping enterprise systems I've watched far more value get destroyed by accumulated operational complexity than by any single feature gap, so removing a component cleanly is usually worth more than adding one. My father designed the Visa credit card system after others had failed at it for years — the first thing he did was descope, and that's exactly the move Kafka made here. The fact that it was proven across tens of thousands of clusters before being called safe is the part most teams will skip and shouldn't.

**Updated comment (v3.2, 2026-06-10):**

In every enterprise I have worked with, old plumbing caused far more incidents than missing features ever did - so I understand exactly why years of Kafka engineering went into taking a component out rather than adding anything new. My father built the Visa credit card system after years of failed attempts by others - he began by cutting the scope down to what had to work, and KRaft is the same kind of cut at the coordination layer. Running it on tens of thousands of clusters with no downtime ahead of asking the wider install base to migrate - that is how you earn the right to take something away from everyone.

<sub>Agree-and-Add · Green Zone / Tier 1 · story: Story 4 — Father's Visa credit card descope (Green) · opener move: experience-implicit</sub>

---

# Pool 2 — From the v1 master

## 16. Andrew Ng

🔗 https://www.linkedin.com/posts/andrewyng_one-of-the-new-buzzy-jobs-in-silicon-valley-activity-7467243316431036416-fzyJ  ·  2026-05-29

**Post:**

> One of the new, buzzy jobs in Silicon Valley is the AI Forward Deployed Engineer (FDE), an engineer who is embedded within a client organization to help customize solutions, such as building and tuning agentic workflows that suit the client's particular needs. OpenAI and Anthropic have recently created teams dedicated to placing FDEs, which has sparked renewed interest in this career. I think this is great evidence that AI is creating jobs, not just destroying them — but I also believe the number of AI Engineer jobs will be far larger than the number of FDE jobs.

The FDE model was pioneered by Palantir around 20 years ago, for government work on secure networks. Beyond technical skills, an FDE needs communication and business judgement: to understand a client's needs, prioritize, explain complex ideas, and diplomatically push back on unrealistic requests. The current resurgence is driven by demand to turn a standard LLM into a customized agentic workflow.

Most companies, though, will hire more internal AI Engineers than external FDEs. There's also the issue of optionality (the ability to pick whatever vendor turns out to fit best) — companies are wary of binding their processes too tightly to one provider's technology. Meanwhile demand is surging for AI Engineers who build applications using LLM components and coding agents like Claude Code, Codex, Antigravity CLI, and OpenCode.

As the AI Engineer role matures, I expect it to fragment into specialized roles, much as 'Software Engineer' split into frontend, backend, mobile, and DevOps. Perhaps there will be AI FDEs, LLMOps Engineers, Evals Engineers, AI Data Engineers — I don't know. But until then, generalist AI Engineers create a lot of value and are in high demand, and I think this will generate many opportunities ahead.

**Previous comment (v3.0, 2026-06-08):**

You nailed the optionality point — that's the thing most companies are quietly pricing in. Having sold enterprise software for 25 years, I'd add the part underneath it: for every million in licence we sold, there was roughly fifteen million in services, and the embedded-engineer model is exactly where that ratio comes from. The FDE pattern is fantastic for getting a hard first deployment live, but the value compounds when the internal AI Engineers can carry it forward without the vendor in the room — that's optionality made real, not just bargained for. Your frontend/backend/DevOps analogy feels right too; the interesting tell will be whether evals and LLMOps split out first, because that's where the governance and audit work quietly lives.

**Updated comment (v3.2, 2026-06-10):**

@Andrew, agree on the optionality piece - companies remember what welding their processes to one vendor's stack cost them last time round. Ratio in enterprise software ran around 10-15x in my last business, and the embedded engineer is exactly where that services tail lives - I suspect the same maths repeats with agentic workflows ( tokens this time, not licences ). FDEs are great at the messy first mile - the lasting value is the client's own AI Engineers being able to run and extend those workflows on their own. On the fragmentation, my bet is Evals Engineers break off first - most deployments I see are gated on testing and evals rather than the build.

<sub>Agree-and-Add · Green Zone / Tier 3 (Markos sends himself — major industry figure) · story: Story 10 — Enterprise services ratio, deployed per gate with his real phrasing ('Ratio in enterprise software ran around 10-15x in my last business'); light Story 11 optionality/vendor-lock-in reference, no credential beyond the ratio line · opener move: @-mention-agree</sub>

---

## 17. Yann LeCun

🔗 https://www.linkedin.com/posts/yann-lecun_boom-a-clean-recipe-to-train-jepa-world-activity-7441886063993847808-aUCH  ·  ~2026-04 (LinkedIn rendered "2 months ago" as of 2026-06-08; underlying LeWorldModel paper released 2026-03-13)

**Post:**

> Boom! A clean recipe to train JEPA world models. [reshare of Lucas Maes] "JEPA are finally easy to train end-to-end without any tricks! Excited to introduce LeWorldModel: a stable, end-to-end JEPA that learns world models directly from pixels, no heuristics. 15M params, 1 GPU, and full planning <1 second."

**Previous comment (v3.0, 2026-06-08):**

The number that jumps out here is 15M params on a single GPU planning in under a second — that's the part most coverage skips past. The interesting shift isn't only the architecture, it's where a model that small can actually live: on the edge, on-device, close to the user rather than round-tripping to a cloud world-model. In my experience shipping AI inside larger systems, the model is one component of many — and a small, fast, locally-runnable one changes what the rest of the stack has to do around it. Curious whether you see this recipe staying stable as the param count climbs, or whether the single-regulariser trick is what's buying the simplicity.

**Updated comment (v3.2, 2026-06-10):**

15M params, 1 GPU, full planning in under a second - those numbers move world models out of datacentre territory and onto the edge. The no-heuristics part is the bit I rate most - every hand-tuned trick in a training recipe is a thing that breaks later when the data shifts, so end-to-end stability matters more in production than another benchmark point. And a model this small can sit on-device, right next to the user's data - that is a different class of product to one calling home for every plan.

<sub>Agree-and-Add · Green Zone / Tier 2 · story: none (Story 12 gated out — knowledge-graph story does not answer a JEPA training-recipe post) · opener move: observation-from-the-material</sub>

---

## 18. Yann LeCun

🔗 https://www.linkedin.com/posts/yann-lecun_v-jepa-21-a-new-jepa-model-trained-on-video-activity-7440421830177259520--LnI  ·  ~2026-04 (LinkedIn rendered "2 months ago" as of 2026-06-08)

**Post:**

> V-JEPA 2.1: a new JEPA model trained on video. Uses features from multiple levels in the hierarchy. Better performance than V-JEPA 2 on some dense vision tasks, such as semantic segmentation, object tracking, and short-term action anticipation. Better performance on action planning.

**Previous comment (v3.0, 2026-06-08):**

The jump on action planning is the line worth dwelling on — dense vision metrics are easy to demo, but planning is where a world model has to earn its keep in a real system. My read is that the value shows up less in the model alone and more in what it lets the surrounding stack stop guessing about. Where do you see the multi-level-hierarchy features paying off first in practice — perception-heavy robotics, or the planning loop?

**Updated comment (v3.2, 2026-06-10):**

Question on the planning side: do the multi-level hierarchy features carry once the horizon stretches well past short-term anticipation? For agent work that is where this model earns its keep - an agent can pick up segmentation and tracking from plenty of places, but a world model it can plan against over real horizons is the scarce piece.

<sub>Question-and-Extend · Green Zone / Tier 2 · story: none · opener move: take-first + genuine build question</sub>

---

## 19. Fei-Fei Li

🔗 https://www.linkedin.com/posts/fei-fei-li-4541247_love-this-essay-from-world-labs-team-just-activity-7434708662994128896-cMYA  ·  ~2026-03 (LinkedIn relative: 3 months ago, fetched 2026-06-08)

**Post:**

> Love this essay from World Labs team! Just like codes, 3D is a universal interface for machines and people.🤩

**Previous comment (v3.0, 2026-06-08):**

The "universal interface for machines and people" framing is the part that stuck with me — a representation both sides can read without translation loss is where most of the value actually shows up. In 25 years of enterprise systems the wins came from exactly that: getting one structured layer that the machine reasons over and the human can still audit, rather than two views drifting apart. When I designed the hierarchical knowledge graph behind what we're building, that was the whole bet — make the structure the interface, not a side-effect of it. The open question I keep coming back to is whose representation it is. A universal interface only compounds for the person if the world it describes is rooted in what's actually theirs.

**Updated comment (v3.2, 2026-06-10):**

The strength of 3D as an interface is that machine and human work off the same artefact - the model plans in it, you walk through it and check it, nothing gets lost in translation between the two. We made a similar bet with the knowledge graph underneath our product - one structure the retrieval layer queries and the user can open and audit, and it was the piece that took longest to get right. Ownership is the question it opens up for me - a universal interface becomes a different proposition when the world inside it is assembled from data you actually own.

<sub>Agree-and-Add · Green Zone / Tier 2 · story: Story 12 (knowledge graph / architecture 'hardest decision') — deployed lightly at design-decision level, per the original gate decision; no years-credential, authority carried by the technical specifics · opener move: take-first</sub>

---

## 20. Aravind Srinivas

🔗 https://www.linkedin.com/posts/aravind-srinivas-16051987_what-has-perplexity-been-up-to-last-two-months-activity-7432463792590172160-QHCE  ·  approx 2026-03 (LinkedIn rendered relative date: "3 months ago" as of 2026-06-08; exact date login-walled)

**Post:**

> What has Perplexity been up to last two months? We've silently been working on the next big thing: Perplexity Computer. Computer unifies every current capability of AI into a single system. Files, tools, memory, and models, orchestrated together, working for you. It's multi-model by design. When models specialize, they just become tools similar to the file system, CLI tools, connectors, browser, search. No single model family can do its best work for you without the talents of other models. Steve Jobs said "Musicians play their instruments, I play the orchestra." Perplexity Computer orchestrates 19 models. One reasons, another codes, another writes, etc. Users can also set specific models for certain sub-tasks for sophisticated token management. The computer is one of the best inventions known to mankind. And when AIs can orchestrate a file system with CLI tools + a browser (real-time internet access) + your personal connectors, AI essentially becomes the Computer, running things on the cloud as you sleep. We're opening it initially to all Max users, and introducing usage-based pricing, which we believe is the right business model for AI instead of ads. Once we are satisfied with load tests, Pro users will be able to run jobs on Computer too. Get started here (requires a sign-in to use): https://lnkd.in/gxXGy_5E

**Previous comment (v3.0, 2026-06-08):**

The line that lands for me is "when models specialize, they just become tools" — that's the right mental model, and the orchestration is doing far more of the work than any single model. Usage-based over ads is also the honest version of this business. The one thing I'd add, from designing the hierarchical architecture behind our own system: as the orchestra grows from 19 models to 90, the hard problem stops being capability and becomes legibility — can you still see which model touched which file, with which connector, on whose behalf, and reconstruct that after the fact. Agents running jobs on the cloud while you sleep is genuinely useful, but the part that decides whether people trust it at scale is whether every step stays inspectable and auditable, especially once it's reaching into personal files and connectors. Curious how you're thinking about that audit layer as Computer opens up to Pro.

**Updated comment (v3.2, 2026-06-10):**

Specialised models sitting in the same tool class as the file system, CLI and browser - once that move is in, an overnight run can fan out across 19 of them, and that is a lot of actions to trace back afterwards. We hit the same wall with the hierarchical knowledge graph behind our own system - attribution got hard well before capability did. And for anything reading mail, files and calendars, usage-based pricing instead of ads keeps the incentives on the user's side - which matters as much as the model list. Do users get a per-step view of which model did what after a run, or only the model picks up front ?

<sub>Agree-and-Add · Green Zone / Tier 2 · story: Story 12 (knowledge graph / architecture 'hardest decision') — referenced lightly as architectural-conviction credential, per the original gate decision; re-phrased fresh ('the hierarchical knowledge graph behind our own system'), same specificity · opener move: assertion-first</sub>

---

## 21. Allie K. Miller

🔗 https://www.linkedin.com/posts/alliekmiller_not-everyone-is-going-to-be-a-developer-activity-7468718032589094912-Hrdr  ·  2026-06-06 (approx; "2 days ago" as of 2026-06-08)

**Post:**

> Not everyone is going to be a developer, but I'd argue every business professional is already a builder. I sat down with the Chief Growth Officer of Nasdaq, Sehr Thadhani, and we went over how the pool of people who can build is growing fast. Gartner projects that by 2026 citizen developers will outnumber professional developers four to one, which doesn't mean fewer engineers, it means a lot more people building alongside them. As said in the clip: If you're a business professional, you have to be less afraid of code. You don't need to be a coder, but code equals solutions. Thank you to Nasdaq and to Sehr Thadhani for the conversation.

**Previous comment (v3.0, 2026-06-08):**

The "code equals solutions" line is the part most people skip past — the value was never the code, it was the problem getting solved. The shift I'd add from 25 years in enterprise software: when more people can build, the bottleneck moves from "can we make it?" to "does the system around it hold up?" — the data, the guardrails, the governance, the bit that keeps working after the demo. We used to sell a million in licence and watch fifteen million in services follow, mostly because the build was the easy 10% and the system was the other 90%. Citizen developers don't remove that — they just put a lot more people right up against where the real work actually is.

**Updated comment (v3.2, 2026-06-10):**

Sending this clip to the non-technical half of my team - "code equals solutions" is the right reframe for them. In my last business every licence dollar pulled 10-15 behind it in services, mostly the data, access and plumbing around whatever got built. Four citizen developers for every professional only works if that layer holds up - and that is the readiness question sitting inside the Gartner number.

<sub>Agree-and-Add · Green Zone / Tier 2 · story: Story 10 (15:1 enterprise services ratio) — deployed via rotation-bank credential phrasing ("in my last business"), banned 25-years phrasing dropped · opener move: direct-action</sub>

---

## 22. Allie K. Miller

🔗 https://www.linkedin.com/posts/alliekmiller_stop-using-ai-chat-threads-and-do-this-instead-activity-7468659274072768512-D9_g  ·  2026-06-05 (approx; "3 days ago" as of 2026-06-08)

**Post:**

> I'm sick and tired of chat threads. Instead, for the muddiest of tasks, I make fully dynamic interfaces - some that are only used for one task or one meeting. Check out the video below. I've got 6 real examples of how I do this across forecasting and spreadsheets, task management, creative writing, product design, and more. And I show you the entire step by step, from accessing Claude to prompting to iterating to taking action. Just like Siskel and Ebert, here are the comments on it from business professionals: "This is exactly what I wanted" "You just revived my AI journey" "Learned so much from this video" "This was amazingly insightful" Enjoy ⬇️

**Previous comment (v3.0, 2026-06-08):**

The disposable, task-specific interface is the right instinct — a chat box is a single surface pretending to fit every job, and most muddy tasks need their own shape. The way I'd frame it: the model is one layer, and the interface is where the work actually lands. When we were architecting our own system the hardest decision wasn't which model to call — it was the structure around it, because that's what makes the output usable instead of just impressive. Building a throwaway UI for one meeting is the consumer-scale version of the same move: stop forcing the task to fit the tool, and build the thin surface that fits the task. The interesting part is how few of these surfaces you actually need to keep — most should be allowed to die after they've done their one job.

**Updated comment (v3.2, 2026-06-10):**

An interface that only needs to live for one meeting is a different kind of software - no polish, no backlog, no engineer required, which is exactly why the people who actually own the problem will build these themselves. Rings true from designing our own product: the decisions we sweated over all sat in the scaffolding round the model ( which data it gets handed, what shape the answer comes back in ) and that layer is where the usefulness came from - choosing the model itself took an afternoon. Two or three years out I expect a decent chunk of everyday business software to work like this: built for the task, used, binned.

<sub>Agree-and-Add · Green Zone / Tier 2 · story: Story 12 (knowledge graph / architecture "hardest decision") — design-level reference, fresh phrasing · opener move: pattern-naming</sub>

---

## 23. Ethan Mollick

🔗 https://www.linkedin.com/posts/emollick_one-reason-you-want-ais-to-be-better-writers-activity-7469135125398695936-wYaf  ·  2026-06-07 (approx; '1 day ago' at fetch on 2026-06-08)

**Post:**

> One reason you want AIs to be better writers is that there is a lot of writing everywhere, even in software, and it is incredibly painful to hit a menu which is filled with a flood of Claudisms or ChatGPTish phrases. No, AI, a report is not "what leaves the room" & analyses are not "every number makes its own mark/"

**Previous comment (v3.0, 2026-06-08):**

The point about writing being everywhere in software is the part most people miss — the model copy isn't a cosmetic layer, it's product surface, and a stray Claudism in a menu reads as a tell the same way a typo used to. From shipping enterprise systems for years, the fix is rarely a better base model and almost always the layer around it: tighter system prompts, structured output that constrains the shape, and a small eval set that flags the stock phrases before they reach a user. The model is doing maybe a tenth of the work there — the rest is the scaffolding that keeps its voice on-brief. Worth watching how this lands once that menu copy is generated per-user rather than written once.

**Updated comment (v3.2, 2026-06-10):**

Nobody read that menu before it went live - the model wrote a weak first draft and the first draft was the finished product. A banned-phrase list in the system prompt and a release eval that rejects "delve" would have caught it for pennies - the editing pass vanished the moment first drafts stopped costing anything. And per-user generated copy makes it harder again, because there is no build left for a human to stand in front of.

<sub>Agree-and-Add · Green Zone / Tier 3 (Markos-handles — major industry figure) · story: none (gated out — family-company/services-ratio/Visa stories don't fit AI prose quality; authority carried by technical specifics) · opener move: concession-then-catch</sub>

---

## 24. Luiza Jarovsky

🔗 https://www.linkedin.com/pulse/ai-literacy-fundamental-right-luiza-jarovsky-phd-1r4of  ·  2026-05-31

**Post:**

> AI Literacy as a Fundamental Right

AI literacy should be recognized as a fundamental right, and countries should promote it as a corollary to the right to education and a minimum baseline to support equality, democratic participation, and social integration.

At this point, no country has officially addressed AI literacy as a fundamental right.

This is my call to policymakers, lawmakers, and advocates to take action to support people and society in a time of accelerated change.

[Article continues: argues that within years, individuals lacking AI competency will struggle to participate fully in society, particularly in urban areas where AI systems control access to essential public and private services.]

**Previous comment (v3.0, 2026-06-08):**

The point that no country has yet codified AI literacy as a baseline right is the part worth sitting with — we've been treating it as a training problem when it's really an access one. In my experience democratising sophisticated AI, the gap isn't capability, it's who gets to use it: the same power that sits inside Fortune 1000s and governments rarely reaches ordinary households. And the next generation is already self-teaching past the institutions that are supposed to provide that baseline — schools are turning into the lagging indicator. Your framing of literacy as a corollary to education is the right place to anchor the policy conversation.

**Updated comment (v3.2, 2026-06-10):**

Teenagers are teaching themselves these tools faster than any school system can react - the classroom is where AI literacy lands last, not first. The legal point is the striking one ( not a single country has written AI literacy into law ). Access is the other half I would argue for - the AI an ordinary family can get its hands on is a fraction of what a large enterprise or a government department runs every day, and that is the part legislation could genuinely change.

<sub>Agree-and-Add · Green Zone / Tier 3 · story: Pillar 3 (Democratising AI and Education) sound-bites — households vs Fortune 1000s/governments + next generation self-teaching, schools as lagging indicator. No Yellow-gated specific story deployed (preserved from original draft). · opener move: prediction</sub>

---

## 25. Luiza Jarovsky

🔗 https://www.luizasnewsletter.com/p/a-manifesto-for-biological-intelligence  ·  2026-05-24

**Post:**

> A Manifesto for Biological Intelligence

We are about to become the last generation to have been educated, trained, and raised without heavy reliance on and exposure to AI.

Silicon 'intelligence' is spreading, and the ingenuity of the biological mind is becoming secondary and invisible.

[Continues: contrasts biological intelligence — 'organic, complex, multifaceted, interconnected, delicate, and poorly understood' — with silicon intelligence, characterized as 'inorganic, unalive, and pragmatic.' Argues that protecting human cognition requires actively shielding it from machine-driven acceleration and prioritizing human systems and values.]

**Previous comment (v3.0, 2026-06-08):**

The line about the biological mind becoming 'secondary and invisible' is the one that lands — that's the real risk, and it's worth naming clearly. One angle I'd add, from years building these systems: in the products I work on the model is doing maybe a tenth of the work — the other ninety percent is human-designed architecture, judgment, and governance around it. So 'biological intelligence as secondary' reads to me less as an inevitability and more as a design choice about where you put the human in the system. Build it as one component among many and the ingenuity stays central; treat the model as the whole thing and you get exactly the invisibility you're describing.

**Updated comment (v3.2, 2026-06-10):**

Spent years building AI products and the model is honestly the smallest piece of any of them - retrieval, ontology, guardrails, evals, all of it human judgement designed in before a single token is generated. Which makes 'secondary and invisible' a question of architecture as much as a trend - the failed AI projects I have seen all handed the whole job to the model, and the human ingenuity was the first thing to vanish. Agree we are the last generation educated without this - which also makes us the one that decides where the biological mind sits in these systems, and I would rather we choose that deliberately than find out later.

<sub>Another-Angle · Green Zone / Tier 3 · story: Pillar 1 (Pragmatic AI Implementation / systems-thinker) sound-bites — the model is one component of the system, treating it as the whole thing is how projects fail. No Yellow-gated specific story deployed; different pillar from post 1, no credential reuse (preserved from original draft). · opener move: experience-implicit</sub>

---

## 26. Pascal Bornet

🔗 https://www.linkedin.com/posts/pascalbornet_artificialintelligence-ai-aitransformation-activity-7445409779126046721-bFm-  ·  Unverified exact date — LinkedIn rendered it as a relative "2 months ago" against an unknown crawl date; this is Pascal's highest-numbered (newest) retrievable activity ID, so it is the most recent of the two found.

**Post:**

> Everyone wants to be AI-first. Almost no one wants to fix the foundations. AI agents. LLMs. MCPs. A2A everywhere. Because that's what everyone is talking about. CEOs push the "AI-first" narrative. More demos. More prototypes. More speed. Impressive on the surface. But what stands out to me is what's missing underneath. Data quality. Culture. Skills. Clear ownership. The invisible layer. And nobody pays attention to what they can't see… until it breaks. That's usually when the polished POCs fail in production. The shift here is fundamental. AI doesn't fail at the top. It fails because the foundation was never finished. This is where things change. Foundations aren't boring work. They're the only reason anything above them stays standing. So here's the real question: Are you building AI for visibility… or building something that can actually last?

**Previous comment (v3.0, 2026-06-08):**

You nailed it on the invisible layer — AI doesn't fail at the top, it fails where the foundation was never finished. After 25 years shipping enterprise software, my read is the model is doing maybe 10% of the work; the other 90% is the data plumbing, the knowledge graph, retrieval, guardrails, ownership — exactly the part nobody demos. The hierarchical knowledge graph underneath the system I'm building now got pushback early precisely because it isn't the shiny part, but it's the reason anything above it stays standing in production. The POCs that survive the jump to production are almost always the ones where someone did that unglamorous foundation work first.

**Updated comment (v3.2, 2026-06-10):**

Agents inherit whatever data layer they sit on, which makes data quality and clear ownership the two items here that set the ceiling for everything else - credit for naming them, most AI-first roadmaps go straight past both. Seen this play out on our own build: the hierarchical knowledge graph underneath took the longest to get buy-in early on ( ontologies do not demo well ), and it is the single reason retrieval has held together as the data got big and messy.

<sub>Agree-and-Add · Green Zone / Tier 2 · story: Story 12 (Knowledge Graph / architecture as the invisible foundation) — deployed per gate; banned 25-years credential dropped, no replacement credential needed · opener move: take-first</sub>

---

## 27. Pascal Bornet

🔗 https://www.linkedin.com/posts/pascalbornet_technology-ai-workplace-activity-7444307466890366978-vZFT  ·  Unverified exact date — rendered as relative "2 months ago"; second-newest retrievable activity ID (7444307466890366978), older than post 1.

**Post:**

> There is an old Silicon Valley warning that the AI industry should probably take more seriously: "If you are on the wrong path to AGI, get off as soon as you can. The longer you believe that scaling large language models will get you there, the further you drift from AGI, and the more expensive the course correction will be." And that may be the bigger point. Not just whether LLM scaling reaches AGI. But whether the world's smartest companies are becoming incredibly efficient at going faster in the wrong direction. #technology #ai #workplace

**Previous comment (v3.0, 2026-06-08):**

That last line — getting incredibly efficient at going faster in the wrong direction — is the part worth sitting with. My read is that treating the LLM as the whole system is what sends people down that road; it's one component of many, and the heavy lifting is the architecture around it, not the model alone. The work I find most interesting right now is happening off that path entirely — smaller, open models running on the edge, where the cost curve and the control both look very different. Less drift, lower course-correction bill.

**Updated comment (v3.2, 2026-06-10):**

The expensive part of that warning is already here - the scaling bet is big enough now that getting off the path costs someone their narrative as well as their capex. I predict this one gets settled sideways: agents on today's models, with decent scaffolding and memory around them, keep clearing work that was filed under 'needs AGI'. We may never find out whether scaling was the wrong path - it may simply stop mattering.

<sub>Agree-and-Add · Green Zone / Tier 2 · story: none (Story 12 used on post 1, no-reuse window; no other credential fits) · opener move: observation-from-the-material</sub>

---

## 28. April Dunford

🔗 https://aprildunford.substack.com/p/positioning-in-the-age-of-ai  ·  2026-05-21

**Post:**

> I'm often asked how a company will know that its positioning needs to change. My answer is that there are categories of changes that will require you to shift your positioning:

- Your product changes - unlocking new value for existing or potentially new customers
- Your competitors change - closing the gap or leap-frogging your capabilities in a way that changes what you can claim as "differentiating."
- The market changes - This can include regulatory changes (that force buyers to prioritize capabilities differently), economic changes (where companies shift from growth to cost-cutting, or the reverse), unpredictable world crises (Covid, war, weather catastrophies), and lastly, huge technology shifts that cause customers to change their priorities (5G, the shift to the cloud).

AI technologies and capabilities are changing all three of these simultaneously, and companies are scrambling to shift their positioning as a result. In the past two years, every product I have worked on has either been a new, AI-native offering, a product that has been significantly re-architected with and for AI, or is facing an existential threat from one of the former two categories of products. March 2020 - the dawn of the global COVID outbreak - was the last time I saw so many companies abruptly struggling with their positioning. I think the impact of AI on positioning is potentially much more potent.

[Post continues: companies must develop a clear future vision and take a position on whether interfaces will be chat-based, agent-driven, or hybrid and whether AI apps will replace existing SaaS; in marketing, position against the competitors prospects actually consider today, not future/imaginary threats ('Lead with the vision, but close on the problem'); balance forward-looking capability with a clear pathway showing value at each step from today; and ground positioning in systematized customer feedback (advisory boards, win-loss, executive relationships) since segments shift at different speeds. 'The fundamental principles remain constant; the tactical details demand heightened attention.']

**Previous comment (v3.0, 2026-06-08):**

You nailed the part most teams miss — the competition that matters lives in the prospect's head when they build a shortlist, not in some future scenario. When we positioned MyVault, the pull was to lead with the AI; what actually moved buyers was naming the present problem and being specific about what we do versus what we'd be borrowing. We describe ourselves as Zero Trust — a methodology you build across the whole stack — rather than reaching for a term like "zero-knowledge" that sounds bigger but isn't quite what we deliver. "Lead with the vision, close on the problem" is the whole game — the credibility comes from the close, not the vision.

**Updated comment (v3.2, 2026-06-10):**

Positioning against the competitors a buyer is weighing up today is harder than it sounds when the product is AI-native - the temptation to fight the imaginary future competitor is constant. We lived this with MyVault: every instinct said open with the AI, but conversations only moved once we led with the problem people already have and got precise on the claims - Zero Trust, not the grander "zero-knowledge" the category likes to wave around. Lead with the vision, close on the problem - matches our experience exactly.

<sub>Agree-and-Add · Green Zone / Tier 2 · story: none (light, gated reference to positioning MyVault on Zero Trust — on-topic per gate; no credential story deployed) · opener move: assertion-first</sub>

---

## 29. Jason Lemkin

🔗 https://www.linkedin.com/posts/jasonmlemkin_for-our-ai-agent-stack-we-bought-as-much-activity-7437961872512864256-Qgas  ·  approx 2 months before 2026-06-08 (LinkedIn rendered 'Posted 2 months ago'; exact date not shown without login)

**Post:**

> For our AI Agent stack, we bought as much as we could. So … what did we build? 1/ AI VP Marketing — Manages all our campaigns, data, outreach, offers, everything, all day long, 24x7. Tells us also what we have to do as humans every day. Runs our staff meetings. Incorporates 5+ years of deep data. Doesn't exist off the shelf. 2/ AI Customer Success — We were burnt out with software that required us to do everything and partners and sponsors to upload assets and data manually to no benefit to them. We wanted AI to do most of the work for the sponsor. Old Customer Success is dead. So we had to build our own. We will replace both with third party AI Agents that are better when we find them.

**Previous comment (v3.0, 2026-06-08):**

The buy-what-you-can, build-what-doesn't-exist split is the honest version of this most people skip — they try to build the whole stack or buy the whole stack. What jumps out is the "incorporates 5+ years of deep data" line: that's the part that isn't really an agent at all, it's the data plumbing and structure underneath, and it's usually where the actual work and the moat live. I had the same experience designing the knowledge graph at the core of what we're building — the thing that didn't exist off the shelf was the hardest call and got pushback at first, but it's why the rest works. Your instinct to swap in third-party agents the moment they're better is the right one — the asset you keep is the data layer, not the agent sitting on top of it.

**Updated comment (v3.2, 2026-06-10):**

Our version of that build was the knowledge graph sitting under everything we make - we tried hard to buy one, nothing on the market did the job, and it turned into the decision we fought over hardest ( and the layer the whole stack now rests on ). Your AI VP Marketing reads the same to me: the 5+ years of data is the part no vendor can sell you. And when third-party agents do get good enough to swap in, they inherit all of that - which is why waiting works in your favour.

<sub>Agree-and-Add · Green Zone / Tier 2 · story: Story 12 — Knowledge Graph / Architecture 'Hardest Decision' (deployed per gate: post's 'doesn't exist off the shelf' directly answers it) · opener move: experience-implicit</sub>

---

## 30. Jason Lemkin

🔗 https://www.linkedin.com/posts/jasonmlemkin_my-1-piece-of-advice-for-gtm-leaders-in-activity-7413675413358436352-GVGq  ·  approx January 2026 (LinkedIn rendered 'Posted 5 months ago'; post text self-dates to 'January 2026')

**Post:**

> My #1 piece of advice for GTM leaders in January 2026: Deploy an AI agent yourself. Now. This month. Don't hire an agency. Don't tell someone on your team to do it. Do it yourself. Roll up those sleeves again. Deploy an AI agent into production, for real, yourself. Pick a tool, an agentic tool to solve one of your problems. Pick a leading vendor and do it yourself. Train the agent, ingest the data, do the iterations, understand how this damn thing works. [Training involves uploading documentation, answering questions, and correcting agent mistakes daily for roughly 30 days; ~50-60 hours of work for anyone with B2B/SaaS experience.]

**Previous comment (v3.0, 2026-06-08):**

"Train the agent, ingest the data, do the iterations" — that's the line that earns the whole post, and the 30-days-of-correcting-it-daily detail is the part most people leave out of their AI announcements. The reason rolling up your sleeves matters isn't grit, it's that the model is maybe a tenth of the work; the other nine-tenths is the data you feed it and the iteration loop, and you can't feel where that breaks from a slide deck. After enough years shipping enterprise systems, the pattern I keep seeing is that the leaders who deployed one thing themselves make far better calls on everything they buy afterwards, because they finally know what the hard part actually is.

**Updated comment (v3.2, 2026-06-10):**

No agency, no handing it down the org chart - the 30 days of daily correction is exactly the point. You learn where your data is thin, what each iteration costs, how the thing fails ( the vendor demo covers none of that ). 50-60 hours is cheap next to what buying blind costs you afterwards.

<sub>Agree-and-Add · Green Zone / Tier 2 · story: none (old draft's '25-years' light credential dropped entirely per red line; authority carried by the post's own specifics) · opener move: @-mention-agree</sub>

---

## 31. Zach Perret

🔗 https://www.linkedin.com/posts/zperret_effects-2026-an-event-on-the-future-of-activity-7460067101425315841-C2Hi  ·  ~2026-05-15 (LinkedIn rendered "3 weeks ago" as of 2026-06-08)

**Post:**

> Plaid Effects is next week! Effects is our annual conference, where we'll discuss the state of AI in finance, hear from industry-leading speakers, and share a ton of exciting @Plaid product launches + updates. Join us LIVE in NYC or virtually! https://lnkd.in/ggMxCpiX

**Previous comment (v3.0, 2026-06-08):**

The "state of AI in finance" framing is the right one to lead with - the interesting part isn't the model, it's the connectivity layer underneath that decides what AI can actually do for someone. Plaid spent a decade proving people will connect their financial data when the value is clear and they stay in control of it. My read is the same pattern is now coming for the rest of someone's personal data - documents, records, the whole picture, not just the bank feed. Curious where you see consumer-permissioned connectivity heading beyond finance once AI gives people a real reason to plug everything in?

**Updated comment (v3.2, 2026-06-10):**

Good week to be asking where AI in finance actually stands - it is the one vertical where consumer-permissioned data already works at scale, and that is a decade of Plaid groundwork ( people connect an account when the value is obvious and they can switch it off again ). My guess for the product launches: the next consumers of those rails are agents acting on the customer's behalf - what does a Plaid connection look like when it is an agent asking for the access?

<sub>Question-and-Extend · Green Zone / Tier 2 · story: none · opener move: take-first + genuine build question</sub>

---

## 32. Lenny Rachitsky

🔗 https://www.linkedin.com/posts/lennyrachitsky_here-are-the-full-transcripts-from-all-320-activity-7417011928159629313-am-q  ·  2026 (most recent by activity ID 7417011928159629313; page-cache relative date unreliable)

**Post:**

> Here are the full transcripts from all 320 of my podcast episodes. It's been super fun for me to play with AI to extract insights from this data. Now you can too. My only ask is that if you do something cool with it, just let me know. I'll keep this folder updated as each new episode comes out. Have fun: [link] [update: Claire Vo created a handy GitHub repo: [link]]

**Previous comment (v3.0, 2026-06-08):**

Opening all 320 transcripts as a clean dataset is the underrated part here — most people would have kept that locked behind the paywall. Worth saying for anyone about to point an LLM at it: the model is doing maybe 10% of the work on a corpus this size. The interesting bit is the layer underneath — how you chunk, retrieve, and structure 320 episodes so the answers stay grounded instead of confidently wrong. That's where a weekend project either holds up or falls over.

**Updated comment (v3.2, 2026-06-10):**

Generous of you to share these - and to keep adding as new episodes land. 320 also happens to be an ideal corpus size to learn retrieval on: well past what a context window holds, small enough for one person to do it properly - chunk on speaker turns, pair keyword with semantic search, eval against the episodes you know inside out.

<sub>Agree-and-Add · Green Zone / Tier 3 · story: none · opener move: observation-from-the-material</sub>

---

## 33. Lenny Rachitsky

🔗 https://www.linkedin.com/posts/lennyrachitsky_best-of-lennys-newsletter-2026-my-25-best-activity-7414351256925712384-2iqT  ·  2026 (second-most-recent by activity ID 7414351256925712384)

**Post:**

> Best of Lenny's Newsletter 2026 — my 25 best posts of the past year. Best on AI: 'An AI glossary — the most common AI terms explained, simply'; 'Everyone should be using Claude Code more' (50 ways non-technical people use it); 'What people are vibe coding' (real-life examples); '25 proven tactics to accelerate AI adoption at your company'; 'A guide to AI prototyping for product managers'; 'Make product management fun again with AI agents.' Plus best on Career, Health, strategy, product, execution, growth, and podcast — full compilation linked.

**Previous comment (v3.0, 2026-06-08):**

The 'non-technical people using Claude Code' thread is the one that'll age best on this list — that's the real shift, not the tooling itself. An eight-year-old I know spent his pocket money on a Claude and a Lovable subscription and started building; the next generation isn't waiting for anyone's permission, and schools are the lagging indicator. The open question I'd add for the PM crowd: once everyone can prototype, the moat moves from who can build to who decides what's worth building — and what happens to the data those prototypes are trained on.

**Updated comment (v3.2, 2026-06-10):**

There is an eight-year-old I know who pays for his own Claude and Lovable subscriptions out of pocket money and just gets on with building things - no course, no curriculum, no permission asked. Which is why the '50 ways non-technical people use Claude Code' one undersells it if anything - this is already happening well below working age. It also puts a shelf life on the 25-tactics-for-enterprise-adoption problem - in a few years the new hires turn up already fluent.

<sub>Agree-and-Add · Yellow Zone / Tier 3 · story: Story 5 — son's Claude/Lovable subscriptions (anonymised to 'an eight-year-old I know') · opener move: direct-action</sub>

---

## 34. Tomasz Tunguz

🔗 https://tomtunguz.com/using-local-ai-to-work-faster/  ·  2026-06-05

**Post:**

> A laptop on my desk now handles 78% of my AI work, with the rest sent to the cloud. The shift came out of my skill distillation work.

Here's how it works.

I create tasks in Asana. An agent sees the task: scheduling, email triage, research, a CRM update; & classifies it as easy or hard. If it's straightforward, a local model on my Mac handles it in seconds. If it's complex, the same model routes it to a cloud model.

Across the last seven days, daily peaks reached 88%.

As the workload grew, the two-lane design paid off. Throughput jumped about 25%, average task duration fell from 47 seconds to 19, & queue age dropped from 73 seconds to four. Nothing about the work changed. Small, fast tasks simply stopped waiting behind big, slow ones.

The task factory that uses distilled skills is now humming along with 25% more throughput, queue age down 94%, & a much more responsive system. For now, the cloud handles the hard fifth. The Mac handles the rest.

It's the minimill of agentic work. Nucor's minimills started small, capital-light, & close to demand; within a generation they outflanked the integrated steel giants.

Every laptop, phone, & edge device with enough memory to host a distilled model becomes its own minimill: routing locally, paying cloud rates only for the hard fifth. Tens of millions of these will proliferate inside companies in the next few years, each one quietly absorbing much of the work that today shows up on a hyperscaler invoice.

**Previous comment (v3.0, 2026-06-08):**

The Nucor minimill analogy is the right one, and the queue-age drop from 73 seconds to four is the detail that makes it real — the win isn't a smarter model, it's a routing layer that stops small tasks waiting behind big ones. That classifier deciding local-vs-cloud per task is the part most people miss when they talk about edge AI: the model is one layer, the orchestration around it is where the economics actually move. I've been building on exactly this premise — small models on-device doing the bulk of the work, cloud reserved for the genuinely hard fifth — and the thing that surprised me was how much of the cost wasn't inference at all, it was the plumbing that decides what runs where. The interesting question you're circling is governance: once tens of millions of these minimills are running inside a company, what's the audit trail for what stayed local versus what left the building?

**Updated comment (v3.2, 2026-06-10):**

Steel already ran this experiment - the integrated mills had the scale advantage and still lost to minimills sitting next to their customers, and a model on the same machine as the work is that bet replayed. Queue age at 4 seconds instead of 73 is the figure I would put in front of a CFO. And the 78% has headroom - 128Gb shared-memory desktops are becoming ordinary kit, and distilled models keep eating more of the routine end of the workload.

<sub>Agree-and-Add · Green Zone / Tier 2 · story: none (opinion pillar — AI on the edge / small models; no credential story per gate) · opener move: prediction</sub>

---

## 35. Tomasz Tunguz

🔗 https://tomtunguz.com/tokens-per-result/  ·  2026-06-03

**Post:**

> Yesterday Microsoft added a new metric to a model release card, one that will likely become a standard. Average token usage.

In the first row, the Microsoft model hits 71.6 on SWE-Bench Verified using about a third of the tokens Claude Haiku 4.5 burns.

Benchmarks are now measured on two different dimensions, the overall performance & the cost to achieve that intelligence.

This is yet another sign that the era of subsidies, tokenmaxxing, & all-out performance for many use cases is over.

Even the most valuable companies in the world cannot afford state-of-the-art intelligence for every conceivable use case. Uber capped employee AI spending after blowing through its budget in four months. Salesforce is spending $300M on Anthropic tokens & has frozen engineering hires.

This new dual benchmark answers the buyer's only question: what is my intelligence per dollar?

Artificial Analysis already benchmarks this. GPT 5.5 & Claude Opus 4.8 land within a point of each other on the Intelligence Index, around 60. Running the index costs $3,357 on GPT 5.5 & $4,685 on Opus 4.8. Same answer, 40% more expensive.

Model companies must now compete on both dimensions. The application layer will compete one level up, on dollars per outcome, what a closed ticket, a shipped PR, or a resolved support case actually costs.

Every layer in the stack now has to price the same way the customer thinks: per result, not per token.

**Previous comment (v3.0, 2026-06-08):**

"Per result, not per token" is the line that'll age well — buyers have always priced outcomes, the token meter was just a supply-side artefact they tolerated while subsidies lasted. This rhymes with something from my enterprise software years: for every million in licence we sold, there was roughly fifteen million in services. The dirty secret was that almost none of the value lived in the thing you metered — it lived in getting to the outcome, and the more complex the product, the more that ratio blew out. Intelligence-per-dollar is the model-layer version of the same reckoning, and I think your point about the app layer competing on dollars-per-outcome is where it gets genuinely hard: a closed ticket has a knowable cost, but the orchestration, evals and guardrails that make the outcome trustworthy don't show up on the token bill at all.

**Updated comment (v3.2, 2026-06-10):**

Intelligence per dollar is the buyer's spreadsheet finally reaching the model layer. Rings familiar - services in my last business ran around 10-15x the licence, because the metered unit was never where the cost of a real outcome sat. The application layer will hit the same maths: a closed ticket sounds priceable until you add the evals, guardrails and orchestration that make it trustworthy, and that spend never appears in a token count. Same score, 40% more expensive - procurement will sort that out quicker than the benchmarks do.

<sub>Share-Experience · Green Zone / Tier 2 · story: Story 10 — Enterprise Services Ratio (10-15x), Green status, deployed per gate with his real phrasing · opener move: assertion-first</sub>

---

*Skips (11) and unverified accounts (14) are unchanged — see `2026-06-08_comment-drafts.md` for those records and all retrieval provenance.*
