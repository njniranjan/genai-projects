# Project 4: AI Research Assistant with Memory

![Project 4 Screenshot](screenshot4.png)

**Built as part of my GenAI from Scratch Journey**

## Overview
I built an interactive AI Research Assistant that can **remember important information** from conversations using a vector database (FAISS). The assistant uses embeddings to retrieve relevant past context and generate responses.

This project demonstrates core concepts of **Retrieval-Augmented Generation (RAG)** and memory systems in a conversational interface.

## Features
- Short-term conversation history
- Long-term memory using vector embeddings (FAISS)
- Semantic search to recall relevant past information
- Clean and simple Gradio chat interface

## Tech Stack
- **Sentence Transformers** (for embeddings)
- **FAISS** (vector database for long-term memory)
- **Hugging Face Transformers** (TinyLlama-1.1B-Chat model)
- **Gradio** (web interface)
- Google Colab (T4 GPU)

## How It Works
1. User messages are embedded using `all-MiniLM-L6-v2`
2. Relevant past information is retrieved from the FAISS vector store
3. The retrieved context is injected into the prompt
4. The LLM generates a response using both current input and memory
5. Important conversations are saved back into long-term memory

## Limitations (Honest)
- The model used (`TinyLlama-1.1B-Chat-v1.0`) is very small, so memory recall and instruction following are limited.
- Responses can sometimes be irrelevant or repetitive.
- Memory works within a single session only (resets when the notebook restarts).
- This project focuses more on demonstrating the **architecture** rather than perfect output quality.

These limitations are due to free resource constraints. In a production setting, a larger model (7B+) would significantly improve performance.

## Key Learnings
- How to implement basic long-term memory using vector stores
- Combining retrieval with language model generation
- Building interactive GenAI applications with Gradio
- Understanding the trade-off between model size and capability in free environments
- Importance of prompt engineering when working with small models

## How to Run
1. Open the notebook in Google Colab
2. Change runtime to **T4 GPU**
3. Run all cells in order
4. Use the public Gradio link to chat with the assistant

## Future Improvements
- Use a larger model (e.g., Mistral-7B or Llama-3-8B)
- Add better memory management and summarization
- Implement persistent memory storage
- Add tool use (web search, calculator, etc.)
