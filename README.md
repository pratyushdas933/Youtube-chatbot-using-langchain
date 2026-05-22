# YouTube AI Chatbot using LangChain & RAG

An AI-powered YouTube Question-Answering chatbot built using LangChain, Hugging Face, FAISS, and Retrieval-Augmented Generation (RAG).
This project extracts transcripts from YouTube videos, converts them into vector embeddings, stores them in a FAISS vector database, and allows users to ask context-aware questions directly from video content.

# Project Overview
This project demonstrates how Large Language Models (LLMs) can interact with long-form video content using semantic search and retrieval pipelines.
Instead of manually watching an entire YouTube video, users can:
* Ask questions about the video
* Retrieve relevant transcript sections
* Generate intelligent context-aware answers
* Perform semantic search over video content

The system uses:
* YouTube Transcript API for transcript extraction
* LangChain for orchestration
* Hugging Face embeddings for vectorization
* FAISS for vector similarity search
* RAG pipeline for grounded response generation


# Features
## ✅ YouTube Transcript Extraction
Automatically fetches subtitles/transcripts from YouTube videos.
## ✅ Text Chunking
Splits long transcripts into manageable semantic chunks for efficient retrieval.
## ✅ Vector Embeddings
Converts text chunks into dense vector embeddings using Hugging Face sentence transformers.
## ✅ FAISS Vector Database
Stores embeddings for fast semantic similarity search.
## ✅ Retrieval-Augmented Generation (RAG)
Retrieves the most relevant transcript chunks before generating responses.
## ✅ Context-Aware Question Answering
Allows users to ask natural language questions directly related to the video.
## ✅ Semantic Search

Finds relevant information even when exact keywords are not present.


# Tech Stack

| Technology             | Purpose                         |
| ---------------------- | ------------------------------- |
| Python                 | Core programming language       |
| LangChain              | LLM orchestration framework     |
| Hugging Face           | Embeddings & transformer models |
| FAISS                  | Vector similarity search        |
| YouTube Transcript API | Transcript extraction           |
| Sentence Transformers  | Text embedding generation       |
| Jupyter Notebook       | Development environment         |



# System Architecture

```text
User Question
      ↓
YouTube Transcript Extraction
      ↓
Text Chunking
      ↓
Embedding Generation
      ↓
FAISS Vector Store
      ↓
Semantic Retrieval
      ↓
LLM Response Generation
      ↓
Final Context-Aware Answer
```


# Project Workflow

## 1️Transcript Extraction

The application extracts transcript data from a YouTube video using the video URL.

Example:

```python
transcript = YouTubeTranscriptApi.get_transcript(video_id)
```


## Text Preprocessing & Chunking

The transcript is split into smaller chunks to:

* improve retrieval accuracy
* reduce token overload
* optimize semantic search



## Embedding Generation

Each chunk is converted into vector embeddings using Hugging Face embedding models.

Example:

```python
HuggingFaceEmbeddings()
```



## FAISS Vector Storage

Embeddings are stored inside a FAISS vector database for efficient nearest-neighbor retrieval.


## Semantic Retrieval

When a user asks a question:

* the query is embedded
* relevant transcript chunks are retrieved
* context is passed into the LLM


## Response Generation

The LLM generates a grounded answer using retrieved transcript context.

This reduces hallucination and improves answer relevance.



# Example Use Cases

## Example Questions

* “What is the main topic of the video?”
* “Summarize the explanation of neural networks.”
* “What tools were mentioned in the tutorial?”
* “Explain the key concepts discussed at the end.”

# Why This Project Matters

This project demonstrates practical implementation of:

* Retrieval-Augmented Generation (RAG)
* Vector databases
* Semantic search systems
* LLM orchestration
* AI-powered information retrieval

It reflects real-world AI engineering workflows used in:

* AI assistants
* enterprise search systems
* knowledge retrieval applications
* intelligent chatbots



# Installation

## Clone Repository

```bash
git clone https://github.com/your-username/youtube-ai-chatbot.git
cd youtube-ai-chatbot
```



## Install Dependencies

```bash
pip install -r requirements.txt
```



# Usage

Run the notebook:

```bash
jupyter notebook
```

Open:

```text
youtube_chatbot_langchain.ipynb
```

Then:

1. Add a YouTube video URL
2. Generate transcript embeddings
3. Ask questions about the video



#  Required Libraries

```python
langchain
faiss-cpu
sentence-transformers
huggingface-hub
youtube-transcript-api
transformers
```

# Future Improvements

* Streamlit/Web App deployment
* Multi-video support
* Conversation memory
* PDF export of summaries
* Hybrid search (keyword + semantic)
* GPU acceleration
* OpenAI/Groq integration
* Persistent vector database storage



# Key AI Concepts Demonstrated

| Concept           | Description                               |
| ----------------- | ----------------------------------------- |
| RAG               | Combines retrieval with generation        |
| Embeddings        | Numerical vector representation of text   |
| Vector Search     | Semantic similarity retrieval             |
| Chunking          | Splitting long text into smaller segments |
| LLM Orchestration | Managing prompts and retrieval pipelines  |



# Learning Outcomes

Through this project, I learned:

* Building end-to-end RAG pipelines
* Implementing semantic retrieval systems
* Working with vector databases
* Using LangChain for LLM workflows
* Integrating Hugging Face models
* Designing scalable AI chatbot architectures





# Author
Developed by Pratyush Das

* AI Engineering
* LLM Applications
* Data Analytics
* Automation Systems
* Retrieval-Augmented Generation (RAG) Systems
