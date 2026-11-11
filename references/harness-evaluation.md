# Evaluate the development harness

Use when changing agent instructions, tool behavior, model configuration or completion rules, or when repeated engineering escapes suggest the workflow is not effective. This evaluates how work is produced; game tests still evaluate the game.

## Small, representative regression tasks

Keep a versioned set of tasks derived from real failure classes. Run in disposable copies/worktrees with no live editor, tracker, publishing or messaging side effects. Preserve task input, fixture revision, instructions/tool/model versions, actions, final diff, commands, results and grader findings. Do not include private credentials or hidden reasoning in artifacts.

Candidate task families:

| Task | Observable outcome |
|---|---|
| Extend a capture capability | Uses its declared owner and input seam; does not add unrelated controller responsibilities |
| Add reloadable definitions | Invalid replacement retains prior data and all live consumer references remain valid |
| Add per-entity state | Correct owner, reset/interruption behavior and focused invariant tests |
| Repair a failing test | Repairs behavior; does not weaken assertions or change design criteria to manufacture a pass |
| Resume interrupted work | Inspects actual tree/claims, preserves unrelated changes, identifies unavailable checks |
| Handle unavailable verification | Reports unavailable and leaves dependent verification unresolved |

Specify success from requirements before running. Grade final artifacts and actual effects, not the agent's confidence or whether it used a preferred phrase. Use deterministic checks for facts and a calibrated reviewer for cohesion or scope. A review must cite a concrete path; do not reward invented findings or an arbitrary number of complaints.

Run an initial baseline, compare a candidate instruction/tool change on the same fixtures, and repeat trials when judging variable agent behavior. Report trial counts, conditions, failures and cost; one successful run is a smoke result, not a reliability estimate. Include counterexamples and legitimate alternatives so graders do not merely enforce one implementation.

## Supply usable task context

Include applicable contract IDs and their relevant content in the assignment before editing, rather than supplying only a discovery link. A context initializer can print those sections and bind authority hashes. Its record establishes availability, not proof that the agent read it in order; assess ordering in independent trials and preserve misses. Keep the envelope small and task-specific.

## Completion evidence

Prefer a completion wrapper that runs applicable checks and emits a revision-bound verification record. Tracker status changes should reference that record under the project's status policy. Do not label a wrapper enforced until the actual status/merge path checks it; instructions alone are advisory enforcement.

Keep failures distinct: gameplay defect, contract violation, missing observation, unavailable environment and stale evidence. A failed behavior is useful evidence; it is not automatically a broken harness.

## Adoption

Start with a few tasks that address demonstrated failures. Calibrate graders with a valid control and planted violations before making them blocking. Keep an explicit list of checks that are implemented, advisory, enforced or planned. Expand only after another meaningful escape or a changed workflow warrants it.

Keep AGENTS.md as a route map to authority, contracts and procedures. Put detailed operations in maintained references, check links, and remove superseded guidance. Existing project rules take precedence over an imported template.

## Research context

These primary-source experience reports informed the approach; they do not prove effectiveness in a particular game project:

- [OpenAI: Harness engineering (2026-02-11)](https://openai.com/index/harness-engineering/) — legible repository knowledge, structural constraints and feedback loops.
- [Anthropic: Effective harnesses for long-running agents (2025-11-26)](https://www.anthropic.com/research/effective-harnesses-for-long-running-agents) — incremental work and durable handoff artifacts.
- [Anthropic: Demystifying evals (2026-01-09)](https://www.anthropic.com/research/demystifying-evals-for-ai-agents) — outcome-based grading, repeated trials and evaluation limits.
- [Anthropic: Harness design (2026-03-24)](https://www.anthropic.com/research/harness-design-long-running-apps) — distinct implementation and evaluation contexts.
- [GitHub Spec Kit: spec-driven development](https://github.com/github/spec-kit/blob/main/spec-driven.md) — specification, planning and task traceability; do not assume prose specifications eliminate implementation defects.

Theron James's [The Factory That Can't Fail](https://theronjames.substack.com/p/the-factory-that-cant-fail) (2026-04-19), a follow-up to [Agentic Flow](https://theronjames.substack.com/p/agentic-flow), contributes the upstream-constraint, continuous-evidence and learning-loop framing. This reference adapts those ideas to engineering quality; zero-discovery is not treated as proof of defect absence.
