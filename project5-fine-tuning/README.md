# Project 5: Fine-Tuning a Small LLM for Technical Explanations (QLoRA)

![Fine-tuned Model Demo](screenshot.png)

**Built as part of my GenAI from Scratch Journey**

## Overview
I fine-tuned a small language model (`TinyLlama-1.1B`) using **QLoRA** (Quantized Low-Rank Adaptation) to improve its ability to give clear technical explanations. The goal was to make the model better at explaining complex AI/ML concepts in simple terms.

This project demonstrates practical knowledge of efficient fine-tuning techniques that are widely used in the industry.

## What I Built
- Fine-tuned a 1.1B parameter model using 4-bit quantization + LoRA
- Created a small custom dataset focused on technical explanations
- Trained the model on Google Colab T4 GPU
- Tested the model on technical questions

## Tech Stack
- **Transformers** + **PEFT** (Parameter-Efficient Fine-Tuning)
- **BitsAndBytes** (4-bit quantization)
- **LoRA / QLoRA**
- **TRL** (Transformer Reinforcement Learning library)
- Google Colab (Free T4 GPU)

## Key Learnings
- How to perform efficient fine-tuning using QLoRA on limited hardware
- Preparing custom datasets for instruction tuning
- Using `BitsAndBytesConfig` for memory-efficient training
- Understanding the trade-offs between model size, training time, and output quality
- The full fine-tuning pipeline (loading → quantization → LoRA → training → inference)

## Limitations (Honest)
- The base model (`TinyLlama-1.1B`) is very small, so the improvement in output quality was limited.
- Responses can sometimes be repetitive or not fully coherent.
- Only trained for a small number of steps due to free resource constraints.
- Output quality is noticeably lower than larger models (7B+).

These limitations are mainly due to using free Colab resources. With a larger base model and more training data/steps, the results would be significantly better.

## How to Run
1. Open the notebook in Google Colab
2. Set runtime to **T4 GPU**
3. Run all cells in order
4. The fine-tuned model is saved in the `fine_tuned_technical_model` folder

## Future Improvements
- Use a stronger base model (e.g. Phi-2, Gemma-2B, or Mistral-7B)
- Create a larger and higher-quality dataset
- Train for more steps with better hyperparameters
- Add evaluation metrics (e.g. using another LLM as judge)
- Deploy the model using vLLM or Hugging Face Inference Endpoints

## Key Takeaway
Even with a small model and limited resources, I was able to complete the full fine-tuning pipeline using QLoRA. This project helped me understand efficient fine-tuning techniques that are essential for real-world GenAI applications.

**Completed**: June 2026
