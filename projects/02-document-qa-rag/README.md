# Project 2: Document Q&A with RAG

## Overview
A Retrieval-Augmented Generation (RAG) system that allows users to upload PDFs and ask natural language questions about their content.

The system retrieves relevant sections and generates accurate answers.

## Features
- Loads and processes PDF documents
- Splits content into chunks
- Creates embeddings using free Hugging Face models
- Stores in local Chroma vector database
- Interactive Gradio UI for chatting with the document
- Tested with "Atomic Habits" book

## Tech Stack
- LangChain
- ChromaDB
- Hugging Face sentence-transformers
- Gradio (interactive UI)
- Python + Jupyter

## How It Works
1. Load PDF
2. Split into chunks
3. Create embeddings and store in vector store
4. Retrieve relevant chunks for user question
5. Generate answer using context

## Demo
Run the notebook and launch the Gradio interface to chat with the document.

## Key Learnings
- How RAG improves accuracy over plain prompting
- Importance of chunk size and overlap
- Building interactive demos with Gradio

## Future Improvements
- Add source citations with page numbers
- Support multiple documents
- Add evaluation using RAGAS
- Deploy as web app on Hugging Face Spaces

## Author
Niranjan  
MSc Business Analytics  
Building practical GenAI tools

**Date**: July 2026
