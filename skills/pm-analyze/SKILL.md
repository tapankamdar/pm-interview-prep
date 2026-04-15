---
name: pm-analyze
description: >
  This skill should be used when the user says "/pm-analyze", "score my interview", "I just finished
  an interview", "analyze this transcript", "how did I do", or pastes an interview transcript or
  their own notes from a completed interview round. Produce a structured PM scorecard: six dimension
  scores, top 3 strengths with transcript evidence, top 3 improvement areas with specific fixes,
  and a hire signal. When multiple rounds exist for the same company, automatically trigger
  pm-panel for a running cross-round scorecard.
metadata:
  version: "0.1.0"
---

# PM Analyze — Interview Transcript Scorer

Score a completed interview round against the six PM dimensions. Every finding must be grounded in specific evidence from the transcript or notes — no generic feedback.

## Accepted Inputs

- Full interview transcript (preferred)
- The candidate's own notes from the conversation (also valid — treat as recall-based evidence)
- Company name and round type (recruiter screen / HM / panel)
- Interviewer name if known

## Step 1: Read for Signals Before Scoring

Before scoring, identify:
- What question types appeared (use `pm-question-taxonomy`)
- Where the candidate went deep vs. stayed surface
- Where they used a framework appropriately vs. as a crutch
- Where they landed an earned insight vs. gave a generic answer
- Where the interviewer probed — probes reveal where they weren't satisfied

## Step 2: Score Six Dimensions (1–5 each)

See `references/scorecard-rubric.md` for detailed anchors per dimension.

| Dimension | What it measures |
|---|---|
| **Product Judgment** | Did they frame the user problem before solutions? Show taste and empathy? |
| **Storytelling & Specificity** | Were answers grounded in real decisions with real details, or framework-level abstractions? |
| **Metrics Fluency** | Did they choose the right metric and defend it? Or name metrics without understanding them? |
| **Strategic Thinking** | Systems-level thinking, second-order effects, sequencing logic, competitive awareness? |
| **Differentiation** | Did answers sound like only this candidate could give them? Or could any prepared PM say the same? |
| **Communication & Structure** | Easy to follow? Appropriate length? Did they know when to stop? |

Score each 1–5 with one line of rationale tied to a specific moment in the transcript.

## Step 3: Top 3 Strengths

Name the three moments that landed best. Be specific — cite the question or topic and what worked.

Format: "When you answered [question/topic], [what worked and why it's signal]."

Not: "You were clear and well-organized." That's generic. The bar: a strength should tell the candidate what to double down on in the next round.

## Step 4: Top 3 Improvement Areas

Name the three highest-priority patterns to change. Each needs:
- The specific moment it showed up
- The exact pattern that cost them (not a vague observation)
- The concrete fix for the next round

Format: "In your answer to [question/topic], [specific pattern]. To fix: [exact change]."

Not: "Be more specific." That's not actionable. The bar: the candidate should be able to make the change immediately.

## Step 5: Hire Signal

**Strong Hire / Hire / Mixed / No Hire** — with one sentence of honest rationale.

If Mixed or No Hire, be direct about which dimension(s) are the gap and whether they're fixable before the next round.

## Step 6: Highest-Leverage Fix

One priority action item before the next round. Not a list — the single thing that would most improve the panel's impression if addressed.

## Step 7: Check for Subsequent Rounds

After delivering the single-round scorecard, check: has the user submitted previous rounds for this company?

If yes → automatically generate the running panel scorecard using `pm-panel`.

If no → close with: "If you complete more rounds with [company], share those transcripts and I'll build a running panel scorecard showing how your scores trend across the loop."

## Output Format

```
## Interview Scorecard — [Company] | [Round] | [Date]

### PM Scorecard
| Dimension | Score | Evidence |
|---|---|---|
| Product Judgment | X/5 | [specific moment] |
| Storytelling & Specificity | X/5 | [specific moment] |
| Metrics Fluency | X/5 | [specific moment] |
| Strategic Thinking | X/5 | [specific moment] |
| Differentiation | X/5 | [specific moment] |
| Communication & Structure | X/5 | [specific moment] |
| **Overall** | **X/5** | |

### Hire Signal: [Strong Hire / Hire / Mixed / No Hire]
[One sentence rationale]

### Top 3 Strengths
1. [Specific moment + what worked + why it's signal]
2.
3.

### Top 3 Improvement Areas
1. [Specific moment + exact pattern + concrete fix]
2.
3.

### Highest-Leverage Fix Before Next Round
[Single priority action]
```
