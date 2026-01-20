# OpenMath
Fine-tuning a Small Language Model (SLM) for Step-by-Step Math Reasoning

## Overview
**OpenMath** is an open-source project focused on fine-tuning a **small language model (SLM)** to solve **math word problems** with clear, step-by-step reasoning.  
The project uses **LoRA/QLoRA fine-tuning** on popular math reasoning datasets and provides a benchmarking pipeline to compare performance against other open-source SLMs/LLMs.


This project is designed to be reproducible on **free Colab (T4)** or **Kaggle (P100)**
---
## What’s Included
- QLoRA fine-tuning code (4-bit)
- GSM8K subset training (example: 1k samples)
- GSM8K evaluation script (accuracy)
- Saved LoRA adapter weights (`adapter_model.safetensors`)

---

## Base Model
- **Qwen/Qwen2.5-Math-1.5B**

---

## Dataset
- **GSM8K** (Grade School Math 8K)
- Training used: **1000 samples**
- Evaluation: GSM8K test split

---

## Results (Baseline)
Training setup:
- Samples: 1000
- Epochs: 1
- Max length: 512
- LoRA rank: 8

**GSM8K Accuracy:** ~**14%**  
(quick baseline run on limited compute)

---

## Repository Files
### LoRA Adapter Folder
This project provides the fine-tuned adapter weights:

- `adapter_model.safetensors` → LoRA weights
- `adapter_config.json` → LoRA configuration
- Tokenizer + template files for correct formatting

> Note: This is **not a full model**.  
> You must load the **base model** and then attach the adapter.


