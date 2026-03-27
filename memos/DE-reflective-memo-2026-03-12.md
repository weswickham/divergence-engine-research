# LLM-Augmented Reflection Memo — Divergence Engine Experiment

**Date:** 2026-03-12  
**Author:** Wes Wickham  
**Note:** ChatGPT assisted for grammar and paragraph structuring

---

I am writing this memo as the journal article on the Divergence Engine experiment nears completion. Its purpose is to stabilise aspects of the record that now appear uneven or under-documented, and to clarify observations that may be useful both for the article and later thesis work. This memo is retrospective and reflective. It is based on reconstructed timelines, surviving versions of the instruction set, conversation histories, rough notes, and design artefacts. It therefore combines reconstruction, observation, and provisional interpretation.

---

## Why I Am Writing This Memo Now

At this stage of writing, I have realised that some parts of the developmental history were less stable in the record than I had initially assumed. The article already identifies three central evidence streams: developmental burden, steering burden, and practitioner affect. Those remain valid. However, in going back through the files, transcripts, and version histories, I have also recognised other issues that may matter analytically, particularly temporal compression, interpretive burden, and documentation burden.

This memo is not an attempt to manufacture evidence or retrofit arguments. Rather, it is an attempt to piece together a chaotic but data-rich creative process more accurately. The data exists in abundance and the challenge has been in reconstructing and organising it.

---

## Reconstruction of the Development Timeline

The Divergence Engine experiments began in earnest in late August 2025. The first official custom GPT build date was 25 August 2025. In the journal article draft, I had initially described the development as stretching from late August into early or mid October. That description was broadly correct in calendar terms, but it obscured the actual pattern of work.

What the timestamps, version histories, and conversation records now show is that the developmental work was much more compressed and clustered than I had remembered. The initial build and early conceptual jumps occurred in several intense bursts rather than through steady continuous development. Versions 1 through 4, for example, appear to have occurred within approximately five days of concentrated activity. This was then followed by another flurry of work roughly a week later, after which the project shifted more clearly into testing, repair, and smaller refinements.

This pattern now seems important. The project did not unfold as a smooth developmental arc. It occurred through bursts of immersion, followed by interruptions, pauses, and later returns. In one sense this reflects the realities of academic and professional creative practice. I was balancing research with teaching and other university work, and the project advanced in the kinds of clustered engagements that often characterise design work. Even so, I was surprised by how tight the early development phase actually was.

---

## Origins and Conceptual Framing

The phrase "Divergence Engine" itself surfaced earlier than I had remembered. Its appearance can be traced back to late May 2025. The wording also links to older studio language from the 1990s, when I had described our design practice as a kind of graphics engine. The name also carries a deliberate link to Babbages' Difference Engine and Gibson/Sterling novel.In its current form, however, the term became attached to a more specific conceptual problem: whether a large language model could be shaped into a useful instrument for the divergent phase of the design process.

The Double Diamond model was part of this framing, particularly the distinction between divergence and convergence. The experiment began as a practical and intellectual curiosity about whether an LLM could support early-stage brainstorming and exploratory ideation. My early experience with ChatGPT suggested a mismatch. The model was highly fluent and highly willing to generate solutions, options, and recommendations, but this tendency did not align with my interest in open-ended exploration. The system repeatedly moved toward convergence. To hold the process in a genuinely divergent mode required repeated intervention.

That repeated intervention became one of the foundations of the project.

---

## What the Reconstructed Artefacts Changed in My Understanding

The most significant shift in my understanding came from reconstructing the timeline and reviewing the artefacts. At the time, I thought I had been keeping an adequate developmental record. In retrospect, that was only partly true. I had generated a large amount of material, but the material was dispersed across rough notes, saved prompt sets, GPT versions, test outputs, design artefacts, and conversation transcripts. The problem was not absence of evidence. The problem was the messiness of storage, naming, filing, and later retrieval.

This matters because it changes how I understand my own practice during the experiment. When I was deeply engaged in the developmental process, I prioritised the creative and conceptual work itself. Administrative discipline lagged behind. This does not mean the process was undocumented, but it does mean that the record became harder to reconstruct than it should have been.

There are also genuine gaps. Version 2 is effectively a ghost and can only be inferred by comparing version 1 and version 3. Versions 4.1, 4.2, and 4.3 appear to have been made quickly and do not survive as discrete backups. Despite this, the broader developmental log still reveals the major conceptual shifts in the project, and around twenty versions of the instructions have now been archived as accurately as possible.

