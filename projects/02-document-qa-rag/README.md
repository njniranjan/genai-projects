# Project 2: Document Q&A with RAG

## Overview
This project demonstrates a Retrieval-Augmented Generation (RAG) system for answering natural language questions over documents.

There are **two versions** of this project to show progression:

| Version | Notebook | Data Used | Status |
|---------|----------|---------|--------|
| **Baseline** | `02a-rag-atomic-habits.ipynb` | Atomic Habits (book) | Completed |
| **Improved** | `02b-rag-apple-filings.ipynb` | Apple SEC Filings (10-K & 10-Q) | Completed |

## Version Comparison

### 1. Baseline Version (Atomic Habits)
- Simple RAG pipeline over a single PDF book
- Basic chunking + ChromaDB + Gradio interface
- Good starting point for learning RAG

### 2. Improved Version (Apple SEC Filings)
- Uses **real business documents** (Apple 10-K and 10-Q filings)
- Multiple documents loaded and cleaned
- Built a fixed evaluation test set (15 questions with ground truth)
- Qualitative evaluation of retrieval quality
- More realistic and portfolio-ready

## Key Improvements in the New Version
- Switched from toy data to real financial filings
- Added proper document cleaning (HTML → clean text)
- Created an evaluation test set with ground truth answers
- Performed qualitative scoring of retrieval quality
- Better structure and documentation

## Evaluation Results (Improved Version)

**Test Set Size:** 15 questions  
**Categories:** Factual, Segment Performance, Risk Factors

**Qualitative Scoring (sample of 6 questions):**
- Good: 4
- Partial: 2
- Poor: 0

The system shows strong retrieval on high-level sales figures and risk factors, with occasional weaker performance on specific quarterly vs annual numbers.

## Tech Stack
- LangChain
- ChromaDB
- Hugging Face Embeddings (`all-MiniLM-L6-v2`)
- Gradio
- BeautifulSoup (for cleaning SEC filings)

## Project Structure
