# Project 2: Document Q&A with RAG

## Overview
This project implements a **Retrieval-Augmented Generation (RAG)** system that allows users to upload PDFs (books, reports, research papers, etc.) and ask natural language questions about their content.

The system retrieves relevant sections from the document and generates accurate, cited answers.

## Features
- Loads and processes PDF documents
- Splits content into manageable chunks
- Creates vector embeddings using free Hugging Face models
- Stores embeddings in ChromaDB (local vector store)
- Retrieves relevant context and generates answers
- Built entirely with free, open-source tools

## Tech Stack
- **LangChain** – Framework for RAG pipeline
- **ChromaDB** – Local vector database
- **Hugging Face sentence-transformers** – Free embeddings
- **PyPDFLoader** – PDF parsing
- Python + Jupyter Notebook

## How It Works
1. Load PDF document
2. Split into chunks
3. Create embeddings and store in vector database
4. Retrieve relevant chunks for a user question
5. Generate answer using context (tested with Grok)

## Example Usage

**Question:** What are the 4 laws of behavior change in Atomic Habits?

**Answer:** 
1. Make it obvious
2. Make it attractive
3. Make it easy
4. Make it satisfying

(The system retrieves relevant sections from the book and generates the answer.)

## How to Run
1. Place your PDF in the project folder
2. Update the `pdf_path` in the notebook
3. Run the cells sequentially
4. Ask questions using the `ask_question()` function

## Future Improvements
- Add source citations with page numbers
- Add Gradio UI for interactive chat
- Support multiple documents
- Add evaluation using RAGAS
- Deploy as a web app on Hugging Face Spaces

## Author
Niranjan  
Building practical GenAI tools

**Date**: July 2026
