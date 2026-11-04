# Which Economic Tasks Are Performed with AI?

### What Millions of Claude Conversations Reveal About AI and Jobs — Explained Simply

> **AI Frontier Lab | Research Readout | Beginner-friendly**  
> **Research organization:** Anthropic  
> **Study discussed:** *Which Economic Tasks Are Performed with AI? Evidence from Millions of Claude Conversations*  
> **Study period:** December 2024–January 2025  
> **Research release discussed in the supplied transcript:** February 2025  
> **Source for this readout:** Supplied Research Readouts video transcript (not an independent verification of the original paper)

---

## 1. Research Overview

**The big question:** When people use AI at work, **which parts of their jobs are they actually using it for?**

A job is not just one activity. A teacher might plan lessons, explain topics, grade work, and help students. A physical therapist might read research, explain a condition, treat patients, and teach families how to help at home.

AI may assist with **some tasks** without being able to perform **the whole job**. Anthropic's researchers wanted to see that distinction using actual conversations with **Claude**, its AI chatbot.

### One-sentence takeaway

**The study found evidence of AI use across tasks in many occupations, but that is not the same as evidence that entire jobs have been automated or replaced.**

---

## 2. A Simple Everyday Example

Imagine a physical therapist who asks Claude:

> “Write a one-page handout explaining this patient's condition in simple language.”

Claude might help draft that handout. It might also summarize recent medical research. But it cannot physically examine the patient or perform hands-on treatment through a text conversation.

| Part of the job | What AI might do |
|---|---|
| Read and summarize research | Help summarize information |
| Explain a condition in plain words | Draft a handout |
| Provide hands-on treatment | Not performed by the chatbot |
| Demonstrate home-care techniques in person | Not performed by the chatbot |

**Why it matters:** Saying “AI is used in physical therapy” does **not** mean “AI can replace physical therapists.” It means some related tasks appeared in the chatbot conversations.

---

## 3. What Problem Was the Research Trying to Solve?

Before this study, many discussions about AI and employment relied on two approaches:

1. **Forecasts:** Experts looked at tasks and estimated what AI *could potentially do*.
2. **Surveys:** Workers were asked what AI they *remembered using*.

Both approaches provide useful information, but neither directly shows what people type into an AI assistant day to day.

The researchers therefore took a different approach: **look at conversation data and classify the tasks people are asking Claude to help with.**

**Important distinction:** This measures *observed activity in one AI product*, not all AI use across every workplace.

---

## 4. How the Researchers Studied AI Use

### Step 1: Examine conversations

The researchers looked at **more than 4 million Claude conversations** from December 2024 and January 2025. The main analysis and the statistics highlighted in the research readout came from **1 million conversations from one week in December 2024**.

### Step 2: Use a catalog of job tasks

They matched conversations to **O\*NET (Occupational Information Network)**, a U.S. occupational database describing jobs and their tasks.

It contained **nearly 20,000 tasks**. Instead of asking “Is AI replacing this job?”, researchers could ask “Which tasks associated with this job appear in AI conversations?”

### Step 3: Classify conversations with AI

The researchers used a tool called **Clio**, developed in 2024, to classify conversations. The tasks were organized into groups and subgroups, beginning with **12 top-level groups**, so a conversation could be assigned to a relevant task.

### Step 4: Check whether the labels made sense

Human reviewers checked **150 conversations** and judged the assigned task labels acceptable **86% of the time**.

**Plain-language warning:** The task classifications were not perfect. Results based on them contain some classification error.

### How the process works

```text
Claude conversations
        |
        v
AI-based task classification (Clio)
        |
        v
Match against O*NET job-task descriptions
        |
        v
Group by occupation and type of AI use
        |
        v
Study which tasks appeared and how AI was used
```

---

## 5. Key Finding #1: AI Use Was Concentrated in Certain Tasks

The research did **not** find that every occupation used AI equally.

| Occupational group | Share of analyzed Claude conversations | Context |
|---|---:|---|
| Computer and mathematical occupations | **37%** | Mostly programming-related tasks |
| Transportation-related work (moving goods and people) | **About 0.33%** | Mainly physical-world activities |

For context, the transcript says computer and mathematical occupations represented about **3% of U.S. workers**, whereas transportation-related work represented about **9%**.

### What does that mean?

Work that can be done through words, documents, or code appeared much more often in the chatbot data than physical work.

But **37% of conversations is not 37% of programmers**, and **0.33% of conversations is not 0.33% of transportation workers**. These figures describe the *types of tasks associated with the conversations*.

**Another crucial caveat:** A conversation classified under a dietitian's task might have been written by an ordinary person asking about nutrition—not by a professional dietitian. The classification identifies the task, **not necessarily the occupation of the user**.

---

## 6. Key Finding #2: AI Touched Parts of Many Jobs, Not Entire Jobs

The researchers asked: *For each occupation, what share of its listed tasks appeared at least once in the analyzed conversations?*

