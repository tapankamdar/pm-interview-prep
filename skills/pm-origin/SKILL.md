---
name: pm-origin
description: >
  This skill should be used when the user says "/pm-origin", "write my origin story for [company]",
  "help me with my opening for [company]", "how do I introduce myself for [company]", or
  "why should I work at [company]". Craft a company-specific origin story (60–75 seconds)
  that connects the candidate's career arc to the specific product problem this company owns.
  Runs a credibility audit on every output.
metadata:
  version: "0.1.0"
---

# PM Origin — Company-Specific Opening Story

Write an origin story that makes the interviewer think: "This person's entire career has been pointing toward this exact problem." Not a general positioning statement — a specific answer to: *Why does your career arc lead inevitably to this company's specific challenge?*

## What an Origin Story Is Not

- Not a career timeline ("I started at X, then moved to Y...")
- Not a mission alignment statement ("I believe in what you're building...")
- Not a general pitch that could work at multiple companies
- Not the `pm-strategy` 3-pillar (that's what you'd do; this is why you're here)

## What It Must Do

Connect three things:
1. A specific problem the candidate has been working on across multiple roles
2. The company's specific version of that problem (not their general mission)
3. Why this company is the right place to work on it — and why now

**Test:** Read the origin story and ask: "Could this be used at a competitor with a find-replace?" If yes, it fails. Rewrite until no.

## Required Inputs

- Company name and role
- Job description or role description
- Candidate's career history (key roles and what they worked on)
- Any prior prep context (coaching state, storybank, prior prep docs)

## Credibility Gradient

See `references/origin-story-guide.md` for the full quality spectrum with examples.

**Strong (target):** Career arc → specific product problem this company uniquely owns.
*"I've been thinking about the context and grounding problem for five years — at one company at the on-device layer, at another at platform scale. This role is the same problem, the real version. That's the combination I've been looking for."*

**Solid:** Personal connection to the mission with a clean bridge to the role.
*"I grew up somewhere that made travel deeply meaningful to me. Across my career I've led AI platforms at scale. This company's mission to power travel for everyone resonates — this role is the first time AI platform work maps directly to that mission."*

**Weak (flag and fix):** Personal connection to broader theme without connecting to the specific product challenge.
*"I volunteer with a food bank. This company's mission to make food more accessible resonates deeply."* → Works for any food or community company. Needs a specific bridge to this company's AI product problem.

## Output Format

Produce both versions:

**Full version (60–75 seconds):**
For HM and panel rounds. Conversational, not recited. Should sound like a practitioner explaining why they're excited, not a candidate performing.

**Condensed version (20–30 seconds):**
For recruiter screens. The essence only.

**Credibility check:**
One-line audit: Pass or Flag, with specific fix if needed.
