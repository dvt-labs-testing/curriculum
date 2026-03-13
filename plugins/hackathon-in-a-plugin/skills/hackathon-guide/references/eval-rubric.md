# Evaluation Rubric — Agent Reference

This document is for the agent only. It defines how you evaluate the learner's work in /evaluate. Follow this rubric precisely — it produces calibrated, evidence-based feedback.

## Evaluation Method: G-Eval with Additive Rubric

For each dimension, you MUST:
1. **Reason step-by-step** through the criteria before assigning a score. Write your reasoning out.
2. **Cite specific evidence** from the artifacts. Quote or reference exact passages.
3. **Score additively.** Each criterion within a dimension earns points. The score is the sum of satisfied criteria, not a holistic impression.

## Bias Guards

Apply these throughout every evaluation:

- **"A 3 is a strong hackathon result."** Do not expect production-quality code or professional-grade documents from a 3-4 hour hackathon. Calibrate to the context.
- **Penalize verbosity, not brevity.** A concise scope doc that nails the idea is better than a long one full of filler. Score substance, not length.
- **Score based on evidence, not assumptions.** If the artifacts don't show something, it didn't happen. Don't fill gaps with charitable assumptions.
- **If evidence is insufficient, say so.** Use "INSUFFICIENT EVIDENCE" for any criterion you can't assess from the artifacts. Explain what's missing. Do not guess.
- **Evaluate against the PRD, not your own taste.** The PRD's acceptance criteria are the external anchor. Did the app do what the learner said it should do? Not what you think it should do.
- **Active learner engagement is a core metric.** A beautiful app built by a passive learner who accepted every suggestion scores lower on Process Quality than a rougher app built by someone who actively shaped every decision.

## Scoring Dimensions

### 1. Scope Clarity (5 points)

How well-defined is the idea? Does `scope.md` give a clear picture of what's being built and why?

| Points | Criterion |
|--------|-----------|
| 1 | The idea is stated — you can tell what the app is supposed to do |
| 1 | A specific user and problem are identified (not "everyone" or "people") |
| 1 | "What's Explicitly Cut" names real features/scope that were removed with rationale |
| 1 | "What Done Looks Like" is concrete enough that someone could verify it |
| 1 | The scope is realistic for 3-4 hours given the learner's stated experience level |

**Anchor — score of 1:**
The scope doc exists but reads like a first draft brainstorm. The idea is vague ("an app that helps people"), no specific user is identified, nothing is explicitly cut, and "done" is described in generalities. The learner accepted the agent's first suggestion without pushing back.

**Anchor — score of 3:**
The idea is clear and specific. A real user and problem are named. Some scope cuts are listed. "Done" is described concretely enough to build toward. The learner engaged in the conversation and made real choices, though some sections could be sharper.

**Anchor — score of 5:**
The idea is razor-sharp — one sentence and you get it. The user, problem, and constraints are specific and grounded. Scope cuts show genuine prioritization thinking with real rationale. "Done" paints a vivid picture. The learner drove the conversation, pushed back on the agent, and made the idea distinctly theirs.

### 2. Requirements Quality (5 points)

Does `prd.md` define complete, testable requirements? Were edge cases surfaced?

| Points | Criterion |
|--------|-----------|
| 1 | User stories follow the format and cover the core user journey |
| 1 | Acceptance criteria are specific and testable (not vague like "works well") |
| 1 | Edge cases and error states are addressed (empty states, bad input, no results) |
| 1 | "What we're building" vs "What we'd add with more time" shows genuine prioritization |
| 1 | The PRD is substantially more detailed than the scope doc — real expansion happened |

**Anchor — score of 1:**
The PRD is a reformatted copy of the scope doc. User stories are vague or missing. Acceptance criteria say things like "it should work." No edge cases are mentioned. It's not clear what "done" means for any feature.

**Anchor — score of 3:**
User stories cover the main flows. Acceptance criteria are mostly testable. A few edge cases are addressed. The PRD is clearly more detailed than the scope doc. The learner engaged with "what if" questions and made prioritization decisions, even if some criteria could be tighter.

**Anchor — score of 5:**
User stories are comprehensive and grouped into meaningful epics. Every acceptance criterion is specific enough to verify by looking at the screen. Multiple edge cases and error states are addressed — the learner anticipated some themselves. The prioritization split shows real thought about what matters for the demo. The PRD reads like the learner deeply understood what they were building.

### 3. Technical Decisions (5 points)

Does `spec.md` show intentional architecture choices? Does the checklist sequence make sense?

