# Hybrid RAG Document Q&A

A document question-answering app built with LangChain, Streamlit, and Groq.
It combines keyword search (BM25) and semantic search (embeddings in Chroma)
and returns answers with page-level citations.

## Features
- PDF loading and overlapping chunking
- Hybrid retrieval with EnsembleRetriever
- Strict, context-only answers with sources
- Streamlit web interface

## Setup
1. Clone the repo and create a virtual environment:
   python -m venv venv
   source venv/bin/activate
2. Install dependencies:
   pip install -r requirements.txt
3. Create a `.env` file with your key:
   GROQ_API_KEY=your_key_here
4. Put a PDF in the `data/` folder and update the file name in `app.py` if needed.
5. Run the app:
   streamlit run app.py

## Tech stack
LangChain, Groq (Llama 3.3 70B), HuggingFace embeddings, Chroma, BM25, Streamlit

## Limitations
Answer quality depends on retrieval. No reranker or automated evaluation yet.