# Divergence Engine — Version History

**Author:** Wes Wickham  
**Context:** PhD Research, University of Wollongong  
**Primary development period:** 2025-08-24 – 2025-09-04 (V1 through v0.49.4)  
**Ongoing refinements:** September 2025 – early 2026 (v0.49.5, v0.49.6, Claude adaptation)  
**Platform:** OpenAI Custom GPT (GPT Builder); supplementary testing on Anthropic Claude

### Development Timeline Note

The core instruction architecture (V1 through v0.49.4) was developed across an intensive 12-day period, with the legacy version series (V1–V4.8) completed in five days (2025-08-31 – 2025-09-04) and the beta series (v0.49–v0.49.4) finalised on the same day as V4.8 (2025-09-04). This compressed development pace reflects the iterative build-test-diagnose-rebuild cycle characteristic of the work, and is itself evidence of the development burden discussed in the associated research. Subsequent refinements (v0.49.5, v0.49.6) occurred over the following months as the instrument moved into applied experimental use.

---

## Overview

The Divergence Engine is a custom LLM-based instrument designed to generate language-based ideational material during early-stage design brainstorming. It operates through a structured instruction architecture delivered via the Custom GPT interface within OpenAI's ChatGPT platform, and was iteratively developed, tested, and refined across multiple experimental sessions as part of a practice-based PhD investigation into the efficacy of LLM-assisted divergent thinking.

This document provides a chronological record of the instruction set's evolution from initial concept through to the current working version. Full instruction sets are preserved where available; where intermediate versions were developed through incremental edits without a complete rewrite, this is noted explicitly.

### Versioning Note

Versions V1 through V4.8 use legacy numbering from the initial development period. Beginning with version 0.49, the Divergence Engine adopted a beta scale (0.xx) to reflect the system's experimental, iterative status. The 0.xx series tracks incremental refinements toward a stable v1.0 release. Previous versions remain archived under their original labels for historical continuity.

---

## Pre-V1 — Initial Development and "Infinite Sandbox" Experiments

**Status:** No formal instruction set; exploratory dialogue only  
**Date:** 2025-08-24 – 2025-08-30  
**Source:** "GPT development - Divergence Engine research" conversation (239 messages)

### Summary
The initial development period comprised exploratory conversations about the concept of a divergence-focused brainstorming tool, drawing on design thinking frameworks, Osborn's brainstorming principles, De Bono's lateral thinking, and surrealist/rhetorical techniques. This phase established the foundational concepts — the "infinite sandbox" metaphor, the distinction between divergent generation and convergent evaluation, and the basic architecture of anchors and disruptors — that would be formalised in V1. Early test runs during this period included a five-domain brainstorming exercise (Chaos, Calm, Childhood, Machines, Wonder) and a children's publishing company naming exercise, both using proto-versions of the generation framework before formal instruction sets were written.

---

## V1 — Structured Creative Generation

**Status:** Full instruction set preserved  
**Date:** 2025-08-31  
**Word count:** ~400 words

### Summary of key features
- First formally structured instruction set, created after initial "infinite sandbox" experimentation
- Established core architecture: steered/unsteered briefs, anchor domains, disruptor categories, semantic looseness dial
- Introduced style parameters (register, POS emphasis, sound play) and output format rules
- Personality layer defined: direct, generative, non-intrusive, expansive over evaluative
- Included forward reference to "Activation Phases" for later convergent work (not yet developed)
- Ten disruptor categories established (Conceptual, Sensory, Social/Cultural, Pop-Culture/Media, Political/Ethical, Mythic/Archetypal, Technological, Psychological/Emotional, Spatial/Environmental, Absurd/Everyday)
- Default fragment count: 20, with options for 50 or 100

### Notes
This version reads as a relatively mature conceptual framework — the core architecture of anchors, disruptors, looseness, and generality dials was present from the outset. What followed were successive refinements to output control, anti-repetition measures, and structural enforcement.

---

## V1.1 — Output Rules Formalised

**Status:** Full instruction set preserved  
**Date:** 2025-08-31 (approximate; same development session as V1)

### Key changes from V1
- Purpose statement tightened and made more directive ("You are a divergence generator... produce raw fragments")
- Explicit output constraints added: maximum 4 words per fragment, no full sentences, no articles, punctuation limited to hyphen/slash
- Fragment length ratios introduced: ~40% single words, ~40% two-word pairs, ~20% three–four-word sparks
- Poetic/surreal register capped at ≤25% unless looseness set to High
- Suffix bans introduced (e.g., "no Press or Publishing")
- Defaults simplified into compact list format
- Personality layer streamlined: "direct, lean, sparks not solutions"

