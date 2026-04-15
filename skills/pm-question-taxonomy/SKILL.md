---
name: pm-question-taxonomy
description: >
  This skill activates automatically whenever a PM interview question appears in conversation.
  Trigger phrases include: "they asked me", "the question was", "how would I answer",
  "practice question", "mock question", or any question that looks like a PM interview prompt
  (product design, metrics, strategy, estimation, leadership, execution, case study).
  Automatically surface the question type and what the interviewer is actually evaluating.
metadata:
  version: "0.1.0"
---

# PM Question Taxonomy

When a PM interview question appears, immediately classify it and surface the real evaluation criteria before coaching begins. Do not wait for the user to ask — this is passive intelligence that runs automatically.

## Classification Table

Classify every question into one of these types. Use the second column to frame all coaching.

| Type | What the interviewer is actually evaluating | Signal phrases |
|---|---|---|
| **Product Sense** | Do you have taste? Can you identify what matters to users before jumping to solutions? | "Design a product for...", "How would you improve...", "What would you build..." |
| **Strategy** | Can you hold multiple timescales and make defensible tradeoffs? | "How would you grow...", "What's your vision for...", "How would you prioritize..." |
| **Metrics / Analytics** | Do you think in systems? Can you separate signal from noise? | "How would you measure...", "DAU dropped X%...", "Define success for..." |
| **Execution / Delivery** | Have you actually shipped things under organizational pressure? | "Tell me about a time you launched...", "How did you handle a missed deadline..." |
| **Estimation / Guesstimate** | Can you reason under ambiguity without needing certainty? | "How many...", "Estimate the market size...", "How would you size..." |
| **Leadership / Influence** | Can you move people and resources you don't control? | "Tell me about a time you influenced...", "How did you align stakeholders...", "How do you manage up..." |
| **Design Critique** | Do you see products as users do, not as builders do? | "What do you think of [product]?", "Critique this design...", "Walk me through your feedback on..." |
| **Behavioral / Situational** | Do your past decisions reveal how you'll behave here? | "Tell me about a time...", "Give me an example of..." |

## Output Format

When a question is detected, output a one-line classification before any coaching:

> **Question type**: [Type] — [One sentence on what this interviewer is actually checking]

Then proceed with coaching, framework guidance, or practice as appropriate.

## Why This Matters

The same answer can be right or wrong depending on what type of question is being asked. A metrics question answered with a story is a miss. A product sense question answered with a framework before identifying users is a miss. Classification is the prerequisite to good coaching.

If a question spans multiple types (e.g., "How would you measure success for a product you'd design for X?"), name the primary type and note the secondary: "This is primarily Product Sense with a Metrics component — lead with user framing, land on metrics."