| Share of an occupation's tasks appearing in conversations | Share of occupations |
|---|---:|
| At least **25%** of tasks | **About 36%** |
| At least **50%** of tasks | **About 11%** |
| At least **75%** of tasks | **About 4%** |

### Read these numbers carefully

“36% of occupations showed AI use in at least a quarter of their tasks” does **not** mean AI completed a quarter of everyone's workload. It means conversations were matched to at least a quarter of the tasks listed for those occupations.

The supplied transcript gives these examples:

- **Physical therapists:** roughly a quarter of listed tasks appeared in conversations.
- **Marketing managers:** roughly half appeared.
- **Foreign language teachers:** roughly three-quarters appeared.

These are examples of **task coverage**, not estimates of how much of a person's working day AI performed.

### Why it matters

Jobs are bundles of activities. AI may change how those activities are completed even when most of the job still requires human skills, judgment, or physical presence.

---

## 7. Key Finding #3: People More Often Worked *With* AI Than Handed Tasks Over

The study categorized interactions into two broad patterns:

### Augmentation — AI assists the person (**57%**)

People **work alongside the chatbot**. Examples include:

- Revising a draft through multiple rounds of feedback.
- Asking for an explanation to understand a topic.
- Having AI review or check work the person already completed.

**Think of this as:** AI acting like a writing partner, tutor, or reviewer.

### Automation — A task is handed to AI (**43%**)

People use AI to produce an output or resolve a problem. Examples include:

- Requesting a finished piece of text or code.
- Providing a programming error, using the suggested fix, and returning with the next error.

**Think of this as:** AI being asked to handle a specific part of the work.

| Pattern | Share of conversations |
|---|---:|
| **Augmentation** — working with AI | **57%** |
| **Automation** — handing over a task | **43%** |

**Important:** These are classifications of *chat interactions*, not proof that AI completed tasks successfully or that users never edited the results afterward. The transcript notes that people might revise the result outside Claude, so collaboration could be undercounted.

---

## 8. Which Jobs Showed More AI Use?

The transcript describes an interesting pattern when occupations were compared by pay:

- AI conversation activity peaked around the **upper quarter of the wage distribution**, where programming jobs are common.
- It was lower at **both ends** of the range.
- **Waiters** and **anesthesiologists** were examples of occupations with relatively little observed activity.

The readout also says tasks associated with jobs requiring a **bachelor's degree** accounted for more than half of conversations, while occupations requiring very advanced qualifications or minimal training appeared less than their respective shares.

**Do not interpret this as “AI helps only high earners.”** The pattern reflects the particular Claude usage data and the way conversations were mapped to occupations.

---

## 9. What Makes This Research Different?

The main contribution was a shift from speculation to **observed usage**.

| Approach | What it measures | Important limitation |
|---|---|---|
| Forecast | What AI might be able to do | Capability does not equal real adoption |
| Worker survey | What people report using AI for | Depends on memory and reporting |
| Claude conversation analysis | What task-related requests appeared in sampled chats | Does not reveal the full workplace or what happened afterward |

This research helps distinguish three questions that are often confused:

1. **Can AI do this task?** A question of capability.
2. **Are people asking AI to help with it?** A question of use.
3. **Did AI successfully complete it and change employment outcomes?** A question this study does **not** fully answer.

---

## 10. Study Limitations — What We Should Not Conclude

### 1. Only one AI product

The analyzed data came from **Claude**, not from all AI tools. Results cannot automatically be applied to ChatGPT, Gemini, Copilot, or every workplace.

### 2. Only personal plans

The dataset described in the transcript excluded Claude's business versions. Enterprise patterns might look very different.

### 3. Only text interactions

The analysis did not capture the full range of voice, image, video, or physical-world AI applications.

### 4. A limited time period

The headline findings came from **one week in December 2024**. They should not be treated as current usage levels or a long-term trend.

### 5. No visibility after the conversation

Researchers could see the chat, but not necessarily whether the code worked, the handout was used, or the AI output was discarded.

### 6. The classification had errors

Human reviewers considered task labels acceptable **86%** of the time in a 150-conversation check—not 100%.

### 7. The job catalog was U.S.-focused

O\*NET describes existing U.S. occupations and tasks. It cannot fully represent emerging tasks created by AI or differences between countries.

### 8. Task labels are not proof of the user's profession

Someone asking about nutrition might be assigned a dietitian-related task even if that person is not a dietitian.

**Bottom line:** This is a study of **what appeared in AI conversations**, not a direct measurement of jobs lost, hours saved, productivity gains, or the quality of completed work.

---

## 11. Does This Mean AI Will Replace Jobs?

**The study does not establish that.**

It shows that AI usage was distributed across *parts* of occupations. That is consistent with many jobs changing in how tasks are performed, but it cannot prove whether total employment in any occupation will rise or fall.

For example, a marketing manager may use AI to draft campaign text and summarize research while still making decisions about budgets, positioning, customers, and team coordination.

**A useful way to think about it:**

```text
A job = Task A + Task B + Task C + Task D

AI helps with A and B

This does NOT automatically mean
AI has replaced A + B + C + D
```

