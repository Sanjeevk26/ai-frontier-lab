# What Is an AI Agent?

AI agents represent a shift from simply **chatting with AI** to **directing AI to perform work**.

A simple definition is:

> **An AI agent is a system that works toward a goal inside a real workspace. It can open files and applications, use tools, create outputs, observe results, and adjust its approach until the task is completed.**

Understanding this distinction is important because the future of working with AI is increasingly moving toward **training and directing agents**, rather than only asking AI questions.

---

# What You Should Understand

By the end of this topic, you should be able to understand:

* What an AI agent is
* How an agent differs from a traditional chatbot
* The core components of an agent
* How agents use goals, memory, and workspaces
* How agents continue working across multiple steps
* Why agentic capability exists on a spectrum
* How the same AI system can behave differently depending on how it is used

---

# Traditional AI Chatbots

For several years, most people experienced AI primarily through chatbots.

The interaction was simple:

```text
User Prompt
    ↓
AI Generates Text
    ↓
User Receives an Answer
```

You might ask AI to:

* Explain something
* Answer a question
* Write something
* Provide advice

This can be extremely useful.

However, traditional chatbots have an important limitation:

> They mainly generate text that helps you perform the work rather than performing the work themselves.

For example:

```text
User:
How do I determine whether an invoice contains a valid tax ID?

AI:
Explains what to look for.
```

The AI provides useful information, but you still need to open the invoices and perform the checks yourself.

---

# AI Agents Go Further

An agent can go beyond generating an answer.

It can connect to the places where the actual work happens.

An agent may be able to:

* Open files
* Read data
* Write documents
* Edit documents
* Search through systems
* Use tools
* Create outputs
* Check whether progress has been made
* Continue working across several steps

The interaction therefore changes from:

```text
Ask AI for an answer
```

to:

```text
Direct AI to perform the work
```

---

# Your Role Changes With Agents

When working with traditional chatbots, you are usually the person executing the work.

With agents, your role begins to look more like that of a manager or director.

You:

1. Define the outcome.
2. Provide relevant context.
3. Set constraints.
4. Supervise the system while it works.

This is an important foundation of **agentic work**.

```text
Human
  ↓
Defines Outcome
  ↓
Provides Context
  ↓
Sets Constraints
  ↓
Agent Performs Work
  ↓
Human Supervises
```

---

# Chatbot vs Agent

There are several important differences between a traditional chatbot and an AI agent.

---

## 1. Agents Have a Workspace

A traditional chatbot is mostly limited to the conversation.

It can:

* Talk about your work
* Give advice
* Generate text
* Help you think through a problem

But it generally cannot act outside the chat.

An agent has a workspace where it can perform actions.

That workspace could contain:

* Files
* Documents
* Applications
* Tools

The agent can work directly with these resources.

---

## 2. Agents Have Goals

A chatbot usually has a simple objective:

```text
Respond to the user's current question.
```

An agent has a broader objective.

It may be asked to:

```text
Produce a result.
```

or:

```text
Complete a task.
```

Instead of only responding, the agent works toward an outcome.

---

## 3. Agents Can Draw on Memory

A traditional chatbot may primarily work with what is available in the current conversation.

An agent can be connected to information outside the chat.

Examples include:

* Files
* Notes
* Emails
* Previous work

This information becomes part of the context available to the agent while it works.

The transcript refers to this outside context as the agent's **memory**.

Providing the right context is therefore an important part of helping an agent succeed.

---

## 4. Agents Work in a Continuous Cycle

A chatbot typically responds once and waits for the next prompt.

```text
Prompt
  ↓
Response
  ↓
Wait
```

An agent can continue working toward the objective.

```text
Goal
  ↓
Use Workspace
  ↓
Use Memory
  ↓
Take Action
  ↓
Observe Result
  ↓
Continue Working
  ↓
Goal Completed
```

It does not necessarily require the user to prompt it after every individual step.

---

# The Core Pieces of an Agent

The lesson introduces three major components that will be explored in more detail later.

They are:

```text
Brain
Memory
Workspace
```

---

## Brain

The brain is the part of the agent responsible for reasoning.

It helps the system determine what needs to happen while working toward the goal.

---

## Memory

Memory is the context the agent can draw from while performing the task.

This can include information such as:

* Files
* Notes
* Emails
* Previous work
* Instructions
* Examples

---

## Workspace

The workspace is where the agent performs actions.

It can include:

* Files
* Applications
* Documents
* Tools

This is where the agent moves from simply generating text to performing actual work.

---

# Example: Invoice Review Agent

Consider a tax accountant who needs to review 40 client invoices.

The goal is:

```text
Identify invoices that are missing a tax ID
and create a summary spreadsheet.
```

