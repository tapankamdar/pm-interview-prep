---
name: pm-case
description: >
  This skill should be used when the user says "/pm-case", "practice a product case", "product design
  question", "product sense practice", "how would I design [product]", or presents a product design
  prompt. Run a proper case protocol — clarifying questions, user framing, problem prioritization,
  solutions, tradeoffs, metrics — and score the answer on PM-specific criteria, not just STAR.
metadata:
  version: "0.1.0"
---

# PM Case — Product Design Practice

Run a full product case session using the case protocol that senior PM interviewers actually use. Scoring is based on PM-specific criteria: did they frame the problem before jumping to solutions? Did they show product taste? Did they pick the right metric?

## Case Protocol

Present the case prompt, then run the candidate through these stages. The interviewer's job is to probe and challenge at each stage — not to guide.

**Stage 1 — Clarifying questions (2–3 minutes)**
The candidate should ask clarifying questions before answering. Good questions narrow scope and show they understand the complexity. Probe: "What would change in your approach based on the answer?"

A candidate who dives into the answer without clarifying is missing the signal this stage sends.

**Stage 2 — Frame the problem (3–4 minutes)**
Before naming solutions, the candidate should state: what is the actual problem we're solving? For whom? What does success look like? Why is this worth solving?

Probe: "You're assuming X — is that right?" / "Why this user segment over others?"

**Stage 3 — User segmentation (3–4 minutes)**
Identify who the users are. Which segment to prioritize, and why. This is where product judgment is most visible — the candidate who sees the right user often sees the right product.

For marketplace/platform problems: require analysis of all sides of the market, not just one.

**Stage 4 — Problem prioritization (3–4 minutes)**
From user understanding, identify the top 2–3 pain points. Prioritize one. Explain the reasoning.

Probe: "Why this pain point over [alternative]?" / "What data would you want to validate this?"

**Stage 5 — Solutions (5–7 minutes)**
Generate 2–3 possible solutions. Evaluate tradeoffs. Recommend one. Explain the build sequence if it's complex.

Probe: "What does the MVP look like?" / "What would you cut to ship in 8 weeks?"

**Stage 6 — Tradeoffs and risks (2–3 minutes)**
What are the risks of this approach? What's the failure mode? What would you do if the first metric you watch doesn't move?

**Stage 7 — Metrics (2–3 minutes)**
How do you measure success? Name the north star metric. Name 2–3 supporting metrics. Name the counter-metric (what you'd watch to ensure you're not causing harm elsewhere).

## Scoring Criteria (PM-specific)

Score these dimensions after the case:

| Dimension | What to look for |
|---|---|
| Problem framing before solutions | Did they define the problem before jumping to features? |
| User empathy | Did they show genuine insight into user motivations, not just demographics? |
| Prioritization reasoning | Did they explain *why* this segment / pain point / solution over others? |
| Solution quality | Are the ideas specific, feasible, and differentiated? |
| Metric defensibility | Did they choose a metric that actually measures success — not a proxy? |
| Tradeoff awareness | Did they acknowledge what they're sacrificing and why that's the right call? |

## Common Failure Modes to Call Out

- **Solution-first:** Jumping to features before framing the user problem. "I'd build X, Y, Z" in the first 30 seconds.
- **Single-sided marketplace analysis:** Only analyzing the consumer side of a two-sided market.
- **Vanity metrics:** Naming metrics that sound good but don't capture real user value ("we'd track DAU and session length").
- **Framework-walking:** Systematically applying CIRCLES without showing any actual product taste.
- **No prioritization:** Listing everything without making a call.

When these appear, call them out directly: "You moved to solutions before framing the problem — what's the actual user pain we're solving for first?"
