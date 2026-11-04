# BrowseComp: Can AI Find Answers Hidden Across the Internet?

> **AI Frontier Lab | Research Paper Explained for Beginners**  
> **Research area:** AI Agents, Web Browsing, AI Evaluation  
> **Paper:** *BrowseComp: A Simple Yet Challenging Benchmark for Browsing Agents*  
> **Organization:** OpenAI  
> **Authors:** Jason Wei, Zhiqing Sun, Spencer Papay, and colleagues  
> **Paper version:** April 16, 2025 (arXiv:2504.12516v1)  
> **Original paper:** https://arxiv.org/abs/2504.12516  
> **Benchmark repository:** https://github.com/openai/simple-evals  
> **Difficulty:** Beginner-friendly

---

## 1. What Is BrowseComp?

**BrowseComp**, short for **Browsing Competition**, is a test designed to measure how good an AI agent is at **finding hard-to-locate facts on the internet**.

Imagine asking an AI a question whose answer isn't on the first page of Google. Instead, it must visit different websites, collect little clues, compare them, and keep searching until everything fits.

That is what BrowseComp tests.

The dataset contains **1,266 challenging questions**. Each question is intentionally difficult to investigate but has a **short answer** that should be relatively easy to check once found.

### In one sentence

**BrowseComp is like an internet detective competition for AI.**

### What BrowseComp is *not*

- It is **not** a new chatbot or AI model.
- It is **not** a search engine.
- It is **not** a website-browsing feature you install.
- It is a **benchmark**: a standardized test used to compare AI systems.

**What is a benchmark?** Think of it like an exam. BrowseComp is the exam; different AI agents are the students.

---

## 2. Why Did Researchers Create It?

Many existing AI tests ask questions whose answers are easy to find through a quick search.

For example:

> What year did the first human land on the Moon?

A search engine can answer this almost immediately.

But real research often requires considerably more effort. The answer may be spread across old news articles, archived event records, research papers, or other sources.

The researchers wanted to measure whether an AI could:

1. **Search deeply** instead of stopping at the first result.
2. **Connect clues** from multiple sources.
3. **Change its strategy** when a search fails.
4. **Check whether an answer is supported by evidence.**
5. **Keep going** through a difficult investigation.

An AI that is good at answering common questions is not automatically good at solving these more demanding research problems.

---

## 3. A Simple Example Anyone Can Understand

**The following example is invented for explanation. It is not a question from the BrowseComp dataset.**

Suppose someone asks:

> Which author wrote a travel book before 2010, previously worked as a marine biologist, and appeared in a documentary filmed in Iceland?

A regular search might fail because no single page contains all those details.

An investigative AI agent could work like this:

| Step | What the AI does | Why it matters |
|---|---|---|
| 1 | Searches for travel authors who worked in marine biology | Narrows down possible people |
| 2 | Looks for travel books published before 2010 | Checks the date condition |
| 3 | Investigates documentaries filmed in Iceland | Finds another important clue |
| 4 | Compares the names found across sources | Connects separate pieces of evidence |
| 5 | Checks the original sources again | Avoids an unsupported guess |
| 6 | Returns a short answer | Provides the requested result |

The challenge is not knowing a random fact. It is **knowing where to look, what to verify, and when the clues really match**.

---

## 4. How Were the Questions Created?

Human researchers and trainers wrote the BrowseComp questions. They generally began with a known fact and worked **backward** to create an investigative question about it.

For instance, a trainer might know a particular research paper and then build a question using clues about the authors, their education, and the publication date.

That approach makes the final answer easier to verify but difficult to discover from scratch.

The question-writing process included these checks:

- **Existing AI systems struggled:** Trainers checked whether models available at the time could solve the problem.
- **Simple searching wasn't enough:** Trainers were asked to perform five basic Google searches and confirm the answer wasn't immediately obvious.
- **Humans should also find it difficult:** Questions were intended to resist being solved by another person within ten minutes.
- **Answers should be short and factual:** Each question aimed for a single, stable, evidence-supported answer.

### An important catch

A question can have a correct reference answer without being guaranteed to have **only one possible valid answer**. The authors acknowledge this issue and tried to reduce it through additional clues and review.

The original collection contained **1,287 questions**. During later review, the researchers removed **21 problematic questions**, leaving **1,266**.

