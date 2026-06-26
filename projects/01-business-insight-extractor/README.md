# Project 1: Multi-Step Business Insight Extractor

## Overview
This project uses advanced prompt engineering to transform unstructured business text (such as earnings reports, news articles, or internal memos) into structured, professional insights suitable for senior leadership and decision-makers.

**Goal**: Demonstrate the power of well-crafted prompts to extract actionable business intelligence without requiring complex model fine-tuning or paid APIs.

## Features
- Extracts key insights, metrics, risks, and opportunities from business text
- Generates structured recommendations with reasoning
- Produces a concise executive summary
- Includes confidence scoring to indicate reliability of the analysis
- Follows a consistent, professional output format

## How It Works
The project uses a carefully designed system prompt combined with Chain-of-Thought reasoning and a few-shot example. This guides the language model to:
1. Analyze the input text step by step
2. Stay grounded in the provided information (minimizing hallucinations)
3. Output results in a clean, standardized Markdown structure

## Example Output

### 1. Summary
Q2 2026 revenue reached $2.8 billion (+12% YoY), driven by strong enterprise segment growth. Operating margins declined from 18% to 15% due to higher cloud and marketing costs. Management guided for 8–10% revenue growth in the second half while noting supply chain risks and AI opportunities.

### 2. Key Insights & Metrics
- Revenue: $2.8B (+12% year-over-year)
- Operating margin declined from 18% → 15%
- Main cost drivers: Cloud infrastructure and marketing spend
- Enterprise segment was the primary growth driver

### 3. Risks and Opportunities
**Risks:**
- Supply chain disruptions in Asia
- Margin pressure from rising costs

**Opportunities:**
- AI-powered product offerings
- Continued enterprise segment growth

### 4. Actionable Recommendations
1. Accelerate AI product development to capitalize on identified growth opportunities.
2. Diversify supply chain sources in Asia to mitigate key operational risks.

### 5. Executive Summary
The company delivered solid top-line growth in Q2 but faced margin compression. While supply chain risks persist, clear opportunities exist in AI. Management expects continued revenue growth of 8–10% in H2 2026.

### 6. Confidence Level
**Level:** High  
**Reason:** All insights are directly supported by the provided earnings text.

## Tech Stack
- Python
- Prompt Engineering (Chain-of-Thought + Few-Shot)
- Large Language Models (tested with Claude, Grok, and Gemini)
- Google Colab / Jupyter Notebook

## How to Use

1. Open the notebook `01-business-insight-extractor.ipynb`
2. Replace the `sample_text` variable with your own business text
3. Run the cell to generate the full prompt
4. Copy the generated prompt and paste it into Claude, Grok, Gemini, or ChatGPT
5. Review and use the structured output

## Sample Input
Any business text such as:
- Earnings call transcripts
- Financial reports
- News articles
- Internal memos or strategy documents

## Future Improvements
- Add support for JSON output format
- Implement basic evaluation of output quality
- Extend to handle longer documents using chunking
- Add source citation when processing multiple documents

## Author
[Your Name]  
MSc Business Analytics  
Transitioning from Data Analytics to GenAI

**Date**: June 2026