---

## The Agent's Goal

The objective is clear:

```text
Find invoices without the required tax ID.
```

The final deliverable is:

```text
A summary spreadsheet containing the flagged invoices.
```

---

## The Agent's Workspace

The agent works with the invoice files.

It may:

1. Open the invoice files.
2. Read each invoice.
3. Extract relevant information.
4. Determine whether a tax ID exists.
5. Create a spreadsheet.
6. Add the required information to the spreadsheet.

---

## The Agent's Memory

The invoices themselves are not the only context available.

The agent might also receive:

```text
A note explaining what counts as a valid tax ID.
```

It could also receive:

```text
An example showing how the final summary should be formatted.
```

This additional information helps the agent understand how the task should be performed.

---

## The Continuous Cycle

The agent does not stop after reviewing one invoice.

It continues:

```text
Open Invoice
    ↓
Read Invoice
    ↓
Check Tax ID
    ↓
Update Spreadsheet
    ↓
Move to Next Invoice
    ↓
Repeat
```

This continues until the objective has been completed.

The user does not need to manually prompt the agent after every invoice.

---

# Applying the Model to Your Own Work

A useful exercise is to take a task you perform regularly and ask:

### What is the goal?

What final outcome should be achieved?

### What workspace is involved?

Which files, applications, documents, or tools are required?

### What memory is required?

What context, instructions, notes, examples, or previous work would help?

### What actions must happen?

Which individual steps need to be completed?

### What does completion look like?

How does the agent know when the goal has been achieved?

This helps you think about ordinary work in an agentic way.

---

# Agentic Capability Is a Spectrum

Not every AI system is equally agentic.

The term **agentic** describes how much a system can act independently toward a goal.

It is useful to think of agentic capability as:

> **A dial, not a switch.**

An AI system does not need to be classified as simply:

```text
Agent
```

or:

```text
Not an Agent
```

Instead, systems can sit at different places along a spectrum.

```text
Basic Chatbot
      ↓
Chatbot with Context
      ↓
Tool-Using Assistant
      ↓
Multi-Step Agent
      ↓
Agent Operating Across Systems Over Time
```

---

# Level 1: Basic Chatbot

At one end of the spectrum is a basic chatbot.

You ask:

```text
What is a tax ID?
```

The AI provides an answer.

The system does not:

* Open files
* Modify anything
* Perform actions
* Complete workflows

It simply responds with text.

```text
Question
   ↓
Answer
```

This is useful, but it is not particularly agentic.

---

# Level 2: Chatbot With Context

A little further along the spectrum is a chatbot that can work with information you provide.

For example, you might:

```text
Upload a document
       ↓
Ask AI to summarize it
```

or:

```text
Provide call notes
       ↓
Ask AI to extract action items
```

or:

```text
Provide a spreadsheet
       ↓
Ask AI to analyze the numbers
```

The system is doing more than answering from general knowledge.

It is reasoning over external information that you provide.

However, it is still limited.

It can work with what you give it, but it cannot independently reach outside the conversation and perform actions elsewhere.

---

# Level 3: Tool-Using Assistant

Further along the spectrum is an assistant that can use tools.

This type of system can perform actions such as:

* Looking something up on your computer
* Building a chart
* Drafting an email
* Updating a record in a connected application

For example:

```text
User Request
     ↓
AI Drafts Email
     ↓
AI Uses Email Application
     ↓
Email Is Sent
```

This is more agentic because the system is now acting inside the application where the work actually happens.

---

# Level 4: Multi-Step Agent

Further along is an AI system capable of completing a multi-step workflow.

Imagine a folder containing customer call notes.

The goal is:

```text
Find every customer that mentioned pricing as a concern
and create one summary document.
```

The agent may need to:

1. Open the folder.
2. Read each customer call note.
3. Determine whether pricing was raised as a concern.
4. Track which files have already been reviewed.
5. Collect the relevant customer information.
6. Create a new summary document.
7. Check whether the output matches the original goal.

This is more agentic because the system is not simply:

```text
Responding
```

or:

```text
Taking one action
```

It is pursuing a goal through a sequence of connected steps.

---

# Example: Reviewing Customer Call Notes

The workflow could look like this:

```text
Open Folder
    ↓
Read Call Note 1
    ↓
Pricing Concern?
    ↓
Record Result
    ↓
Read Call Note 2
    ↓
Pricing Concern?
    ↓
Record Result
    ↓
Continue Through Files
    ↓
Create Summary Document
    ↓
Check Output Against Goal
```

The system has to reason about what counts as a pricing concern while also keeping track of its progress.

---

# Level 5: Agent Operating Across Systems Over Time

