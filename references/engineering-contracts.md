# Engineering contracts and continuous evidence

Use for implementation that changes responsibilities, state ownership, lifecycle, dependencies, scheduling, persistence, or evidence production. Routine repairs inherit existing contracts; they do not need a new design process. Keep game rules and values in the project's authoritative design sources.

## Contract before implementation

An outcome describes what should become possible and why. A capability contract describes the boundary within which it is built. Read applicable contracts before choosing an implementation. Missing contracts are recorded gaps, not evidence that any architecture is acceptable.

Use the project's existing contract format. Where none exists, record:

| Field | Required meaning |
|---|---|
| ID and scope | Stable identifier; subsystem and source locations covered |
| Responsibility | What it owns; neighboring owners and excluded responsibilities |
| State and mutation | Owner of mutable state, permitted operations, read-only observations |
| Lifetime | Fighter/world/session/process; reset, interruption, reload, travel and teardown behavior |
| Execution | Scheduling/phase, cross-entity reads, when decisions become effects |
| Dependencies | Direction of dependencies; definition, asset and borrowed-reference lifetime |
| Failure | Invalid input, unavailable resource and partial-operation behavior; retained valid state |
| Evidence | Named checks, tested conditions, known limits, and invalidation triggers |
| Conformance | Established, gap, exception or unverified; links to actual evidence and repair work |

Prefer a few coherent contracts over one per class. Immutable process-wide definitions can be appropriate; mutable state needs a deliberate lifetime. Do not require a world-scoped rewrite when sequential single-world operation is the supported mode. A bounded prototype shortcut may be explicit without becoming the permanent architecture.

## Build prevention into interfaces

- Give each state group one owner and invariant-preserving operations. Separate test configuration from ordinary gameplay mutation.
- Keep input, console and UI entry points thin where they coordinate unrelated capabilities. Moving methods to another file does not separate responsibilities.
- Place interactions in the project's scheduler, including actor ticks, movement helpers and presentation callbacks. Do not add independently ticking components merely to reduce class size.
- Keep references valid across supported replacement/reload operations. Choose stable handles, retained snapshots or an equally explicit lifetime strategy.
- Validate replacements before publishing; preserve the prior valid state on failure where the contract requires it. State whether rollback preserves exact progress or rebuilds declared starting conditions.
- Check required writes and expose failure. Do not claim evidence exists when its write failed; bound retained buffers and report exhaustion rather than growing memory indefinitely.
- Declare runtime asset dependencies and verify the packaged path when relevant. A successful editor run does not establish cook/staging coverage.
- Use one serialization schema and verify emitted values by name after parsing, including escaping.

These are engineering properties, not a demand for a particular framework or class hierarchy. Use the smallest implementation that satisfies the actual contract.

## Verification and freshness

Link stable requirement/contract IDs to implementation boundaries, named checks and evidence. Reuse existing manifests; do not create a second status database.

A verification record identifies source revision plus relevant dirty-file hashes, applicable contract versions/hashes, commands and outcomes, environment, evidence paths, skipped checks and remaining gaps. Valid states include pass, fail, unavailable and stale. A successful process exit alone does not establish the intended effect.

Changes to a relevant source, contract, data sheet, asset, engine/tool version or test environment invalidate affected evidence until impact is assessed or checks rerun. Preserve historical evidence unchanged. Revalidate only affected claims; a documentation spelling correction need not invalidate unrelated gameplay recordings. A missing tool is unavailable verification, never a pass inherited from an older run.

Keep functional correctness, architecture, evidence validity and player experience separate. Do not average away a failed critical invariant. Human acceptance remains a separate recorded decision.

## Implementation and review loop

Before work: identify applicable contracts, state/lifetime changes, implementation seam and decisive failure cases. During work: implement through the owner, run focused feedback, update the contract if its agreed engineering boundary changes. At handoff: record evidence, limits and outstanding violations.

Use independent architecture review for changes to ownership, scheduling, definition lifetime or destructive replacement. Give the reviewer requirements, contracts, diff and raw evidence; require traced paths and concrete counterexamples. This is different from an experiential gate evaluator, whose packet may deliberately exclude code and build history. Independence is a separate context/reviewer, not necessarily another model. If unavailable, record that limitation and leave dependent architectural verification unresolved; unrelated checks may still be recorded. Do not describe self-review as independent.

Existing contract violations are tracked baseline debt. Do not certify them by writing a contract or silently redesign adjacent systems. Do not worsen them. Any temporary exception names the invariant, supported conditions, risk, owner/tracker item and expiry or concrete removal trigger. The owner resolves engineering details within authorized scope; changes to game rules or acceptance remain with the developer.

## Learning without accumulating a manual

For an escaped issue, record cause, evidence, missing prevention, applicable scope, the resulting interface/check change and a test that demonstrates detection. A planted failure plus a valid control establishes that a proposed check discriminates; initially advisory checks become blocking only under the project's agreed promotion rule.

Track late discoveries by severity and cause, along with independent-check coverage. Zero discoveries does not prove zero defects. Retain independent inspection to challenge shared blind spots and reward honest reporting.
