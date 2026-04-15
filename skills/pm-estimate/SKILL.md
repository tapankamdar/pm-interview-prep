---
name: pm-estimate
description: >
  This skill should be used when the user says "/pm-estimate", "practice an estimation question",
  "how would I estimate [X]", "TAM sizing", "guesstimate", "how many [X] are there", or presents any
  question requiring quantitative reasoning under ambiguity. Coach PM-calibrated estimation: TAM sizing,
  investment thresholds, revenue potential, and feature impact sizing — not piano tuners.
metadata:
  version: "0.1.0"
---

# PM Estimate — Estimation & Guesstimate Practice

PM estimation questions at senior levels are rarely about piano tuners. They're about whether you can reason quantitatively about a business decision under ambiguity, and whether you signal appropriate confidence without false precision.

## PM-Relevant Estimation Types

| Type | Example | What it tests |
|---|---|---|
| TAM sizing | "Estimate the total market for grocery delivery AI" | Market framing and decomposition |
| Investment threshold | "How many users would justify building this feature?" | Unit economics and prioritization thinking |
| Revenue potential | "Estimate the revenue impact of this product initiative" | Business modeling and assumption-making |
| Feature impact | "If we improve checkout conversion by 2%, what's the impact?" | Data fluency and back-of-envelope rigor |
| Operational sizing | "How many support agents would this automation replace?" | Operational math and cost modeling |

## The Estimation Protocol

Run this sequence for every estimation question:

**Step 1 — Clarify the question**
What specifically are they asking for? Is this a market size or a revenue estimate? Is it global or US-only? Current state or projected? Clarifying doesn't signal weakness — it signals precision.

**Step 2 — State the approach before calculating**
Name the decomposition method before running numbers. "I'll approach this top-down from population → segment → penetration → ARPU." This shows structured thinking, not just arithmetic.

**Step 3 — Label every assumption**
Every number that isn't a known fact is an assumption. Say so. "I'm assuming ~40% of US households order groceries online at least once a month — I could be off by 50% here but let's use it as an anchor."

**Step 4 — Round aggressively**
Estimation is about order-of-magnitude confidence, not precision. Use round numbers. $50M not $47.3M. 100M users not 94.2M. False precision signals the candidate doesn't understand what estimation is for.

**Step 5 — Sanity check the answer**
After calculating, ask: "Does this feel right?" Compare to a known reference point. "That gives us $2B TAM. The US grocery market is ~$1T total, and online is ~$100B, so $2B for AI-assisted grocery delivery feels plausible — roughly 2% of online."

**Step 6 — State confidence and what would change it**
What assumption, if wrong, would most change the answer? "If delivery penetration is 20% instead of 40%, the TAM halves. That's the most uncertain number in this model."

## Coaching Focus Areas

**Decomposition structure:** Did they break the problem into components cleanly? A good decomposition makes the assumptions visible and the math checkable.

**Assumption quality:** Are the assumptions reasonable? Are they labeled as assumptions? Did they sanity-check against known facts?

**Communication of uncertainty:** Did they signal appropriate confidence — enough to be useful, not so much as to be misleading?

**The "so what":** Senior PM estimation questions usually lead somewhere. "So with a $2B TAM and assuming 5% market share at scale, this is a $100M revenue opportunity — which at 5x revenue multiple is a $500M value creation play. That's why it's worth prioritizing over the $30M opportunity on the roadmap." The estimate should inform a decision, not just demonstrate arithmetic.

## Common Mistakes to Flag

- **Starting to calculate without decomposing:** Running numbers without explaining the approach
- **False precision:** "$47.3M" instead of "~$50M"
- **Unlabeled assumptions:** Treating estimates as facts
- **No sanity check:** An answer that's clearly off-scale with no recognition
- **No "so what":** Completing the estimate without connecting it to the decision it should inform
