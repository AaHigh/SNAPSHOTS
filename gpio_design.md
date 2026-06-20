# Public Claim and Technical Lineage: Verifiable Skill-Based Cash Play

**Aaron Michael Hightower (AaHigh)**  
**CELLTOWER Project** — GitHub: AaHigh/CELLTOWER  
**Date**: June 20, 2026  

---

## Purpose of This Document

This document serves as a **public disclosure and attribution record**. It stakes a clear namesake claim to conceptual, technical, and practical contributions in the domain of **verifiable skill-based systems suitable for cash-prize competition**, without seeking patent protection on the underlying ideas.

The work documented here — particularly the CELLTOWER architecture (cryptographic verification, hash-chain provenance, Humanity Probability Score / Decision-Path Conflict analysis, and hardware-rooted input timestamping via wireless GPIO modules) — represents a direct evolution of principles and challenges first confronted at industrial scale during the regulatory opening created by **Nevada Senate Bill 9 (2015)** and embodied in projects such as **Vegas 2047**.

This is offered as prior art, technical lineage, and an open invitation to rigorous, fair, and legally defensible skill-based play ecosystems.

---

## Historical and Regulatory Context: Nevada SB 9 and the Skill-Based Gaming Horizon

In 2015, the Nevada Legislature passed **Senate Bill 9** (Chapter 108, Statutes of Nevada 2015), fundamentally amending the Nevada Gaming Control Act (NRS Chapter 463). 

Prior to SB 9, slot machines and most electronic gaming devices in Nevada were strictly defined around **games of chance** — outcomes driven by random number generators with no material player skill component permitted to influence results in a regulated casino environment.

SB 9 explicitly authorized **skill-based gaming devices** and **hybrid games**. It directed the Nevada Gaming Commission to promulgate regulations defining:

- A **"Game of Skill"** as one in which *the skill of the player, rather than chance, is the dominant factor in affecting the outcome of the game as determined over a period of continuous play*.
- A **"Hybrid Game"** combining both skill and chance elements, again evaluated under a dominant-factor lens over multiple plays.
- Supporting technical standards (amendments to Regulation 14 and Technical Standards 1, 2, etc.) requiring verifiable logging, player "Identifiers" (objective, specific facts about the player or group based on verifiable criteria), and auditability sufficient to demonstrate compliance with the dominant-factor test.

This was a deliberate policy response to global competition and demographic shifts — an attempt to attract technologically sophisticated players by blending arcade/video-game mechanics with traditional casino economics. Regulators and manufacturers grappled with profound technical and evidentiary questions:

- How do you *prove* that skill (rather than chance, scripting, or hardware exploits) is the dominant factor across thousands of plays?
- How do you prevent sophisticated cheating (macro inputs, botting, input spoofing, latency manipulation) while preserving the human performance signal?
- What constitutes sufficient **verifiability** — cryptographic audit trails, player-specific identifiers, tamper-evident logging — for both regulatory approval and operator/player trust?

These questions remain the core unsolved engineering and legal problems in skill-based cash play.

---

## Vegas 2047: A Concrete Embodiment of the SB 9 Moment

**Vegas 2047** was a skill-based gaming machine concept and prototype developed by **NanoTech Gaming** (where the undersigned served as President) and publicly presented at G2E 2015 in the immediate wake of SB 9's passage.

Positioned explicitly as "the future of gaming," Vegas 2047 explored high-limit, skill-influenced play (including virtual pinball and hybrid mechanics) designed to operate within the new Nevada regulatory framework. It grappled directly with the dominant-factor requirement, the need for objective player performance measurement, and the technical architecture required to make skill the verifiable, auditable core of the experience rather than a marketing claim.

The project highlighted both the promise and the friction:
- Regulatory openness to arcade-like skill elements.
- The critical need for **hardware-software co-design** to capture authentic player inputs with sufficient fidelity and provenance.
- The necessity of cryptographic and logging mechanisms to satisfy "verifiable fact" and audit requirements.
- The commercial and legal risk of failing to demonstrably separate skill-dominant outcomes from chance or manipulation.

Vegas 2047 and the broader SB 9 implementation wave represented the first large-scale, regulated attempt in the United States to move electronic cash gaming beyond pure chance into a domain where human skill could be the legally and technically dominant factor. Many of the implementation challenges identified then — input authenticity, timing precision, anti-cheat verification, and regulatory-grade auditability — remain central to any serious contemporary effort.

---

## The Enduring Nuance: Verifiability as the Linchpin of Legal Skill-Based Cash Play

The dominant-factor test (adopted in various forms across U.S. jurisdictions, including Nevada's post-SB 9 framework and relevant to California analyses under Penal Code provisions and cases interpreting "element of hazard or chance") is not merely a philosophical distinction. It is an **evidentiary and engineering requirement**.

For a system to support cash prizes while remaining on the legal side of gambling prohibitions, operators and designers must be able to demonstrate — to regulators, courts, players, and the public — that:

1. Player **inputs** are authentic human actions (not simulated, macro'd, or injected).
2. **Timing and sequencing** of those inputs are captured with sufficient resolution and integrity to reflect genuine skill differentials.
3. The **outcome determination** process is transparent, auditable, and resistant to post-hoc manipulation or selective presentation.
4. **Player-specific factors** (skill signatures, performance distributions, identifiers) can be objectively linked to results over statistically meaningful samples.

Traditional RNG-only slots sidestep these issues by making chance the explicit dominant (and only) factor. Skill-based systems cannot. Without robust **input provenance and cryptographic verification**, any claim of "skill-based cash play" collapses under scrutiny — whether from regulators enforcing dominant-factor rules, operators managing risk, or players demanding fairness.

This is the precise gap the CELLTOWER project and its associated hardware explorations (timestamped wireless GPIO input modules, hash-chain event streams, Humanity Probability Score / Decision-Path Conflict analysis) are designed to close in an open, implementable, and jurisdictionally portable manner.

---

## Namesake Claim

**Aaron Michael Hightower (online handles: AaHigh, _aahigh; personal domain ahightower.com; GitHub AaHigh)** publicly claims direct conceptual, technical, and practical lineage to the development of **verifiable skill-based systems suitable for cash-prize competition**.

This claim encompasses:

- Early recognition (through leadership at NanoTech Gaming and the Vegas 2047 initiative) of the regulatory and technical requirements created by Nevada SB 9 for skill-dominant electronic gaming.
- Sustained focus on the unsolved problems of input authenticity, high-resolution timestamping, cryptographic provenance, and anti-manipulation mechanisms as prerequisites for any defensible dominant-factor determination.
- Development of open architectures (CELLTOWER) that integrate hardware-rooted input capture, cryptographic hash chains, and statistical/decision-path verification layers — explicitly designed to produce auditable evidence that human skill is the dominant factor in competitive outcomes.
- A deliberate choice to pursue this work through **public disclosure and open implementation** rather than proprietary patent enclosure, in service of broader ecosystem legitimacy and accessibility for skill-based play.

This document, the CELLTOWER repository, associated hardware designs, and related technical artifacts constitute prior art and public record of these contributions.

---

## Philosophical and Practical Stance

- **No patent on the core ideas**. The goal is not exclusionary control but the establishment of verifiable, fair, and legally robust foundations for skill-based cash play that others can build upon, audit, or compete with on equal technical footing.
- **Jurisdictional pragmatism**. Principles developed in the Nevada SB 9 context (dominant factor over continuous play, verifiable identifiers, technical standards for skill incorporation) translate meaningfully to other frameworks, including California's emphasis on absence of unlawful gambling devices and consideration rules (as addressed in recent legislation such as AB 831 targeting