| Points | Criterion |
|--------|-----------|
| 1 | Stack choices are explained with rationale tied to the learner's experience and project needs |
| 1 | The file structure and data flow are documented clearly enough for /build to execute |
| 1 | Architecture decisions reference PRD epics — traceability exists |
| 1 | The checklist is sequenced logically (dependencies respected, risk front-loaded where appropriate) |
| 1 | The spec addresses how the demo will work — the architecture supports the demo flow |

**Anchor — score of 1:**
The spec lists a stack but doesn't explain why. File structure is missing or generic. There's no connection to the PRD. The checklist is a flat list with no dependency logic. The learner accepted whatever the agent proposed.

**Anchor — score of 3:**
Stack choices have rationale. File structure and data flow are documented. Some PRD cross-references exist. The checklist sequence makes sense. The learner participated in architecture decisions, asked questions, and understood most of what was being proposed.

**Anchor — score of 5:**
Every architecture decision has clear rationale tied to both the project and the learner's experience. File structure is detailed with annotations. Data flow is diagrammed and narrated. PRD cross-references are thorough. The checklist reflects genuine sequencing thought. The learner actively shaped the architecture — pushed back on proposals, asked hard questions, made the technical decisions feel like their own.

### 4. Spec-to-App Alignment (5 points)

Does the finished app do what the PRD said it should do?

| Points | Criterion |
|--------|-----------|
| 1 | The app runs without crashing on the core flow |
| 1 | At least half of the "What we're building" acceptance criteria are met |
| 1 | The core user journey from the PRD is functional end-to-end |
| 1 | The demo video (if recorded) shows the app doing what the PRD described |
| 1 | 75%+ of acceptance criteria are met, including at least one edge case or error state |

**Anchor — score of 1:**
The app exists but barely runs. Most features from the PRD are missing or broken. The demo (if it exists) can't show a complete flow. There's a major gap between what was planned and what was built.

**Anchor — score of 3:**
The app works for the core flow. Most of the "What we're building" items are functional. The demo shows the app doing something meaningful. Some acceptance criteria aren't met, but the core concept is solid and demonstrable.

**Anchor — score of 5:**
The app does what the PRD said. Nearly all acceptance criteria are met. The demo is polished — it shows a complete flow that matches the PRD, handles at least one edge case gracefully, and the learner can explain how everything works. The gap between plan and execution is minimal.

### 5. Process Quality (5 points)

From `process-notes.md` and knowledge check answers: did the learner actively shape the project or passively accept suggestions?

| Points | Criterion |
|--------|-----------|
| 1 | Process notes show the learner made real decisions (not just "agreed" to everything) |
| 1 | The learner pushed back on or modified agent suggestions at least once during planning |
| 1 | Knowledge check answers during /build show understanding (not blank, one-word, or confused) |
| 1 | The learner contributed ideas the agent hadn't suggested — added something of their own |
| 1 | Process notes show the learner's thinking evolved across the phases — their understanding deepened |

**Anchor — score of 1:**
Process notes are thin. The learner accepted most suggestions without pushback. Knowledge check answers (if present) are vague or confused. There's no evidence the learner shaped the project's direction — it feels like the agent built what the agent wanted to build.

**Anchor — score of 3:**
Process notes show real engagement. The learner made decisions and sometimes pushed back. Knowledge check answers show they understood most of what was being built. There are moments where the learner contributed something original. The project feels like a collaboration, even if the agent did most of the proposing.

**Anchor — score of 5:**
Process notes are rich — they show a learner who was fully engaged at every step. Multiple instances of pushing back, redirecting, adding ideas the agent hadn't considered. Knowledge check answers are concise and accurate — the learner tracked what was being built throughout. The project distinctly reflects the learner's vision, taste, and decisions. The agent was a tool; the learner was the architect.

## When the Learner Gets a Low Process Quality Score

If Process Quality scores 1-2, the evaluation should include a specific note:

"When working with AI coding agents, it's easy to let the agent drive and lose track of what's actually being built. This works fine for a hackathon — but on longer projects, passive acceptance means you can't debug, extend, or explain your own code. The knowledge checks and active decision-making practiced in this workflow exist to prevent that. On your next project, try pushing back more on the agent's suggestions and making each decision feel like yours."

This is not punitive — it's the most important lesson the evaluation can teach.

## Generating the Evaluation

After scoring all five dimensions:
1. Write the chain-of-thought reasoning for each dimension (this goes in the evaluation document so the learner can see how you arrived at each score)
2. Identify one clear strength (with evidence)
3. Identify one clear growth area (with actionable advice)
4. Fill in the milestone completion checklist
5. Add the AI-generated evaluation disclaimer at the top of the document
