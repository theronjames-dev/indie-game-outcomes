---
name: indie-game-outcomes
description: Plan indie game experiments, brief AI implementation, tune a settled design in whole-experience play, independently assess prototype gates, and calibrate assessments against developer playtests. Use for prototype decisions, tuning passes, gate reviews, playtest interpretation, or connecting a backlog to design intent. Do not impose this workflow on routine fixes or unrelated implementation.
---

# Indie Game Outcomes

Help an indie developer use playable evidence to make design and production decisions. A working feature establishes implementation success; it does not by itself establish a worthwhile player experience. Scale the process to the decision: a short paragraph is often enough.

## Choose the useful mode

- **Explore:** Identify the current uncertainty and propose the smallest meaningful experiment. The result is a decision to keep, change, cut, or investigate a specific remaining question.
- **Deliver:** Define how an already chosen experience should work for its intended players, then identify implementation and acceptance evidence.
- **Tune:** The design is settled and its systems are built or being built. Play the whole experience (a full encounter, level, or loop) and adjust values until the design's acceptance criteria hold. The result is a set of dial changes, not a verdict on whether the design should exist.
- **Review:** Examine a feature idea, backlog, prototype, or playtest. Separate what exists, what was observed, and what the developer can conclude. Group related tasks under shared design intent.

Infer the mode from the request; do not force the user to select one. Exploration and delivery can share a brief, but label their completion conditions separately. Do not silently turn an experiment into a production commitment, and do not silently turn a settled design into an experiment: not every design is a hypothesis.

## Find the intent

Establish the game promise, the player and situation, and the decision this work should support. Use available project context. If context is missing, proceed with a clearly labeled working assumption unless the answer would materially change the experiment; ask only the necessary question.

An outcome can be a player experience, a player capability, a development decision, or an improvement to the developer's workflow. Tension, wonder, mastery, expression, and deliberate difficulty are valid ends. Faster completion and fewer failures are not universal improvements.

Connect the work in plain language:

**Game promise → design question or intended outcome → playable work → evidence → decision.**

For production tools, use the developer's workflow goal in place of the game promise. Do not invent a commercial goal or claim that a local playtest proves demand. If the question is commercial, identify the audience and market evidence needed separately.

## When the premise is settled

A developer who assembles a design from mechanics that already work in shipped games is making a fresh mix of proven parts, not testing whether those parts can work. Treat the premise as settled when the developer or the design document says so. Do not ask for it to be proved, and do not word its criteria as proof.

- **Read the criteria as tuning and balance acceptance.** An unmet criterion means the game is not tuned yet. Change values first. Propose a system change only when play shows that no value in the available range gets there, and say which criterion and which range.
- **Build every specified system to verified, then judge feel in the whole.** A component is finished when it works as specified and is tested. Do not hold each part behind its own feel review: the feel of a part in isolation says little about the game. The developer judges feel by playing a whole encounter, level, or loop once the major systems function.
- **Do not block on pending assets.** When animation, audio, or art is still on its way, build the systems on reasoning from the reference games with stand-ins. Park only the checks that depend on the missing asset, and expect to retune when it arrives.
- **Keep everything adjustable through data.** Put values in a data sheet, give alternatives a switch, and document each dial, so the developer can try another setting or variant during play without a code change. A design that is easy to iterate on through spec changes matters more than getting a first value right.
- **Reason the details.** Where the design leaves a detail open, choose what best serves its stated direction, record the choice where the developer can see and reverse it, and continue. Ask only when the design documents do not make clear what game to build. Do not ask about wording or refinements you can reason through.

Use the tuning brief in [references/briefs.md](references/briefs.md) for a tuning pass.

## Shape the experiment or acceptance brief

This section applies to Explore and Deliver. A tuning pass does not need a hypothesis or a smallest build; it needs the whole experience and its dials.

1. State the primary uncertainty or intended player experience. Avoid asking one prototype to establish feel, progression, production feasibility, and demand at once.
2. Identify the smallest build that can fairly test it. Include presentation, audio, animation, content, or multiplayer participants when they are part of the hypothesis. Placeholder art is not automatically adequate.
3. Define evidence before building: observed behavior, player accounts, technical measurements, and a human interpretation where appropriate. Name what would contradict the hypothesis.
4. Specify how the findings will inform the next decision. Use meaningful thresholds when available; label proposed values as provisional. Do not fabricate benchmarks or require numerical scores for experiential judgments.
5. Bound effort and scope. State the time or effort budget if known, the exclusions, and what happens when the budget is reached. Do not invent a deadline as an agreed commitment.

Use [references/briefs.md](references/briefs.md) when producing a reusable brief, implementation handoff, or evidence record. Use [references/examples.md](references/examples.md) when a concrete game example would clarify the work. Adapt their structure instead of filling every field mechanically.

## Assign AI concrete work

When implementation is requested, supply the intended experience alongside the required mechanics, constraints, and verification. Identify which choices AI may make and which remain design decisions. Honor engine, architecture, and asset choices already established by the developer.

AI can implement test scenes, variants, resets, instrumentation, technical checks, and summaries of supplied playtest evidence. Keep architecture and content proportional to the experiment. Do not add progression, reusable frameworks, polished pipelines, or extra content solely because they could be useful later.

