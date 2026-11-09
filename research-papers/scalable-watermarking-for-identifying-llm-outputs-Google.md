# How Google Hides Watermarks in AI-Generated Writing

> **AI Frontier Lab · Research Readout · Beginner-friendly explanation**  
> **Paper:** *Scalable watermarking for identifying large language model outputs*  
> **Authors:** Sumanth Dathathri, Abigail See, Sumedh Ghaisas, Po-Sen Huang, Rob McAdam, and colleagues (24 authors total)  
> **Organizations:** Google DeepMind and Google  
> **Published:** October 23, 2024, in *Nature*  
> **Paper:** https://doi.org/10.1038/s41586-024-08025-4

## 1. The Big Idea in One Minute

Imagine a student submits an essay, or a job applicant sends a cover letter. Can you tell whether a chatbot generated the words?

**SynthID-Text** is Google's method for putting a **hidden statistical watermark** into text *while an AI model writes it*. The watermark is not a visible logo, unusual font, or secret sentence. Instead, the system subtly changes how the model chooses among possible next words (more precisely, **tokens**). A detector with the appropriate secret key can later look for the resulting statistical pattern.

The headline finding: in a live experiment involving **nearly 20 million Gemini responses**, users rated watermarked and unwatermarked replies essentially the same. The method was also more detectable than comparable earlier techniques in the paper's evaluations.

**Important:** This is a method for detecting a particular watermark, *not* a universal test of whether any text was written by AI.

## 2. What Problem Were Researchers Trying to Solve?

AI chatbots can write convincing essays, product descriptions, answers, emails, and other material. That creates a difficult question: **Where did this text come from?**

Traditional AI-text detectors look at writing style and attempt to guess whether a person or model wrote it. Those guesses can be unreliable. They may incorrectly flag human writing, including writing by people using a second language.

The Google team explored a different approach: **the model producer intentionally adds a hidden signal at generation time**, so detection is based on the signal rather than impressions of the writing style.

### Everyday analogy

A banknote has security features designed into it during production. You do not have to guess whether it is genuine by examining how elegant the printing looks. Likewise, SynthID-Text attempts to make AI provenance checkable through a deliberately inserted signal.

The analogy has limits: a text watermark is probabilistic, may be weakened by edits, and only exists if the model maker actually enables it.

## 3. First, Understand How a Chatbot Writes

A language model does not normally write an entire paragraph in one instant. It generates a sequence of **tokens**, which can be words or pieces of words.

At each step, it calculates probabilities for possible next tokens, then chooses one using a sampling procedure.

For example, consider the unfinished sentence:

> My favorite tropical fruit is ...

An **illustrative** probability list from the research explanation might look like this:

| Possible next word | Probability |
|---|---:|
| Mango | 50% |
| Lychee | 30% |
| Papaya | 15% |
| Durian | 5% |

These are teaching-example numbers, not the measured probabilities of Gemini in ordinary use.

The model can produce more than one reasonable answer. **SynthID-Text uses that flexibility to insert a pattern without needing to add visible characters.**

## 4. How SynthID-Text Adds a Hidden Mark

At a high level, the process has five parts:

1. **Start with a secret key.** The watermarking system holds a secret value.
2. **Look at the recent text.** The method combines the key with recent tokens to generate repeatable, apparently random scores. The narrated example uses the previous four tokens; the precise setup is configurable.
3. **Score possible next tokens.** Candidate tokens receive hidden values based on that seed.
4. **Use tournament sampling.** Instead of choosing directly from the original probabilities, the system uses a tournament-inspired method that subtly favors candidates with certain hidden scores.
5. **Repeat for the whole response.** Each generated token adds a little statistical evidence to the watermark.

### The tournament explained like a game

Imagine drawing eight candidate words, using the model's original probabilities. Pair the candidates against one another:

- Each pair compares its secret scores; the higher-scoring candidate advances.
- The four winners compete in the next round.
- Two finalists remain, and one token wins.

The transcript demonstrates **three rounds with eight candidates**. The paper studies a deeper setup with **30 tournament layers** and uses an efficient mathematical implementation rather than literally simulating an enormous tournament at each token.

The resulting text still uses words the model considered plausible. The key difference is **which plausible option gets selected**.

### Does this mean the output is always unchanged?

No. The *exact words* may differ. The claim is that in the paper's **non-distortionary configuration**, the underlying token probabilities are preserved **on average over random watermark keys**, and real-world quality tests found no meaningful degradation. The paper also discusses a *distortionary* configuration with a different detectability-versus-quality trade-off.

## 5. How Can Someone Detect the Watermark Later?

The detector needs **the text and the correct secret key**. It does **not** need to run the original large language model again.

In simplified terms, it:

1. Reads the token sequence.
2. Reconstructs the secret scores that would apply at each position.
3. Checks whether the selected tokens show the expected preference for high-scoring choices.
4. Combines evidence across the text to calculate a detection statistic.

For text without the watermark, hidden scores should generally behave like random noise. For appropriately watermarked text, a detectable pattern accumulates.

**Longer passages usually give the detector more evidence.** Very short responses are harder to assess reliably.

A detection result is statistical evidence, not guaranteed proof of authorship. A missing watermark also **does not prove** a human wrote the text.

## 6. What Did the Researchers Actually Test?

The researchers investigated three practical questions:

- **Quality:** Does adding the mark make responses less useful or less natural?
- **Detectability:** Can a detector find this mark more effectively than comparable watermarking methods?
- **Efficiency:** Can watermarking operate quickly enough inside a chatbot serving real users?

The research involved the live Gemini system as well as controlled experiments on open models such as Gemma and Mistral.

## 7. Key Result: Nearly 20 Million Gemini Responses

Researchers directed a random selection of Gemini requests to either a **watermarked** or an **unwatermarked** model and compared user feedback.

| User-feedback measure | Difference between versions |
|---|---:|
| Thumbs-up rate | 0.01 percentage points |
| Thumbs-down rate | 0.02 percentage points |

The reported differences were **not statistically significant**. In everyday language, users did not appear to notice a meaningful decline in response quality.

The paper also used smaller controlled human evaluations and automatic benchmarks, which similarly found no significant degradation for non-distortionary SynthID-Text.

**What this does not mean:** It does not guarantee that every possible text or application will be completely unaffected.

## 8. Does It Detect Watermarks Well?

The paper compared SynthID-Text with earlier approaches to generative text watermarking.

Across tested open models and response lengths, the researchers found that SynthID-Text offered **better watermark detectability** than relevant earlier methods, including comparisons at a **1% false-positive-rate setting**.

### What is a false positive?

A false positive means a detector flags text as watermarked when it was not. If a test uses a 1% false-positive-rate threshold, it allows approximately **one false alarm per hundred unwatermarked examples under the test conditions**. It does *not* mean any specific result is 99% certain to be correct.

Detection generally improves with more usable text, while rewriting or other transformations may erase the signal.

## 9. Does Watermarking Slow the Chatbot Down?

The method was designed to impose minimal extra computation. The transcript cites a Gemma setup with approximately **15.5 milliseconds per token** and around **0.5% added slowdown** under the tested conditions.

That number is a measurement from a specific experimental setup, **not a universal speed guarantee** for all models, hardware, or deployments.

The paper also describes how watermarking can work with *speculative sampling*, a technique used to make production language-model generation faster.

## 10. Why Editing Matters

A watermark is attached to statistical patterns in the **generated token sequence**. If the sequence changes, the pattern can weaken.

| What happens to the text? | General implication |
|---|---|
| Original, long watermarked reply | Most favorable for detection |
| Short excerpt | Less evidence is available |
| Small manual edits | May reduce detection strength |
| Significant deletion or rewriting | Can substantially weaken the mark |
| Complete rewrite by another AI model | Particularly challenging for the detector |

This table expresses the overall pattern reported in the research, not guaranteed results for each edited document.

## 11. Other Important Limitations

### Not all AI text is watermarked

A watermark must be enabled by the model's operator. Open-weight or self-hosted models may produce completely unwatermarked text.

### It is not a universal AI detector

Finding one company's watermark does not identify outputs from every other chatbot. Conversely, failing to detect it does not establish human authorship.

### Access to detection is a separate question

A detector needs the relevant key or authorized verification mechanism. Publishing the research or code does not necessarily give everyone access to a private product's detection key.

### False alarms still matter

Even a strong statistical system must be used cautiously, particularly where a mistaken accusation could affect a student's education, an employee's job, or someone's reputation.

### AI-written text can be heavily transformed

Paraphrasing, translation, or other editing can make detection harder. No perfect resilience to all modifications is established here.

## 12. How Is It Different From Traditional AI Detectors?

| Question | Style-based AI detector | SynthID-Text watermark detector |
|---|---|---|
| What does it analyze? | Patterns in how the text is written | An intentionally embedded statistical pattern |
| Must the generator cooperate? | No | Yes; watermarking must be enabled |
| Can it assess arbitrary AI text? | It may attempt to | Not unless the relevant watermark exists |
| Does it need a special key? | Usually no | Yes, for the keyed detection scheme |
| Main weakness | Unreliable stylistic guesses | Missing, weakened, or inaccessible watermarks |

**Neither should be treated as conclusive proof of whether a specific person did or did not write a document.**

## 13. Practical Use Cases

These are **potential applications**, not all outcomes tested in the paper:

- **Education:** Support a wider investigation into the provenance of submitted work, without automatically accusing students.
- **Recruitment:** Help institutions understand whether a participating AI system generated a submitted passage, subject to consent and fair-use policies.
- **Publishing and journalism:** Support provenance checks where the originating AI service provides a verifier.
- **Online platforms:** Help label or study machine-generated content when appropriate verification is available.
- **Responsible AI:** Give model providers another tool to support transparency about generated material.

## 14. What Does This Mean for AI Companies?

The paper provides evidence that **production-scale text watermarking is technically practical** without noticeably affecting user-rated quality in the measured experiment.

That may encourage model builders to consider text provenance features. But interoperability, access to verification, false positives, user protections, and removal through rewriting remain significant challenges.

A common cross-company watermarking standard is **not demonstrated** by the study.

## 15. A Simple End-to-End Example

**Scenario:** A teacher receives an essay and wants to know whether a particular chatbot produced it.

1. The chatbot provider has enabled a text watermark.
2. The chatbot writes the essay, subtly biasing token selection according to its hidden key.
3. The student submits the text.
4. An authorized verifier checks the text using that provider's detection mechanism.
5. The verifier reports whether the watermark signal is present strongly enough to pass its threshold.
6. The teacher treats that result as **one piece of evidence**, not an automatic misconduct verdict.

If the essay came from another model, contains only a short excerpt, or was substantially rewritten, this check may not be helpful.

## 16. Beginner's Glossary

| Term | Plain-English meaning |
|---|---|
| **Large Language Model (LLM)** | A system that predicts and generates sequences of text tokens |
| **Token** | A chunk of text, such as a word or part of a word |
| **Sampling** | The process of choosing the next token from model probabilities |
| **Watermark** | A deliberately embedded pattern that can help identify the source |
| **Secret key** | A hidden value needed to reconstruct and verify this particular signal |
| **Random seed** | A value used to make pseudorandom choices repeatable |
| **Tournament sampling** | SynthID-Text's method for selecting tokens through score-based competition |
| **Detection threshold** | The score at which a checker decides the evidence is strong enough |
| **False positive** | Incorrectly saying a watermark is present |
| **False negative** | Missing a watermark that really is present |
| **Non-distortionary** | A configuration that preserves the model's output probabilities when averaged over keys |
| **Speculative sampling** | A speed-up technique for generating tokens efficiently |

## 17. What the Paper Does *Not* Establish

It does **not** establish that:

- All AI-generated writing can be detected.
- Every Gemini response forever contains an equally detectable watermark.
- A watermark cannot be removed by rewriting.
- Teachers or employers should make consequential decisions from detection alone.
- A detector can prove who typed or submitted a document.
- The same quality and efficiency outcomes will hold in every future deployment.

## 18. Key Takeaways

1. **SynthID-Text embeds an invisible statistical signal while AI text is generated.**
2. **It works by changing token selection, not by adding visible labels.**
3. **A detector with the proper key can inspect text without rerunning the model.**
4. **Nearly 20 million Gemini replies were studied**, with no statistically significant decline in user feedback for the watermarked version.
5. **The method improved detectability** against comparable earlier watermarking methods in the paper's experiments.
6. **The processing overhead was small** in the tested configuration.
7. **Editing and AI rewriting can weaken the signal.**
8. **No watermark can identify unmarked output from every AI system.**
9. **Watermark detection is evidence, not a final judgment about authorship or misconduct.**

## 19. Final Summary

SynthID-Text tackles a growing problem: when writing looks equally natural whether a person or a chatbot created it, **style alone is a weak basis for deciding the source**. Google's approach adds a quiet signature during text generation and checks for that signature later using statistics and a secret key.

The research's major achievement is demonstrating that this can be done **at the scale of a real chatbot**, while maintaining the measured quality of replies and adding little computational cost. Its main unresolved challenge is that the watermark is **optional, provider-dependent, and vulnerable to substantial rewriting**.

The bigger lesson is that **AI provenance is not the same as AI-style detection**—and neither one replaces careful human judgment.

---

**Suggested repository location:** `ai-frontier-lab/research-papers/synthid-text-watermarking.md`

