# Independent AI gate assessment and calibration

Use for a prototype or production gate the developer wants assessed. Adapt the record to existing project conventions. This workflow does not require a second agent, special tooling, or invented confidence scores.

## Component gate or tuning read

Use a component gate when a specific question is open: an experiment, or one behavior the developer asked to have assessed. When the design is settled and the developer is tuning the whole experience, do not gate the parts on feel. Verify each part works as specified, then make one tuning read of the whole encounter, level, or loop.

A tuning read uses everything below (independent evaluator, claim types, sealed predictions, comparison after play) with these differences:

- The layers are the design's acceptance criteria. Report each as holds, not yet, or cannot tell.
- For each "not yet", name the dial you would turn, the direction, and the evidence. Suggest a system change only when the evidence shows no setting reaches the criterion.
- There is no overall pass or fail. The output is a proposed set of dial changes and predictions of what the developer will want changed.
- Hold back perceptual judgments that depend on assets still on their way, and say which.

## Before assessment

Read the active gate, relevant design rules, supporting tasks, and applicable prior calibration entries. State the build and relevant test settings. Freeze the criteria for this assessment; record later criterion changes explicitly rather than retroactively passing the old test.

Identify the evaluator. A gate verdict should come from a context that did not build the work under review (see SKILL.md). Record the evaluator's model and what it was given.

Choose observations that can establish the claim. Logs establish state transitions and timings. Images support pose and composition judgments. Video supports motion and pacing judgments. Audio requires actual audio access. Interactive control can support responsiveness judgments, but tool latency must be distinguished from game latency. An unavailable channel is an evidence gap, not a successful check.

## Claim types

Tag each important statement in an assessment with what kind of claim it is. Keep them apart; they carry different weight.

| Claim type | What it can carry |
|---|---|
| **Measured finding** | Exact only within what was instrumented. Give frames, milliseconds and the frame rate for timing. Instrumented event timing excludes input-device, render, display and remote-viewing delay. |
| **Project requirement** | Pass or fail against the design document. Not a feel verdict. |
| **Reference-supported interpretation** | Stylistic alignment with reference material the developer chose. A reference shows rhythm and presentation; it cannot establish input latency or rules it doesn't show. |
| **Prediction to calibrate** | The only kind that speaks to the developer's experience. Stated before they play, compared after. |

Name the claims that are weak by nature in every assessment: perceived weight at normal speed, whether a sound sells an action, pose readability in motion versus stills, and small latency differences on the developer's own setup.

## Assessment record

**Identity:** Gate, attempt, build or revision, settings, date, and evidence locations.

**Access:** What was actually run, viewed, heard, or controlled; unavailable observations.

| Layer | Verdict: pass / revise / inconclusive | Evidence and interpretation | Missing evidence |
|---|---|---|---|
| Mechanical correctness | | | |
| Perceptual quality | | | |
| Design effectiveness | | | |

**Overall verdict:** Make a clear recommendation about this gate. A known material failure warrants revise. Missing essential evidence warrants inconclusive. Pass means the observed evidence meets the gate criteria, not that human acceptance already exists. Explain mixed layer verdicts; do not average them into a score.

**Predictions:** A few specific statements about what the developer will notice or do, tied to scenarios. Include the strongest expected success and the most plausible weakness. State the basis and any important uncertainty. Avoid vague predictions such as “some players may dislike it.”

**Repairs and retests:** Changes actually made within scope, checks rerun, and remaining problems. Preserve earlier failed attempts when they explain the result. Stop at the agreed budget; if none exists, after a bounded assessment and targeted repair pass report unresolved issues instead of tuning indefinitely.

Save this record before receiving the developer's feedback, with the predictions in a separate file the developer opens after playing. When file tools are unavailable, provide a clearly dated assessment in the conversation. Do not claim it was independently predicted if the feedback was already known.

## Developer review and comparison

Offer a neutral test sequence. The developer can record first impressions before reading the verdict to reduce steering. Do not withhold the report if requested.

| Original prediction | Developer observation | Match / mismatch / not tested | Explanation | Next evaluation change |
|---|---|---|---|---|

Preserve the original prediction and feedback wording or an attributed faithful summary. The same build and conditions are preferred. If they differ, identify the comparison as confounded and avoid treating it as a clean calibration result.

The developer is authoritative about their own experience and design preference. Their experience does not automatically identify the implementation cause. Distinguish “it felt automatic” from the untested diagnosis “warp is too large.” Investigate the cause with a focused comparison.

Record successful judgments as well as misses. For each reusable lesson, keep its context, evidence, applicability, and next verification. Scope taste preferences to the developer or project; do not silently make them universal skill rules.

**Final decision:** The developer's acceptance or requested revision, remaining work, and next active gate. If no decision has been provided, leave it pending.
