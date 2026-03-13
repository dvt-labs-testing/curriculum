<!-- Every item MUST use the five-field format below. /build reads each item
     and relies on all five fields being present and consistently formatted.
     The header encodes methodology choices so /build doesn't re-ask. -->

# Build Checklist

## Build Preferences

- **Git:** [Commit cadence and style — e.g., "Commit after each item with message: 'Complete step N: [title]'"]
- **Verification:** [How the learner checks each step — e.g., "Run dev server and visually confirm"]
- **Check-in cadence:** [Learning-driven / balanced / speed-run — how much discussion during build]

## Checklist

- [ ] **1. [Clear title — what's done when this step is complete]**
  Spec ref: `spec.md > [Section] > [Subsection]`
  What to build: Concrete description of the work. Specific enough that /build can execute without guessing.
  Acceptance: Testable criteria from prd.md. What the learner verifies with their own eyes.
  Verify: Specific action — "Run dev server and confirm [what you should see]."

- [ ] **2. [Title]**
  Spec ref: `spec.md > [Section] > [Subsection]`
  What to build: [...]
  Acceptance: [...]
  Verify: [...]

<!-- Continue for all items. Typical project: 8-12 items, each 15-30 minutes.
     Sequence respects dependencies — earlier items unblock later ones.
     Last item is always demo video preparation. -->

- [ ] **N. Prepare and record Devpost demo video**
  Spec ref: `prd.md > What We're Building` (the core flow to demonstrate)
  What to build: Script a 2-5 minute demo walkthrough. Open with the problem (10-15 sec), show the app's core flow in action, close with what you learned or what you'd build next. Record with clear audio and visible UI.
  Acceptance: Video clearly shows the app working. Problem statement is stated upfront. Core user flow is demonstrated. Audio is clear and narration is coherent.
  Verify: Watch the recording end to end. Would a judge who knows nothing about your project understand what it does and why it matters?
