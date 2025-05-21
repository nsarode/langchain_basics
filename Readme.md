# Basics
## Large language models (LLMs) 
- Deep learning models trained on massive amounts of text data to understand and generate human language
- They can perform tasks like answering questions, generating text, translating languages etc

## LangChain
- An open-source framework for building applications powered by LLMs
- Allows to build complex workflows by chaining together different steps e.g. retrieving info from database --> processing it with a LLM --> formatting the output for consumption 


# Prerequisite
API key - Gemini used here, but any of HuggingFace, Anthropic, OpenAPI would work

# Setup

```bash
conda create -n llm python=3.13
conda activate llm
pip install google-generativeai # if using Google API
pip install langchain langchain-openai openai  # if using OpenAI API
pip install huggingface_hub # if using HuggingFace API
pip install python-dotenv
pip install pillow # to read and manipulate images
```

## OpenAI API key

Put your API key in `.env` file 

```bash
OPENAI_API_KEY=your_api_key
```
