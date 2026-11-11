# Briefs and evidence records

Use the smallest relevant set of fields. Unknowns should be explicit assumptions or questions, not invented facts. Preserve the developer's existing document conventions.

## Prototype brief

**Game promise:** The experience this experiment serves.

**Decision:** What the developer will decide from the results.

**Player and situation:** Intended participants, relevant experience, and session conditions.

**Hypothesis:** The proposed interaction or presentation, the expected experience, and why they might be connected.

**Smallest meaningful build:** What must exist for the hypothesis to receive a fair test.

**Evidence:** What to observe, ask, or measure; what would contradict the hypothesis; who interprets it.

**Decision rule:** Findings that would support keeping, changing, cutting, or testing a specific follow-up. Numerical targets, if used, are agreed targets or explicitly provisional proposals.

**AI assignment:** Deliverables, technical checks, permissible implementation choices, and reserved design decisions.

**AI self-validation:** Scenarios and observation methods for an independent verdict before developer feedback; predictions and applicable prior calibration lessons.

**Budget and exclusions:** Known effort limit, excluded work, and a stopping point.

**Result:** Link or identify the tested build, observations, decision, and next action. Leave this unfilled until evidence exists.

## Tuning brief

For a settled design whose systems are functional (see "When the premise is settled" in SKILL.md). One brief per pass over the whole experience.

**What to play:** The whole encounter, level, or loop; the build and how to start it; the starting settings for this pass.

**Acceptance criteria:** The design's own tuning and balance criteria, each with what it looks like in play when it holds. These are not hypotheses and the pass does not test whether the design should exist.

**Dials:** The values and switches most likely to matter for each criterion, where they live, their current setting, and how to change them during play. Mark provisional values.

**Not yet representative:** Parts standing in for pending assets (animation, audio, art) and the judgments to hold back until they arrive.

**What to bring back:** What felt wrong or right, in the developer's own words, and anything they want to try. The developer does not need to diagnose the cause or pick the dial.

**AI read:** A separate evaluator's sealed predictions for this pass, if one was made: which criteria hold, which dials it would turn, what the developer will ask for.

**Result:** Dial changes made, criteria status after the pass, and the next pass. Record a system change only with the evidence that no setting reached the criterion.

## Delivery brief

**Intended experience:** Who should experience what, in which situation.

**Acceptance evidence:** Behaviors, player accounts, measurements, and the developer's judgment that will establish the result.

**Supporting requirements:** Mechanics, performance, accessibility, compatibility, and other constraints relevant to this work. Retain explicit user requirements even if their connection to the experience is indirect.

**Implementation boundary:** What may change and what is outside scope.

**Verification:** Technical checks and human sessions, with their respective responsibilities.

**Applicable capability contracts:** Stable IDs, implementation boundary, owner/lifetime and failure behavior affected by this delivery. Use [engineering-contracts.md](engineering-contracts.md); omit a new contract when the existing one is sufficient.

**Evidence identity and freshness:** Tested revision/dirty inputs, applicable contract versions, commands/results, unavailable checks and changes that invalidate the claims. Reuse the project's manifest.

**Acceptance status:** Ready to test, evidence available, AI verdict recorded, accepted, or requires revision. Identify who makes the final call. For gate judgments use [gate-calibration.md](gate-calibration.md).

## AI implementation handoff

Translate a chosen brief into an actionable assignment:

> Implement [bounded playable work] in [existing project/engine] so we can test [question]. Preserve [known constraints]. You may choose [implementation details]. Ask or report before changing [material design choices outside the assignment]. Provide [reset/test setup and relevant instrumentation]. Verify [observable technical behavior]. Independently assess the gate using available evidence and record a verdict and predictions before my review. Report the build or changed files, checks actually run, remaining issues, and how to conduct the playtest. After my feedback, compare it with your original predictions and update the implementation and evaluation method where justified. Human acceptance depends on [evidence]; do not report it as achieved from technical checks alone.

Resolve bracketed fields from context. Omit irrelevant fields rather than handing an agent an unfinished template.

For assignments that affect an engineering boundary, also identify the applicable contracts, permitted mutation/phase, decisive failure cases, and supported reset/reload behavior before building. Report contract conformance, remaining exceptions and revision-bound verification at handoff. Independent architecture review sees code and evidence; independent experiential gate review retains its sealed evidence boundary. Do not describe self-review as independent or claim a planned check is enforced.

## Evidence and decision record

- **Test:** Date, build, participant context, and conditions.
- **Observed:** Concrete actions, measurements, and attributable player statements. Identify missing evidence.
- **Interpretation:** What those observations suggest and any specific competing explanation that could change the decision.
- **Decision:** Keep, change, cut, accept, or a narrowly defined follow-up; who made the call and why.
- **Next action:** The smallest justified next step and what work is now unnecessary.

An experiment can succeed by ruling out an idea. Do not delete negative results or rewrite the original hypothesis to match the outcome.
