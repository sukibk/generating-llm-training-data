# 🖼️ Prompt Simplifier for Text-to-Image Models

This project builds a **prompt simplifier** for enhanced MidJourney prompts. It uses OpenAI's GPT-4o model to reverse engineer complex, high-quality prompts into simple, base-level prompts that a user might have originally typed in a text-to-image model.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-repo/prompt-simplifier/blob/main/prompt_simplifier.ipynb)

---

## 🔧 Features

- Loads 1000 high-quality MidJourney prompts from HuggingFace 🤗
- Extracts the core enhanced prompt from each entry
- Uses GPT-4o to reverse-engineer a simplified version of each prompt
- Saves the dataset as `training_data.jsonl` for further use in finetuning or analysis

---

## 🚀 Quickstart

1. **Open in Google Colab**
2. **Install dependencies**:
   ```python
   !pip install -qU openai datasets