At the more agentic end of the spectrum are systems that operate across multiple applications over time.

Imagine an agent responsible for reviewing a sales pipeline every Monday morning.

The rule is:

```text
If a deal has not moved in two weeks,
notify the team.
```

The agent could:

1. Review the sales pipeline.
2. Identify deals that have not progressed.
3. Determine the deal owner.
4. Post a message in the team's communication channel.
5. Remain silent when no action is needed.

The workflow may look like:

```text
Monday Morning
      ↓
Review Sales Pipeline
      ↓
Has Deal Been Stuck for 2 Weeks?
      ↓
     Yes
      ↓
Identify Deal + Owner
      ↓
Post Team Notification
```

If everything is progressing:

```text
No Action Required
      ↓
Remain Silent
```

This represents a highly agentic workflow.

---

# Why This Example Is Highly Agentic

The system has:

* A recurring goal
* Access to multiple parts of the workspace
* A decision rule
* Tools for taking action
* The ability to decide when action is unnecessary

An important capability here is knowing when **not** to act.

The agent does not need to generate output when everything is working correctly.

---

# The Same AI Tool Can Behave Differently

An important idea is that the same AI system can exist at different points on the agentic spectrum depending on how you use it.

Consider the following request:

```text
What is a tax ID?
```

The system is being used like a chatbot.

Now consider:

```text
Here is a folder containing invoices.

Review the invoices,
identify the missing tax IDs,
and create a spreadsheet containing the flagged invoices.
```

The same system is now being used more like an agent.

Therefore:

> How agentic a workflow is depends less on the name of the software and more on how the system behaves during the task.

---

# Software Does Not Determine Agentic Capability by Itself

It is easy to think:

```text
Product A = Chatbot
Product B = Agent
```

But this is not always accurate.

The same AI product may be used in different ways.

For one task:

```text
Question
  ↓
Answer
```

For another:

```text
Goal
  ↓
Files
  ↓
Tools
  ↓
Multiple Actions
  ↓
Completed Deliverable
```

The second workflow is more agentic even if both workflows use the same AI system.

---

# What Makes a System More Agentic?

A system becomes more agentic as it increasingly does the following:

### Pursues a Goal

It works toward an outcome rather than only answering a question.

### Acts in a Workspace

It interacts with files, applications, documents, and tools.

### Uses Context

It draws from information connected to the task.

### Performs Multiple Steps

It can continue working without requiring a new prompt for every action.

### Observes Progress

It checks the result of its work.

### Adjusts Its Approach

It can respond to what happens during the task.

### Produces a Deliverable

It aims to create a useful outcome rather than only provide information.

---

# The Agentic Spectrum

The complete spectrum introduced in this lesson can be represented as:

```text
┌──────────────────────────────┐
│       Basic Chatbot          │
│                              │
│ Question → Text Answer       │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│   Chatbot Using Context      │
│                              │
│ Reads information provided   │
│ by the user                  │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│   Tool-Using Assistant       │
│                              │
│ Can perform actions inside   │
│ connected applications       │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│      Multi-Step Agent        │
│                              │
│ Pursues a goal through       │
│ several connected actions    │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│ Agent Operating Across       │
│ Multiple Systems Over Time   │
│                              │
│ Recurring goals, decisions,  │
│ actions, and monitoring      │
└──────────────────────────────┘
```

The further down the spectrum a system moves, the more independently it can work toward a goal.

---

# The Most Important Mental Model

The simplest distinction is:

```text
Chatbot
   ↓
Talks to you
```

while:

```text
Agent
   ↓
Acts for you
```

This does not mean chatbots are not useful.

It means agents extend AI from **conversation** into **execution**.

---

# A Chatbot Talks to You

A chatbot generally:

* Responds to a prompt
* Generates text
* Explains information
* Answers questions
* Waits for another prompt

Its interaction looks like:

```text
User
 ↓
Prompt
 ↓
Chatbot
 ↓
Response
 ↓
Stop
```

---

# An Agent Acts for You

An agent goes further.

It has:

### A Goal

The system aims to achieve something beyond simply creating an answer.

### A Workspace

It can access the place where the work occurs.

### Memory

It can use connected context while performing the task.

### A Continuous Cycle

It continues working step by step until the objective has been achieved.

The overall model becomes:

```text
                GOAL
                 ↓
              AGENT
                 ↓
        ┌────────┼────────┐
        ↓        ↓        ↓
      Memory  Workspace  Tools
        │        │        │
        └────────┼────────┘
                 ↓
             Take Action
                 ↓
           Observe Result
                 ↓
          Continue Working
                 ↓
             Goal Met
```

---

# Continuous Agent Work