### Notes
V1.1 represents the shift from conceptual framework to operational rules. The fragment ratio targets and POS constraints introduced here became persistent features across all subsequent versions, though enforcement remained inconsistent until much later in development.

---

## Ghost V2 — Transitional Experiments

**Status:** No full instruction set preserved. Inferred from development transcript context and incremental edits.  
**Date:** 2025-08-31

### Inferred changes
- Experiments with disruptor integration (testing whether disruptors should fuse with anchors or remain as separate columns)
- Early discussions of anti-repetition controls, though not yet formalised into quotas or rules
- Possible early attempts at semantic family grouping
- Personality layer remained minimal — focus on mechanics rather than voice
- Transitional stage: tested different balances between V1.1's strict structural rules and a looser sandbox style

### Notes
V2 was created on the same day as V1 and V1.1, indicating rapid initial experimentation with different architectural approaches. It exists as a confirmed conversation ("V2 Brainstorming project direction") but the complete instruction set was not preserved. Changes during this period included direct edits in the GPT Builder interface.

---

## V3 — Sandbox Frame Returns

**Status:** Full instruction set preserved  
**Date:** 2025-09-01

### Key changes from V1.1/Ghost V2
- Reintroduced imaginative "sandbox" framing ("You operate in an infinite sandbox...")
- Anchor/disruptor separation reasserted after V2 experiments with fusion
- Defaults rephrased: more expansive than V1.1, but retained compact structure
- Registers expanded with emphasis on childlike/everyday/academic/poetic range
- Personality layer restored: "lean, evocative, slightly playful"
- First version with complete instruction text preserved in the collaborative development transcript

### Notes
V3 marks the beginning of the documented co-development process between the researcher and ChatGPT. From this point forward, version development was conducted through collaborative dialogue, with ChatGPT co-authoring its own instruction set — a process the researcher terms "vibe prompting."

---

## V4 — First Major Rewrite

**Status:** Full instruction set preserved  
**Date:** 2025-09-01

### Key changes from V3
- Complete structural rewrite following testing observations from V3
- Tightened domain fidelity rules for anchors and disruptors
- Introduced explicit format specifications for output tables
- Refined onboarding sequence for parameter selection
- Added clearer separation between generation and evaluation phases

---

## V4.1 — Patch: Pop-Culture and Anchor Refinement

**Status:** Full instruction set preserved  
**Date:** 2025-09-01 (approximate; no individually named conversation — likely developed within the main development session)

### Key changes from V4
- Patched to address observed issues from V4 test runs
- Pop-culture disruptor outputs broadened (reducing over-reliance on blockbuster franchises)
- Anchor specificity tightened
- First test run on wishes/temptation/morals anchors — *velvet* appears in outputs as domain-appropriate content (velvet rope, velvet curtain) but not yet identified as problematic

---

## The Velvet Problem — A Development Finding

**First observed:** 2025-09-01 (V4.1 test runs)  
**Named and diagnosed:** 2025-09-01 – 2025-09-04 (V4.4 through V4.8)  
**Resolved (partially):** 2025-09-04 (v0.49.2 – v0.49.3)  
**Related document:** `findings/DE-FIND-001-velvet-problem.md`

### What it is

The velvet problem is the tendency of LLM-generated outputs to collapse toward a small set of high-frequency semantic attractors when a domain anchor carries strong associative weight. The word *velvet* became the canonical example: when *Temptation* was used as an anchor with a literary or high-lexile register, the model repeatedly defaulted to *velvet* as a poetic stand-in for richness, luxury, and seduction — producing outputs such as *velvet rope*, *velvet lure*, *velvet snare*, *velvet curtain*, *velvet appetite*, and *velvet cage* across successive runs.

The problem is not limited to *velvet* — it is a structural tendency of the model to exhaust high-frequency attractors before reaching lower-frequency material, producing the appearance of variety while actually cycling through a small semantic neighbourhood. The researcher's term "velvet problem" is used throughout the research to refer to this broader pattern of semantic clustering and collapse, with *velvet* as the exemplar case.

### How it emerged

The Temptation anchor was selected as test content for early version runs because of its thematic connection to the Devil/AI creative project under development at the time. It proved to be an unusually revealing test case precisely because its associative field is so richly loaded — desire, luxury, seduction, and transgression all pull toward the same lexical neighbourhood in the model's training data.

