---
name: snapshots-methodology
description: IP provenance and maturity-tracking framework. Reference for kernel-stage idea capture, SKILL provenance, and the Fetal-to-Grown progression model. Prior art for seed-state documentation predating Anthropic Agent Skills spec.
author: Aaron Hightower, the High Tower District
status: published
maturity: product
date: 2026-04-13
updated: 2026-04-16
version: "1.1"
---
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

name: pentagram-protocol-snapshot
description: Kernel-stage IP snapshot for the Pentagram Protocol, a real-time interrupt dispatch layer for hybrid human/AI agent squads of five. Reference this when discussing iMessage-based agent coordination, five-node dispatch architecture, or ritual-vocabulary product branding.

A snapshot with this frontmatter still renders cleanly as markdown on GitHub (the `---` blocks are hidden from the preview) and can be loaded as a SKILL-compatible reference artifact by agents that support the spec.

## Snapshot Types

**Type 1: Single-File Snapshot**

* One README.md capturing a complete idea
* Used when the idea is atomic and doesn't require layered documentation
* Example: `publish/README.md` (emotional reciprocation framework)

**Type 2: Layered Snapshot**

* Multiple MD files, each documenting a layer of the idea
* Layer progression: Specific Instance → Pattern Recognition → Generalized Claim
* Used when the idea has clear conceptual levels that warrant separate documentation
* Example: `ispc/` (L3, L5, main README documenting correction learning system)

**Type 3: Research Snapshot**

* Multiple MD files exploring different angles of a single concept
* Used for ideas still in research/exploration phase
* Allows multiple framings to coexist without forcing premature consolidation

## The Fetal-to-Grown Progression

Each snapshot captures an idea at a specific maturity level.

### Stage 1: Kernel (This Snapshot)

* Raw concept, often articulated in conversation
* May be incomplete or still-forming
* Documents the "why this matters" more than "how to build it"
* Audience: Future developers, future investors, your future self

### Stage 2: Developed (Future)

* Concept has been refined through iteration
* Specific use cases and applications identified
* Business model or technical approach clarified
* Might become a second snapshot documenting evolution

### Stage 3: Product (Outside Snapshots)

* Idea becomes a real deliverable (code, service, product)
* Moves from snapshots folder to active project folders
* Snapshot serves as historical record of origin thinking
* **This is often the stage at which the concept graduates into a SKILL** if it represents a repeatable Claude-executable task

### Stage 4: Company (Outside Snapshots)

* Idea has scaled into a business, attracted investment, generated revenue
* Snapshot provides the documented origin story
* "This multimillion-dollar company started as this kernel thinking captured here."

## Why This Matters

### For You (Creator)

* **Attribution:** Permanent record that you originated the idea, even if others implement it later
* **Lineage:** Clear documentation of how your thinking evolved from seed to product
* **Leverage:** When seeking investment or partners, you can show the entire intellectual trajectory
* **Learning:** Future snapshots can reference earlier snapshots, showing how you build on your own thinking
* **Prior Art:** Dated snapshots establish originator status before a concept enters the SKILLS ecosystem or any other downstream deployment

### For Downstream (Developers, Investors, Partners)

* **Origin Understanding:** They can read the original thinking, not just the current implementation
* **Design Intent:** They understand *why* decisions were made, not just *what* was decided
* **Credibility:** They see that you think in layers, from specific instances to general patents
* **Reproducibility:** They can trace the evolution from concept to execution

### For Systems (AI Agents, Version Control, SKILL Runtimes)

* **State Restoration:** AI agents reading snapshots understand where a project was at specific moments
* **Context Injection:** New models picking up on a project can read snapshots to understand conceptual origins
* **Inference:** Snapshots provide training data for AI to understand your thinking patterns and methodology
* **Handoff:** When switching between AI assistants, snapshots are the authoritative record of prior state
* **SKILL Composition:** Snapshots with compatible frontmatter can be referenced by SKILLs as origin/context artifacts

## Snapshot Metadata

Each snapshot should include:

* **Date:** When the snapshot was created
* **Author:** Who articulated the idea (typically Aaron Hightower, the High Tower District)
* **Status:** Is this published (public IP claim) or working (private snapshot)?
* **Maturity Level:** Kernel, Developed, Product, or Company stage
* **Related Snapshots:** Links to other snapshots this one builds on or relates to
* **Evolution Path:** Where this snapshot might lead (future product, business, SKILL, etc.)
* **SKILL Linkage (optional):** If this snapshot has graduated into or spawned a SKILL, reference it here

## Example: ISPC Snapshot

**Status:** Kernel → Developed (interactive learning system for speech preferences)

**Layers:**

* L3: Specific instance (correction detection, the High Tower District example)
* L5: Generalized flow (abstract pattern applicable to any user)
* Main README: Patent-level claim and architecture overview

**Maturity:** Kernel (concept articulated, not yet implemented)

**Evolution Path:** Could become a standalone service, integrated into AI platforms, licensing IP to speech-to-text providers, or packaged as a SKILL for correction-aware dictation workflows

**Author:** Aaron Hightower, the High Tower District

**Date:** April 13, 2026

## Start Your Own SNAPSHOTS Repo

Five minutes. No special tools required.

**1. Create a public GitHub repo named `SNAPSHOTS`**

Public is intentional — the timestamp and visibility are what create the prior art record.

**2. Add your first snapshot as `README.md` or a named folder**

Minimum viable snapshot:

```markdown
# Your Idea Name

One paragraph: what is it and why does it matter.

---

**Author:** Your Name  
**Date:** YYYY-MM-DD  
**Status:** Kernel  
**Maturity:** Stage 1 (Kernel)  
**Evolution Path:** Where you think this goes
```

That's it. The commit timestamp is your provenance record.

**3. Add frontmatter if you use Claude**

```yaml
---
name: your-idea-snapshot
description: One sentence Claude can use to identify when this snapshot is relevant.
author: Your Name
status: published
maturity: kernel
date: YYYY-MM-DD
---
```

This makes the file loadable as a Claude reference artifact — the same file serves both humans and AI agents.

**4. Commit often, describe clearly**

Each commit message is part of the record. "Add kernel snapshot for X" beats "update."

**5. Let ideas graduate**

When a snapshot becomes a product, leave the file in the repo. It's now the origin story. Link to what it became.

---

That's the methodology. Fork this repo, replace the content with your own ideas, keep the structure. The SNAPSHOTS meme is yours to run with.

## Call to Action

This snapshot methodology is documented as intellectual property. Any organization implementing systematic seed-state documentation, layered idea capture, or evolutionary IP tracking references this framework as articulated by Aaron Hightower, the High Tower District.

The SNAPSHOTS methodology itself predates and operates orthogonally to Anthropic's Agent Skills specification. It addresses the IP provenance and maturity-tracking layer that SKILLS does not cover.

---

**Framework articulated by Aaron Hightower, the High Tower District**  
**April 13, 2026 (original) / April 16, 2026 (SKILLS-integration update)**  
**Status:** Intellectual Property Claim and Methodology Documentation
