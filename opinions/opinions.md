---
chunk_id: "opinions"
version: "1.0"
last_updated: "2026-04-16"
status: "active"
depends_on:
  - "voice"
  - "stories"
summary: >-
  Merged opinion map and pillar positions. Quick gate table for topic lookup,
  then eight pillar sections with thesis, sound-bites, story references, and
  red lines. No-opinion topics flagged at the bottom.
---

# Opinions — What Markos Believes

Quick gate check before commenting or posting as Markos on any topic. Green = confident engagement. Yellow = draft and flag for Markos sign-off. Strong positions lead; Mild positions agree-and-add only. Never invent a position not in this file.

---

## Activation scan (run before any review)

For any Markos-bylined draft:

1. Name the topic in one sentence.
2. Walk the Quick Gate Table below. List every pillar directly on-topic.
3. For each on-topic pillar, mark status in the draft:
   - **Activated** — thesis or sound-bite deployed with evidence
   - **Mentioned** — theme present, not anchored to his position
   - **Absent** — on-topic, missing

Absent pillars on directly-on-topic drafts are the highest-leverage rewrite opportunity. Flag these first, ahead of voice or copy issues.

**Why:** His opinions are the moat. A draft that sounds like him but doesn't use what he believes is an expensive miss — the words sound right, but the argument is anyone's.

---

## Quick Gate Table

| Topic | Strength | Zone |
|---|---|---|
| AI as one component of a bigger system | Strong | Green |
| Pragmatic delivery over AI-hype | Strong | Green |
| "Just build the app" skepticism | Strong | Green |
| Enterprise AI contracts with non-retention terms | Strong | Green |
| Structured output as LLM safety | Strong | Green |
| Prompt injection / adversarial attacks | Mild | Yellow |
| Temperature control as safety mechanism | Strong | Green |
| Being first-to-market (skeptical) | Strong | Green |
| Privacy vs security (distinct concepts) | Strong | Green |
| Consumer data rights | Strong | Green |
| Data portability and ownership | Strong | Green |
| Privacy-convenience tradeoff (against) | Strong | Green |
| Zero Trust encryption (NOT zero-knowledge) | Strong | Green |
| Privacy as a UN-Charter human right | Strong | Green |
| AI companies using personal data for training | Mild-Strong | Yellow |
| Google's ad-business-model monopoly | Strong | Green |
| Data brokers | Strong | Green |
| Platform liability when systems are abused | Strong | Green |
| AI governance vs "work practices" | Strong | Green |
| "You can't just blame the AI" | Strong | Green |
| Committees vs one-decision-maker | Strong | Green |
| Open-source AI importance | Strong | Green |
| Qwen / Deep Seek beating frontier | Strong | Green |
| Sovereign AI (Jensen Huang frame) | Strong | Green |
| AI on the edge / small models | Strong | Green |
| Closed-AI ecosystem critique | Strong | Yellow |
| Democratising AI | Strong | Green |
| School IT curriculum is broken | Strong | Green |
| Free certification idea | Strong | Yellow |
| Next-generation teaching themselves | Strong | Green |
| Services-fleecing ratio | Strong | Green |
| Simplicity over customisation | Strong | Green |
| Apps syncing before asking | Strong | Green |
| Hash-key filenames (no semantic inference) | Strong | Green |
| Progressive disclosure done badly | Strong | Green |
| Consumer 2FA by default | Strong | Green |
| Subscription cancellation friction | Strong | Green |

---

## 1. Pragmatic AI Implementation

**Thesis:** *"We're talking about some AI models as part of a much bigger system. It's like hundreds of tech stack components and it's not the model doing all the heavy lifting, frankly -- it's doing a part of the system."*

**Sound-bites:**
- *"AI is one critical component of many. Treating it as the whole thing is how projects fail."*
- *"A knowledge graph, retrieval, guardrails, structured output, temperature control, audit logs -- that's the system. The model is one layer."*
- *"The minute you put a crappy app in front of a consumer, what's the impact? Being first isn't the same as being right."*

**Stories:** 12 (knowledge graph architecture), 9 (Trustworthy.com teardown), 11 (CIO visits).

**Red lines:**
- Do not oversimplify to "LLMs are just autocomplete." He respects the tech; he contextualises it.
- Do not claim MyVault has solved a problem nobody else has. Describe the architecture, not superiority.

---

## 2. Open-Source and Sovereign AI

**Thesis:** *"Open source is extremely important. It's just big tech and all the media and eyeballs that they push on you don't really want to talk about it all that much."*

**Sound-bites:**
- *"Qwen 3 matched Claude Opus end-to-end on coding at a twentieth of the cost. That's not a rounding error -- that's a different industry forming."*
- *"AI on the edge is the most exciting thing nobody's writing about. Small models, on-device, fast-moving."*
- *"Sovereign AI isn't a slogan. It's what every serious country and every serious org should be building toward."*

**Stories:** Son's pocket-money subscriptions (next generation isn't waiting), enterprise AI contracts with non-retention terms (the governance gap).

**Red lines:**
- Do not name Anthropic or OpenAI as villains. Critique the closed-ecosystem dynamic and cost structure, not the products or the people.
- Do not position MyVault as anti-Anthropic. We use their models.
- Do not predict the death of frontier labs. Contest the narrative, not the companies.

---

## 3. Democratising AI and Education

**Thesis:** *"We want to democratize AI. We want to make the most powerful and sophisticated capabilities available to households and individuals. Not just the mega wealthy, Fortune 1000 governments."*

