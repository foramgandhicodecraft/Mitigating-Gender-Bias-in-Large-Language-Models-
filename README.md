# Mitigating Gender Bias in LLMs through Prompt-Level Fairness Intervention

A lightweight, model-agnostic framework that detects bias-prone prompts and injects context-aware fairness guidelines - **no retraining or parameter modification required.**

> Research conducted under the guidance of **Dr. Rupa Mehta**, SVNIT Surat.

## Overview

LLMs inherit gender stereotypes from training data. Instead of expensive retraining, this framework intervenes at the **prompt level** — classifying input prompts, generating targeted fairness constraints, and appending them before generation.

**Pipeline:**  
Input Prompt → Preprocessing → Prompt Classification (Question / Creative / Other) → Fairness Guideline Generation → Fair Prompt Construction → Bias Evaluation

## Key Results

| Metric | Value |
|---|---|
| Bias reduction (Mistral-7B) | **95.9%** of biased outputs corrected |
| Bias reduction (DeepSeek-7B) | **96.0%** of biased outputs corrected |
| Semantic preservation | 4.50 / 5.00 |
| Fluency | 4.38 / 5.00 |
| Classification accuracy | 90.8% |

## Tech Stack

- **Classification:** `facebook/bart-large-mnli` (zero-shot)
- **Generation:** `Mistral-7B-Instruct-v0.3`, `DeepSeek-7B`
- **Dataset:** 250 expert-curated prompts (Question: 98, Creative: 87, Other: 65)
- **Evaluation:** Bias Score, Gender Neutrality Index, Fleiss' κ = 0.78

# Remarks

If you find this work useful or are working on similar projects, feel free to reach out - I'd love to talk about it!

## License

This project is for academic and research purposes.
