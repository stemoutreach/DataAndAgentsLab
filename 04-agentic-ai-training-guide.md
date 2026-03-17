# Agentic AI Training Guide

This guide prepares students for challenge-style work that involves prompts, tools, workflows, and multi-step AI systems in **Jupyter notebooks**.

The focus is not just on getting an answer from a model. The focus is on learning how to guide a system, check its output, and improve it.

---

## Learning Goals

By the end of this guide, students should be able to:
- explain the basic idea of an LLM-powered system
- write clearer prompts
- separate role, task, constraints, and output format
- use Python functions as tools
- understand what context needs to be passed forward
- reason through a multi-step workflow
- evaluate weak or misleading outputs
- test and improve prompts
- explain where human judgment is still needed

## Core Skills Needed First

Before starting this path, students should be comfortable with:
- Jupyter notebook basics
- Python variables, lists, dictionaries, loops, and functions
- reading starter code
- basic debugging
- using AI carefully while learning

Helpful support guides:
- [06 Python for Jupyter Notebook Challenges](./06-python-for-jupyter-notebook-challenges.md)
- [08 APIs, JSON, and Live Data](./08-apis-json-and-live-data.md)

## Part 1: What Agentic AI Means

A simple way to think about agentic AI:

An AI system is given a goal, some instructions, and sometimes tools. It works through steps to try to complete the task.

Students should understand that:
- the model does not “just know” everything
- the prompt matters
- the tools matter
- the workflow matters
- humans still need to verify results

## Part 2: Prompt Structure

Students should practice writing prompts that include:
- role
- task
- constraints
- context
- output format

Example structure:
- You are helping with...
- Your task is to...
- Only use...
- Return the answer as...

Students should learn that vague prompts often create vague outputs.

### Worked Example: Weak vs Strong Prompt

Weak prompt:

```text
Summarize this alert.
```

Possible weak output:

```text
Something may be wrong with the machine.
```

Stronger prompt:

```text
You are a maintenance assistant. Summarize this alert in 1 sentence. Include machine ID, temperature, and whether review is needed.
```

Possible stronger output:

```text
Machine M-102 is at 89.7 and needs review.
```

What to notice:
- the stronger prompt gives role, task, and output expectations
- the result is more specific and easier to use
- prompt structure changes output quality

## Part 3: Functions as Tools

A big part of agentic work is turning Python functions into useful tools.

Students should practice:
- defining a function clearly
- choosing inputs
- returning clean outputs
- keeping tool behavior simple and predictable
- understanding why the tool exists

This is where Python skill matters a lot.

### Worked Example: Tool Function

```python
def build_alert_record(machine_id, temperature, status):
    return {
        "machine_id": machine_id,
        "temperature": temperature,
        "status": status
    }

print(build_alert_record("M-102", 89.7, "review"))
```

Expected output:

```python
{'machine_id': 'M-102', 'temperature': 89.7, 'status': 'review'}
```

What to notice:
- the function returns structured data
- that structure can be reused in later steps
- tools make workflows more reliable

## Part 4: Context and State

In multi-step systems, one step often produces information that the next step needs.

Students should ask:
- What information was created?
- What needs to be passed forward?
- What happens if something important is missing?
- Is the next step using the right context?

This can be explained simply as:
**What does the system need to remember?**

## Part 5: Workflow Thinking

Students should practice breaking an AI system into steps, such as:
1. gather input
2. call a tool
3. summarize findings
4. decide what to do next
5. return a final answer

This helps students understand that good systems are often built from smaller parts.

### Worked Example: Small Workflow

```python
record = build_alert_record("M-102", 89.7, "review")
prompt = f"Summarize this alert in 1 sentence: {record}"
print(prompt)
```

Expected output:

```python
Summarize this alert in 1 sentence: {'machine_id': 'M-102', 'temperature': 89.7, 'status': 'review'}
```

What to notice:
- one step builds structure
- the next step uses that structure to prepare an AI call
- workflows connect steps together

## Part 6: Evaluating Output Quality

Students should be able to tell the difference between:
- output that sounds confident
- output that is actually useful
- output that follows the format
- output that ignores constraints
- output that needs revision

Questions to ask:
- Did it answer the real task?
- Did it follow the required format?
- Did it make things up?
- Did it use the available information correctly?

## Part 7: Testing and Debugging Agents

Students should test:
- a normal case
- a missing-information case
- a confusing case
- an edge case
- a case where the output format matters a lot

Helpful habits:
- test one step at a time
- inspect intermediate outputs
- change one prompt element at a time
- compare weak vs improved prompts

## Part 8: Reliability and Guardrails

Students should understand:
- LLMs can hallucinate
- tool outputs can be incomplete
- vague instructions cause problems
- risky outputs may need human review

Guardrail ideas:
- require a structured output format
- restrict what tools can be used
- check for missing fields
- add simple validation steps
- require explanation before final output

## Part 9: Using AI Well in Agentic Work

Good uses of AI:
- explain why a prompt is weak
- suggest a clearer output format
- help debug a Python function
- compare two workflow ideas
- explain why a tool call failed

Weak uses of AI:
- blindly accepting the first response
- assuming a nice-looking answer is correct
- using AI to avoid understanding the workflow
- submitting a system the student cannot explain

## Practice Checklist

Students should be able to:
- explain what an LLM-based system is doing
- write a prompt with role, task, constraints, and format
- define a simple function as a tool
- explain what context needs to be passed forward
- describe a small multi-step workflow
- notice a weak or misleading output
- improve a prompt after testing
- explain where human review is still needed
