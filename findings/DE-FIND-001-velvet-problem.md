# DE-FIND-001 — The Velvet Problem

---

## Document Metadata

| Field | Value |
|:------|:------|
| **Document ID** | DE-FIND-001 |
| **Document type** | Analytic Finding — Researcher Memo |
| **Date authored** | 2026-03-15 |
| **Finding first observed** | 2025-09-01 |
| **Finding named** | 2025-09-01 – 2025-09-04 |
| **Related documents** | `divergence_engine_version_history.md` / `DE-EXP-001-transcript.md` / `DE-EXP-002-vanilla-transcript.md` |
| **Source transcripts** | conversations-004a.json (GPT development - Divergence Engine research) |
| **Researcher** | Wes Wickham |
| **Institution** | University of Wollongong |

---

## Defining the Velvet Problem

The velvet problem is a term I use to describe the tendency of large language model output to collapse around a single term, phrase, word, or concept that has a strong association — a "high-frequency semantic attractor" — within the model's training set.

The term comes from the word *velvet*, which recurred multiple times during the testing and development of the Divergence Engine when using the conceptual anchor of temptation, richness, luxury, and seduction to generate creative sparks. The word appeared repeatedly across different runs, different sessions, and different versions of the tool — in compound words and phrases that essentially became mix-and-match recycling: *velvet curtain*, *velvet drapes*, *velvet rope*, *velvet snare*, *velvet lure*, *velvet cage*, *velvet appetite*.

The problem is not limited to the word *velvet*. It is representative of the tendency of the model to exhaust high-frequency attractors, tropes, and clichés before producing lower-frequency or more genuinely rare alternatives. The velvet problem has become shorthand in my research for this broader pattern of semantic clustering and collapse.

The same phenomenon was clearly visible in the vanilla dinosaur naming experiment (DE-EXP-002), where the default ChatGPT output was dominated by compound words built from the same small set of components — *jaw*, *fang*, *blood*, *skull*, *maw* — recycled in the same mix-and-match pattern, producing two hundred nominally different outputs that occupied an extremely narrow semantic neighbourhood.

---

## When and How It Appeared

The Temptation/Wishes/Genie anchor set was not an arbitrary test choice. At the time of early DE development (August–September 2025), I was simultaneously developing a creative project exploring the metaphor of generative AI as a devil figure — seductive, tempting, offering easy shortcuts at a hidden cost. The semantic fields of temptation, wish-granting, luxury, and seduction were therefore thematically live and personally resonant, making them a natural choice for repeated test runs across successive DE versions. The anchors Wishes/Temptation/Morals (with Pop-Culture and Mythic-Archetypal disruptors) were used as a consistent test brief across versions V1 through V4.8 and into the early v0.49 series — providing a stable comparative baseline across iterations while stress-testing the tool's output behaviour. This repeated use was what made the velvet problem visible: running the same anchors across multiple versions at increasing fragment counts exposed the pattern in a way that a single run would not have.

Initially the velvet problem was largely invisible. At lower spark or fragment counts — around twenty responses per column — the propensity for repetitive outputs was not obvious. However, at larger output counts, when pushed to fifty or one hundred fragments per column, the issue became visible as the model struggled to produce authentically divergent responses.

The moment of identification is recorded in the development transcript. After running a fifty-fragment test on version 4.5, I flagged the problem directly:

> "I went ahead with a 2nd run and played with the parameters 'just to see' and the results have some good potential but there's a ton of repetition when I asked for 50 responses. Refer to use of Velvet, IOU or the list of rewards in column 3."
> — Wes Wickham, development transcript, 2025-09-01

The tool's own diagnosis of the pattern followed shortly after, when I raised the issue again during version 4.8 testing:

> "I have some results of 4.8 testing — there's lots of repetition creeping back in. 'Velvet' seems to be a VERY popular word."
> — Wes Wickham, development transcript, 2025-09-04

The tool's response to this observation is methodologically significant. ChatGPT diagnosed its own tendency:

> "Not surprising — *velvet* is one of those statistical magnets in the model's training data. When you push for high lexile / literary register, Temptation / desire fields, 50+ fragments per column… the model defaults to 'velvet' as a poetic stand-in for richness, luxury, seduction."
> — ChatGPT (development session), 2025-09-04

This exchange is notable for two reasons. First, it confirms that *velvet* was functioning as a predictable statistical attractor rather than a random occurrence. Second, it illustrates the feedback loop at the centre of the development process: I identified the problem through expert observation, and the tool was then used to help diagnose its own behaviour — a form of metacognitive collaboration that was itself part of the steering burden.

---

## Findings

