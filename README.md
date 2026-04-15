# PM Interview Prep Plugin

Company-specific prep docs, transcript scoring, positioning tools, and practice drills for senior PM interviews. Each skill is built around one principle: output that couldn't be reused at a competitor with a find-replace.

---

## The Problem

Most PM interview prep teaches frameworks. Interviewers at senior levels evaluate judgment — product taste, prioritization reasoning, and earned conviction. The candidate who walks through CIRCLES on a product design question at Director level signals they learned interviewing from a prep course, not from actually building products.

This plugin is built for that gap: the space between knowing the frameworks and being able to make the interviewer think *"this person has already done the job."*

---

## Who This Is For

**Best for:**
- Senior PM, Staff, Principal, Director, VP, GM candidates
- Big Tech, AI-first, Hypergrowth SaaS, and enterprise interviews
- Candidates who know frameworks but struggle to stand out

**Not for:**
- First-time PM prep (start with frameworks first)
- Memorization-driven approaches

---

## Installation

### Claude Cowork (recommended for non-developers)
1. Open **Customize** (bottom-left corner)
2. Go to **Browse plugins → Personal → +**
3. Select **Add marketplace from GitHub**
4. Enter: `tapankamdar/pm-interview-prep`

All 17 skills and commands install automatically.

### Claude Code

Run these slash commands inside Claude Code:

```
# Step 1: Add the marketplace
/plugin marketplace add tapankamdar/pm-interview-prep

# Step 2: Install the plugin
/plugin install pm-interview-prep@tapankamdar/pm-interview-prep
```

### Other AI assistants (skills only)

The `skills/*/SKILL.md` files follow the universal skill format and work with any tool that reads it. Slash commands (`/pm-prep`, `/pm-analyze`, `/pm-mock`, etc.) are Claude-specific, but the passive intelligence skills (`pm-question-taxonomy`, `pm-framework-guide`, `pm-company-archetype`, `pm-depth-cue`) work in any compatible tool.

| Tool | How to use | What works |
|---|---|---|
| Gemini CLI | Copy skill folders to `~/.gemini/skills/` | Skills only |
| OpenCode | Copy skill folders to `.opencode/skills/` | Skills only |
| Cursor | Copy skill folders to `.cursor/skills/` | Skills only |
| Kiro | Copy skill folders to `.kiro/skills/` | Skills only |

```bash
# Example: copy all skills for OpenCode (project-level)
cp -r skills/* .opencode/skills/

# Example: copy all skills for Gemini CLI (global)
cp -r skills/* ~/.gemini/skills/
```

---

## Skills & Commands

17 skills across four groups. Active commands are triggered by slash command or natural language. Passive skills trigger automatically in the background.

---

### Company Prep

#### `/pm-prep`

Stage-specific prep document for a target company. Recruiter screen, HM conversation, and panel interview each get a different structure — the recruiter screen is a condensed cheat sheet, the HM prep includes a deep psychological decode of who you're talking to, and the panel adds a story routing table that prevents repeating the same story twice in one day.

**Provide:** Company name, role title, job description, interview stage. Add interviewer LinkedIn URLs for sharper per-interviewer cards.

**Every prep doc includes:** Company snapshot, origin story, 3-pillar strategy, fit map, per-interviewer cards, and day-of reminders.

**Natural language triggers:**
- "prepare me for my interview at [company]"
- "build my prep doc for [company]"
- "I have an HM conversation at [company] next week"

**Example:**
> `/pm-prep [Company] VP AI panel — here's the JD and the 4 panelist LinkedIn URLs`

---

#### `/pm-decode`

Reads a job description the way a practitioner would — not a keyword scan. Surfaces the actual top 5 evaluation criteria in priority order, what the JD implies but doesn't say, the role type (product-building vs. operational vs. platform vs. GM), fit verdict with frameable vs. structural gaps, and the 5 questions this company will likely ask.

**Natural language triggers:**
- "decode this JD"
- "what are they really looking for"
- "is this role a good fit for me"
- "should I apply to this"

**Example:**
> `/pm-decode [paste JD] — tell me what they're actually optimizing for and whether my background maps`

---

#### `/pm-interviewer`

