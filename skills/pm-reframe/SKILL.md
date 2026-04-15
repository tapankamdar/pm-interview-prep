---
name: pm-reframe
description: >
  This skill should be used when the user says "/pm-reframe", "how do I handle the question about [gap]",
  "they'll ask about my short tenure at [company]", "I don't have [domain] experience", "how do I explain
  [career gap / transition / rejection]", or "what's my biggest liability for this role". Generate the
  assertive reframe for the single most likely concern an interviewer will have — not a defensive
  explanation, a genuine repositioning.
metadata:
  version: "0.1.0"
---

# PM Reframe — Proactive Liability Handler

Generate the assertive reframe for the candidate's most likely liability with a specific company. This is not damage control. A reframe is a genuine repositioning: why the apparent gap is actually an asset or irrelevant for this specific role.

## The Difference Between Defense and Reframe

**Defense:** "I know I don't have [domain] experience, but I've learned quickly in every new domain and I'm confident I can get up to speed."

**Reframe:** "I don't come from [domain] — and I'd argue that's an asset here. The companies that have struggled with [domain] AI have mostly approached it as a [domain] problem. The companies winning are treating it as a trust problem. That's a design and product problem. My background is in building AI products where the stakes of being wrong are high. The domain is different; the challenge isn't."

The reframe doesn't apologize. It repositions the gap as a feature, not a bug — grounded in a specific insight about what this role actually requires.

## Required Inputs

- Company name and role
- The specific concern the candidate anticipates (or ask: "What do you think they'll push back on most?")

## Step 1: Name the Real Concern

Don't address the surface question. Identify what the interviewer is actually worried about underneath it.

| Surface question | Real concern |
|---|---|
| "You were only at [company] X months..." | Will you stay? Are you coachable? Did something go wrong? |
| "You don't have [domain] experience" | Will you have a learning curve that costs us time? |
| "We heard you were interviewing for another role there..." | Are we your second choice? Will you leave if that opens up? |
| "Your last role was at a smaller company than this..." | Can you operate at our scale and complexity? |
| "You've been VP-level — is this role a step down?" | Will you be frustrated? Will you leave when something bigger opens? |

Address the real concern in the reframe, not the surface question.

## Step 2: Build the Reframe

Structure:
1. **Acknowledge without hedging** — one sentence that names the fact directly
2. **The reframe** — why this is actually different from the concern it looks like, grounded in a specific insight
3. **The evidence** — one or two concrete examples that make the reframe credible
4. **The forward close** — what this means for how you'd operate in this role

Keep it to 4–6 sentences. Practiced confidence, not practiced length.

## Step 3: Decide When to Deploy

Some reframes should be deployed proactively — early in the conversation before they ask. Others should be held ready for when the question comes.

**Deploy proactively if:** The concern is so obvious that not addressing it would make the interviewer wonder why you avoided it. Domain gap, major company change, very short tenure.

**Hold for when asked if:** The concern requires them to raise it first, or proactively addressing it would draw more attention than it deserves.

Output both the reframe and a deployment note: "Deploy proactively in your opening / Hold for when asked."

## Common Reframe Patterns

**Domain gap reframe:** "I don't come from [domain] — and I'd argue that's an asset here. [Domain] approaches this as a [domain] problem. The companies winning are approaching it as a [your expertise] problem. That's my training."

**Short tenure reframe:** "I completed my time at [company] when [specific event] — [brief factual reason]. Long enough to [specific achievement]. The right moment to [bring learnings forward]."

**Scale regression reframe:** "Moving from [larger] to [smaller] isn't a regression — it's a deliberate choice. At [larger company], I spent [X]% of my time on organizational navigation. Here, the leverage is [specific thing smaller company can do that larger can't]. That's the bet I'm making."

**Second-choice concern reframe:** "I'm in conversation with several companies, but I want to be direct: [this role / this problem / this team] maps most closely to [specific reason]. I'm not managing optics — I'm telling you which problem matches my toolset best."
