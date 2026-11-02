# The Agent Feedback Loop

So far, we have built a basic picture of an AI agent.

An agent has:

* A **brain**: the Large Language Model, or LLM
* **Memory**: the context it can use
* A **workspace**: the apps, folders, and systems where it can act

At this point, it may seem like working with an agent should be simple:

```text
Give the Agent a Goal
        ↓
Provide the Right Access
        ↓
Run the Agent
        ↓
Receive a Perfect Result
```

Sometimes this happens.

But often, the first attempt is not perfect.

The result may be:

* Too generic
* Missing an important constraint
* Based on the wrong source
* Technically complete but not useful
* Mostly correct but wrong on one important judgment

This does not always mean that the agent is incapable of performing the task.

Often, it means the agent needs better instructions, better context, better workspace access, or clearer feedback.

This is where the **feedback loop** becomes important.

---

# What Is the Feedback Loop?

The feedback loop is the process of:

1. Giving the agent a goal
2. Letting it perform the task
3. Reviewing what it produced
4. Inspecting how it performed the work
5. Identifying what went wrong
6. Adjusting the setup
7. Running the task again

A simple mental model is:

```text
Set Goal
   ↓
Agent Works
   ↓
Review Output
   ↓
Inspect the Path
   ↓
Identify the Problem
   ↓
Adjust the Setup
   ↓
Run Again
```

Each cycle helps improve the next attempt.

---

# Agents Rarely Get Everything Perfect on the First Attempt

A useful analogy is supervising a new intern.

You would probably not expect a new intern to receive a real task on their first day and return flawless work immediately.

Instead, you would expect something like:

```text
First Attempt
      ↓
Review
      ↓
Feedback
      ↓
Second Attempt
      ↓
Improvement
```

You would:

* Look over their work
* Identify what needs improvement
* Explain what should change
* Ask them to try again

The same principle applies to an agent.

---

# First Attempts Are Often Setup Problems

When an agent produces weak work, it is tempting to conclude:

```text
The agent cannot do this task.
```

But that conclusion may be wrong.

An agent is not a human teammate with:

* Full judgment
* Stable memory
* Deep understanding of your priorities

The system acts based on what you provide.

That includes:

```text
Instructions
     +
Context
     +
Workspace
```

Therefore, weak output may be caused by weak setup rather than weak capability.

---

# Evaluate the Entire Setup

After an agent completes a task, do not only ask:

> Was the output good?

Also ask:

> What did the agent have to work with?

Useful questions include:

* Was the goal clear?
* Did the agent have the right context?
* Did it have access to the right tools?
* Did it have access to the right applications?
* Did it understand what a good output should look like?

This changes the mindset from:

```text
Judge the Final Answer
```

to:

```text
Diagnose the Entire System
```

---

# The Feedback Loop in Practice

The overall process can be represented as:

```text
Goal
 ↓
Instructions
 ↓
Context
 ↓
Workspace
 ↓
Agent Attempt
 ↓
Output
 ↓
Review
 ↓
Feedback
 ↓
Adjust
 ↓
Run Again
```

The goal is not to repeatedly ask the same question.

The goal is to improve the underlying setup that produced the weak result.

---

# Inspect More Than the Final Output

The final output does not always tell you why something went wrong.

For example:

A polished brief may still be based on the wrong source.

```text
Polished Brief
     ↓
Looks Correct
     ↓
Wrong Source Used
```

A clean spreadsheet may look correct while an important rule was applied incorrectly.

```text
Clean Spreadsheet
      ↓
Looks Correct
      ↓
Incorrect Rule Applied
```

The result tells you **what** the agent produced.

It does not always tell you **how** the agent produced it.

And the problem often exists in the **how**.

---

# Inspect the Path the Agent Took

A more useful approach is to inspect the sequence of steps the agent followed.

You can ask the agent to document:

* What it inspected
* What it changed
* What it decided
* What it was unsure about

This gives you an auditable trail.

Instead of saying:

```text
Something about this result seems wrong.
```

you may be able to identify:

```text
The agent used the wrong file at Step 3.
```

or:

```text
The agent made the wrong judgment when applying this rule.
```