**The model exhausts high-frequency attractors first.** The tests and investigations revealed that the model will produce common, familiar, and high-frequency responses before expanding into rarer or less predictable territory. The fluency with which the model can produce large outputs initially masks the low diversity. In other words, quantity can look like quality — until you look carefully at what the outputs actually are.

**The model cannot evaluate its own novelty prior to output.** The experiments revealed that the model cannot accurately predict or assess its own output, since the system is producing tokens based on statistical probability. Since it is not sentient and does not truly understand its own outputs, it cannot experience repetition the way a practitioner does. This reinforced for me the sense that I was using a tool rather than working with a self-aware collaborator — despite the temptation to treat it as such. The diagnostic conversation quoted above illustrates this precisely: the tool could explain *why* velvet was recurring, but only after I had already identified the problem. It could not have flagged it unprompted.

**Fixing the velvet problem introduced a new problem.** The experiments and successive versions of the Divergence Engine largely focused on solving the velvet problem. The goal was to limit semantic collapse while simultaneously keeping responses steered and targeted at the specific creative task. However, enforcing rare, novel, or diverse outputs to avoid the velvet problem increased the likelihood of non-useful outputs — responses that tended toward the abstract, the poetic, and the nonsensical. This back-and-forth between limiting the velvet problem and eliciting useful, diverse sparks became central to the development of the tool and to the question of whether LLMs are genuinely useful in this early creative phase of ideation.

**The problem generalises beyond a single anchor.** Once identified with the Temptation anchor, the pattern was predicted to recur across other anchor domains. The development transcript records this explicitly: the model was noted to cluster around stems predictably — "if you pick *food* as an anchor, you'll see 'bread/bread roll/breadcrumb' type echoes." The Temptation anchor was particularly revealing because its associative field — desire, luxury, seduction, transgression — is so richly loaded in literary and creative writing training data, making *velvet* a near-inevitable default at high lexile register.

---

## Development and Steering Costs

Diagnosing and attempting to fix the velvet problem drove a significant proportion of the Divergence Engine's development from version V4.2 through v0.49.3. This constitutes direct evidence of both the development burden and the steering burden as defined in this research: the cognitive and metacognitive labour required to build the tool and to use it effectively.

The primary instrument of that response was the progressive introduction and refinement of tuning dials — parameters governing semantic looseness, reference depth, generality, novelty bias, and style register. These dials served a dual and sometimes competing function. On one side, they were tools for limiting semantic collapse: setting novelty to Rare, capping semantic family clusters, introducing anti-repetition rules, and enforcing stem detection all aimed to push the model away from its high-frequency attractors. On the other side, the same dials had to maintain containment within the brief — because pushing too hard toward rare and novel outputs produced a different failure mode: outputs that tended toward the abstract, the poetic, and the nonsensical, with little actionable value for design brainstorming. The vocabulary register dial was particularly consequential in this regard: a literary or high-lexile register consistently amplified the velvet problem by pulling the model toward ornate, richly associative language — precisely the territory where *velvet* thrived. Managing the tension between these two failure modes — semantic collapse on one side, unanchored abstraction on the other — became the central design challenge of the tool's development and remained unresolved through multiple versions.

The fixes required my own practitioner expertise at every stage: identifying the problem in the first place, diagnosing its structural cause, formulating the appropriate constraints and parameter adjustments, implementing them iteratively, and evaluating whether each adjustment was effective. This was not work the tool could do for itself. See `divergence_engine_version_history.md` for the full version-by-version record of attempted solutions.

---

## Significance for the Research

The velvet problem is the clearest single illustration of the gap between LLM fluency and LLM value in the context of creative brainstorming. The model produced outputs that were formally correct and domain-appropriate — *velvet* is a genuine and appropriate word in the semantic neighbourhood of temptation and luxury — but the repetition collapsed the semantic range that divergent brainstorming requires. High output velocity masked low diversity.

It was my own analysis and expert judgment that identified the issue, surmised its cause, and formulated the various constraints and parameter adjustments that were subsequently built into the instruction set. This episode demonstrates the central and non-delegable role of the human practitioner at the present stage of generative AI development.

This finding connects directly to the broader research argument about why LLM-assisted brainstorming requires sustained expert orchestration rather than simple deployment. Gittelman and Weisberg (2025) distinguish between outputs that appear divergent and the actual cognitive process of Divergent Thinking — the velvet problem is a computational instance of that same gap, where apparent variety masked repetition that only expert evaluative judgment could identify.

---

*Document authored: 2026-03-15*  
*Part of the Divergence Engine research archive — University of Wollongong PhD research, Wes Wickham*
