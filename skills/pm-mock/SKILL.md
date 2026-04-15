---
name: pm-mock
description: >
  This skill should be used when the user says "/pm-mock", "run a mock interview", "simulate an interview
  at [company]", "practice a full interview", or "mock me for [company] [role]". Run a complete simulated
  PM interview calibrated to the company archetype and seniority level, then score every answer using
  the six PM dimensions. Adapt question mix to match how that company actually interviews.
metadata:
  version: "0.1.0"
---

# PM Mock — Full Simulated Interview

Run a complete mock PM interview, score every answer, and deliver a full scorecard at the end. Calibrated to company archetype and seniority — not a generic question bank.

## Required Input

- Company name (to calibrate archetype and culture)
- Seniority level (IC PM / Senior PM / Director / VP / GM)
- Available time (default: 45 minutes = 4–5 questions with scoring)

Optional:
- Role title / JD (for question targeting)
- Specific format to simulate (behavioral screen / product sense / HM / panel round)

## Step 1: Calibrate Before Starting

Select question mix based on:
- **Company archetype** (from `pm-company-archetype`): FAANG emphasizes product sense + leadership; hypergrowth SaaS emphasizes execution + business outcomes; AI-first tests conviction + technical depth
- **Seniority**: IC = product craft + execution; Director+ = systems thinking + org navigation + vision
- **Format**: If simulating a specific round, match that round's known question types

## Step 2: Run the Interview

State format upfront: "I'll ask [N] questions, give you time to answer each, then score them as we go. Ready?"

**Warmup (first question, unscored):**
Open with an easy question to reduce performance anxiety. State clearly: "This first one is a warmup — I won't score it. Just get your thoughts flowing."

**Scored rounds (questions 2–N):**
Ask one question. Wait for full answer. Score it before asking the next. This gives the candidate real-time feedback, not a dump at the end.

Scoring after each answer:
- Quick dimension scores (3–4 most relevant for that question type)
- One strength, one gap
- "Ready for the next one?"

**Pacing:** 8–10 minutes per question including scoring. Adjust for available time.

## Step 3: Question Selection

Pull from `references/question-library.md` based on archetype and seniority. Aim for:
- 1–2 behavioral / leadership questions
- 1 product sense or design question
- 1 strategy or vision question
- 1 metrics or execution question (optional, based on time)

Never ask the same question type twice in a row.

## Step 4: End-of-Mock Scorecard

After all questions, deliver:
- Full dimension scorecard (average across all rounds)
- Overall hire signal
- Top 3 patterns that worked
- Top 3 patterns to change
- Single highest-leverage thing to practice before the real interview

## Step 5: Save to Panel Scorecard

If this mock is for a company the candidate has real rounds with, offer to add the mock scores to the panel scorecard as a "practice" round: "Want me to track this in your [Company] panel scorecard? I'll label it as a practice round."
