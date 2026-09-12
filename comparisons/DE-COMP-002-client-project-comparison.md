# DE-COMP-002 — Early Start Publishing: ChatGPT vs Claude Platform Comparison

---

## Document Metadata

| Field | Value |
|:------|:------|
| **Document ID** | DE-COMP-002 |
| **Document type** | Platform Behaviour Comparison — Researcher Reflection |
| **Date authored** | 2026-03-15 |
| **Related experiments** | DE-EXP-006 (ChatGPT v0.49.6) / DE-EXP-007 (Claude v0.49.4c) |
| **Brief** | Naming and identity for Early Start publishing company |
| **Researcher** | Wes Wickham |
| **Institution** | University of Wollongong |

---

## Methodological Note

This document compares two sessions run on the same brief on the same day across two different platforms — ChatGPT (DE v0.49.6) and Claude (DE v0.49.4c). These are not controlled experimental conditions: the anchor sets differed across some runs, parameter settings varied, and the number of runs differed (3 vs 4). This was a deliberate reflection of genuine design practice — following the brief as it developed, responding to outputs as they arrived. The sessions are therefore not directly comparable in a quantitative or scientific sense, and no claim is made that they are. The value of this comparison lies in the platform behaviour observations it surfaces, consistent with the autoethnographic methodology underpinning this research.

---

## Output Character

The two platforms produced outputs with noticeably different textures. ChatGPT outputs tended toward concrete, noun-based words and phrases that are more immediately interpretable as visual or identity material. Examples from the Childhood Perspectives anchor — *chalk galaxies*, *playground republic*, *mud architects*, *cardboard telescope*, *fort architect* — have direct visual purchase and suggest design directions without requiring additional interpretive work.

Claude outputs, by contrast, tended toward the literary and conceptual. Fragments like *ask again*, *chapter without end*, and *woven memory* are interesting but require an additional layer of cognitive translation before they become actionable identity sparks. Claude's outputs were often either too abstract, too verb-heavy, or — at the opposite end — entirely predictable and flat.

That said, some of the most genuinely interesting sparks in the entire session came from Claude's Child & World anchor: *pocket world*, *paper map*, *pocket-sized*, *named work*. These resonate with the brief's core concepts of curiosity, exploration, and new-found understanding in a way that feels earned rather than generated.

ChatGPT outperformed Claude in spark-to-noise ratio across the early runs. This is largely attributable to the concrete, noun-forward output character that the ChatGPT instruction set produces more reliably at this stage of the DE's development.

---

## Onboarding Behaviour

The onboarding experience differed between platforms in ways that reflect deeper differences in how each model interprets the instruction set. ChatGPT followed the onboarding protocol step-by-step, presenting options in sequence and waiting for input at each gate. It functions more like a piece of software in this regard — literal, precise, and adherent to the instruction set unless prompted otherwise. The v0.49.6 version also includes the supervisor-friendly experience mode selection (Introductory / Intermediate / Advanced) at the start of the session.

Claude, by contrast, presented the onboarding through a pop-up interface with selectable options — an interpretation of the instruction set rather than a literal execution of it. This is more conversational but less predictable. I also noticed that Claude did not offer the predicted semantic family forecast — the step where likely families per anchor are surfaced so the researcher can set caps and forbids before generation. This is a gap in the v0.49.4c Claude adaptation that needs to be reviewed. It is possible that elements of the onboarding sequence present in the ChatGPT version were not fully carried across in the adaptation.

---

## Repair Pass Behaviour

The repair pass system appeared more robust and explicit on Claude. Rather than a brief summary of changes, Claude produced a detailed violation log in Run 2 — naming each overrun family, the number of instances, and the resolution applied, with ~40 replacements documented. This transparency is useful from a research documentation perspective and is itself interesting archival evidence of platform behaviour.

However, Frankenstein constructions — where words or phrases are recycled and conjoined with other words to produce outputs that technically comply with anti-repetition rules while delivering the same semantic outcome — were still present in Claude outputs despite the more verbose repair pass. This raises the question of whether the repair pass is genuinely detecting and resolving semantic repetition, or merely satisfying formal structural constraints while leaving the underlying problem intact.

---

## Unsolicited Commentary