This makes the problem much easier to diagnose.

---

# Output vs Path

A useful distinction is:

```text
Output
   ↓
Tells You Whether There Is a Problem
```

while:

```text
Path
   ↓
Helps Tell You Where the Problem Happened
```

Both are important when evaluating agent performance.

---

# Agent Attempt

In AI discussions, an agent's full effort to complete a task may be called an:

* **Agent attempt**
* **Model run**

These terms refer to the full execution of the task.

A simple model is:

```text
Goal
 ↓
Agent Works
 ↓
Output
```

That complete process is the **attempt** or **run**.

---

# Agent Trajectory

The individual sequence of steps taken during the run is often called the agent's **trajectory**.

For example:

```text
Goal
 ↓
Open File
 ↓
Inspect Data
 ↓
Use Tool
 ↓
Make Decision
 ↓
Create Output
 ↓
Check Result
```

This sequence is the trajectory.

A simple distinction is:

```text
Attempt = The Full Run

Trajectory = The Path Through the Run
```

---

# Why the Trajectory Matters

When someone asks:

> Was the trajectory good?

they are not only asking whether the final result looked good.

They are asking whether the agent used a sensible process.

For example:

* Did it look in the right places?
* Did it use the right tools?
* Did it recover from mistakes?
* Did it stop at the correct time?
* Did it leave behind a useful output?

This is a deeper way of evaluating agent performance.

---

# Evaluate the Process, Not Just the Result

A good-looking result does not guarantee a good process.

The stronger evaluation approach is:

```text
Final Output
     +
Trajectory
     =
Better Understanding of Agent Performance
```

This lets you determine whether the agent:

* Used the right information
* Took the right actions
* Made the right decisions
* Used the right tools
* Completed the task properly

---

# The Three Main Levers

Once you have reviewed the output and trajectory, the next question is:

> What should be changed?

There are three main levers to adjust:

```text
1. Context

2. Workspace

3. Instructions
```

These three areas are the main parts of the setup that influence agent performance.

---

# Lever 1: Context

Start by checking the context.

Context is the information the agent uses while completing the task.

If the output is:

```text
Too Generic
```

or:

```text
Too Vague
```

the agent may not have received enough relevant context.

---

# Missing Context

Suppose the agent creates a generic result.

The issue may be:

```text
Missing Context
      ↓
Generic Output
```

The fix is to provide the missing information.

Examples from this lesson include:

* A missing file
* Client details
* A strong example of what good looks like

---

# Wrong Context

Sometimes the output is very specific but still wrong.

In this case, the problem may not be too little context.

The agent may have accessed the wrong information.

```text
Wrong Context
      ↓
Confident but Wrong Output
```

The fix is to ground the agent in the correct information.

---

# Context Diagnostic

A useful mental model is:

```text
Generic or Vague Output
        ↓
Check for Missing Context
```

and:

```text
Specific but Wrong Output
        ↓
Check for Wrong Context
```

The goal is to make sure the agent is working from the correct information.

---

# Lever 2: Workspace

The second lever is the agent's workspace.

Workspace problems appear when the agent cannot access something it needs.

For example:

```text
Agent Did Not Review Contracts
        ↓
Could Not Open Contracts
```

or:

```text
Agent Did Not Create Spreadsheet
        ↓
Had No Way to Create One
```

These are not reasoning failures.

They are **workspace access failures**.

---

# Workspace Access Failure

A workspace problem can be represented as:

```text
Correct Goal
    +
Correct Reasoning
    +
Missing Access
    =
Incomplete Task
```

The agent may understand exactly what it should do but still be unable to perform the action.

---

# Fixing Workspace Problems

The solution is to make sure the agent:

* Has access to the required applications
* Has access to the required tools
* Knows which tools or systems you want it to use

A useful diagnostic is:

```text
Agent Could Not Access Something
        ↓
Check Workspace
```

or:

```text
Agent Could Not Create Something
        ↓
Check Workspace
```

---

# Lever 3: Instructions

The third lever is the instructions you give the agent.

These instructions tell the system what you want it to do.

Even when the agent has:

```text
Correct Context
      +
Correct Workspace
```

it may still produce an output you do not want.

