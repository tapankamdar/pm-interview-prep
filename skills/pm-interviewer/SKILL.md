---
name: pm-interviewer
description: >
  This skill should be used when the user says "/pm-interviewer", "build a card for [interviewer name]",
  "prep me for my interview with [name]", "decode [name]'s background", or provides an interviewer
  name with their LinkedIn URL or profile information. Build a psychological profile of the interviewer,
  infer their evaluation role, predict their top questions, and generate response frameworks and
  fit-demonstrating questions to ask them.
metadata:
  version: "0.1.0"
---

# PM Interviewer — Per-Interviewer Intelligence Card

Build a complete interviewer card from a name and LinkedIn URL (or pasted profile). Decode what their career arc tells you about what they value — then translate that into predicted questions, response frameworks, and strategic questions to ask.

## Required Input

Interviewer name + one of:
- LinkedIn URL (preferred)
- Pasted LinkedIn profile text
- Role title + company + brief background

Also helpful: company name, role title, interview stage (HM vs. panel).

## Step 1: Decode the Arc, Not the Resume

Do not summarize where they worked. Decode what their trajectory tells you about what they value in candidates.

Ask for each role in their history:
- What problems did they work on?
- What scale and complexity did they operate at?
- What failures or pivots are visible (company shutdowns, role changes, public writing)?
- What kind of thinking do they demonstrate in public writing, talks, or posts?

Then synthesize: "Their arc tells you they value [X]. The rapport hook is [Y] — something in your background that creates peer-level connection."

**What good looks like:** "They ran an internal incubator for 6 years — they know the difference between an experiment and a product thesis. They left a high-profile role to come back and build this. They want a partner with conviction, not a candidate." This is a psychological reading, not a resume summary.

## Step 2: Infer Their Evaluation Role

In structured panels, different interviewers own different dimensions. Infer from:
- Their title and function (engineering = technical depth, design = user empathy, PM = product craft, business = GTM/strategy)
- Their seniority relative to the role (senior = bar calibration, peer = team fit, cross-functional = collaboration signal)
- Any information from the recruiter about the round format

State it explicitly: "Owns: [2–3 competencies]. Will likely probe: [specific angle]."

## Step 3: Generate Top 5 Predicted Questions

Not generic PM questions. Questions specific to this person's lens and this company's priorities. For each question:

```
### [Question]
- Framework: [How to approach it — one sentence]
- Beat 1: [15–20 seconds spoken]
- Beat 2:
- Beat 3:
- Beat 4:
- Earned secret: [The counterintuitive insight to land — the line that makes this answer unmistakably specific]
```

## Step 4: Generate Top 3 Questions to Ask Them

These are not generic curiosity questions. They are questions that demonstrate the candidate is already thinking like someone in the role.

The bar for each question: it must imply a specific company data point, a formed hypothesis, or a strategic insight the candidate has developed. "What does success look like in this role?" fails. "You've scaled products at [context] — what's the constraint you'd protect against most as this team grows?" passes.

Include a note on what each question signals to the interviewer.

## Output Format

```
## [Interviewer Name] — [Title]
**Background decode:** [3–4 sentences on what their arc tells you they value]
**Evaluation role:** [What they own in this interview]
**Rapport hook:** [One thing that creates peer-level connection]

### Predicted Q1: [Question]
- Framework: [approach]
- Beats: [4–5 bullets at 15–20s each]
- Earned secret: [the line to land]

[Q2–Q5]

### Questions to ask them:
1. [Question] — *signals: [what this demonstrates]*
2. [Question] — *signals: [what this demonstrates]*
3. [Question] — *signals: [what this demonstrates]*
```
