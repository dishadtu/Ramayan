# Ramayan
This repository contains Python code for evaluating fine-tuned Language Models (LLMs) on educational tasks related to the Ramayana. It demonstrates setup and assessment of various LLMs using QLora fine-tuning, with evaluation metrics including hallucination, faithfulness, and answer relevancy.

# Overview
The project includes several Jupyter notebooks that:

**Process PDF Documents**: Load and index documents from the Ramayana.

**Query Models**: Utilize various fine-tuned language models to answer specific questions.

**Evaluate Responses**: Assess the performance of the models using different evaluation metrics.

# Notebooks and Scripts
**1. RAMGPT_Openchat_3_5.ipynb**

**Description:** 

Implements a RAG pipeline using the OpenChat 3.5 model. Loads PDF documents, creates an index, queries the model, and evaluates the responses.

**Features:**
Load and index documents.
Query using OpenChat 3.5.
Evaluate using metrics like Answer Relevancy and Faithfulness.

**2. LLAMA2_zephyr7B.ipynb**

**Description:**

Uses the Zephyr 7B model for the RAG pipeline. Similar to the OpenChat implementation but with different model configurations and evaluation criteria.

**Features:**
Load and index documents.
Query using Zephyr 7B.
Evaluate using metrics such as Contextual Relevancy and Hallucination.

**3. NurtureAI_Model.ipynb**

**Description**: Implements a RAG pipeline using the NurtureAI model. This notebook follows similar steps as the other implementations but with specific configurations for NurtureAI.
**Features**:
Load and index documents.
Query using NurtureAI.
Evaluate using various metrics such as Answer Relevancy, Faithfulness, and Contextual Relevancy.


# Installation
Ensure you have Python 3.8 or later. Install the required packages using:
pip install pypdf transformers einops accelerate langchain bitsandbytes llama_index sentence_transformers llama-index-llms-huggingface llama-index-embeddings-langchain llama-index-embeddings-huggingface -U deepeval

# Setup
Download the PDF Documents: Place your PDF files in the ./Data directory or adjust the path in the scripts as needed.

API Access: Log in to Hugging Face CLI using your credentials:
huggingface-cli login

Adjust Configurations: Modify model names, paths, and evaluation parameters in each notebook as needed.

# Running the Notebooks
Open each notebook in Jupyter or Colab and run the cells sequentially to execute the RAG pipeline, query the model, and evaluate the results.

# Evaluation Metrics
**Answer Relevancy:** Measures how well the answer aligns with the question.

**Faithfulness:** Checks if the answer accurately reflects the content of the documents.

**Contextual Relevancy:** Assesses the relevance of the context used in generating the answer.

**Hallucination:** Identifies whether the model generates incorrect or fabricated information.

**Toxicity:** Evaluates the presence of harmful or inappropriate content.

# Acknowledgements

**Hugging Face**: For providing pre-trained models.

**Langchain**: For tools used in embedding and indexing.

**DeepEval**: For evaluation metrics.