---

## 5. What Topics Does BrowseComp Cover?

BrowseComp is not limited to computers and technology. It includes many everyday subjects:

| Topic | Questions |
|---|---:|
| TV shows and movies | 205 |
| Other topics | 197 |
| Science and technology | 173 |
| Art | 127 |
| History | 125 |
| Sports | 123 |
| Music | 116 |
| Video games | 71 |
| Geography | 70 |
| Politics | 59 |
| **Total** | **1,266** |

**Why this matters:** The test checks whether AI can investigate unfamiliar topics, not just subjects commonly discussed in AI training materials.

---

## 6. How Difficult Is BrowseComp for People?

The research team asked human trainers to solve questions they had **not** written themselves. They could search the internet but could not use AI assistants.

Humans attempted **1,255** of the 1,266 questions.

| Human evaluation result | Outcome |
|---|---:|
| Questions attempted | 1,255 |
| Questions humans solved | 367 (29.2%) |
| Questions humans gave up on | 888 (70.8%) |
| Solved responses matching reference answers | 317 of 367 (86.4%) |

The people who gave up generally searched for **at least two hours** first.

### What does this tell us?

These aren't ordinary trivia questions. Even people familiar with the task had trouble finding most answers within a few hours.

**Important:** The **29.2%** figure measures how often trainers reported solving a question. It is **not** the same metric as automatically graded correctness. The paper separately notes that 86.4% of those reported answers matched the reference answers.

Also, the participants weren't necessarily professional investigators; the results should not be interpreted as the maximum performance any human could achieve.

---

## 7. How Did AI Models Perform?

The authors evaluated several OpenAI systems available during the study.

### Original 2025 benchmark results

| AI system tested | Correct answers |
|---|---:|
| GPT-4o (without browsing) | 0.6% |
| GPT-4o (with browsing) | 1.9% |
| GPT-4.5 | 0.9% |
| OpenAI o1 | 9.9% |
| **OpenAI Deep Research** | **51.5%** |

**Note:** These are historical results from the April 2025 paper. They do not describe the capabilities or rankings of today's versions of these products.

### What was surprising?

**Giving GPT-4o web access helped only a little.** Its accuracy increased from 0.6% to 1.9%.

In other words, **having access to the internet is not enough**. An AI must also decide what to search, how to connect findings, and whether to try another approach.

OpenAI o1 achieved 9.9% without browsing, suggesting that strong reasoning and existing knowledge can sometimes help even when web access is unavailable.

Deep Research performed much better because the evaluated agent was designed to investigate questions through persistent browsing. The paper also notes that this Deep Research model had been **trained on data specifically teaching BrowseComp-style tasks**, an important qualification when interpreting the results.

---

## 8. Why Did Deep Research Perform Better?

Think of two people trying to answer a difficult question:

- **Person A** checks the first few search results, doesn't find the answer, and guesses.
- **Person B** searches across different websites, rewrites the query, follows new clues, checks sources, and keeps investigating.

BrowseComp rewards behavior more like **Person B**.

The researchers identified three especially important abilities:

1. **Reasoning:** Understanding whether the available facts actually support an answer.
2. **Persistence:** Continuing to investigate rather than giving up after one failed search.
3. **Creative searching:** Finding less obvious ways to locate the answer instead of repeatedly using the same query.

**A key distinction:** BrowseComp evaluates the *outcome* of this research process; it isn't a complete step-by-step instruction manual for building a web-browsing agent.

---

## 9. Does More Browsing Help?

The researchers tested how performance changed when their Deep Research agent was given **more computing effort while answering questions**.

The paper found that accuracy improved as the agent was allowed to use more effort.

In everyday terms, the AI benefited from having more opportunity to investigate, evaluate, and search again.

### What does “test-time compute” mean?

It means the computing resources spent **while the AI is answering a question**, rather than while it is originally being trained.

A simple analogy:

> An exam student might perform better when given more time to work through a difficult problem, even though they have not studied any new material beforehand.

More compute, however, can also mean more cost and time. The paper demonstrates a performance improvement; it does not establish that unlimited additional browsing is always worthwhile.

---

## 10. What Happens If the AI Tries Several Times?

The researchers also tried having Deep Research generate **multiple answers for the same problem** and then select one.

