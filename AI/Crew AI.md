## Overview

It is a `framework` for orchestrating `autonomous agents` and `tools` to solve complex problems. It's designed to help you coordinate multiple large language models (LLMs) working together as agents.

#### Each agent in CrewAI has:

* A role.
* A goal.
* A set of tools or APIs it can use.
* Access to a shared memory for collaboration.

## How to Install CrewAI

```python
pip install crewai

# optional
pip install openai langchain
```

## Core Concepts

| Term    | What it means                                 |
| ------- | --------------------------------------------- |
| Agent   | A single AI entity with a goal and tools      |
| Tool    | API, database, plugin or model interface      |
| Crew    | A group of agents working together            |
| Task    | A job assigned to an agent                    |
| Memory  | Shared information between agents             |
| Process | Sequential or hierarchical interaction method |

# Structure

### Key Components

* Crew (Leadership)
* Task Management Workflow (Company Internal Workflow)
* Task
* Agents (Employee)

![[Pasted image 20251215215114.png]]


## How Flows Work

While Crews excel at autonomous collaboration, Flows provide structured automations, offering granular control over workflow execution.

![[image_flows_ai_diagram_1.png]]
## How to use

```bash
export OPENAI_API_KEY="your-api-key"
```

or set it directly in Python:

```python
os.environ["OPENAI_API_KEY"] = "your-api-key"
```

```python
from crewai import Agent

researcher = Agent(
	role="Stock Researcher",
	goal="Research Apple's stock performance over the past year",
	backstory="An expert in financial analysis"
)

sumarizer = Agent(
	role="Summary Writer",
	goal="Summarize stock trends and deliver a report",
	backstory="An AI trained in report generation"
)
```

```python
from crewai import Task

task1 = Task(
	description="Find out Apple's stock trends from 2023 to now".,
	expected_output="bullet-point list of key financial movements",
	agent=researcher
)

task2 = Task(
	description="Write a clear summary of the findings from the researcher.",
	expected_output="a short report with recommendations",
	agent=summarizer
)
```

```python
from crewai import Crew

crew = Crew(
	agents=[researcher, summarizer],
	tasks=[task1, task2],
	verbose=True
)

result = crew.run()
print(result)
```

## Creating a project

```
```
## Summary

It is necessary to set a env variable: `export OPENAI_API_KEY`.
A **Crew** has arrays of `Tasks` and `Agents`.
A `Task` has it own Agent and also description and expected_output.
A `Agent` has a `role` , `goal` and `backstory` and `tool`.
The imports are: from crewai import Crew, Task, Agent.
to run: result = crew.run().
The crewai framework has Crews and Flows.
==it uses `uv` as its dependency management and package handling tool==.


#tech #ai