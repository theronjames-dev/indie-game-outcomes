# Worked game-development examples

These are hypothetical briefs, not reports of completed tests. Their decision rules require the developer's judgment; no numerical benchmark is implied.

## Mechanic discovery: positional combat

**Promise:** Win through manipulation of enemy positioning.

**Decision:** Should shove be a core combat action?

**Hypothesis:** Setting up a shove is satisfying because players can anticipate and create a positional advantage.

**Build:** One arena, hazards, two enemy behaviors, shove, clear feedback, and fast reset. Enough feedback to distinguish intention from accidental physics outcomes.

**Evidence:** Observe whether players deliberately arrange setups after discovering the interaction. Ask them to explain a particular decision. Look for repetition caused by a universally dominant shove, accidental victories, or unclear responses.

**Decision:** Keep if setups create the intended tactical experience. Revise a specific constraint if setups are promising but one action dominates. Cut if the action adds execution without choices the developer values. If players never understand shove, first resolve whether that is a communication failure before judging the underlying tactical idea.

**AI work:** Implement the bounded encounter, reset, and useful event capture. Verify collision, shove eligibility, and hazard resolution. No progression tree or generalized ability framework is required by this experiment.

## Presentation discovery: oppressive exploration

**Promise:** Explore a place that feels inhabited by an unseen threat.

**Decision:** Does the audio treatment support the intended atmosphere?

**Build:** A short traversal with working spatial sound, pacing, lighting, and a comparison treatment. Combat and extensive lore are unnecessary unless they affect this test.

**Evidence:** Note changes in attention, pauses, and route choices. Ask which moments shaped the player's expectation and why. Distinguish intended apprehension from confusion about navigation or audio defects. If variants are compared, record their order and player familiarity.

**Decision:** The developer judges whether the accounts and observed behavior match the intended atmosphere. Faster traversal is not the target. A numeric fear score is optional and cannot replace examination of the moments that produced it.

## Delivery: readable enemy attacks

**Chosen outcome:** Intended players can recognize an attack's preparation and deliberately choose a response, while the fight retains its intended challenge.

**Supporting work:** Telegraph animation and sound, hit timing, response windows, and feedback for failed attempts.

**Evidence:** Compare player accounts of specific hits with the actual attack sequence. Observe whether later responses demonstrate understanding. Separate recognition from execution: a player can understand the attack and still mistime a dodge.

**Technical checks:** Telegraph and damaging phases occur in the intended order; interruptions reset state correctly; timing remains consistent under the project's relevant conditions.

**Acceptance:** The developer reviews play evidence for readability and challenge. Automated timing checks establish supporting behavior, not the whole outcome.

## Tuning: a settled combat design

**Design:** Melee combat assembled from mechanics the developer has studied in several shipped games: limb damage, a turn-taking enemy group, and a deflect with a counter window. The design document states that the premise is settled and lists balance criteria such as "a fight against three is survivable by positioning, not by trading hits."

**Wrong approach:** Review the deflect for feel, then the limb damage, then the group spacing, each as its own gate, and wait for final animation before building the rest.

**Tuning pass:** Build every specified system to verified with stand-in animation. Put the values in a data sheet with a switch for each variant. Give the developer one encounter with three enemies, a short list of the dials tied to each criterion, and a way to change them during play.

**Evidence:** The developer plays the whole encounter and says what felt off. A separate evaluator's sealed read names which criteria it expects to hold and which dials it would turn.

**Result:** Dial changes and the criteria still not met. If trading hits stays the best strategy at every spacing and timing value tried, that is the point to propose a system change, with the settings that were tried.

## Developer workflow: encounter generation

**Goal:** Try encounter ideas sooner without shifting effort into cleanup.

**Decision:** Is an AI-assisted encounter generator useful in this project's workflow?

**Build:** A narrow generator for an existing scene format and asset set, with validation and manual editing available.

**Evidence:** Compare representative manual and assisted tasks. Include prompting, generation wait, inspection, repairs, integration, and reaching a playable encounter. Record whether the encounter actually expresses the requested design. Keep failed attempts in the record.

**Decision:** Adopt if the workflow improves the developer's chosen measure and yields usable encounters. Revise or drop if gains disappear once repair and review are included. The number of generated rooms alone establishes little.

## Backlog review: group by purpose

Input tasks might include controller buffering, camera collision, landing sound, checkpoint reset, and an upgrade menu.

Do not assume they all serve one outcome. Buffering, camera, and landing feedback may support confident traversal; reset may support rapid retries. The upgrade menu may belong to a separate progression question.

Propose those connections as hypotheses, confirm them from project context, and retain each task's useful technical checks. Do not manufacture a new spec for every task or block an already requested camera fix while waiting for a design document.
