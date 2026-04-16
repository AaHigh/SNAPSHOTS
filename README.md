# SNAPSHOTS

Snapshot files for public IP documents documenting AI sessions.

## Relationship to Agent Skills

This repository predates Anthropic's public Agent Skills specification (`anthropics/skills`) and serves a different layer of the stack.

| Layer | Purpose | Audience | Temporal Orientation |
| --- | --- | --- | --- |
| **SKILLS** (`SKILL.md` + YAML frontmatter) | Runtime instruction bundles Claude loads dynamically to perform specialized tasks | Claude (machine) | Forward-looking: "do this task this way" |
| **SNAPSHOTS** (this repo) | Kernel-stage IP provenance artifacts with attribution, dates, and maturity progression | Humans, future collaborators, investors, AI agents reconstructing context | Backward-looking: "this idea originated here, on this date, by this person" |

The two are orthogonal and composable. A SKILL teaches Claude *how* to do something. A SNAPSHOT documents *who thought of something and when*. An idea captured as a SNAPSHOT at Kernel stage can later graduate into a SKILL once the concept has matured into a repeatable task, at which point the SNAPSHOT becomes the provenance record for the SKILL's origin.

### Dual-Format Snapshots

Snapshot files in this repo may optionally include YAML frontmatter compatible with the Agent Skills specification. This makes them discoverable by Claude as reference material without altering their human-readable IP function. The frontmatter is additive, not substitutive — the snapshot remains an IP artifact first and a Claude-loadable reference second.

Example frontmatter on a snapshot file:
