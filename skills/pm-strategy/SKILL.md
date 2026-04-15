---
name: pm-strategy
description: >
  This skill should be used when the user says "/pm-strategy", "build my 3-pillar strategy for [company]",
  "what would I focus on in this role", "how would I approach this role", "what's my vision for [company]",
  or when a prep document needs a strategy section. Build a role-type-adapted 3-pillar strategy with
  a 1-line version and L1/L2/L3 depth cues for a specific company and role.
metadata:
  version: "0.1.0"
---

# PM Strategy — 3-Pillar Strategy Builder

Build a company-specific strategy that tells the interviewer: "This person has actually thought about what they'd do here." Every pillar must be grounded in a company fact. Generic priorities fail.

## Step 1: Detect Role Type First

The 3-pillar format adapts to the role. Using a product-vision format for an operational role signals you didn't understand the JD.

| Role type | What "3 pillars" means |
|---|---|
| Product-building (IC to Lead PM) | What you'd build and in what order — near-term product bets |
| Platform / org leader (Dir, VP) | The strategic architecture — the system, not the features |
| Functional leader (support, ops, growth) | How you'd run the function — the operational thesis |
| GM / business owner | The growth engine — P&L frame, unit economics, expansion logic |

Identify the role type from the JD before writing anything.

## Step 2: Gather Company Facts

A strategy without grounding facts is a template, not a strategy. For each pillar, require:
- A specific company metric, user signal, competitive event, or regulatory detail
- The "only you" angle: why this candidate's background makes them credible here
- The sequencing logic: why these three, why this order, why they form a system

If the user doesn't have enough company context, recommend running `/pm-decode` on the JD first or `/pm-prep` for full research.

## Step 3: Build the Three Levels

Every strategy gets all three depth levels. See `references/strategy-formats.md` for templates by role type.

**L1 — Soundbite (15–30 seconds)**
One sentence that names the strategic frame. Should be memorable and specific. Not "improve the product in three ways" — a frame that could only come from someone who thought about this company.

*Examples:*
- "Make support the lowest-cost, highest-trust learning engine." (operational role example)
- "Context over query. Authority over relevance. Action over retrieval." (platform role example)
- "Infrastructure first, the flagship second, the trust engine third — these aren't three workstreams, they're a system." (product-building role example)

**L2 — Summary (90 seconds)**
Three pillars with sequencing logic. Why these three. Why this order. Why they form a reinforcing system rather than independent bets. Stop at 90 seconds and let them probe.

**L3 — Deep dive (available on request)**
Full detail per pillar: specific company data, competitive context, 30/60/90 execution plan, risk acknowledgment. Flag this section: "Have this ready but let them pull the depth."

## Step 4: Run the Credibility Audit

Before delivering:
- Does each pillar reference a specific company fact?
- Could any pillar be used at a competitor with a find-replace?
- Does the sequencing logic explain why these three compound rather than trade off?
- Does the candidate's background specifically justify each pillar?

Flag any pillar that fails and provide the fix.

## Output Format

```
**L1:** [One-sentence soundbite]

**L2 (90-second version):**
"[Three pillars with sequencing logic — conversational prose, not bullet points]"

**L3 (on request):**
Pillar 1 — [Name]
- Grounding fact: [specific company data]
- What: [what you'd do]
- Why now: [timing rationale]
- "Only you" angle: [why your background makes this credible]
- Competitive context: [what others are / aren't doing]

[Pillar 2, Pillar 3]

**Credibility audit:** [Pass/Flag per pillar]
```