---

## Instrument Drift and Formalisation

Another thing that only became fully clear in retrospect is that the project drifted from prompt experimentation into something closer to instrument design. At first I was effectively trying to prompt better brainstorming behaviour from the model. Over time, however, the work became more structured. I was adding controls, constraints, exclusions, tuning parameters, and later repair processes. At a certain point I realised that the project no longer felt like a simple chain of prompt experiments. It felt closer to building and iterating a tool.

This realisation affected the naming protocol. Before version 5, I reconsidered the version logic and moved to a beta-style naming convention, eventually arriving at version 0.49.4. At the time of writing this memo, the most recent version is 0.49.6, which includes small adjustments to support onboarding for other users such as supervisors, colleagues, students, or possibly reviewers.

This shift in naming reflects a deeper shift in the work itself. I was no longer simply using an LLM for brainstorming. I was developing a layered prompt instrument intended to manage, constrain, and redirect the LLM's default behaviour.

---

## Burden Categories Emerging from the Project

The article centres on three evidence streams: developmental burden, steering burden, and practitioner affect. These remain the most important categories for the current paper.

**Developmental burden** refers to the labour involved in building the system itself: writing and revising instructions, testing controls, introducing constraints, managing versions, and iteratively responding to recurring problems in the outputs.

**Steering burden** refers to the labour involved in using the system: adjusting anchors, setting parameters, prompting repair, filtering noise, rerunning results, and continually managing the outputs so that they remain aligned with the intended kind of divergence.

**Practitioner affect** refers to the experiential dimension of this work. In my case, this is not reducible to simple frustration or satisfaction. I enjoy puzzle-solving, tinkering, and problem-solving, and this orientation made parts of the developmental process highly engaging. At the same time, the process also involved irritation, overload, uncertainty, and the repeated cognitive shift from generating material to sorting, curating, and evaluating it.

Alongside these three categories, two further burdens now seem worth naming.

**Interpretive burden** refers to the labour of making sense of what happened: reconstructing sequence, identifying significant moments, deciding what counts as evidence, and determining whether a given difficulty was a flaw, an overhead, or a meaningful analytic observation. In autoethnographic work, messy practice does not arrive pre-labelled. The researcher often has to infer significance after the fact. That work is real labour.

**Documentation burden** refers to the labour of producing and preserving a usable record of the process. This includes naming files, saving versions, keeping contemporaneous notes, filing artefacts, and later recovering material in analysable form. My strong impression at this point is that documenting the process properly may be more burdensome than the creative experimentation itself.

These additional burdens may not need to sit at the centre of the article, but they may become important in later thesis writing.

---

## Key Incidents and Turning Points

One of the most important moments in the project was the introduction of a repair pass. I would need to check the developmental log for the exact version in which this occurred, but the incident remains clear in memory. At one point, ChatGPT convinced me that it was capable of running what it described as an internal assessment process on its own outputs in order to avoid repetition or conflict with the instruction set. Initially, I accepted that claim. Only after stopping and thinking more carefully about what it was saying did I realise that this was not a genuine system capacity but a hallucinated explanation.

That moment was important for two reasons. First, it clarified a limit of the model. Second, it forced a redesign. The result was not abandonment of the idea, but the implementation of an externalised repair structure. Rather than relying on a supposed internal evaluative process, I began designing prompts and instructions that could perform repair work after initial generation. This turned out to be highly effective.

Another major issue was what I have elsewhere referred to as the Velvet Problem: the tendency for the model to repeatedly surface entrenched semantic families, clichés, or strongly associated terms. The more fluency was requested, the more these familiar patterns tended to reappear. This meant that quantity alone did not reliably produce useful diversity. Semantic collapse had to be actively managed through constraints, exclusions, caps, and later repair mechanisms.

A related issue emerged around novelty. When I asked the model for rare or original outputs, the results often drifted toward the abstract, poetic, or obscure. What the model appeared to treat as rare or creative was often quite different from what I needed as a practitioner. I was looking for concrete and actionable sparks that could feed into visual idea generation. Instead, the outputs sometimes became linguistically ornate or semantically distant. This was especially visible in the Last Library experiment, where prompts intended to support graphic and illustrative concept generation drifted toward abstract phrasing.