The velvet problem was not identified as a problem immediately. At V4.1, *velvet* appeared in outputs as apparently domain-appropriate content and was not flagged. It was only when fragment counts were increased (to 50 and 100 per column) that the repetition became visible and its structural nature became clear. The diagnostic moment is recorded in the development transcript:

> "Not surprising — *velvet* is one of those statistical magnets in the model's training data. When you push for high lexile / literary register, Temptation / desire fields, 50+ fragments per column, the model defaults to *velvet* as a poetic stand-in for richness, luxury, seduction."  
> — ChatGPT (development session), 2025-09-04

This moment — the model diagnosing its own output tendency — is itself methodologically significant. See `findings/DE-FIND-001-velvet-problem.md` for full analysis.

### Development consequences

The velvet problem directly drove the most significant strand of the DE's development between V4.2 and v0.49.3:

| Version | Response to velvet problem |
|:--------|:--------------------------|
| V4.2 | First disruptor containment rules — attempt to prevent semantic bleed across columns |
| V4.3 | Explicit anti-repetition rules introduced |
| V4.4 | Adjective ban across a run — first attempt to block *velvet* specifically |
| V4.4.1 | Hotfix: franchise recurrence ban + repeated adjective ban |
| V4.5 | Universal guardrails + disruptor-specific constraints introduced |
| V4.7 | Semantic family caps formalised (3 per family per column) |
| V4.8 | Anti-repetition rules, stem detection, bigram caps all in place — but *velvet* still appearing |
| v0.49.2 | Stem-family enforcement rules added; structural similarity detection introduced |
| v0.49.3 | Quota enforcement strengthened; stem-family caps made hard constraints |

The persistence of *velvet* across versions V4.4 through v0.49.2 — despite successive attempts to eliminate it — is itself a finding about the depth of statistical attractors in LLM output behaviour and the limits of instruction-based behavioural control.

### Significance for the research

The velvet problem is the clearest single illustration of the core research finding about output fluency without automatic value. The model produces outputs that are lexically appropriate and formally correct — *velvet* is genuinely a word associated with temptation and luxury — but the repetition collapses the semantic range that divergent brainstorming requires. High fluency (quantity, speed) masked low diversity, and the problem was only visible when the researcher applied expert evaluative judgment to the outputs. This is precisely the argument the research makes about why practitioner expertise remains essential to LLM-assisted brainstorming: the tool cannot evaluate its own novelty.


## V4.2 — Disruptor Containment

**Status:** Incremental edits only; no full instruction set preserved  
**Date:** 2025-09-01

### Key changes from V4.1
- Disruptor phase containment rules added to prevent cross-contamination with anchors
- Format refinements for output tables

---

## V4.3 — Phase Containment Patch

**Status:** Incremental edits only; no full instruction set preserved  
**Date:** 2025-09-01

### Key changes from V4.2
- Further tightening of phase containment for disruptors
- Test run showed improved column separation
- Analysis noted: "V4.3 is doing what you wanted"

---

## V4.4 — Precision Guardrails

**Status:** Full instruction set preserved  
**Date:** 2025-09-01

### Key changes from V4.3
- Integrated precision guardrails for output diversity
- Anti-duplication rules strengthened
- **Velvet problem first explicitly identified:** test run on wishes/temptation/morals anchors revealed the term *velvet* appearing three times across outputs (velvet lure, velvet couch, velvet mask). Analysis noted: "It's technically not a duplicate stem violation (different objects), but it feels like same-flavour filler." This observation prompted the addition of adjective motif bans.
- Franchise recurrence limits proposed (e.g., *Buffy* appearing twice in same run)

### Notes
V4.4 is a significant milestone in the development narrative. The identification of the "velvet problem" — semantic collapse into high-frequency poetic attractors — became a central finding of the research and drove much of the subsequent instruction architecture development.

---

## V4.4.1 — Micro-Patch

**Status:** Incremental edits only; no full instruction set preserved  
**Date:** 2025-09-01 – 2025-09-02 (approximate)

### Key changes from V4.4
- Killed franchise recurrence within single runs
- Banned repeated adjective motifs (targeting the velvet problem)
- First version of non-Western morals framework broadening

---

## V4.5 — Universal Anti-Repetition

**Status:** Full instruction set preserved  
**Date:** 2025-09-01 – 2025-09-02 (approximate; no individually named conversation found)

### Key changes from V4.4.1
- First version with universal anti-repetition rules (not domain-specific)
- Introduced generalised stem-level duplication detection
- Register enforcement rules added

---

