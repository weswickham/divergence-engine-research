# Divergence Engine — Research Archive

**Researcher:** Wes Wickham  
**Institution:** University of Wollongong, Faculty of the Arts, Society and Business  
**Supervisors:** Brian Yecies (primary), Christopher Moore  
**Research context:** PhD Candidate, Design and Visual Communications  
**Archive established:** March 2026  

---

## About This Research

This archive contains the primary evidence materials for a journal article investigating the efficacy of large language model (LLM) assisted divergent thinking in graphic design practice. The research examines the early textual ideation phase of the design process — a phase that precedes visual production and has received little scholarly attention despite widespread practitioner adoption of AI tools.

The central instrument under investigation is the **Divergence Engine**: a custom LLM-based brainstorming tool developed iteratively by the researcher using OpenAI's Custom GPT platform, with a supplementary adaptation for Anthropic Claude. The Divergence Engine was designed to generate raw text fragments — words, phrases, associations, and conceptual sparks — for use as fuel in early-stage design ideation. It is not a solution-generating tool. Its purpose is to support and extend the divergent phase of creative thinking before convergence and evaluation begin.

The research methodology is **analytic autoethnography** (following Anderson, 2006) combined with a grounded theory approach. The researcher's thirty years of professional experience in graphic design and visual communications, and twenty years as a design educator, function as both the research instrument and the interpretive lens. A central methodological commitment is transparency: the full development process is documented in inspectable form here, in contrast to existing LLM creativity studies that typically obscure their methods.

The research examines three evidence streams:

- **Output quality** — whether the tool produces linguistically and conceptually useful brainstorming material, assessed through expert practitioner judgment
- **Process requirements** — the developmental and steering labour required to build and operate the tool effectively
- **Practitioner experience** — whether the tool sustains or depletes creative engagement across sessions

---

## Key Concepts

**The Velvet Problem** — the tendency of LLM outputs to collapse toward high-frequency semantic attractors when an anchor domain carries strong associative weight. Named for the word *velvet*, which recurred persistently across multiple sessions when *Temptation* was used as a brainstorming anchor. See `findings/DE-FIND-001-velvet-problem.md`.

**The Firehose Effect** — the overwhelming volume of output that LLMs can produce almost instantly, creating a secondary curation burden for the practitioner. Term coined collaboratively with primary supervisor Christopher Moore.

**Frankenstein Constructions** — a failure mode in which words or phrases are recycled and recombined to produce outputs that technically satisfy anti-repetition rules while delivering the same narrow semantic outcome as the velvet problem.

**Steering Burden** — the metacognitive labour required to keep the tool producing useful outputs: adjusting anchors, setting parameters, prompting repair passes, filtering noise, and continually managing outputs so they remain aligned with genuine divergent intent.

**Developmental Burden** — the labour involved in building the instrument itself: writing and revising instruction sets, testing controls, managing versions, and iteratively responding to recurring output problems across approximately twenty versions.

---

## Repository Structure

```
divergence-engine-research/
│
├── README.md                          — this file
│
├── instructions/                      — full instruction sets for each DE version
│   ├── DE_v0.49.4_ChatGPT.md         — primary instrument (ChatGPT Custom GPT)
│   └── DE_v0.49.4c_Claude.md         — Claude platform adaptation
│
├── version-history/                   — chronological development record
│   └── divergence_engine_version_history.md
│
├── experiments/                       — raw transcripts and session records
│   ├── DE-EXP-001-transcript.md      — How to Name Your Dinosaur (DE condition)
│   ├── DE-EXP-001-session-record.md
│   ├── DE-EXP-002-vanilla-transcript.md  — How to Name Your Dinosaur (Vanilla condition)
│   ├── DE-EXP-002-session-record.md
│   ├── DE-EXP-003-transcript.md      — The Last Library (DE sessions)
│   ├── DE-EXP-003-session-record.md
│   ├── DE-EXP-004-artefact-record.md — The Last Library (Human brainstorm)
│   ├── DE-EXP-004-session-record.md
│   ├── DE-EXP-005-transcript.md      — Typographic Collage (DE sessions)
│   ├── DE-EXP-005-session-record.md
│   ├── DE-EXP-006-transcript.md      — Early Start Publishing (ChatGPT)
│   ├── DE-EXP-006-session-record.md
│   ├── DE-EXP-007-transcript.md      — Early Start Publishing (Claude)
│   └── DE-EXP-007-session-record.md
│
├── comparisons/                       — cross-condition and cross-platform analysis
│   ├── DE-COMP-001-last-library-comparison.md
│   └── DE-COMP-002-early-start-comparison.md
│
├── findings/                          — named analytic findings
│   └── DE-FIND-001-velvet-problem.md
│
├── memos/                             — reflective and analytic memos
│   └── DE-reflective-memo-2026-03-12.md
│
└── templates/                         — blank documentation templates
    ├── DE-TEMPLATE-transcript.md
    └── DE-TEMPLATE-session-record.md
```

