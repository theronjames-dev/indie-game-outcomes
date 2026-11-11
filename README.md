# Indie Game Outcomes

A lightweight AI skill for indie developers who want playable experiments to answer design questions.

Use it to decide what to prototype, brief an AI coding assistant, interpret playtests, and connect implementation work to an intended player experience. It supports solo developers and small teams, across engines and genres. No scripts, paid services, or engine integrations are required.

## What it does

- Turns a feature idea into a bounded experiment and a keep/change/cut decision.
- Treats a design built from proven mechanics as settled: builds its systems on reasoning, then tunes the whole experience instead of gating each part.
- Treats tension, wonder, expression, and mastery as valid outcomes.
- Separates a technically working build from a human-accepted design result.
- Keeps AI assignments focused on the current question.
- Evaluates developer tooling by the full workflow, including review and repair.
- Records an independent AI gate verdict before your playtest, then calibrates future assessments against your feedback.
- Applies capability boundaries and revision-bound evidence to engineering changes, and evaluates agent workflows against representative failure cases.

It does not measure fun automatically, guarantee commercial demand, or require a spec for every bug fix.

## Install

The skill entrypoint is [SKILL.md](SKILL.md). Keep it together with `references/` when adding the folder to a compatible assistant's skill collection.

- **Claude Code:** copy or clone this folder to `~/.claude/skills/indie-game-outcomes/` (all projects) or `.claude/skills/indie-game-outcomes/` inside one project.
- **Claude apps:** zip the folder and upload it as a custom skill.
- **Codex:** add the folder to your skills directory. `agents/openai.yaml` supplies optional interface metadata; the core instructions do not depend on it.

```bash
git clone https://github.com/theronjames-dev/indie-game-outcomes ~/.claude/skills/indie-game-outcomes
```

## Use

Where named skill invocation is supported, try:

```text
Use $indie-game-outcomes to help me decide whether a grappling hook
belongs in my exploration game. I have a movement prototype and
one evening for the next experiment.
```

Other starting requests:

- “Turn this combat idea into a small experiment and a bounded AI build brief.”
- “Review this backlog and group the work by the player experience it serves.”
- “Here are my playtest notes. Recommend what to keep, change, or cut.”
- “The design is settled and the systems are in. Set up a tuning pass for the full encounter.”
- “Help me evaluate whether my AI level-generation workflow actually saves time.”

You can also supply the skill's Markdown as context to an assistant that does not support skill discovery. State that you want it applied to your request. Compatibility depends on the host; this package has not been tested across assistant products.

## Files

- [SKILL.md](SKILL.md): scope, workflow, and decision guidance.
- [references/briefs.md](references/briefs.md): prototype, tuning, delivery, handoff, and evidence formats.
- [references/examples.md](references/examples.md): mechanics, atmosphere, tuning, delivery, tooling, and backlog examples.
- [references/gate-calibration.md](references/gate-calibration.md): independent AI judgments, tuning reads, predictions, and developer-feedback comparisons.
- [references/engineering-contracts.md](references/engineering-contracts.md): ownership, lifecycle, failure handling, architecture review and evidence freshness.
- [references/harness-evaluation.md](references/harness-evaluation.md): agent regression tasks and the distinction between planned checks and enforced protection.
- [CHANGELOG.md](CHANGELOG.md): what changed in each version and why.
- [ATTRIBUTION.md](ATTRIBUTION.md): provenance and upstream sources.
- [LICENSE](LICENSE): MIT license for this package.

## Background

This skill applies [Agentic Flow](https://theronjames.substack.com/p/agentic-flow), a spec-driven operating model for agent-assisted development, to indie game R&D and production. The longer argument is on [Theron James's Substack](https://theronjames.substack.com).

## Contributing

Useful contributions include real cases where the skill chose an unhelpful experiment, confused implementation with experience, or added unnecessary process. Include the request, relevant project context, the response, and what would have been more useful. Remove private project material before sharing it.

Prefer focused improvements over universal rules derived from one game. Clearly distinguish hypothetical examples from observed results. Keep the core instructions engine-neutral and route substantial examples into references.

## License

MIT. See [LICENSE](LICENSE). Provenance is in [ATTRIBUTION.md](ATTRIBUTION.md).
