![Google Gemini](https://img.shields.io/badge/google%20gemini-8E75B2?style=for-the-badge&logo=google%20gemini&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C.svg?style=for-the-badge&logo=LangChain&logoColor=white)

# Overview

This repo contains code examples of using LangChain. The material follows and extends from following sources
1. [Gemini Developer API documentation](https://ai.google.dev/gemini-api/docs)
2. [First steps with LangChain tutorial by RealPython](https://realpython.com/courses/first-steps-langchain/)

## Topics covered

1. Use **chat models** with LangChain
2. Scaffold & reuse **prompts** with **templates**
3. Build **chains** to connect multi-step processes
4. Inspect input & outputs with **debug mode**

# Basics
## Large language models (LLMs) 
- Deep learning models trained on massive amounts of text data to understand and generate human language
- They can perform tasks like answering questions, generating text, translating languages etc

## LangChain
- An open-source framework for building applications powered by LLMs
- Allows to build complex workflows by chaining together different steps e.g. retrieving info from database --> processing it with a LLM --> formatting the output for consumption 


# Prerequisite
You'll need to set up your own API key (LLM of your choice)
API key - Gemini used here, but any of HuggingFace, Anthropic, OpenAPI would work

# Setup

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
