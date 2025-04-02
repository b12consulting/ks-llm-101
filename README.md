# ks-llm-101

## Knowledge sharing on fundamentals of LLMs

In this repo we go over the basics of working with LLMs.  
Each topic is covered by a notebook:  
- [Chat Templates](./chat_template.ipynb) - What do LLMs actually receive when we send them a prompt? We discuss the concept of chat templates and how to are used to format conversations and tool calls in such the format expected by the LLM.
- [Tool Calling](./tool_calling.ipynb) - How to allow LLMs to make tool calls. This is a crucial ingredient in creating Agentic applications.
- [Structured Output](./structured_output.ipynb) - How to get LLMs to return structured output. This is a crucial ingredient in creating robust LLM applications.

We provide hands-on code examples with both OpenAI, Ollama and LangChain/LangGraph.

## Getting started

To run these examples, you will need an OpenAI API key and put it in a `.env` file in the root of the repo.
For part of the examples, you may also need an `HF_TOKEN`.  
Get it from [Hugging Face](https://huggingface.co/settings/tokens) and put it in the `.env` file as well.
Finally, you will need [`Ollama` installed](https://ollama.com/download) and running.  
For example on Linux:
```bash
curl -fsSL https://ollama.com/install.sh | sh
```
Once Ollama is installed, pull the `mistral-small` model as follows:
```
ollama pull mistral-small
```

To run the python examples, we setup an environment with `uv`. Install it as follows:
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```
Create and activate a virtual environment with the dependencies installed
```bash
uv sync --frozen
source .venv/bin/activate
```
You now have a virtual environment with the dependencies installed.
To run the notebooks, we recommend using VSCode with the Jupyter extension.
Alternatively, spin up a Jupyter server and open the notebooks in your browser.
