
# 🖼️ Prompt Simplifier for Text-to-Image Models

This project builds a **prompt simplifier** for enhanced MidJourney prompts. It uses OpenAI's GPT-4o model to reverse engineer complex, high-quality prompts into simple, base-level prompts that a user might have originally typed in a text-to-image model.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sukibk/generating-llm-training-data/blob/main/Untitled0.ipynb)

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
   ```

3. **Authenticate with OpenAI**:
   ```python
   import getpass, os
   os.environ["OPENAI_API_KEY"] = getpass.getpass("Enter your Open AI API key:")
   ```

4. **Run the pipeline**:
   - Load the dataset
   - Extract enhanced prompts
   - Generate simple prompts with GPT-4o
   - Save results to a `.jsonl` file

---

## 📦 Output Format

The final `training_data.jsonl` will contain objects like:

```json
{
  "enhanced_prompt": "Ultrarealistic photo of a radiant Labrador Retriever, tongue lolling out in sheer joy, standing atop a grand championship podium",
  "simple_prompt": "A champion Labrador Retriever"
}
```

---

## ⚠️ Note on Compatibility

There may be dependency warnings related to `torch` and `nvidia-cuda-*` packages during installation. These do not affect the prompt simplification functionality if you're not using GPU-dependent models like PyTorch in this notebook.

---

## 📚 Dataset Source

- [MidJourney Prompts - High Quality](https://huggingface.co/datasets/gaodrew/midjourney-prompts-highquality)

---

## ✨ Credits

- OpenAI GPT-4o for prompt generation
- HuggingFace Datasets for prompt loading
- You, for running this cool project 🙌

---

## 📄 License

MIT License
