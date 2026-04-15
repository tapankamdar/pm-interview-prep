---
name: pm-metrics
description: >
  This skill should be used when the user says "/pm-metrics", "practice a metrics question", "how would
  I measure [product]", "walk me through a metric drop", "north star metric", "DAU dropped", or presents
  any question about measuring product success, diagnosing metric changes, or defining success metrics.
  Drill the diagnostic tree approach, north star selection, and the difference between measuring
  what's easy vs. measuring what matters.
metadata:
  version: "0.1.0"
---

# PM Metrics — Metrics & Analytics Practice

PM metrics questions have two failure modes: naming metrics without understanding them, and choosing proxies that can be gamed. This skill drills the thinking behind the answer, not just the answer.

## Two Types of Metrics Questions

**Type 1 — Define success:** "How would you measure the success of [product/feature]?"
The test: Did they choose a metric that actually captures whether users are better off — or a metric that's easy to move?

**Type 2 — Diagnose a change:** "DAU dropped 15% last Tuesday. Walk me through how you'd investigate."
The test: Did they decompose systematically — or jump to conclusions?

## Type 1 Protocol: North Star Selection

Run this sequence when coaching a "how would you measure" question:

**Step 1 — Name the user outcome**
What does success look like for the user, not the business? "Users saved time," "users made a better decision," "the SMB owner got a qualified lead." The north star should capture this.

**Step 2 — Apply the north star test**
For any proposed metric, ask: "If this metric goes up but users aren't better off, is that still a win?"
- If yes → it's a proxy, not a north star. Find a better one.
- If no → it might be the right metric.

**Step 3 — Name the leading indicators**
What moves before the north star? These are the metrics the team can act on week-to-week.

**Step 4 — Name the counter-metric**
What would go wrong that this metric wouldn't catch? Picking a counter-metric signals the candidate understands the system, not just the target.

**Step 5 — Name the metric not to use**
What's the tempting but wrong metric here? Explaining what you'd avoid is often more revealing than naming what you'd use.

## Type 2 Protocol: Metric Drop Diagnosis

Run this sequence when coaching a "metric dropped" question:

**Step 1 — Clarify before diagnosing**
What metric dropped? By how much? Over what time window? Is it sustained or a one-day blip? What's the baseline? Don't assume — ask.

**Step 2 — Decompose the metric**
Break the top-level metric into components. DAU = new users + retained users + resurrected users. Which component dropped?

**Step 3 — External vs. internal causes**
Did something change in the product? Did something change externally (holiday, competitor launch, press coverage, platform change)? Always check external before assuming internal.

**Step 4 — Segment the drop**
Where did it drop? By platform (iOS/Android/web)? By geography? By user cohort (new vs. retained)? By feature entry point? The segment tells you where to look.

**Step 5 — Hypothesize and prioritize**
List 3–5 hypotheses. Rank by likelihood and ease of investigation. "What would I look at first and why?"

**Step 6 — Determine the fix**
Once the root cause is identified: is this something to fix now, fix in the next sprint, or accept as expected? Not every metric drop is a crisis.

## Common Mistakes to Flag

- **Jumping to hypotheses before decomposing:** "It might be a bug in the checkout flow" before checking which segment dropped
- **Treating correlation as causation:** "We launched feature X on Tuesday" ≠ "feature X caused the drop"
- **Forgetting external factors:** No check for app store changes, competitor moves, holidays, or news events
- **No counter-metric:** Proposing a north star with no acknowledgment of what it might incentivize incorrectly
- **Metric ≠ outcome:** "We'd measure session length" when the real outcome is "users accomplished their goal"