They investigated three methods:

| Method | Beginner-friendly explanation |
|---|---|
| **Majority voting** | Choose the answer that appears most often |
| **Weighted voting** | Give more weight to answers the AI rates as more confident |
| **Best-of-N** | Choose the single answer with the highest confidence score |

For this experiment, the researchers generated up to **64 responses per question**.

These selection methods improved performance by around **15% to 25% compared with a single attempt**, as described in the paper. **Best-of-N** consistently performed best among the three tested methods.

### Easy analogy

Imagine asking a detective to independently investigate the same case several times, then selecting the result backed by the detective's strongest assessment.

This can improve the final answer, but there is a major warning: **an AI can feel confident and still be wrong**.

---

## 11. Can AI Reliably Tell When It Is Wrong?

Not necessarily—and this was one of the paper's most important findings.

The researchers asked models not only to answer questions but also to give a **confidence score** between 0% and 100%.

Ideally, when an AI says it is 90% confident across many answers, roughly 90% of those answers should be correct. This relationship is called **confidence calibration**.

The study found that browsing-enabled models often had **poor calibration**. Deep Research obtained a **91% calibration error** under the paper's reported measure, despite its much stronger answer accuracy.

### Why is that a problem?

Imagine an AI says:

> “I am 95% sure this is the correct answer.”

If it regularly makes mistakes when sounding that certain, users could trust incorrect information.

**Important lesson:** A confident-looking answer is not the same as a verified answer.

Interestingly, confidence scores were still useful for **ranking multiple attempts**, even though they were unreliable as literal probabilities of correctness. That helps explain why Best-of-N selection performed well.

---

## 12. Why Were Some Questions Almost Impossible for the AI?

The authors ran **64 attempts per question** to study how difficulty varied.

For Deep Research:

- It got the right answer on **every attempt** for approximately **16% of questions**.
- It **never** found the correct answer in any of the 64 attempts for approximately **14% of questions**.
- Many questions fell between those extremes.

The researchers then revealed the correct answer to the model for particularly difficult questions and asked it to find supporting web evidence.

In most of those cases, the AI **could verify the answer once it knew what to look for**.

This is a crucial distinction:

**Finding an answer can be much harder than verifying an answer you have already been given.**

It is similar to finding a specific house in an unfamiliar city without an address versus confirming the house exists once someone gives you its address.

---

## 13. What Are the Limitations of BrowseComp?

BrowseComp is useful, but it does **not** measure every skill an AI research assistant needs.

### 1. Answers are short

The questions are designed to produce brief, easy-to-grade answers. This does not test the quality of lengthy reports, detailed explanations, or polished presentations.

### 2. Questions are unusually difficult

The dataset deliberately emphasizes obscure, deeply buried information. This is different from the typical question an everyday user asks.

### 3. Real-world ambiguity is limited

Most questions aim at one stable factual answer. Real users often ask vague questions that require clarification or judgment.

### 4. Reference answers are not guaranteed to be unique

Even carefully written questions may sometimes admit another valid answer.

### 5. High accuracy does not guarantee trustworthy confidence

A system can solve many questions yet remain poor at estimating when it may be wrong.

### 6. Browsing is only part of research

Being able to locate a fact does not automatically mean the AI can write a balanced report, interpret conflicting evidence, or make sound real-world decisions.

### 7. It focuses on web information

The paper primarily tests internet information retrieval; it proposes that future evaluations could also cover searching images, video, audio, and interactive webpages.

---

## 14. Why Does This Research Matter for Agentic AI?

**Agentic AI** refers broadly to AI systems that can carry out multi-step tasks by choosing actions and using tools, rather than only producing a one-shot answer.

BrowseComp demonstrates why powerful AI agents need more than a web-search button.

Consider a future AI research assistant asked to identify an obscure regulation, track the original source of an industry statistic, or investigate a complex historical fact.

A capable agent would need to:

1. Understand the question and identify the required clues.
2. Choose appropriate web searches and sources.
3. Examine what it finds.
4. Detect gaps or contradictions.
5. Change search strategy where necessary.
6. Verify the final result.
7. Communicate uncertainty accurately.

The **first six steps** reflect the abilities BrowseComp is designed to exercise. The **seventh** remains a major concern highlighted by the study.

