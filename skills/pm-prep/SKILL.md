---
name: pm-prep
description: >
  This skill should be used when the user says "/pm-prep", "prepare me for my interview at [company]",
  "build my prep doc for [company]", "I have an interview at [company]", or provides a company name,
  role, job description, and interview stage (recruiter screen, HM, or panel). Generates a
  complete stage-specific prep document including company snapshot, origin story, 3-pillar strategy,
  fit map, per-interviewer cards, and day-of reminders.
metadata:
  version: "0.1.0"
---

# PM Prep — Stage-Specific Prep Document Generator

Generate a complete, company-specific prep document calibrated to the interview stage. Every output must be specific enough that it could not be reused at a different company with a find-replace.

## Required Inputs

Collect before generating. If missing, ask — but ask all at once.

- **Company name** and **role title**
- **Job description** (paste or summarize)
- **Stage**: recruiter screen / HM / panel
- **Interviewer names + LinkedIn URLs** (optional but high-value, especially for HM and panel)

## Step 1: Classify Before Building

Before writing any content:
1. Identify the company archetype (use `pm-company-archetype` skill)
2. Identify the role type: product-building / operational / platform / GM
3. Note the seniority band: IC / Lead / Director / VP / GM
4. Check for available interviewer profiles — these change the entire HM and panel output

## Step 2: Select and Generate the Right Format

See `references/stage-formats.md` for the full specification of each stage format.

**Recruiter screen** → Condensed, cheat-sheet format. 6 sections. Emphasis on opening pitch, difficult Q&A pairs, 3-pillar at L1/L2, 3 anchor stories, one question, day-of reminders.

**HM conversation** → Deep, conversational format. 10 sections. Emphasis on interviewer decode, conversation angles, 3-year vision (not just 3 pillars), earned secrets, and 5 deep questions with rationale.

**Panel** → Multi-interviewer coordination format. Emphasis on per-interviewer cards, story routing table, panel overview. See `references/stage-formats.md` for per-interviewer card format.

## Step 3: Apply Quality Gates

Run these checks on every output before delivering:

**Origin story:** Does it connect to a specific product problem this company uniquely owns, or just their general mission? If find-replace would work for a competitor, it fails. See `references/credibility-audit.md`.

**3-pillar strategy:** Is each pillar grounded in a specific company fact (metric, user feedback, competitive signal, regulatory event)? If a pillar could be used at another company, flag it.

**Fit map:** Does the left column quote the JD directly (not paraphrase)? Is the right column specific enough to be challenged?

**Per-interviewer cards:** Is the background decode a psychological reading (what their arc tells you they value), not a resume summary?

**Questions to ask:** Does each question imply a specific company data point, a formed hypothesis, or a strategic insight? "What does success look like?" fails. A question that implies you know a specific metric and have a hypothesis passes.

## Step 4: Depth Cues

For every strategy section and talking point, include L1/L2/L3 versions. Flag L3 content: "Have this ready but let them pull the depth."

## Credibility Audit (always run)

After generating, run these three checks:
1. Could any section be reused at a competitor with a find-replace? Flag it.
2. Does the candidate's background specifically justify each pillar? Or could any senior PM claim it?
3. Does the origin story connect to a *specific product problem* or just the company's mission?

Report audit results at the end of every prep doc: "Credibility check: [pass/flag] — [one line on any issues]."