One of the strongest distinctions between a chatbot and an agent is continuity.

A chatbot often works like:

```text
Prompt 1
   ↓
Answer 1

Prompt 2
   ↓
Answer 2

Prompt 3
   ↓
Answer 3
```

The user repeatedly drives the interaction.

An agent can instead operate like:

```text
Goal
 ↓
Step 1
 ↓
Step 2
 ↓
Step 3
 ↓
Check Progress
 ↓
Step 4
 ↓
Final Output
```

The agent drives more of the intermediate execution itself.

---

# Agents Change the Human Role

When AI only generates information, humans perform most of the execution.

```text
AI
 ↓
Provides Information
 ↓
Human
 ↓
Executes Work
```

When using agents:

```text
Human
 ↓
Defines Goal
 ↓
Provides Context
 ↓
Sets Constraints
 ↓
Agent
 ↓
Executes Work
 ↓
Human
 ↓
Supervises Outcome
```

This moves the human role toward:

* Management
* Direction
* Context setting
* Constraint setting
* Supervision

---

# Why the Distinction Matters

Understanding whether an AI system is simply answering or actually acting changes how you work with it.

With a chatbot, you might ask:

```text
How should I do this?
```

With an agent, you might instead define:

```text
Here is the outcome I need.

Here is the relevant context.

Here are the constraints.

Complete the task.
```

The skill therefore moves from only knowing how to ask questions toward knowing how to **direct work**.

---

# Key Takeaways

## 1. An Agent Works Toward a Goal

An agent is not limited to answering a question.

It aims to produce a real result.

---

## 2. An Agent Has a Workspace

It can operate where the work actually happens.

Examples from this lesson include:

* Files
* Documents
* Applications
* Connected tools

---

## 3. An Agent Uses Memory

Its memory comes from the context available to it.

Examples include:

* Notes
* Files
* Emails
* Previous work
* Instructions
* Examples

---

## 4. An Agent Takes Actions

It can move beyond generating text and perform actions inside a workspace.

---

## 5. An Agent Can Work Across Multiple Steps

It can continue working toward the objective instead of requiring the user to prompt every individual action.

---

## 6. An Agent Checks Progress

The system can observe the results of its actions and determine what should happen next.

---

## 7. Agentic Capability Is a Spectrum

AI systems can range from:

```text
Basic Chatbot
```

to:

```text
Chatbot with Context
```

to:

```text
Tool-Using Assistant
```

to:

```text
Multi-Step Agent
```

to:

```text
Agent Operating Across Multiple Systems Over Time
```

---

## 8. Agentic Is a Dial, Not a Switch

A system does not have to be completely autonomous to have agentic capabilities.

Different workflows can have different levels of agentic behavior.

---

## 9. The Same Tool Can Be Used Like a Chatbot or an Agent

The level of agentic behavior depends on:

* What you ask the system to do
* What information you connect to it
* What tools it can access
* What actions it can perform
* How many steps it can complete independently

---

## 10. The Simplest Distinction

The entire lesson can be summarized as:

> **A chatbot talks to you. An agent acts for you.**

An agent:

```text
Has a Goal
   +
Uses Memory
   +
Works in a Workspace
   +
Takes Actions
   +
Observes Results
   +
Continues Across Steps
   =
Works Toward an Outcome
```

---

An AI agent is a system that works toward a goal by acting inside a real workspace.

Unlike a traditional chatbot that mainly responds with text, an agent can potentially:

```text
Open Files
    ↓
Read Information
    ↓
Use Tools
    ↓
Take Actions
    ↓
Create Outputs
    ↓
Observe Results
    ↓
Continue Working
    ↓
Complete the Goal
```

Agents combine three important pieces:

```text
Brain
  +
Memory
  +
Workspace
```

They use these components in a continuous cycle to move toward a desired outcome.

Agentic capability is not all or nothing.

> **It is a dial, not a switch.**

The same AI system may behave like a simple chatbot in one workflow and like an agent in another.

The more the system:

* Pursues a goal
* Acts in a real workspace
* Uses connected context
* Performs multiple steps
* Tracks progress
* Works independently toward an outcome

the more agentic the workflow becomes.

As AI moves from simply answering questions toward performing work, the human role also changes.

Instead of only asking AI for information, people increasingly need to learn how to:

```text
Define Outcomes
      ↓
Provide Context
      ↓
Set Constraints
      ↓
Direct Agents
      ↓
Supervise Results
```

That mental model provides the foundation for understanding the next major components of an AI agent:

* The **brain** that reasons
* The **memory** it draws from
* The **workspace** where it acts

The broader shift is simple:

> **The future of working with AI is not only about chatting with it. It is increasingly about putting AI to work.**