---

## 12. What This Could Mean for the AI Industry

> **Interpretation beyond the study:** The following points are possible implications, not findings directly proved by the researchers.

### Better AI product design

If people frequently use AI for code, writing, and revisions, product teams might build tools that support these specific workflows more effectively.

### Greater emphasis on human-AI collaboration

Since **57%** of the classified interactions involved augmentation, interfaces for review, feedback, editing, and learning may be particularly valuable.

### More frequent usage measurement

Companies and researchers could repeat similar analyses over time to learn whether AI adoption spreads into different tasks and occupations.

### New research on work outcomes

A logical next step is to measure **what happens after the chat**: Did the output work? Did it save time? Did it improve quality? Did it create new work?

### Enterprise implications

Organizations considering AI tools should evaluate **individual tasks and workflows**, rather than assuming that introducing a chatbot automatically transforms or replaces entire roles.

---

## 13. What This Means for an Everyday AI User

A practical way to start is to identify tasks where AI can assist without taking away your responsibility for the result:

1. Pick a repeatable task such as drafting, summarizing, or reviewing.
2. Ask AI to help with that specific task.
3. Check the output for errors and missing context.
4. Improve it through follow-up instructions.
5. Measure whether it actually saves time or improves quality.

**Example:** Instead of saying, “AI should manage my entire project,” try asking it to summarize a meeting, organize action items, or prepare a first draft of a weekly update—and then validate the result.

This is **practical advice inspired by the findings**, not an intervention tested by the study.

---

## 14. Beginner's Glossary

| Term | Plain-English meaning |
|---|---|
| **Occupation** | A type of job, such as teacher or programmer |
| **Task** | One activity performed as part of a job |
| **O\*NET** | A U.S. database that describes occupations and job tasks |
| **Claude** | Anthropic's AI chatbot |
| **Clio** | A tool used to analyze and classify Claude conversations |
| **Augmentation** | AI assists a person while the person remains involved |
| **Automation** | A task is handed to a system to perform |
| **Task coverage** | How many of a job's listed tasks appear in the conversation data |
| **Benchmark** | A standardized test used to evaluate performance; this study is primarily usage analysis rather than a model-performance benchmark |

---

## 15. Key Numbers to Remember

| Number | Meaning |
|---|---|
| **4+ million** | Conversations examined across December 2024 and January 2025 |
| **1 million** | Conversations used in the main one-week December analysis |
| **Nearly 20,000** | Job tasks in the O\*NET catalog |
| **86%** | Task labels judged acceptable in a 150-conversation human check |
| **37%** | Conversations associated with computer and mathematical occupations |
| **36%** | Occupations with at least one-quarter of their tasks represented |
| **11%** | Occupations with at least half of tasks represented |
| **4%** | Occupations with at least three-quarters of tasks represented |
| **57%** | Conversations classified as augmentation |
| **43%** | Conversations classified as automation |

**Note:** The percentages describe different denominators. For example, **37%** describes a share of conversations, while **36%** describes a share of occupations. Do not compare them as if they measure the same thing.

---

## 16. Key Takeaways

1. **AI is being used for specific tasks across many kinds of work**, not necessarily entire jobs.
2. **Programming and writing-related activities featured prominently** in the sampled conversations.
3. **Computer and mathematical tasks accounted for 37% of conversations**, much higher than that occupational group's share of U.S. employment.
4. **About 36% of occupations had at least a quarter of their listed tasks represented** in the conversation data.
5. **Working alongside AI was more common than handing over a task** in the study's interaction classifications (57% versus 43%).
6. **Actual usage differs from predictions about possible AI capability** and is worth measuring separately.
7. **The data cannot tell us whether AI outputs were successfully used**, how many hours were saved, or whether jobs were lost.
8. **The strongest practical lesson is to think at the task level**, while keeping people responsible for judging outcomes.

---

## 17. Final Summary

Anthropic examined millions of Claude conversations to better understand how people were using AI in activities related to work. Rather than predicting which jobs AI *could* perform, the team matched actual chatbot conversations to tasks within occupations.

The findings suggest that AI usage was concentrated in certain activities—especially software and text-related work—and that many interactions involved people working **with** AI rather than simply handing work over to it.

However, the data came from a narrow slice of Claude usage, and the study could not observe whether generated results were used successfully. It therefore supports conclusions about **patterns of chatbot use**, not definitive conclusions about **job replacement**.

### The central message

> **AI can change individual tasks without replacing an entire job. To understand its real impact, measure what people actually use it for—and what happens afterward.**

---

## 18. Source and Research Scope

- **Research:** *Which Economic Tasks Are Performed with AI? Evidence from Millions of Claude Conversations*
- **Organization:** Anthropic
- **Research period described:** December 2024–January 2025
- **Source material:** User-provided *Research Readouts* transcript, discussing the February 2025 study

> **For GitHub:** Save this file to `ai-frontier-lab/research-papers/which-economic-tasks-are-performed-with-ai.md`.