### Practical relevance (interpretation, not directly tested business outcomes)

The skills measured by BrowseComp could be useful in:

- **Research assistance:** Finding hard-to-locate information across multiple sources.
- **Competitive intelligence:** Tracking specific facts about companies, products, or markets.
- **Fact-checking:** Tracing claims back to supporting evidence.
- **Academic research:** Locating obscure publications and connecting references.
- **Enterprise knowledge discovery:** Investigating information spread across many documents and systems, although internal enterprise searching was not directly evaluated in this paper.

These are potential use cases, **not proof** that the evaluated system performs reliably in all these settings.

---

## 15. BrowseComp vs. a Normal Search Engine

| Ordinary search | BrowseComp-style investigation |
|---|---|
| Looks for relevant webpages | Searches for evidence that fits several clues |
| Often works with one or two searches | May require many searches and changes in approach |
| Usually answers obvious factual questions quickly | Targets unusual questions whose answers are hard to discover |
| Presents search results | Requires finding and validating a particular answer |
| A good match may be enough to get started | Multiple constraints must be checked before answering |

This comparison is simplified: ordinary search engines can also support complex research, especially when used skillfully by humans.

---

## 16. Mini Glossary

| Term | Meaning |
|---|---|
| **Benchmark** | A standardized test for comparing the performance of AI systems |
| **AI agent** | An AI system that can take actions or use tools to complete a task |
| **Web browsing agent** | An AI agent that searches and examines webpages as part of its work |
| **Ground-truth answer** | The answer the benchmark uses as its correct reference |
| **Accuracy** | How often the system gives the right answer |
| **Confidence score** | How certain the system claims to be about its answer |
| **Calibration** | How closely confidence matches actual correctness |
| **Test-time compute** | Computing effort spent when generating an answer |
| **Best-of-N** | Trying multiple times and selecting the highest-scored answer |
| **Multi-hop reasoning** | Connecting several separate facts or clues to reach one conclusion |

---

## 17. Key Takeaways

1. **BrowseComp is an AI evaluation benchmark, not a new AI model.**
2. Its **1,266 questions** require persistent internet searching and connecting scattered clues.
3. The benchmark is **hard to solve but designed to be easy to grade** once a short answer is found.
4. Human trainers solved **29.2%** of attempted questions, illustrating the difficulty of the task.
5. In the **2025 evaluation**, GPT-4o with browsing scored **1.9%**, while Deep Research scored **51.5%**.
6. **Web access by itself is not enough**; reasoning and search strategy matter.
7. **More searching effort and multiple attempts** improved performance in the researchers' experiments.
8. **AI confidence remained unreliable**, even when answer accuracy improved.
9. Some questions were **easy to verify after revealing the answer but very hard to solve from scratch**.
10. BrowseComp measures an important but **limited part of real-world research capability**.

---

## 18. Final Summary

BrowseComp asks a deceptively simple question:

> **Can an AI behave like a persistent internet investigator rather than a quick-answer machine?**

The 2025 research showed a major gap between ordinary chatbot browsing and more persistent research-oriented agents. But it also showed that finding obscure information is difficult, additional effort matters, and AI systems can remain overconfident even when they get more answers right.

The broader lesson is that the future of useful AI research agents depends not only on **finding information**, but also on **checking the evidence, adapting their searches, and knowing when they might be wrong**.

---

## 19. Source and Further Reading

**Primary source:** Wei, J., Sun, Z., Papay, S., et al. (2025). *BrowseComp: A Simple Yet Challenging Benchmark for Browsing Agents*. arXiv:2504.12516v1, April 16, 2025.

- [Read the original paper](https://arxiv.org/abs/2504.12516)
- [BrowseComp benchmark in OpenAI's Simple Evals repository](https://github.com/openai/simple-evals)

**Research note:** This beginner-friendly explanation is based on the supplied 11-page BrowseComp paper. Illustrations such as the travel-author example are original teaching examples, **not** real benchmark questions. Results are historical measurements from the paper, not current model comparisons. Original benchmark questions and their reference answers are intentionally not reproduced, consistent with the authors' request to avoid benchmark-answer leakage.

---

**AI Frontier Lab — Researching Today's AI, Understanding Tomorrow's Possibilities.**

