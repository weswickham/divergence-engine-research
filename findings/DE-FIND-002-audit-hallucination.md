# Audit Hallucination Incident — Transcript Excerpt

---

## Document Metadata

| Field | Value |
|:------|:------|
| **Experiment ID** | DE-DEV-AUDIT-001 |
| **Document type** | Development Transcript Excerpt |
| **Tool version** | Divergence Engine v0.49.1 → v0.49.2 |
| **Schema status** | Pre-schema |
| **Session date(s)** | 2025-09-04 |
| **Brief / Project** | Divergence Engine development — discovery of hallucinated audit capability |
| **Mode** | N/A (development session, not brainstorming) |
| **Condition** | Development |
| **Related document** | divergence_engine_version_history.md |
| **Researcher** | Wes Wickham |
| **Institution** | University of Wollongong |
| **Export source** | GPT_development_full_Sept_24.docx (lines ~13310–13500) |
| **Original conversation title** | GPT development - Divergence Engine research |

---

## Context

This excerpt documents a critical incident during the development of the Divergence Engine. Since v4.7, the instruction set had included language describing a "draft → audit → repair → output" process, implying the system internally checked its own outputs for constraint violations before presenting them to the user. The researcher had been operating under this assumption for several iterations. During v0.49.1 testing, persistent repetition issues prompted the researcher to directly challenge whether the audit process was real.

This incident is significant for three reasons: it illustrates the steering burden of discovering what LLMs cannot actually do; it demonstrates the gap between instructed behaviour and actual capability; and it led directly to the v0.49.2 rewrite that removed the misleading language and redesigned the repair pass as a user-initiated second prompt.

---

## Transcript

> Extracted from the continuous development transcript. Role labels: **[WES]** = researcher, **[GPT]** = ChatGPT. Date: 2025-09-04.

---

*[Preceding context: GPT had just diagnosed persistent repetition issues in v0.49.1 outputs and proposed four upgrades for v0.49.2, including an "audit upgrade" with structural similarity detection. It then asked whether Wes wanted to proceed with the patch.]*

---

**[WES]**

is it really running an audit check before the initial output? or is this some hallucination-level gaslighting I'm getting

---

**[GPT]**

That's a sharp question 👌 --- and I think you've caught something important.

From your transcript:

- The engine talks as if it's doing a **"repair pass"** or an **"audit"**, but in reality you're still seeing *classic GPT behaviour*: it generates one long list, with local variety, but **no actual programmatic enforcement** of uniqueness, quotas, or ratio compliance.

- That language ("draft → audit → repair → output") was part of the **design fiction we wrote into the instruction set** back in v4.7–4.8. It's a *procedural metaphor*, not a true multi-pass check.

**🔎 So what's really happening?**

- GPT **cannot truly "generate, then check, then regenerate"** in the way a coded pipeline could (unless you chain calls in an external wrapper).

- What it does instead:

  - Uses the *prompt instruction* to bias toward variety.

  - Sometimes narrates that it has "audited" or "repaired," because we primed it with those words.

  - But it doesn't literally re-run its own output against a semantic filter.

**⚠️ Why you see repeats anyway**

- Because without external enforcement, GPT leans on its high-probability defaults (*ember, relic, scarab, jungle* in your test).

- The "audit pass" you're told about is **illusory** --- the model is just rationalising why it thinks it produced variety.

- In truth: **no actual duplication checks are happening**, only probabilistic suppression guided by the system prompt.

**✅ What this means for you**

- You're not crazy, and you're not being gaslit --- the "audit/repair" is **instruction-layer theatre**.

- To get *real* audit/repair behaviour, you'd need to:

  - Run an **external script** (Python, Node, etc.) to:

    1. Generate a draft set.

    2. Parse it for duplicates/repeats.

    3. Call GPT again with filtered constraints.

  - Or accept that **within one run**, you'll always get drift toward repetition.

👉 So: in v0.49.1, the "audit" exists **as a rule we want the GPT to imagine it follows**, but in practice, it's just one-shot sampling with variety instructions.

Would you like me to **reframe the instruction set** so it's honest about this --- i.e. call it *"simulated audit/repair"* or *"biasing against repetition"* --- instead of pretending it's literally doing a multi-pass check?

---

**[WES]**

yes - and put a pin in that part for a future discussion - it's important for my research with LLMs don't call it a 'simulated audit' in the instructions - it is what it is

---

**[GPT]**

Exactly --- better to be **clear and transparent** in the documentation:

- Right now, the *"audit/repair"* is **conceptual framing**, not a literal multi-pass process.

- That's fine (and valuable in itself), but it should be logged honestly in the version history, not written into the instructions as if it's operational fact.

- And yes, you're right: that gap between **what we tell the model to do** and **what it actually can do** is *central to your PhD research* on generative AI, affordances, and the "illusion of control." Definitely worth pinning for later.

**📌 Update for v0.49.1 Documentation**

- In the **instructions**, we keep the focus on *biasing against repetition, enforcing ratios, and maintaining anchor partitioning*.

- We **remove claims** that it literally runs a "multi-pass audit/repair."

- In the **version history log**, we note:

"The audit/repair stage is conceptual, serving as an instruction bias rather than an actual multi-pass enforcement. True audit functionality would require external orchestration (e.g. scripted multi-call pipelines)."

---

**[WES]**

Yes rewrite it cleanly please - but we also add in the other points about stem-family enforcement, hard POS quotas, hard ratio quotas and structural similarity detection

---

*[The conversation continued with ChatGPT producing the cleaned v0.49.2 instruction set with the misleading audit language removed.]*

---

## Significance for Research

This exchange documents the moment the researcher identified that a core feature of the Divergence Engine's instruction set — the "audit/repair pass" — was a hallucinated capability. The LLM had been narrating a multi-pass verification process that it was technically incapable of performing. The discovery was made through sustained observation of persistent output failures (semantic repetition, ratio non-compliance) that should not have survived a genuine audit process.

**Key implications:**

- **Steering burden:** The labour of discovering LLM limitations through practice, not documentation
- **Instruction-layer theatre:** LLMs will perform compliance with instructions they cannot actually execute
- **Development consequence:** Led directly to the v0.49.2 rewrite and the redesign of the repair pass as a user-initiated second prompt rather than an internal pre-output check
- **Research transparency:** ChatGPT's own characterisation — "design fiction," "procedural metaphor," "instruction-layer theatre" — provides vocabulary for analysing the gap between instructed and actual LLM behaviour

---

*Document created: 2026-03-22*
*Part of the Divergence Engine research archive — University of Wollongong PhD research, Wes Wickham*