Per-interviewer intelligence card. Decodes the interviewer's career arc to understand what they value — not a resume summary, a psychological reading. Outputs background decode, their evaluation role in the interview, top 5 predicted questions with 90-second beat scaffolds, and top 3 questions to ask them that demonstrate you're already thinking like someone in the role.

**Natural language triggers:**
- "build a card for [name]"
- "prep me for my interview with [name]"
- "decode [name]'s background"

**Example:**
> `/pm-interviewer [Hiring Manager Name] — linkedin.com/in/[profile]`

---

### Positioning

#### `/pm-origin`

Company-specific origin story — 60–75 seconds that answers: *why does your entire career arc lead inevitably to this company's specific problem?* Outputs both the full version (HM and panel) and a condensed version (recruiter screen), plus a credibility audit checking whether the story connects to a specific product problem or just the company's general mission.

**Natural language triggers:**
- "write my origin story for [company]"
- "help me with my opening for [company]"
- "how do I introduce myself for [company]"

**Example:**
> `/pm-origin [Company] — I'm interviewing for the VP AI role`

---

#### `/pm-strategy`

3-pillar strategy for the role, adapted to role type. Product-building roles get a product vision. Operational roles get a function thesis. GM roles get a P&L frame. Every strategy includes three depth levels: L1 soundbite (15–30 seconds, for when interrupted), L2 summary (90 seconds, standard deployment), and L3 deep dive (available on request, never volunteered).

**Natural language triggers:**
- "build my 3-pillar strategy for [company]"
- "what would I focus on in this role"
- "how would I approach this role"

**Example:**
> `/pm-strategy [Company] Sr. Director Gen AI — operational role, here's the JD`

---

#### `/pm-reframe`

Assertive reframe for the most likely liability. Not a defense — a genuine repositioning of why the apparent gap is an asset or irrelevant for this specific role. Outputs the reframe plus a deployment note: use it proactively in the opening, or hold it for when they ask.

**Natural language triggers:**
- "how do I handle the question about [gap]"
- "they'll ask about my short tenure at [company]"
- "I don't have [domain] experience"
- "what's my biggest liability for this role"

**Example:**
> `/pm-reframe [Company] — I don't have [domain] background`

---

### Analysis & Scoring

#### `/pm-analyze`

Paste a transcript or interview notes and get a structured scorecard across 6 PM-specific dimensions. Every finding is anchored to a specific moment in the transcript — no generic feedback.

**Six dimensions:** Product Judgment · Storytelling & Specificity · Metrics Fluency · Strategic Thinking · Differentiation · Communication & Structure

**Outputs:** Dimension scores with evidence, top 3 strengths (citable), top 3 improvement areas (with exact pattern and concrete fix), hire signal, and single highest-leverage thing to fix before the next round.

When multiple rounds for the same company exist, automatically builds the running panel scorecard.

**Natural language triggers:**
- "score my interview"
- "I just finished my interview at [company]"
- "analyze this transcript"
- "how did I do"

**Example:**
> `/pm-analyze [Company] HM round — [paste transcript]`

---

#### `/pm-panel`

Running cross-round scorecard for a company loop. Shows dimension scores across rounds with trend arrows, consistency signals (dimensions that hold or break across multiple interviewers), panel-level red flags (weaknesses appearing in 2+ rounds — what the hiring committee will discuss), and a momentum read.

**Natural language triggers:**
- "show me my panel scorecard for [company]"
- "how am I tracking across rounds at [company]"

**Example:**
> `/pm-panel [Company] — I've now done 4 rounds`

---

#### `/pm-sixlens`

Six adversarial perspectives on a story or answer: Engineering, Design, Data, Business, Competitor, and Skeptic. Finds where the story breaks before the interview does. After all six, identifies the most vulnerable lens and the specific fix needed.

**Natural language triggers:**
- "stress test my story"
- "poke holes in this"
- "will this story hold up"
- "challenge my answer"

**Example:**
> `/pm-sixlens [describe your story]`

---

### Practice

#### `/pm-mock`

Full simulated PM interview calibrated to company archetype (FAANG, hypergrowth SaaS, AI-first, marketplace, enterprise) and seniority. Question mix adapts to how that company actually interviews. Scores each answer in real time with a warmup round (unscored) to reduce performance anxiety.

