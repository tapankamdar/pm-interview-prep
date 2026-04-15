---
name: pm-company-archetype
description: >
  This skill activates when a company name appears in interview prep context, or when the user
  asks how a specific company interviews, what they look for, or how to prepare for a particular
  type of company. Trigger phrases include: "how does [company] interview", "what does [company]
  look for", "preparing for [company]", or any time a company is named alongside interview prep intent.
  Classify the company's interview archetype and calibrate all coaching to match.
metadata:
  version: "0.1.0"
---

# PM Company Archetype

PM interview criteria differ fundamentally by company type. Before generating any prep content, classify the company into an archetype and use it to calibrate the entire coaching output. See `references/archetype-profiles.md` for detailed profiles.

## Archetype Classification

| Archetype | Examples | What they optimize for |
|---|---|---|
| **FAANG / Big Tech** | Large public tech companies | Structured loops, calibrated bar, behavioral + product sense separated, bar raiser culture, seniority precision |
| **Hypergrowth SaaS** | Fast-growing B2B SaaS, Series B–D | Speed and ownership over polish. "I decided, I owned, here's the number." Founder-accessible culture |
| **Enterprise / B2B** | Established enterprise software, industrial | Stakeholder complexity, org navigation, change management, long sales cycles |
| **AI-first / Frontier** | AI labs and AI-native startups | AI product conviction, not just AI experience. Defensible POV on where AI creates durable value |
| **Marketplace / Platform** | Two-sided or multi-sided platforms | Supply-demand balance, network effects, multi-sided platform thinking |
| **Travel / Commerce** | Travel, e-commerce, transactions | Transaction optimization, search and discovery, personalization at scale |
| **Series B–C Growth Stage** | Variable | Generalist PM, ambiguity tolerance, 0-to-1 comfort, wearing multiple hats |

## How Archetype Affects Coaching Output

**Story selection:** FAANG wants depth and scale. Hypergrowth SaaS wants ownership and speed. Enterprise wants stakeholder navigation.

**3-pillar strategy:** FAANG pillars should show platform-level thinking. Hypergrowth SaaS pillars should be operationally specific with business metrics. AI-first pillars should demonstrate AI conviction beyond feature familiarity.

**Origin story:** Calibrate the bridge to match what this company uniquely cares about. A FAANG origin story should connect to platform leverage and scale. A marketplace origin story should connect to the specific supply-demand or access problem they solve.

**Answer depth:** At FAANG, going 3 levels deep on a decision earns credibility. At hypergrowth SaaS, 3 levels deep signals overthinking — they want the decision and the outcome.

**Questions to ask:** FAANG interviewers respond to vision probes and platform-leverage questions. Hypergrowth SaaS interviewers respond to speed and prioritization questions. AI-first interviewers respond to honest uncertainty and conviction questions.

## Classification Logic

If the company doesn't fit a clean archetype, use the combination that best matches:
- Stage (early-stage vs. growth vs. public) takes priority over industry
- The specific role type (product-building vs. operational vs. platform) adjusts scoring weights within the archetype
- When uncertain, ask the user: "What's the company size and stage? That affects how I'll calibrate this."
