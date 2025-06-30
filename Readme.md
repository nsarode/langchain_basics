![Google Gemini](https://img.shields.io/badge/google%20gemini-8E75B2?style=for-the-badge&logo=google%20gemini&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C.svg?style=for-the-badge&logo=LangChain&logoColor=white)

# Overview

This repo contains code examples of using LangChain & its suite of LLM framework tools. The material uses and extends from following sources
1. [Gemini Developer API documentation](https://ai.google.dev/gemini-api/docs)
2. [First steps with LangChain tutorial by RealPython](https://realpython.com/courses/first-steps-langchain/)
3. [Building ambient agents with LangGraph](https://academy.langchain.com/courses/ambient-agents)

## Topics covered

Topics are organized by directories. If you are new to LangChain, start with the Basics directory. Advanced topics, as they get added will have self-explanatory directory names

### Basics

#### LangChain concepts

1. Use **chat models** with LangChain
2. Scaffold & reuse **prompts** with **templates**
3. Build **chains** to connect multi-step processes
4. Inspect input & outputs with **debug mode**



### Ambient_agents

Build and deploy ambient email agent to manage email

1. What are Ambient agents
2. LangGraph101
3. Building agents - LangGraph
4. Agent evaluation - using LangSmith
5. Human-in-the-Loop
6. Memory - how your agent remembers and adapts to your feedback over time
7. Deployment - LangGraph platform

# Summary & key takeaways

## Large language models (LLMs) 
- Deep learning models trained on massive amounts of text data to understand and generate human language
- They can perform tasks like answering questions, generating text, translating languages etc

## LangChain
- An open-source framework for building applications powered by LLMs
- Allows to build complex workflows by chaining together different steps e.g. retrieving info from database --> processing it with a LLM --> formatting the output for consumption 

## LangGraph

- Agent orchestration framework
- LangGraph platform can be used long-running and bursty workloads

## LangSmith

- Platform for obeservability, evaluation and prompt engineering. Can be leveraged for monitoring and improving long-running (ambient) agents

## Ambient agents

- Traditional agents are extremly capable at handling single user requests in the chat interface. Howoever agents have advanced tremendously and can be autonomously triggered by event streams (e.g. slack messages, github issues) & work in background for long periods of time and perform many tasks at once.
- Unlike chat agents, which need to respond instantly to user input, ambrient agents are designed for long-running, complex operations (thousands can run in the background, automating and orchestrating complex workflows)
- Even though the term 'ambient' suggests fully autonomous, ambient agents are not that. Having a human-in-the-loop is critical, where humans can approve/reject actions, edit tool calls, answer clarifying questions or even revisit and modify an agent's state. In fact, interaction with human-in-the-loop improves outcomes, increases trust and enhances agent memory & performance over time. This can be achieved through building a persistance layer with langGraph

# Prerequisites

- Python 3.11 or later
- API key - for LLM model of choice (Gemini, OpenAPI etc)

## Setup

```bash
conda create -n llm python=3.13
conda activate llm
pip install langchain google-genai langchain_google_genai # if using Google API
#pip install langchain langchain-openai openai  # if using OpenAI API
#pip install huggingface_hub # if using HuggingFace API
pip install python-dotenv
```

## OpenAI API key

Put your API key in `.env` file 

```bash
OPENAI_API_KEY=your_api_key
```
## LANGCHAIN_API_KEY

Needed for the Ambient agents project. Your `.env` file should contain the following lines

```bash
OPENAI_API_KEY=your_api_key
LANGCHAIN_API_KEY=your_api_key
LANGSMITH_TRACING=true
LANGSMITH_PROJECT="interrupt-workshop"

```

## Pyproject.toml 

Ambient agents project has `pyproject.toml` file. Activate virtual environment of choice (venv, conda) and install required packages as follows

```bash
pip install --upgrade pip
pip instal -e .

```