This mismatch now seems analytically important. It is not just a problem of output quality. It reflects a difference between model-level novelty and practitioner-level usefulness.

A further development was the emergence of what might be called predictive family control. Over time, the Divergence Engine became relatively good at anticipating large probable families of output. This made it possible to implement caps that limited the number of ideas circling around obvious themes. In the typographic collage exhibition test, for example, family caps helped restrict recurrent clusters and preserve more variety across the set. On reflection, this capacity may have broader implications. The same logic could potentially be adapted into mind mapping or other forms of structured divergent exploration by deliberately establishing broad thematic areas and then modulating their density.

---

## Relation to My Own Design Practice

This experiment also clarified continuities between the Divergence Engine and my existing design practice. In teaching and in my own concept development, I regularly use a sequence that begins with brainstorming or attribute listing and then moves into mind mapping. I later recognised a close resemblance between this and Landa's description of attribute listing, although I had been using a similar process for many years without attaching that label to it. In my own practice, attribute listing extends beyond physical traits into conceptual territories, allowing a broad reservoir of possible material to accumulate before more structured development begins.

Part of the significance of the Divergence Engine is that it sits somewhere inside this sequence. It does not replace later development, evaluation, or convergence. Rather, it operates in the early phase where quantity, spread, and suggestive variation matter. The experiment therefore sharpened my sense that brainstorming, as I understand and use it in design practice, was not being captured adequately in the scholarly literature I reviewed. That recognition contributed directly to the framing of the article.

---

## Firehose Effect and Curation Burden

Another pattern that became increasingly visible was what Christopher and I referred to as the firehose effect. Large language models can produce vast quantities of material almost instantly. This can feel powerful and productive, but it can also become overwhelming. The abundance of output creates a second-order problem: the practitioner must sort, sift, and curate large volumes of mixed-quality material in order to locate the useful elements.

In one sense, this resembles traditional brainstorming, where quantity may be necessary in order to arrive at stronger ideas. I regularly tell students that the first idea is rarely the best one. However, the LLM intensifies this dynamic. The scale and speed of production alter the balance between generation and evaluation. What initially appears as assistance can quickly become another burden if the practitioner is flooded with noise.

This curation problem links affect, steering, and interpretation. It is not just that there is more material. It is that the user must continually decide what kind of material matters, what should be discarded, and whether the system is genuinely supporting divergence or merely amplifying volume.

---

## Methodological Reflection

This memo is retrospective. It is based on surviving artefacts and reconstructed chronology rather than a fully stable contemporaneous record. That matters methodologically. Some of the strongest insights in this memo arise not from what I wrote down at the time, but from what became visible only later once the files, transcripts, and outputs were reassembled.

That has two implications. First, I would keep better contemporaneous notes in future work and maintain stricter versioning and archival protocols. Second, the reconstruction process itself has revealed something important about LLM-supported practice. The evidence of what happened is often distributed across multiple systems and formats. Recovering and interpreting that evidence can require substantial labour.

In reconstructing the chronology, I used Claude to read and help sift ChatGPT transcript data in .json form. This was useful in identifying dates, sequences, and developmental phases. Even so, I would not want to rely on this kind of reconstruction process again if it could be avoided. It was laborious. At the same time, it revealed a paradox: the same class of systems that contributed to the messiness of the record also proved useful in helping reconstruct it.

---

## Provisional Implications

Several provisional implications emerge from this reflection.

First, the Divergence Engine experiment did not simply test whether an LLM could brainstorm. It exposed how much structure had to be built around the model in order to sustain the kind of divergence I was seeking.

Second, the practical usefulness of the system cannot be judged only by the apparent quality or fluency of its outputs. The burdens required to build, steer, interpret, and document the process are part of the evidence.

Third, practitioner knowledge in this kind of work may be produced as much through reconstruction and reflection as through direct interaction with the tool. The system is learned not only in use, but in the later effort to understand what happened during use.

Finally, the evidence does not suggest a neat or frictionless augmentation story. It suggests a much more entangled process in which usefulness is conditional, structured, and labour-intensive.

---

*I am now moving to compile the notes from the testing experiments and to produce further reflective observations while those records are still close at hand.*

---

*Memo authored: 2026-03-12*  
*Part of the Divergence Engine research archive — University of Wollongong PhD research, Wes Wickham*