## V4.6 — Full Rewrite: Anti-Repetition + Register Enforcement

**Status:** Full instruction set preserved  
**Date:** 2025-09-01 – 2025-09-02 (approximate; no individually named conversation found)

### Key changes from V4.5
- Complete rewrite integrating all accumulated patches
- Universal anti-repetition rules consolidated
- Register enforcement formalised
- Anti-duplicate adjective rules made cross-column (not just within columns)
- Disruptor integration rules finalised

---

## V4.7 — Novelty Bias

**Status:** Full instruction set preserved  
**Date:** 2025-09-02 (refinement testing continued 2025-09-03)

### Key changes from V4.6
- Introduced Novelty dial (Common / Balanced / Rare) to control vocabulary frequency
- Novelty bias as safeguard against high-frequency poetic attractors
- All previous anti-repetition and register rules retained

### Test observations
V4.7 was stress-tested with 50 fragments × 4 columns (200 total) at Rare novelty and high lexile/literary register. The test revealed that while column-level guardrails held, **adjective stems remained a persistent weak point**: velvet, honeyed, jeweled, gilded, and covenant cycled across the wishes and temptation columns. The analysis termed this the 'velvet problem' and identified the underlying mechanism as high-frequency poetic attractors in the model's training data. This stress test directly motivated the V4.8 rewrite.

The "2 pass audit" described in this version's title and instruction set was subsequently discovered during v0.49.1 testing to describe a capability the system could not technically execute. The language implied an internal draft → audit → repair → output process; in practice no such multi-pass verification occurred. See v0.49.2 and the Audit Hallucination incident document [Cite GitHub Data] for full documentation.

---

## V4.8 — Scaling Fix and Onboarding Revision

**Status:** Full instruction set preserved  
**Date:** 2025-09-04

### Key changes from V4.7
- Adjective stem quota per run: no single descriptor more than 2× across the whole table
- Semantic partitioning between semantically close anchors
- Revised onboarding flow with anchor framing built in
- Scaling logic for high fragment counts

### Notes
V4.8 was the final version under the legacy numbering system. A V5 was planned on the same day but was immediately reconceptualised as v0.49 under a new beta numbering scheme, reflecting a shift from rapid iterative patching to a more considered pre-release development approach.

---

## Naming Protocol Transition

Beginning with version 0.49, the Divergence Engine adopted a beta scale (0.xx) for version numbering. This shift reflects the system's experimental, iterative status during the research period. Versions V1–V4.8 remain archived under their original labels for historical continuity. The 0.xx series tracks incremental refinements toward a stable v1.0 release.

---

## v0.49 — Beta Baseline

**Status:** Full instruction set preserved  
**Date:** 2025-09-04

### Key changes from V4.8
- Adopted beta versioning scale
- Introduced anchor suggestion mode: system proposes anchors when user provides a steered brief without specifying domains
- Default parameter configurations formalised
- All V4.8 rules and guardrails carried forward

### Known issues
Initial implementation introduced a regression: anchor partitioning and ratio/POS quotas were not consistently enforced. Corrected in v0.49.1.

---

## v0.49.1 — Corrective Patch

**Status:** Full instruction set preserved  
**Date:** 2025-09-04

### Key changes from v0.49
- Restored anchor partitioning (outputs had been merging across columns)
- Reapplied hard ratio (40/40/20) and POS quota enforcement
- Patch release — no new features, purely corrective

---

## v0.49.2 — Cleaned Instruction Set

**Status:** Full instruction set preserved  
**Date:** 2025-09-04

