---
name: pm-sixlens
description: >
  This skill should be used when the user says "/pm-sixlens", "stress test my story", "challenge my answer",
  "poke holes in this", "will this story hold up", or describes a product decision or initiative they
  plan to use in an interview. Apply six adversarial perspectives to a story or answer to reveal whether
  it holds under real panel pressure or collapses when probed.
metadata:
  version: "0.1.0"
---

# PM Six-Lens Stress Test

Take a story or product answer and attack it from six perspectives that real interviewers use. The goal is to find where it breaks before the interview does.

## Required Input

A story, decision, or product answer the candidate plans to use. Can be:
- A STAR story from the storybank
- An answer they've drafted to a specific question
- A product initiative or decision they led

## The Six Lenses

Apply each lens in sequence. For each: ask the hardest version of the challenge, then evaluate the candidate's response (if they respond) or surface the weakness they need to prepare for.

**1. Engineering Lens**
Challenge the technical and execution reality.
- "This sounds like 6 months of work. How'd you scope it?"
- "What technical debt did this create?"
- "Walk me through the build vs. buy decision."
- "What did engineering push back on, and how did you resolve it?"
- "What would you do differently given what you know now?"

**2. Design Lens**
Challenge the user research and UX reasoning.
- "What user research backed this decision?"
- "How did you balance user needs vs. business goals?"
- "What did you sacrifice for simplicity?"
- "What did users hate that you shipped anyway? Why?"
- "How many design iterations? What changed and why?"

**3. Data Lens**
Challenge the measurement and analytical rigor.
- "How did you measure success?"
- "What was your null hypothesis?"
- "What metrics didn't move that you expected to?"
- "How did you handle selection bias or confounds?"
- "If I looked at your data, what would concern me?"

**4. Business Lens**
Challenge the commercial and strategic reasoning.
- "Walk me through the unit economics."
- "What was the opportunity cost of this vs. other projects?"
- "How did this affect revenue / retention / engagement?"
- "What would have happened if you'd done nothing?"
- "How did this affect your competitive position?"

**5. Competitor Lens**
Challenge the competitive context and defensibility.
- "Competitor X tried this and failed. Why'd you succeed?"
- "What stops them from copying this tomorrow?"
- "Who else considered this approach and abandoned it?"
- "How does this change your moat?"

**6. Skeptic Lens**
Challenge the narrative itself.
- "This seems like a solution looking for a problem."
- "Your success metrics feel cherry-picked."
- "How do you know this wasn't regression to the mean?"
- "Sounds like you got lucky. What was actually skill?"
- "What would you do differently with hindsight?"

## Scoring Per Lens

After each lens, score three things (1–5):
- **Acknowledging the tension** (vs. dismissing it)
- **Specific evidence** (vs. hand-waving)
- **Admitting uncertainty** (vs. false confidence)

The lowest-scoring lens is the most important to fix before the interview.

## Output Format

For each lens: state the hardest challenge, identify whether the story holds or breaks, and give the specific language fix if it breaks.

At the end: "Your story is strongest against [lens]. Your biggest vulnerability is [lens] — specifically: [what the gap is and how to close it before the interview]."
