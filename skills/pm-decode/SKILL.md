---
name: pm-decode
description: >
  This skill should be used when the user says "/pm-decode", "decode this JD", "analyze this job description",
  "is this role a good fit", "should I apply to this", "what are they really looking for", or pastes a
  job description. Analyze the JD to surface hidden evaluation criteria, role type, PM maturity level,
  fit verdict, and the questions this company will actually ask — beyond what the JD says explicitly.
metadata:
  version: "0.1.0"
---

# PM Decode — JD Analysis

Read a job description like a practitioner, not a keyword matcher. Surface what the company is actually optimizing for — including what they didn't write.

## Required Input

A job description (pasted or linked). Role title and company name if not in the JD.

## Step 1: Read for Signal, Not Keywords

Apply the JD parsing guide from `references/jd-parsing-guide.md` before writing anything. The most important signals are usually implicit.

## Step 2: Classify the Role

Identify before analyzing:

**Role type:**
- Product-building (0-to-1, scale, or optimization of an existing product)
- Operational / functional leader (support, growth, ops — outcomes are efficiency and quality, not roadmaps)
- Platform / infrastructure (building the system others build on)
- GM / business owner (P&L accountability, cross-functional ownership)

**PM maturity at this company:**
- **Early-stage PM culture:** PMs are generalists. Process is what they build, not what they follow.
- **Mid-stage:** Defined PM role. JD has meaningful specificity about scope and metrics.
- **Mature:** PM function is established. JD has precision about seniority, influence vs. authority, cross-functional norms.

## Step 3: Generate the Decode Output

Produce all five sections:

**Top 5 evaluation criteria (priority order)**
Derived from JD parsing. Not keywords — the actual competencies the hiring committee will score. Include what's implied but not stated.

**Hidden criteria (what they didn't write)**
Based on company archetype, role type, and what's conspicuously absent. Examples: "They didn't mention data/analytics — that's either a gap in the team or a signal they want someone to build it."

**Role-type frame**
What kind of PM this role actually requires. "This is a scale PM role — 0-to-1 energy would be the wrong match." Or "This is an operational leadership role — they want a function leader who uses product thinking, not a PM building a roadmap."

**Fit verdict**
Strong Fit / Investable Stretch / Long-Shot Stretch / Weak Fit — with one paragraph of rationale. For a stretch, specify what's frameable vs. structural. A frameable gap can be bridged with narrative. A structural gap cannot.

**Predicted interview questions (top 5)**
Based on the top evaluation criteria. Not generic PM questions — questions this specific company, at this specific role level, will likely ask based on what the JD signals they care about.

## Step 4: Batch Triage (when decoding multiple JDs)

When the user provides 2+ JDs for comparison, rank them by fit verdict with a one-line rationale per role. Format:

```
1. [Company A] — Strong Fit: [reason]
2. [Company B] — Investable Stretch: [gap + bridge]
3. [Company C] — Long-Shot: [structural gap]
```

Recommend which to prioritize for full prep investment.