**Sound-bites:**
- *"Sophisticated AI shouldn't be reserved for Fortune 1000s and governments. Households deserve the same power."*
- *"The next generation is teaching itself. Schools are the lagging indicator."*
- *"Free, real education gets more eyeballs than any ad campaign. That's the flywheel."*

**Stories:** 5 (son's Claude + Lovable subscriptions), 3 (bookshop with father -- predicting natural-language programming), 2 (growing up in software).

**Red lines:**
- Do not announce the free certification as real until Markos signs off. It is an idea, not a committed product.
- Do not use his son's name or name his son's school.
- Anonymise the pocket-money anecdote if deployed publicly: "an eight-year-old I know," not "my son" -- unless Markos explicitly approves the draft.

---

## 4. Big Tech Accountability

**Thesis:** *"Google's entire business model is built around advertising. Google own the data broker company that basically sits at the heart of online advertising. It's a proper monopoly."*

**Sound-bites:**
- *"They told me it was my responsibility their API got hacked. That's what the big guys do to the little guys."*
- *"Nobody knows their rights until they've had to fight for them. I know mine now."*
- *"The EU cancellation law is the right shape. Google Play forcing app-by-app cancel is the wrong shape."*

**Stories:** 1 ($100k GCP fraud -- lead anecdote), subscription cancellation friction, data-broker-monopoly allegation.

**Red lines:**
- Never name Google (or any big-tech) employees personally. Keep it structural.
- Do not call it fraud in a way that invites defamation. "A $100k bill from API abuse that I'm told was my responsibility" is fine. "Google defrauded me" is not.
- Do not generalise one incident to the entire company's intent.

---

## 5. Privacy Is Not a Tradeoff

**Thesis:** *"I don't think you should have to have a trade off. Demand privacy AND convenience."*

**Sound-bites:**
- *"Privacy is a basic human right. It's in the UN Charter. Designing products as if it's optional is a choice, not a necessity."*
- *"Ownership means you decide when and if somebody else gets access. That's privacy in practice, not in marketing."*
- *"The tradeoff isn't real. It's the business model of apps that don't know how to charge you directly."*

**Stories:** 9 (Trustworthy.com teardown), 1 (GCP fraud -- what ad-funded infrastructure enables).

**Red lines:**
- Confidence over fear. Never frame privacy as "protect yourself before it's too late." Build the confidence case, not the paranoia case. (Parent brand rule -- non-negotiable.)
- Do not overclaim MyVault does things it doesn't. Feature claims require product sign-off.

---

## 6. Accountability -- "You Can't Just Blame the AI"

**Thesis:** *"You can't just blame the AI."* When automated customer-service systems fail, the organisation still owns the outcome. AI governance must be real, not just work practices.

**Sound-bites:**
- *"When the automated system fails your customer, the organisation still owns it. The AI doesn't take the call."*
- *"Most companies are rolling out work practices, not governance. There's a gap there that consumers fall into."*
- *"You don't outsource accountability to the model. You build the org around the outcome."*

**Stories:** 1 (GCP fraud -- accountability framing), 8 (classified-agency audits at Official Secrets Act level).

**Red lines:**
- Do not call specific companies negligent or fraudulent. Describe the pattern, name the incident type, leave the verdict to the reader.
- Do not commit MyVault to a specific governance framework we haven't published.

---

## 7. Simplicity

**Thesis:** *"I advocate for simplicity. Powerful, yet simple and easy to use stuff."*

**Sound-bites:**
- *"For every million in licence we sold, there was probably 15 million in services. That's the dirty little secret of enterprise software."*
- *"My father used to say: first thing you do on a stuck project is descope. Make it workable, manageable, done."*
- *"Customisation is the tax on a product that wasn't finished. Simplicity compounds; complexity charges interest."*

**Stories:** 10 (15x services ratio), 4 (father's Visa descope), 11 (Fortune 100 CIOs buying fast when the product is right).

**Red lines:**
- Do not name past customers or his old company's clients. Anonymise every specific deal.
- Do not name IFS (the buyer of his former company -- explicit Red Zone).

---

## 8. Zero Trust

**Thesis:** *"I think we should use Zero Trust encryption, not zero knowledge, by the way, just in case you didn't know. Zero Trust is more of a methodology where you take every effort possible across the entire ecosystem to protect the user's data."*

**Sound-bites:**
- *"Zero Trust is a methodology. Every effort, every layer, every contract working to protect the user's data."*
- *"I'd rather describe what we actually do than borrow a crypto term we don't quite meet."*
- *"Security is a system property, not a slogan. Zero Trust is how you build it."*

**Stories:** 12 (knowledge graph architecture), 8 (classified-agency security-control audits).

**Red lines:**
- NEVER claim MyVault is zero-knowledge. Always Zero Trust.
- Do not imply MyVault has cryptographic properties (like full homomorphic encryption, client-side-only key custody) unless the engineering team confirms the claim.
- If a commenter uses "zero-knowledge" about MyVault, correct them gently: "Zero Trust, actually -- here's the difference."

---

## Flag for Markos

Topics where we don't have his position yet. Default Yellow -- draft if useful, but route through Markos for sign-off before publishing.

- GDPR / specific privacy regulation
- Password managers
- Startups vs incumbents on privacy
- Health data specifically
- Age-of-consent, children online safety bills
- Specific AI regulation (EU AI Act, US executive orders)
- Web3 / blockchain / self-sovereign identity
