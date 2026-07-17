# Project 2: Document Q&A with RAG

## Overview
This project explores Retrieval-Augmented Generation (RAG) as a practical approach to question-answering over documents. Rather than treating RAG as a simple demo, the focus has been on understanding how retrieval quality changes when moving from clean, structured learning data to real-world business documents.

The project is intentionally split into two versions to make that learning progression visible.

## Project Evolution

### Baseline Version
The first version was built on a single PDF (*Atomic Habits*). This served as a controlled environment to implement the core RAG pipeline:

- Document loading and chunking
- Embedding generation
- Vector storage with ChromaDB
- Retrieval + Gradio interface

This version was useful for understanding the mechanics of RAG without the noise of messy real-world documents.

### Improved Version
The second version replaces the book with real Apple SEC filings (2025 Form 10-K and 2026 Form 10-Qs). This change was deliberate. Financial filings are longer, more complex, and less cleanly structured than a typical learning dataset. They introduce practical challenges such as:

- HTML noise and formatting artifacts
- Dense numerical tables
- Repeated boilerplate language
- Mixed narrative and structured content

Working with this type of data provides a more realistic test of whether a basic RAG system can surface useful information under less ideal conditions.

## Technical Approach

**Document Processing**
SEC filings were downloaded as HTML and cleaned using BeautifulSoup to remove scripts, styles, and excessive whitespace before chunking. This step alone significantly improved the quality of the text available for retrieval.

**Chunking Strategy**
Documents were split using a recursive character text splitter (chunk size 1000, overlap 200). This is a standard starting point and was kept intentionally simple so that retrieval behavior could be observed without introducing too many variables.

**Retrieval**
Embeddings were generated using `sentence-transformers/all-MiniLM-L6-v2` and stored in ChromaDB. The system retrieves the top 5 most relevant chunks for each query.

**Interface**
A Gradio interface was added to make testing interactive and to support faster iteration when inspecting retrieval quality.

## Evaluation

A fixed test set of 15 questions was created with ground truth answers derived directly from the filings. Questions covered three categories:

- Factual / numerical
- Segment performance
- Risk factors

A qualitative review was then performed on a sample of questions by comparing the retrieved context against the ground truth.

**Sample Scoring Results:**
- Good: 4
- Partial: 2
- Poor: 0

**Observations:**
- The system performs reliably on high-level financial figures and risk-related questions.
- Retrieval is generally stronger when the answer appears in narrative sections rather than dense tables.
- Performance is more variable on questions that require distinguishing between annual and quarterly figures.

These results are not presented as a complete evaluation. They are an initial signal of retrieval quality and a baseline for future improvement.

## Why This Matters
Many RAG tutorials stop at “it works on a clean PDF.” In practice, the harder and more relevant question is how the system behaves on real business documents that contain noise, repetition, and mixed content types. This project is an early attempt to move in that direction.

The evaluation, while still basic, is also intentional. Building a fixed test set and reviewing retrieval quality forces clearer thinking about what “good” looks like, rather than relying on a few manually tested examples.

## Limitations
- Chunking strategy has not yet been systematically tuned
- No automated metrics (e.g. faithfulness or context precision) have been applied yet
- Financial tables are not specially handled
- The test set is still relatively small

These limitations are acknowledged and form the basis for the next iteration.

## Next Steps
- Introduce automated evaluation metrics
- Experiment with different chunk sizes and retrieval settings
- Improve handling of tabular financial data
- Expand the test set
- Deploy a public version for external testing

## Author
Niranjan  
MSc Business Analytics  

This project is part of a broader effort to build practical GenAI systems grounded in real business data, with an emphasis on measurement and iterative improvement.

**Last Updated:** July 2026
