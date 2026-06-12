# Project 2: Sentiment Analysis + Text Summarizer

<image-card alt="Project 2 Screenshot" src="screenshot1.png" ></image-card>

**Built as part of my GenAI from Scratch Journey**

## Overview
Built a web tool that performs **Sentiment Analysis** and **Text Summarization** on any given text using free Hugging Face models.

## Tech Stack
- Hugging Face `transformers`
- Gradio (web interface)
- Google Colab (T4 GPU)
- Models: `distilbert-base-uncased-finetuned-sst-2-english` (sentiment) + `sshleifer/distilbart-cnn-12-6` (summarization)

## What I Built
- Combined tool for analyzing text (useful for reports, reviews, customer feedback)
- Clean Gradio interface with examples
- Proper error handling

## Key Learnings
- Working with different NLP pipelines
- Loading and using multiple models in one app
- Text preprocessing and output formatting
- Building practical GenAI tools

## Limitations
- Summarization works best with medium-length text
- Running on free Colab GPU has some speed limits

## How to Run
Open the notebook in Colab → Runtime → T4 GPU → Run all cells → Click public URL