**Natural language triggers:**
- "run a mock interview for [company]"
- "simulate an interview at [company]"
- "practice a full interview"

**Example:**
> `/pm-mock [Company] Director level`

---

#### `/pm-case`

Full product case protocol: clarifying questions → problem framing → user segmentation → problem prioritization → solutions → tradeoffs → metrics. Scored on PM-specific criteria — did they frame the problem before solutions? Did they pick the right metric? Calls out common failure modes as they happen.

**Natural language triggers:**
- "practice a product case"
- "product design question"
- "how would I design [product]"

**Example:**
> `/pm-case How would you improve [product] for [user segment]?`

---

#### `/pm-metrics`

Metrics and analytics question practice. Two types: define success ("how would you measure [product]?") and diagnose a change ("DAU dropped 15% — walk me through it"). Drills the north star test, decomposition approach, segmentation before hypotheses, and the counter-metric.

**Natural language triggers:**
- "practice a metrics question"
- "how would I measure [product]"
- "walk me through a metric drop"
- "north star metric"

**Example:**
> `/pm-metrics [Product]'s core engagement metric dropped 12% last Tuesday`

---

#### `/pm-estimate`

PM-calibrated estimation practice. TAM sizing, investment thresholds, revenue potential, feature impact. Coaches the full protocol: state approach first, label every assumption, round aggressively, sanity check against a known reference, connect the estimate to the decision it informs.

**Natural language triggers:**
- "practice an estimation question"
- "how would I estimate [X]"
- "TAM sizing"
- "guesstimate"

**Example:**
> `/pm-estimate What's the revenue potential of an AI-powered checkout feature for an SMB platform?`

---

### Background Intelligence (auto-triggered)

These four skills run automatically — no command needed.

**`pm-question-taxonomy`** — When a PM interview question appears, immediately classifies the type and surfaces what the interviewer is actually evaluating. A metrics question answered with a story is a miss regardless of quality — classification is the prerequisite.

**`pm-framework-guide`** — When a named framework appears (CIRCLES, HEART, AARRR, RICE), evaluates whether it helps or hurts in this specific context and stage. At Director+ level, walking a framework signals template thinking.

**`pm-company-archetype`** — When a company name appears in prep context, classifies the interview culture (FAANG, hypergrowth SaaS, AI-first, marketplace, enterprise) and calibrates all subsequent coaching.

**`pm-depth-cue`** — When a prep answer exceeds what the stage warrants, flags the depth mismatch and surfaces the L1 soundbite to fall back to. Going too deep signals poor read of the room.

---

## Gold Standard Example: Hiring Manager Prep

**Role:** VP AI  
**Company:** AI SaaS company (~$200M ARR, Series D)  
**HM:** CPO (joined 6 weeks ago, building the AI team)

---

### 1. Interviewer Decode

**Background:** Previously CPO at an SMB fintech. Technical foundation (ML certification). Built products for non-technical business owners. Public framing: this company is not just a workflow tool — it's an intelligence platform. New to the role, actively shaping the team and strategy.

**What they value:**
- Real POV on where AI needs to go for this domain — not a summary of their own public statements
- Deep understanding of evals — the recruiter flagged this explicitly
- Player-coach who can hold strategy and do hands-on work
- Cross-functional instincts across EPD, domain experts, and GTM

**What they're evaluating:**
- Do you have a real point of view or a polished summary of the JD?
- Do you understand evals as a practice, not just a concept?
- Can you hold a strategic vision AND do the hands-on work?

---

### 2. Opening (60 seconds)

*"I've spent years building AI products where the stakes of being wrong are high — privacy-first AI at a major browser, AI at scale for a billion users on a social platform, revenue-driving AI for tens of millions of small businesses.*

*What makes this company different is that the domain is where the stakes are highest. A missed detail is a liability. A stalled workflow is a deal that didn't close. An AI that's impressive in a demo but wrong 20% of the time isn't a product — it's a risk.*

*The opportunity here is to build AI that a domain expert will stake their reputation on. Not just more capable — but trustworthy. That's a different problem, and a harder one. It's also the one I've been working toward."*

