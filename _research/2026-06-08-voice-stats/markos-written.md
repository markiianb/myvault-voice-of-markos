<!-- CORPUS FIREWALL: statistics only. Measurement input for voice_stats.py.
     NEVER an exemplar to imitate; do NOT load into a drafting context.
     This is the canonical WRITTEN rendering of Markos's voice — the hand-curated
     "✅ real Markos" after-examples and LinkedIn projections from the voice system.
     It is the correct source for PUNCTUATION and written-rhythm targets (em-dash
     rate especially): the Fireflies speech transcript renders his asides as
     commas/periods, but on the page his self-corrections and nested thoughts
     become em-dashes. Provenance: craft/antipatterns.md (After/real-Markos),
     _analysis/markos-linguistic-study.md Part 2 F/G/H/K/L, voice/voice.md. -->

The model is doing maybe 10% of the work in any real AI product. The other 90% is the architecture around it — retrieval, data plumbing, structured output, guardrails, the knowledge graph your files sit in, the permissions layer, the vector indexes you rebuild when schemas change.

Most orgs rolling out AI are mistaking work practices for governance frameworks. The ones that actually govern AI started with data lineage and access control — not a policy document.

When we designed MyVault, I pushed for a hierarchical knowledge graph that most of my team thought was overkill. I was getting pushback. Now it exists — and it's the thing that makes the whole product work. The LLM on its own would just hallucinate over a pile of PDFs.

Qwen 3 just beat Claude Opus on coding end to end. It's twenty times cheaper. That's not a rounding error — that's a different industry forming.

I downloaded a well-funded competitor's app this week. Twenty-five million raised. It started syncing my email before it asked for permission. It used random hash filenames instead of recognising that a photo is a driver's licence. These are the UX decisions that tell you what a company actually cares about.

In an AI system done properly, you don't let the model send output unverified. You have multiple ways to verify — knowledge graph, embeddings, structured output, audit logs.

If you're building with AI this year, the question worth spending a week on is not "which model?" — it's: what's the system around the model?

Bedrock has contractual guardrails: your data is not collected, not used for training, not saved. That's why the banks pick it. The business model underneath the API design shapes who can trust it.

35 years ago, I asked my father what generation of language it would be when we could speak to a computer and it programs. I'm telling my son this now — and we're in that generation.

A few months back I got a $100,000 Google Cloud bill while on vacation. They told me it was my responsibility their API got hacked. Two corroborating cases surfaced within weeks — a student hit for $80,000, a developer hit just before me. These are not isolated. They're just not being talked about.

Privacy isn't a trade-off you make for convenience — it's control over when, and if, someone else gets access to what's yours. The tradeoff isn't real. It's the business model of apps that don't know how to charge you directly.

Zero Trust is a methodology — every layer, every contract, every effort working to protect the user's data. I'd rather describe what we actually do than borrow a crypto term we don't quite meet.

If you're building with AI in 2026, this is the conversation to be having. Where have you seen this work — or not work?
