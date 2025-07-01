# 🧠 Hermes‑Lite: Instruction-Tuned LLaMA 3.1 8B by Nous Research (PEFT-Optimized)

**A lightweight, LoRA-finetuned variant of the Hermes 3 LLaMA 3.1‑8B model for efficient, instruction-following language tasks.**

[![Model](https://img.shields.io/badge/model-Hermes--3--LLaMA--3.1--8B-purple)]() [![License: Apache-2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)]() [![🤗 Transformers](https://img.shields.io/badge/HuggingFace-Compatible-yellow.svg)]()

---

## 📖 Overview

**Hermes‑Lite** builds on the impressive instruction-following capabilities of [Nous Research's Hermes 3 LLaMA 3.1 8B model](https://huggingface.co/NousResearch/Hermes-3-Llama-3.1-8B), using **parameter-efficient fine-tuning (PEFT)** via **LoRA** to adapt the model for your own dataset or tasks without the need for full-scale retraining.

This notebook walks through:
- Loading and preparing the base LLaMA 3.1 8B model
- Applying LoRA adapters using Hugging Face's PEFT
- Finetuning on instruction-style datasets
- Saving and testing the resulting checkpoint

---

## 🧪 Key Features

✅ Based on **Hermes 3 LLaMA 3.1 8B**  
✅ Plug-and-play **LoRA adapter** finetuning  
✅ Instruction-following dataset integration  
✅ Compatible with `transformers`, `peft`, `accelerate`, `bitsandbytes`  
✅ Evaluation-friendly with logging and sample inference  

---

## 🛠 Setup

> **Requirements:** Python 3.10+, CUDA (for GPU), and the following libraries:

```bash
pip install -r requirements.txt
# Key dependencies:
# transformers, peft, accelerate, datasets, bitsandbytes, trl, einops
```

---

## 🚀 How to Use

### 🔧 Clone & Prepare

```bash
git clone https://github.com/yourhandle/hermes-lite.git
cd hermes-lite
```

### 💻 Run the Notebook

```bash
jupyter notebook Finetuning_Llama_3_1_8B.ipynb
```

> Optionally convert to script:
```bash
jupyter nbconvert --to script Finetuning_Llama_3_1_8B.ipynb
python Finetuning_Llama_3_1_8B.py
```

---

## 📂 Notebook Sections

| Step | Description |
|------|-------------|
| ✅ Model Load | Loads `NousResearch/Hermes-3-Llama-3.1-8B` |
| ✅ Tokenizer | Applies appropriate tokenizer config |
| ✅ Dataset | Loads your dataset for SFT (e.g., Alpaca-style) |
| ✅ LoRA Config | Adds LoRA adapters via PEFT |
| ✅ Training | Runs SFT using HuggingFace Trainer |
| ✅ Save & Push | Saves adapter + base, or pushes to Hub |
| ✅ Eval | Performs inference + evaluation post training |

---

## 🔍 Evaluation

- Generates model outputs on sample prompts
- Logs training metrics: loss curves, epochs, steps/sec
- Optional: upload to [Hugging Face Hub](https://huggingface.co/)

---

## 📌 Example Output

```text
### Instruction:
Write a short summary of the Great Wall of China.

### Response:
The Great Wall of China is a historic fortification built to protect Chinese states from invasions. Stretching over 13,000 miles, it symbolizes strength, perseverance, and architectural brilliance.
```

---

## 🛣️ Roadmap

- [x] Hermes-3 8B finetuning with PEFT
- [x] Alpaca-format SFT dataset
- [ ] Support multi-turn chat format
- [ ] Merge and quantize weights for deployment
- [ ] Streamlit/Gradio inference demo

---

## 🤝 Contributing

Pull requests welcome! If you have custom datasets or inference tools to integrate, feel free to fork and contribute. Be sure to check out `CONTRIBUTING.md`.

---

## 📜 License

Distributed under the **Apache 2.0 License**. See `LICENSE` for more information.

---

## 📬 Contact

Built by **Nivedita Sivakumar**  
📬 [LinkedIn](https://www.linkedin.com/in/niveditasivakumar) | 🧠 [Medium](https://medium.com/@niveditasivakumar) | 🧪 [GitHub](https://github.com/Nivz-28)

> *Inspired by Nous Research. Powered by small, fast, smart LLaMAs.*