Examples include:

* Wrong format
* Wrong level of detail
* A judgment decision you would have made differently

This often indicates that something important was missing from the instructions.

---

# Hidden Requirements

Humans often have standards in their heads that are never clearly stated.

For example, you may know:

* The exact format you want
* The amount of detail expected
* Which constraints matter
* What a good result should look like

But if you never tell the agent, it has to make assumptions.

```text
Requirement Not Stated
        ↓
Agent Makes Assumption
        ↓
Unexpected Output
```

---

# Fixing Instruction Problems

The solution is straightforward:

> Say the part you left out.

For example:

### Name the Format

```text
Return the result as a one-page brief.
```

### State the Constraint

```text
Use only the information from the supplied documents.
```

### Define What Good Looks Like

```text
Keep the output concise and focused on the three most important issues.
```

The more clearly expectations are stated, the less the agent has to guess.

---

# Tacit Knowledge

A major part of getting strong results from agents is turning **tacit knowledge** into explicit instructions.

Tacit knowledge is the information you understand naturally from experience but may not normally write down.

For example:

```text
What You Know in Your Head
        ↓
Make It Explicit
        ↓
Agent Can Follow It
```

The agent cannot automatically know the hidden quality standards in your head.

You need to explain them.

---

# Choosing Which Lever to Adjust

When something goes wrong, diagnose the type of failure.

---

## If the Output Is Generic

Check:

```text
Context
```

You may need to provide more relevant information.

---

## If the Output Is Confidently Wrong

Check:

```text
Context
```

The agent may have used the wrong information.

---

## If the Agent Could Not Access Something

Check:

```text
Workspace
```

It may not have access to the required file, system, or application.

---

## If the Agent Could Not Create Something

Check:

```text
Workspace
```

It may not have the tool required to create the output.

---

## If the Format Is Wrong

Check:

```text
Instructions
```

You may not have specified the desired format.

---

## If the Detail Level Is Wrong

Check:

```text
Instructions
```

You may need to explain the expected level of detail.

---

## If the Agent Made the Wrong Judgment Call

Check:

```text
Instructions
```

You may need to explain what decision standard should be used.

---

# Feedback Loop Diagnostic Model

A useful troubleshooting model is:

```text
Output Is Too Generic?
        ↓
Improve Context
```

```text
Output Is Specific but Wrong?
        ↓
Correct the Context
```

```text
Agent Cannot Access or Create Something?
        ↓
Improve Workspace Access
```

```text
Output Is in the Wrong Format or Style?
        ↓
Improve Instructions
```

---

# Run the Agent Again

Once you identify the problem:

1. Adjust the context
2. Adjust the workspace
3. Adjust the instructions
4. Give feedback
5. Run the task again

The agent can repeat this process quickly.

```text
Attempt 1
   ↓
Review
   ↓
Adjust
   ↓
Attempt 2
   ↓
Review
   ↓
Adjust
   ↓
Attempt 3
```

Each cycle can improve the result.

---

# The Mistake Many People Make

A common pattern is:

```text
Write One Prompt
      ↓
Receive Mediocre Result
      ↓
Give Up
```

or:

```text
Write One Prompt
      ↓
Receive Mediocre Result
      ↓
Do the Task Manually
```

This skips the most important part of agentic work.

The stronger approach is:

```text
Write Prompt
   ↓
Run Agent
   ↓
Review Result
   ↓
Diagnose Setup
   ↓
Adjust
   ↓
Run Again
```

The feedback loop is where much of the improvement happens.

---

# Directing an Agent Does Not End When You Press Go

Starting the agent is only the beginning.

The human role continues after execution starts.

You need to:

* Review the result
* Inspect the path
* Identify problems
* Provide feedback
* Adjust the system
* Run another attempt

A useful way to think about it is:

```text
Set Direction
      ↓
Agent Executes
      ↓
Human Evaluates
      ↓
Human Refines
      ↓
Agent Improves
```

---

# The Full Agent Model

At this point, the basic model of an agent includes four important parts.