Claude offered unsolicited qualitative commentary on its own outputs throughout the session — noting register tensions, diagnosing why certain outputs were landing poorly, and suggesting parameter adjustments. For the most part these observations were accurate and useful: the diagnosis of the register/depth conflict in Run 3 was directly actionable and led to a qualitatively better Run 4. 

However, I would note that both ChatGPT and Claude consistently overestimate the usefulness of their own outputs. Both platforms described their outputs enthusiastically and cheerfully offered options for further improvement. This self-promotional tendency — the tool narrating its own performance in positive terms regardless of actual output quality — is worth noting as a practitioner experience observation. Over time, the unsolicited commentary from Claude risks becoming distracting and somewhat patronising, particularly as familiarity with the tool increases.

---

## Steering Burden

Claude required slightly more intervention and steering than ChatGPT across this session. It took four runs before outputs began to approach the quality and spark-to-noise ratio I was seeing from ChatGPT, and progress depended on a diagnostic conversation that identified register/depth interaction as the problem. The first three Claude runs yielded too much noise and insufficient actionable material.

This difference reflects how differently the two models interpret the same instruction architecture. What v0.49.6 on ChatGPT has been tuned to produce: concrete, noun-forward, visually grounded fragments, does not emerge automatically from Claude running v0.49.4c. The novelty and abstraction parameters are interpreted differently, and the register settings interact with depth settings in ways that require practitioner expertise to navigate. By Run 4, the outputs were beginning to converge on the quality level I associate with ChatGPT performance — similar character, different vocabulary.

---

## The Disruptors Question

I independently flagged the disruptors parameter as ineffective in both sessions. The disruptor concept was established in early DE versions as a mechanism to inject unexpected semantic material and to jar the model sideways from the anchor domains. In practice, the disruptor column functions as little more than an additional anchor column with a different subject. It is not doing what it was designed to do.

This is a structural issue with the current instruction set rather than a platform-specific problem. Both models exhibit the same behaviour. The disruptor mechanism requires fundamental rethinking and possibly a full rewrite of the relevant section of the instruction set. This is flagged as a development priority but is outside the scope of the current research period.

---

## On the Lack of Controlled Conditions

I did pause during these sessions and consider whether I should be using identical parameters and anchors across both platforms to enable a more controlled comparison. On reflection, I decided against it, and that decision is itself consistent with the methodology. This research is firmly autoethnographic and situated in lived design practice. My developing expertise with the tool is part of the evidence, not a confounding variable to be controlled away. The slightly different approaches across platforms open up additional areas of investigation rather than compromising the findings.

That said, if I run this brief again in a future session (which I expect to do as the Early Start project develops), I will be more deliberate about establishing matched anchors and parameters. Not to produce a benchmark ranking, but to give myself cleaner evidence about how the two platforms perform on the same brief. The distinction matters: I am not evaluating platform performance for its own sake, but examining the practitioner experience of using these tools in creative design work.

---

## Research Argument

The sessions reinforced several existing findings, particularly around the velvet problem and steering burden. But they also surfaced something I want to examine more carefully: the relationship between the velvet problem and Frankenstein constructions.

The velvet problem describes the model defaulting to high-frequency semantic attractors: in which is the cycling through the same words and concepts regardless of instruction. Frankenstein collisions describe a different failure mode: recycled words and concepts being conjoined with other material to produce outputs that technically satisfy the anti-repetition rules while delivering the same narrow semantic outcome. The DE's development has largely focused on negotiating between these two patterns: pushing the model away from velvet-problem attractors while simultaneously preventing it from circumventing the rules through Frankenstein collisions. It is worth asking whether these are the same problem in different forms, or genuinely distinct failure modes that require different solutions.

Finally, one observation that resists easy categorisation: my own limitations in the domain of language. The DE is a tool centred on linguistic production, and a significant proportion of its parameter architecture deals with things like verb-to-noun ratios, parts of speech, lexical register, and figures of speech. My expertise is in visual communications, not linguistics. I find myself wondering whether someone with stronger grounding in language such as an English scholar, a writer, or a linguist might develop and evaluate this tool more rigorously than I can. This is not a methodological flaw, but it is an honest limitation worth acknowledging, and one that points toward possible future collaborative or interdisciplinary directions for this research.

---

*Document authored: 2026-03-15*
*Part of the Divergence Engine research archive — University of Wollongong PhD research, Wes Wickham*
