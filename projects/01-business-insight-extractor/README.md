# Project 1: Multi-Step Business Insight Extractor

## Overview
A prompt engineering tool that converts unstructured business text into structured, leadership-ready insights.

**Live Demo**: Gradio Interface (local)

## Features
- Multi-step prompt chaining
- Structured output: Summary, Metrics, Risks/Opportunities, Recommendations, Executive Summary, Confidence
- Interactive Gradio UI for easy testing
- No paid APIs used

## Tech Stack
- Python
- Advanced Prompt Engineering (Chain-of-Thought, Role Prompting, Few-Shot)
- Gradio (for interactive UI)
- Tested with Grok, Claude, and Gemini

## How to Run
1. Open `01-business-insight-extractor.ipynb`
2. Run the cells
3. Launch the Gradio interface at the end
4. Enter business text and get a ready-to-use prompt

## Example
**Input:** Q2 revenue grew 12% to $2.8B but margins declined due to higher costs.

**Output:** Structured insights with recommendations and executive summary.

## Key Learnings
- Importance of clear system prompts and output formatting
- How Chain-of-Thought improves reasoning quality
- Building interactive demos with Gradio

## Future Improvements
- Integrate direct LLM call (Grok API)
- Add JSON output option
- Support longer documents

## Author
Niranjan  
MSc Business Analytics  
Transitioning from Data Analytics to GenAI

**Date**: July 2026
