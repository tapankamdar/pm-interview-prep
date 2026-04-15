---
name: pm-panel
description: >
  This skill should be used when the user says "/pm-panel", "show me my panel scorecard for [company]",
  "how am I tracking across rounds at [company]", or when pm-analyze detects that multiple rounds
  exist for the same company. Generate a running cross-round scorecard showing dimension scores,
  trends, consistency signals, red flags, and a momentum read for the full interview loop.
metadata:
  version: "0.1.0"
---

# PM Panel — Running Cross-Round Scorecard

When multiple interview rounds exist for the same company, generate a cumulative panel view. The individual round scorecard tells you how one conversation went. The panel scorecard tells you what the hiring committee will see.

## Trigger Conditions

Generate the panel scorecard automatically when:
- The user submits a second or later round transcript for a company already in the session
- The user explicitly requests it with `/pm-panel [company]`

## Required Input

Two or more scored rounds for the same company. Each round needs:
- Scores across six dimensions (from `pm-analyze`)
- Round type (recruiter screen / HM / specific panel interviewer)
- Date or sequence number

## Panel Scorecard Output

```
## Panel Scorecard — [Company] | Round [N] of [N] | Updated [Date]

| Dimension | R1 | R2 | R3 | Trend | Panel Avg |
|---|---|---|---|---|---|
| Product Judgment | | | | ↑/→/↓ | |
| Storytelling & Specificity | | | | | |
| Metrics Fluency | | | | | |
| Strategic Thinking | | | | | |
| Differentiation | | | | | |
| Communication & Structure | | | | | |
| **Overall** | | | | | |

### Hire Signal Trajectory
[Trending toward: Strong Hire / Hire / Mixed / No Hire]
[One sentence on whether the trajectory is building or drifting]

### Consistency Signals
[Dimensions that showed consistent strength across multiple rounds — these will stand out positively in the debrief]
[Dimensions that showed consistent weakness — these will be the committee's concern]

### Panel-Level Red Flags
[Any weakness that appeared in 2+ rounds — name it directly. This is what the hiring committee will align on.]

### Momentum Read
[Honest read on whether the panel is building toward a hire signal or drifting away. Not just the most recent round.]

### Recommended Focus for Remaining Rounds
[What to double down on: dimensions scoring 4+ that should be made unmissable]
[What to recover: dimensions scoring below 3 that need to move before the committee decision]
```

## Trend Calculation

- ↑ = Score improved by 0.5+ from prior round
- → = Score within 0.3 of prior round (stable)
- ↓ = Score dropped by 0.5+ from prior round

For 3+ rounds, show the directional trend across the full loop, not just last-to-current.

## Consistency Signal Logic

A dimension is a **positive consistency signal** if it scores 4+ in 2+ rounds. Name it as a strength that will register in the debrief.

A dimension is a **red flag** if it scores below 3 in 2+ rounds. Name it explicitly — this is the conversation the hiring committee will have about the candidate.

## Momentum Read Logic

The momentum read is not just the average. It weights:
- Recent rounds more than early rounds (interviewers debrief together at the end — recency matters)
- HM and panel rounds more than recruiter screen (recruiter scores don't weigh as heavily in committee)
- Differentiation disproportionately (at senior levels, a strong performer with low differentiation still loses to someone who made the committee remember them)

When Differentiation is below 3 in the most recent round, flag it explicitly: "The most recent round shows low Differentiation — at this seniority level, that's the dimension the committee focuses on most. Address it before any remaining rounds."