---

## Experiment Index

| ID | Experiment | Condition | Tool version | Date(s) | Sessions |
|:---|:-----------|:----------|:-------------|:--------|:---------|
| DE-EXP-001 | How to Name Your Dinosaur | DE | v0.49.5 Beta | 2025-09-07 – 2025-10-09 | 3 |
| DE-EXP-002 | How to Name Your Dinosaur | Vanilla ChatGPT | None | 2025-09-07 – 2025-09-24 | 2 |
| DE-EXP-003 | The Last Library | DE | v0.49.4 (Partial schema) | 2025-09-20 – 2025-09-24 | 5 |
| DE-EXP-004 | The Last Library | Human brainstorm | None | 2025-09-20 – 2025-09-21 | — |
| DE-EXP-005 | Typographic Collage | DE | v0.49.6 | 2025-12-15 – 2025-12-17 | 2 |
| DE-EXP-006 | Early Start Publishing | DE — ChatGPT | v0.49.6 | 2026-03-15 | 3 runs |
| DE-EXP-007 | Early Start Publishing | DE — Claude | v0.49.4c | 2026-03-15 | 4 runs |

**Note on DE-EXP-006 and DE-EXP-007:** These are supplementary demonstration sessions conducted during the article write-up period and are transparently labelled as such. They were run against a real ongoing design brief — a publishing company identity project — using the fully formalised v0.49.6 schema. They are not retrospective reconstructions.

---

## Comparisons Index

| ID | Comparison | Type |
|:---|:-----------|:-----|
| DE-COMP-001 | Last Library: Human vs DE (ChatGPT) vs DE (Claude) | Cross-condition output comparison |
| DE-COMP-002 | Early Start: ChatGPT v0.49.6 vs Claude v0.49.4c | Cross-platform behaviour observation |

---

## Document Types

Each experiment in this archive consists of two documents:

**Transcript** (`-transcript.md`) — the raw session record. Contains: document metadata, DE-generated session summary log, and the full conversation between researcher and tool. Role labels distinguish researcher input ([WES]) from tool output ([GPT] or [CLAUDE]).

**Session Record** (`-session-record.md`) — the evaluative document. Contains: summary data, process notes, output quality ratings (Likert scale), practitioner affect ratings, spark examples, noise examples, and open reflection. Completed by the researcher following each session. This is the primary evidence document for practitioner experience assessment.

**Artefact Record** (`-artefact-record.md`) — used for DE-EXP-004 (human brainstorm), which produced a physical journal artefact rather than a digital transcript.

---

## Methodological Note

This archive is a core component of the research methodology rather than supplementary material. The decision to make the development process publicly inspectable — including version histories, instruction sets, failed attempts, and reflective memos — addresses a gap identified in existing LLM creativity research, where methods are frequently opaque. The archive is designed to allow any reader to trace the evidence trail from raw session data through to the interpretive claims made in the associated article.

Session records include both quantitative ratings (Likert scales) and qualitative reflection. The quantitative ratings are not intended to produce statistical findings. They function as structured prompts for consistent reflective attention across sessions, enabling pattern recognition across the experiment set.

The researcher's expert practitioner judgment is the primary evaluative instrument throughout. This is consistent with the Colton and Wiggins (2012) computational creativity framework, which requires an expert human evaluator to assess creative output rather than relying on output metrics alone.

---

## Version History Summary

The Divergence Engine developed across approximately twenty versions between August and December 2025, with ongoing refinements continuing into 2026. The core architecture (V1 through v0.49.4) was developed in a twelve-day intensive period (2025-08-24 to 2025-09-04). The full chronological record, including version-by-version changes and the development finding on the Velvet Problem, is available in `version-history/divergence_engine_version_history.md`.

---

## Associated Publications

Wickham, W., Moore, C., & Yecies, B. (forthcoming). [Article title]. [Journal name].

*This repository will be updated with full citation details upon publication.*

---

## Blog Context

Contextual narrative linking to these materials is available at [AAABestPrompts.com](https://aaabestprompts.com).

---

## Licence and Reuse

All materials in this archive are the intellectual property of Wes Wickham. They are made publicly available for academic inspection and peer review in connection with the associated research publication. Any reuse, citation, or reproduction should reference the associated article and this repository.

---

*Repository established: 2026-03-15*  
*University of Wollongong, Faculty of the Arts, Social Sciences and Humanities*