### Key changes from v0.49.1
- Removed internal audit and repair language introduced in V4.7 following the discovery that the described capability was a hallucination. The system had been narrating a multi-pass verification process it could not technically perform. The discovery was made through sustained observation of persistent output failures that should not have survived a genuine audit, and confirmed through direct challenge to the system. This incident prompted a redesign of the repair pass as a user-initiated second prompt rather than an internal pre-output check. Full documentation of the incident is available in the research archive [Audit Hallucination incident](https://github.com/weswickham/divergence-engine-research/findings/DE-FIND-002-audit-hallucination.md)
- Added stem-family enforcement rules
- Hard quotas for fragment ratios formalised
- Structural similarity detection introduced

[See V4.7 entry](#v47--anti-repetition-and-audit-language)


### Test observations
Tested with wish granting / strange technologies / adventure anchors + absurd-everyday disruptor. Analysis noted the engine was "behaving closer to spec" with improved column partitioning and disruptor contrast. Persistent issues: ratio balance still soft (almost all outputs were two-word sparks), verb representation below 20% target.



---

## v0.49.3 — Quota Enforcement and Stem Caps

**Status:** Full instruction set preserved  
**Date:** 2025-09-04

### Key changes from v0.49.2
- Strengthened quota enforcement mechanisms
- Added stem-family caps as hard constraints
- Disruptor suggestion clamp added (preventing engine from over-steering disruptor choice)

### Test observations
Tested with same anchor set, literary × comic-book register. Showed improved structural variety but identified further refinements needed for forecast mode and family prediction.

---

## v0.49.4 — Forecast Mode and Recompiled Build

**Status:** Full instruction set preserved  
**Date:** 2025-09-04  
**Note:** This is the version referenced as the primary experimental instrument in the journal article. Still active as of March 2026.

### Key changes from v0.49.3
- Integrated Forecast Mode: system surfaces predicted semantic families per anchor before generation, allowing user to set caps and forbids
- Family caps enforced as hard stop-points during generation
- Complete recompiled build incorporating all 0.49.x refinements
- Layered internal instructions governing output behaviour alongside user-facing steering controls
- Parameters available: novelty, register, parts-of-speech constraints, repair pass function

### Architecture at this version
The instruction set comprised approximately 900 words of structured rules covering: personality layer, purpose statement, onboarding flow (brief → anchors → disruptors → tuning dials → format/quotas), generation rules (fragment ratios, POS quotas, family caps, anti-repetition), repair mode protocol, and operating principles.

### Full instruction set
Available as supplementary material: see `instructions/DE_v0.49.4_ChatGPT.md`

---

## v0.49.5 — Forecast Boosts and Hard Stop-Points

**Status:** Full instruction set preserved  
**Date:** Between 2025-09-04 and 2025-11-02 (in use by the Genie/Temptation experiment session of 2025-11-02)

### Key changes from v0.49.4
- Forecast Mode enhanced with "boosts" (ability to amplify specific semantic families)
- Hard stop-points added to onboarding flow (preventing the engine from skipping configuration steps)
- Personality layer refined to include explicit research context framing
- Gate tokens introduced to enforce sequential onboarding progression

---

## v0.49.6 — Session Summary Function

**Status:** Instruction set preserved in GPT Builder  
**Date:** Between 2025-11-02 and 2025-12-17 (in use by the typographic collage experiment session of 2025-12-17)

### Key changes from v0.49.5
- Added built-in session summary function: engine can generate a structured summary of the brainstorming session on request
- Summary format covers: brief, anchors, disruptors, tuning settings, family controls, repair passes, output counts, and integrity checks
- This feature enabled more consistent session documentation, producing the standardised session record format used in later experimental work

### Notes
v0.49.6 is the current working version deployed in the ChatGPT Custom GPT. The session summary function was a significant quality-of-life addition for the research process, reducing the documentation burden that had been identified as a persistent challenge throughout development.

---

## Claude Adaptation

**Status:** Adapted instruction set preserved  
**Approximate date:** [To be confirmed]  
**Platform:** Anthropic Claude

### Summary
A Claude-optimised version of the Divergence Engine instructions was created by having Claude interpret the ChatGPT Custom GPT instruction set and recompile it for Claude's architecture and interaction patterns. This adaptation was used for supplementary testing sessions to examine whether output behaviours observed with ChatGPT were model-specific or generalisable across LLM platforms.

### Full instruction set
Available as supplementary material: see `instructions/DE_v0.49.4_Claude.md`

---

## Development Process Note

The Divergence Engine was developed through a process the researcher terms "vibe prompting" — an extended collaborative dialogue in which ChatGPT co-authored its own instruction set through iterative testing, diagnosis, and refinement. The full development transcript (approximately 70,000 words) is preserved as primary evidence documenting the labour, decision-making, and emergent problem-solving involved in building an effective LLM-based creative instrument.

Key characteristics of the development process:
- Instruction refinements were driven by observed output failures rather than predetermined specifications
- Each version responded to specific diagnosed problems (semantic collapse, ratio drift, register inflation, adjective clustering)
- The development transcript constitutes a continuous record of the "development burden" discussed in the associated research: the substantial, largely hidden labour required to make an LLM useful for creative brainstorming
- Not all intermediate versions were preserved as complete instruction sets; some were developed through incremental edits made directly in the GPT Builder interface

---

*This version history document is part of the supplementary research materials for: Wickham, W., Moore, C., & Yecies, B. (forthcoming). [Article title]. Full materials available at [GitHub repository URL].*