---

### 3. 3-Pillar Strategy

**Pillar 1: Agentic Infrastructure**
The company has shipped several agents independently. Extract the common patterns — tool use, memory, guardrails — into shared scaffolding. New agents in weeks, not months. Proprietary domain data is the moat no competitor can replicate.

**Pillar 2: AI Flagship Product**
Strong ARR growth, but a significant share of customers haven't adopted AI features. The fix: standards-first onboarding. Make uploading the customer's own rules and preferences the first action on Day 1 — so the AI starts from their bar, not a generic one.

**Pillar 3: The Trust Engine**
Build golden datasets annotated by domain experts (not engineers), continuous regression testing, and customer-specific accuracy scores visible to the customer. The eval framework is the evidence a power user needs to expand usage. Upcoming regulations in this space make this a compliance moat as well.

**1-line version:**
*"Infrastructure first, the flagship product second, the trust engine third — these aren't three workstreams, they're a system."*

---

### 4. 3-Year Vision

**Year 1:** Ship the shared agent infrastructure. Standards-first onboarding live for the flagship product. Eval pipeline and golden datasets in production.

**Year 2:** The flagship AI becomes the expert's daily assistant — standards-aware suggestions, contextual memory across interactions, integrations where experts already work. Adoption moves from 65% to 85%+.

**Year 3:** Intelligence platform. Every agent built on the shared layer. Proprietary domain data becomes an industry benchmark. Cross-org agent protocol: your agent talks to your counterpart's agent, authenticated through the company's identity layer.

---

### 5. Earned Secrets

- *"The eval framework IS the trust product. It's not backend infrastructure — it's the evidence an expert user needs to expand AI usage. Make it visible to customers."*
- *"The trust gap closes when the AI starts from the customer's own standards, not a generic baseline. Standards-first onboarding on Day 1 is the unlock."*
- *"Domain-grade AI needs to be a measurable claim, not a marketing one."*

---

### 6. Story Routing

| If conversation goes to... | Deploy... |
|---|---|
| AI eval and trust | On-device AI story — anchored eval to stable user behavior, not model performance |
| Product infrastructure vs. features | Build vs. buy decision — proprietary signal is the moat |
| Cross-functional alignment | Cross-org AI launch story — shared readout, shared criteria |
| SMB / non-expert user trust | Metric evolution story — "does improving this number make the customer better off?" |

---

### 7. Questions to Ask

- *"You joined recently with a clear vision for where AI should take this company. What's the biggest unlock you see in the next 12 months to make that real for customers?"*
- *"A meaningful share of customers haven't adopted AI features yet — what do you understand about why?"*
- *"The JD calls out eval rigor and golden datasets explicitly. Where does that capability sit today — building from scratch, or scaffolding something that exists?"*

---

### 8. Day-of Reminders

- Lead with thesis, not background
- The eval question is the highest-stakes topic — treat it as 10–15 minutes, not 2
- Stop at 90 seconds, let them probe — Q&A is your highest-leverage moment
- Be honest about what you don't know in the domain — they'll respect it more than overclaiming
- Deploy earned secrets early — they signal conviction, not prepared answers

---

## What Makes This Different

- Frameworks are optional — judgment is mandatory
- Specificity beats correctness at senior levels
- Each stage (recruiter, HM, panel) requires a fundamentally different document
- The probe after your answer is where you win, not the answer itself
- Generic prep fails the find-replace test — if it works at a competitor, it's not ready

---

## Philosophy

Good candidates answer the question.

Great candidates:
- Reframe the question to show what's really at stake
- Show conviction backed by earned insight, not enthusiasm
- Sound like they've already done the job

The goal isn't a better answer. It's a better thinking process that makes better answers inevitable.

---

## About

Tapan Kamdar is a product leader with 15+ years at Meta, Mozilla, GoDaddy, eBay, and Yahoo. He writes the *Building Blocks* newsletter and is the author of *Level Up: From Good Product Manager to Great Product Manager* ([a.co/d/0dxmUyJJ](https://a.co/d/0dxmUyJJ)).

Great PM interviews are not about better answers. They are about better thinking.