```text
                 AI AGENT

        ┌──────────┼──────────┐
        ↓          ↓          ↓

      BRAIN      MEMORY    WORKSPACE
       LLM       Context    Place to Act

                    +
                    ↓

              FEEDBACK LOOP
                    ↓
             Review + Improve
```

---

# Brain

The agent's brain is the **LLM**.

It:

* Reasons
* Interprets
* Plans
* Decides

But it does not have reliable memory of its own.

---

# Memory

The agent's memory comes from the **context** you provide or connect it to.

This helps the agent understand the specific task and situation.

---

# Workspace

The workspace is where the agent:

* Reads information
* Takes actions
* Creates outputs
* Leaves finished work

---

# Feedback Loop

The feedback loop is how the system improves.

You:

```text
Set Goal
   ↓
Review Output
   ↓
Review Trajectory
   ↓
Adjust Setup
   ↓
Run Again
```

The setup may be improved by changing:

```text
Context
Workspace
Instructions
```

---

# A Complete Agentic Workflow

The combined mental model is:

```text
Human Sets Goal
      ↓
Agent Uses LLM
      ↓
Agent Uses Context
      ↓
Agent Operates in Workspace
      ↓
Agent Produces Output
      ↓
Human Reviews Output
      ↓
Human Reviews Trajectory
      ↓
Human Identifies Problem
      ↓
Adjust Context / Workspace / Instructions
      ↓
Agent Runs Again
      ↓
Improved Output
```

---

# Why Feedback Matters

A mediocre first result does not necessarily mean:

```text
Agent Is Incapable
```

It may instead mean:

```text
Setup Needs Improvement
```

The feedback loop helps distinguish between the two.

Instead of immediately abandoning the workflow, you can improve the environment around the agent.

---

# Key Takeaways

## 1. Agents Often Need Multiple Attempts

A first attempt may be incomplete, generic, or misaligned.

This is normal.

---

## 2. Weak Output Is Often a Setup Problem

The issue may come from:

```text
Context
Workspace
Instructions
```

rather than from the agent's basic ability.

---

## 3. Review More Than the Final Output

A polished output can still come from a poor process.

Inspect how the agent reached the result.

---

## 4. The Full Run Is an Agent Attempt

The complete execution of a task can be called:

* An agent attempt
* A model run

---

## 5. The Sequence of Steps Is the Trajectory

The trajectory is the path the agent took while completing the task.

---

## 6. Good Trajectories Matter

Ask whether the agent:

* Looked in the right places
* Used the correct tools
* Recovered from mistakes
* Stopped at the correct time
* Produced a useful output

---

## 7. Context Is the First Lever

If the output is generic or based on incorrect information, improve the context.

---

## 8. Workspace Is the Second Lever

If the agent cannot access or create something, check its workspace and tools.

---

## 9. Instructions Are the Third Lever

If the output is in the wrong format, wrong level of detail, or makes the wrong judgment call, improve the instructions.

---

## 10. Make Tacit Knowledge Explicit

Do not assume the agent understands the quality standards in your head.

State them clearly.

---

## 11. Run the Feedback Loop

The process is:

```text
Set Goal
   ↓
Run Agent
   ↓
Review Output
   ↓
Inspect Trajectory
   ↓
Adjust
   ↓
Run Again
```

---

# Final Summary

An AI agent has:

```text
Brain
  ↓
LLM

Memory
  ↓
Context

Workspace
  ↓
Where It Reads and Acts
```

But these pieces alone do not guarantee excellent work.

Strong agentic work also requires a **feedback loop**.

The feedback loop allows you to:

```text
Run the Agent
      ↓
Review the Result
      ↓
Inspect the Path
      ↓
Identify the Problem
      ↓
Adjust the System
      ↓
Run Again
```

When the result is not good enough, there are three main levers to inspect:

```text
Context
   +
Workspace
   +
Instructions
```

If the output is too generic or grounded in the wrong information, improve the **context**.

If the agent cannot access or create something, improve the **workspace**.

If the output is in the wrong format, has the wrong detail level, or uses the wrong judgment standard, improve the **instructions**.

The key idea is:

> **Directing an agent does not end when you press go. That is where the feedback process begins.**

The real leverage comes from repeatedly improving the system until the agent becomes better at performing the task for you.
