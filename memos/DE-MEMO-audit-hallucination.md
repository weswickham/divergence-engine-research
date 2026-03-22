# Analytic Memo — Audit Hallucination Incident

**Date written:** 2026-03-23  
**Researcher:** Wes Wickham  
**Related document:** DE-DEV-AUDIT-001_transcript.md  
**Related versions:** v0.49.1 → v0.49.2 (2025-09-04)

---

*TODO: Add discussion of tool affordances. Add Yampolskiy citation — 'can prompt themselves better than we can.'*

I was faced with the issue of repetitive outputs that kept circling common attractors and tropes and repetitive language outputs. I was attempting to mitigate this by developing guardrails in parameters to constrain and control the output. Pushing it into useful divergence.

A strategy employed throughout the build process was based on the observation by Roman Yampolskiy ("Roman Yampolskiy: These Are The Only 5 Jobs that Will Remain In 2030 & Proof We're Living In a Simulation!" 2025), which is LLMs are often better at generating their own prompts than we are. Therefore a collaborative build process was used — querying the tool about its capabilities and developing the Divergence Engine step-by-step and version by version, as limitations and capabilities were uncovered and tested.

Part of this conversation, or development journey, was a discussion that happened around a concept of building in a repair pass into the system. ChatGPT suggested that it could run an internal audit repair on its output to trim repetitive outputs prior to giving me the output. Language was developed around this process and added to the custom GPT instructions and yet I continued to see the same problem (now referred to as the velvet problem). A day or so later and across 2 iterations of working with the tool instructions, I finally realised that ChatGPT was hallucinating its own capabilities when it became obvious that the audit pass was having no appreciable effect. I challenged ChatGPT on this and got some clarification. "That language ('draft → audit → repair → output') was part of the **design fiction we wrote into the instruction set** back in v4.7–4.8. It's a *procedural metaphor*, not a true multi-pass check."

Of course, it was never a 'design fiction written as a procedural metaphor': ChatGPT had assured me it was capable of the capability until I discovered otherwise. The post-rationalisation is another tendency of LLMs that makes it complicit in justifying its own mistakes.

This highlights the challenges of working with LLMs and an affordance issue. The tool itself has uncertain capabilities that need to be tested and verified by the user. Yet, the tool can (and will) fabricate descriptions of its own capabilities, which can make understanding the true workings and capabilities of this black box technology even more difficult to assess.

In this case, what should have been obvious to me finally became clear: a LLM cannot predict what it will actually output, since it is a predictive system of outputs. It is not aware of what it will output until it already has done so. This realisation and the hallucination incident was the provocation to implement the current repair pass strategy for the DE. The instructions now tell it to review the output it has created and then remove and replace outputs that do not comply with the instructions (repetitions, parts of speech, verb-noun balance etc — refer to the instruction parameters).

---

*Part of the Divergence Engine research archive — University of Wollongong PhD research, Wes Wickham*