For work changing responsibilities, state/lifetime ownership, scheduling, dependencies, reload/replacement, or evidence production, read [references/engineering-contracts.md](references/engineering-contracts.md) before choosing the implementation. Apply the project's capability contracts; record actual conformance and gaps, rather than assuming passing gameplay tests establishes architectural quality. Routine repairs inherit these constraints without requiring another outcome brief.

When updating agent workflows or diagnosing recurring engineering escapes, use [references/harness-evaluation.md](references/harness-evaluation.md). Distinguish documented guidance from executable and enforced protection. Bind verification to the tested revision and conditions; affected evidence can become stale. Use existing tracker/manifests instead of parallel status systems.

Distinguish these states in reports:

- **Ready to playtest:** Required behavior and a usable test setup have been verified. Say exactly which checks ran and which remain unverified.
- **Evidence collected:** Actual sessions or measurements exist and are associated with the tested build and conditions.
- **AI verdict recorded:** The AI has made and recorded its own evidence-backed judgment before seeing the developer's review. This is not human acceptance.
- **Decision recorded / outcome accepted:** The developer has made the design decision or accepted the result using that evidence.

An agent's simulated player, self-review, automated playthrough, or second-agent review can reveal technical problems or suggest hypotheses. It cannot substitute for human experience evidence. Never invent sessions, quotes, preferences, or acceptance. If testing is unavailable, finish the authorized preparation and clearly identify the remaining human test.

## Independently assess and calibrate gates

For a gate review, read [references/gate-calibration.md](references/gate-calibration.md). Take responsibility for a judgment: evaluate mechanical correctness, perceptual quality, and design effectiveness using the available evidence. Do not substitute a blanket statement that only humans can judge experience for an actual assessment.

Exercise relevant scenarios, inspect the available audiovisual or interactive evidence, and address established failures within the authorized scope. Record pass, revise, or inconclusive for each layer and overall, with evidence, limitations, and specific predictions of the developer's experience. A missing observation method limits the relevant claim; it does not excuse skipping other available validation.

Preserve the assessment before the developer's playtest. Compare feedback against those original predictions, keeping both correct and incorrect predictions. Investigate whether mismatches arose from observation gaps, faulty interpretation, preference differences, implementation defects, or changed test conditions. Update the evaluation guidance as well as the game when warranted. Persistent calibration comes from records future sessions read, not an assumption that the underlying model permanently learns.

Separate building from grading. The agent or context that implemented the slice should not write the gate verdict: it has seen its own intentions and will read them into the evidence. Give the verdict to a fresh context (a new session, a separate agent, or a different model) that receives only the gate brief, prior calibration entries, and the evidence (results, logs, captures), not the code changes or build history. Store predictions separately from the assessment so the developer can play before reading them. When two evaluators review the same evidence, record both verdicts; disagreement is information. Record which evaluator made each prediction so calibration shows whose judgments hold up.

In Tune mode the unit of review is the whole experience, not a component. The same separation of builder and grader and the same sealed predictions apply, but the read reports each acceptance criterion as holds, not yet, or cannot tell, names the dial it would turn and in which direction, and predicts what the developer will want changed. It does not pass or fail the design.

Keep the game's rules in its design document, tasks in its backlog, current evaluation criteria in a short gate brief, and evidence in assessment records. Do not create a parallel comprehensive specification or silently alter rules or acceptance criteria to rescue a failed gate.

## Interpret evidence without flattening the design

Separate observation from inference. Repeated retries could indicate fascination, confusion, or frustration; record the context before choosing an explanation. Ask players about concrete moments and decisions rather than leading them toward the intended answer.

Record relevant participant experience, coaching, build version, test conditions, and unresolved failures. Use small exploratory playtests to choose the next iteration, without turning their counts into population claims. If comparing variants, note order, familiarity, and other differences that could explain the result.

A human judgment is usable when its intended experience, evidence, judge, and rationale are explicit. The developer may own both implementation and acceptance. Criteria written in advance and fresh-player tests can improve that judgment without inventing separate team roles.

When the user asks for a recommendation, give one grounded in the available evidence. Distinguish your recommendation from their recorded acceptance. If evidence is inconclusive, identify the narrow follow-up that could change the decision; do not respond with an open-ended demand for more testing.

## Work with several agents

When more than one AI agent works on a project (for example, one for code and QA, another for art or review), keep the working rules in a tool-neutral file in the repository (such as `AGENTS.md`) rather than in one assistant's settings, so every agent reads the same rules. Divide work by file area, require a short handoff note when an agent's output enters another agent's area, and keep a single current-state block that any agent can resume from. If the experiment includes how much the developer had to intervene, log interventions by cause: a spec gap is charged to the spec, not the agent.

## Keep the workflow small

Use one brief per meaningful experiment or shared outcome, not one per ticket, and one tuning brief per pass over the whole experience, not one review per system. Routine repairs, maintenance, and already authorized execution do not need an outcome gate. Preserve useful technical requirements as supporting checks rather than rewriting each as player-facing prose.

Do not install tooling, create files, run playtests, publish builds, or change project policy merely because this skill was invoked. Perform those actions when they are part of the user's request. A planning request should yield a practical plan; an execution request should proceed through the authorized work.
