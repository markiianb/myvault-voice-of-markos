---
chunk_id: "stories"
version: "1.1"
last_updated: "2026-06-08"
status: "active"
---

# Stories — Markos

Twelve personal stories from the voice session transcript. Search by pillar when drafting. Check status before using.

**Status:** Green = use freely. Yellow = needs Markos sign-off per post. Red = abstract the principle only, never use directly.

---

## Activation scan (run before any review)

For any Markos-bylined draft:

1. Identify the pillars the draft touches.
2. Cross-reference against the pillar tags below. List every Green story directly on-topic.
3. For each on-topic Green story, mark status in the draft:
   - **Deployed** — story told with anchor details (numbers, named tools, specific scene)
   - **Referenced** — story alluded to without specifics
   - **Absent** — on-topic, missing

Zero stories deployed on a directly-on-topic draft is a failure. Markos's authority runs on lived specifics; abstract claims without anchoring stories flatten him into any-consultant voice.

**Why:** Stories carry the credential work. Without them, the voice sounds like anyone with the right opinions.

---

## Scope: stories are post material; gated for comments (v3.0, MVM-153)

**For posts, this file is core material** — Markos is the speaker, and stories carry the credential work.

**For comments, this file loads *conditionally*, behind a gate.** The `markos_comment` and `markos_reply` profiles in `_retrieval-rules.yaml` v2.3 include this chunk in `load_if_relevant`, not `always_load`. Deploy a credential story in a comment **only when the post topic is *at least part* of what the story answers**, and **never reuse the same credential within a short window**. (This reverses the v2.1 blanket exclusion: Markos's own 20-post review found the comment defect was the *contrarian opener*, not the credential — and he endorsed credential stories where the topic fit, e.g. direct-pay and services-scale posts, while declining loose-fit and reuse.)

If you are drafting a comment and a credential surfaces on a post whose topic the story doesn't answer, **the gate failed** — cut it and react to the post instead. See `craft/comment-craft.md` v3.0 § story-gating and `craft/antipatterns.md` § The Ungated Credential.

---

### 1. The $100k Google Cloud Fraud
**Status:** Yellow (first full public telling needs framing sign-off)
**Pillars:** `#big-tech-accountability` `#consumer-data-rights` `#platform-liability` `#ai-personal-advocacy`
**Quote:** *"It's been a battle since the end of October, guys, you know, since I got $100,000 bill, while I was on vacation."* Google told him it was *"my responsibility that they got hacked. Someone used my API and spent 100 grand."* 75% credit months later — *"That's still $20,000. So that's what the big guys will do to the little guys."*
**Caution:** Don't soften the numbers. Don't name individual Google employees.

### 2. Growing Up in the Software Business
**Status:** Green
**Pillars:** `#origin` `#credibility` `#inflection-points`
**Quote:** *"I was literally grew up in the software business… it was founded in the family home in the attic, not in the garage as happens in California, but in the attic of the family home."* At 9 he made presentations for his father on character-based systems — *"He'd scribble like on a brilliant sheet of paper and I'm in there using the equivalent of, I don't know what the hell it's called some, you know, package."*
**Caution:** None. The story he tells most often.

### 3. The Bookshop with His Father
**Status:** Green
**Pillars:** `#historical-perspective` `#natural-language-programming` `#inflection-points`
**Quote:** *"I was like, I wonder what generation language it will be when we can speak to the computer and it can program. I'm telling my son this yesterday."* / *"That will be an inflection point. And it is an inflection point, a huge inflection point."*
**Caution:** None.

### 4. His Father and the Visa Credit Card Descope
**Status:** Green
**Pillars:** `#simplicity` `#descoping` `#pragmatic-delivery`
**Quote:** *"It was my father that said this. He used to. He was designing the Visa credit card system. Somebody before him was trying for years and failed. And they brought him in. The first thing he did was descope. Bunch of stuff. He's like, you're trying to do too much here."*
**Caution:** None.

### 5. His 8-Year-Old Son's Claude and Lovable Subscriptions
**Status:** Yellow
**Pillars:** `#democratising-ai` `#education` `#next-generation`
**Quote:** *"My son, now about 8, I saw his pocket money, he signed up for a cloud [Claude] subscription and a lovable subscription. I was like, I'm impressed. That's good use of your pocket money, son."*
**Caution:** Anonymise always. Never use son's name, school, city, or age beyond "8". Abstract to "my son" / "kids his age".

### 6. Selling the Family Software Company
**Status:** Green (at disclosed level; anything more specific goes Yellow)
**Pillars:** `#credibility` `#authority` `#track-record`
**Quote:** *"Four or five years ago sold a global software company privately held by my family and I'd been running it for, you know, the last decade or so… we owned 100% of the company when we sold it and it was profitable. And we never borrowed a penny."*
**Caution:** No dollar amounts, no buyer name (see Never Engage section in `guardrails/guardrails.md` for IFS).

### 7. Eloqua / First Marketing Automation in Europe
**Status:** Green
**Pillars:** `#range-of-experience` `#first-mover`
**Quote:** *"Were the first in the world to roll out marketing automation in Europe. Well, first in Europe, third in the world which is now Oracle Marketing Cloud. But it was Eloqua at the time."*
**Caution:** None.

### 8. Official Secrets Act Classified Work
**Status:** Yellow (abstract framing only; any concrete detail needs sign-off)
**Pillars:** `#security-credibility` `#zero-trust`
**Quote:** *"When you're dealing with sensitive information, like highly sensitive and classified sort of stuff… you know, very sort of sensitive classified type agencies and governments… They really do go through the very fine detail of these fisma and security and controls audits."* / *"Security is a living breathing thing."*
**Caution:** Never name agencies, customers, projects, countries, or time-periods. He signed the Official Secrets Act.

### 9. Trustworthy.com Competitor Teardown
**Status:** Red on naming. Yellow for anonymised UX observations. Green for the MyVault principles it generates.
**Pillars:** `#anti-dark-pattern` `#ux-onboarding` `#differentiation`
**Quote:** *"It doesn't even tell you what it's doing. It just starts syncing… just got like 16 characters. It's like, what the."* / *"25 Mil [raised]. With 25 mil we could build something a little bit better than that."*
**Caution:** Never name Trustworthy.com on LinkedIn. Anonymise to "a competitor I just tried" at most.

### 10. Enterprise Services Ratio (15:1)
**Status:** Green
**Pillars:** `#simplicity` `#anti-enterprise` `#why-software-is-broken`
**Quote:** *"For every million of license we sold, there was probably 15 million of services. I mean it's mental… It's the dirty little secret. You know, the more complicated the software is, the more services dollars, the more the consultants recommend your software."*
**Caution:** Keep it structural — don't name firms or consultants.

### 11. Visiting CIOs at Fortune 100s
**Status:** Green
**Pillars:** `#decision-making` `#enterprise-reality`
**Quote:** *"I have visited CIOs, you know, heads of tech at big, you know, Fortune 100 companies. And when they're bought in… things happen quickly. They just do."* / *"If many people have to make a decision, if it's a group to say nobody makes a decision, it's no decision."*
**Caution:** No customer names ever.

### 12. Knowledge Graph / Architecture "Hardest Decision"
**Status:** Green
**Pillars:** `#product-credibility` `#architectural-conviction`
**Quote:** *"Having sophisticated hierarchical knowledge graph. I mean I haven't seen anything like it. But you know, this was my design and I'm getting pushed back at first. But now it exists."*
**Caution:** Don't over-claim technical specifics — keep at design-decision level.
