# 📘 Comparative Analysis of Few-Shot Learning and Fine-Tuning for Automated MCQ Generation

This repository contains the implementation and experiments for an academic study comparing two modern approaches in Large Language Models (LLMs) for automated MCQ generation:

- **Few-Shot Learning** using GPT-3.5 / Claude 3.5 Haiku  
- **Parameter-Efficient Fine-Tuning (LoRA)** using Llama-2-7B  

Inspired by *“Language Models are Few-Shot Learners” (Brown et al., 2020)*, this project evaluates whether prompting alone can match the quality of a fine-tuned model for generating educational MCQs.
## 🎯 Objective

This project compares two strategies for automated MCQ generation:

### 1. Few-Shot Prompting (GPT-3.5 / Claude Haiku)
- Requires **no training**
- Uses **3–5 curated MCQ examples**
- Extremely **low compute cost**

### 2. LoRA Fine-Tuning (Llama-2-7B)
- Fine-tuned on **400 Geography MCQs**
- Runs efficiently on a **free Google Colab GPU**
- Produces a **domain-specialized model**

The goal is to determine which approach yields better:
- MCQ quality
- Context relevance
- Distractor plausibility
- Cost and performance balance
---
## 🔍 Research Questions

This study investigates the following:

1. **Can few-shot prompting match the quality of a fine-tuned model?**
2. **Does fine-tuning improve domain-specific accuracy and distractor quality?**
3. **What are the trade-offs between model size, cost, and performance?**
4. **Which approach is more practical for scalable MCQ generation in education systems?**
## 🧪 Methodology

### Dataset
- **400 Geography MCQs** (AI-assisted + human-reviewed)
- Balanced across:
  - Physical Geography  
  - Human Geography  
  - Regional Geography  
  - Environmental Geography  
  - Geospatial Skills  
- Difficulty levels: Easy / Medium / Hard  
- Stored in **JSONL** format

### Models Compared

| Approach            | Model               | Notes                                   |
|--------------------|---------------------|-----------------------------------------|
| Few-Shot Prompting | GPT-3.5 / Claude Haiku | No training required                    |
| Fine-Tuning        | Llama-2-7B + LoRA      | Efficient training on free Colab GPU    |

### Evaluation Metrics
- **ROUGE-1, ROUGE-2, ROUGE-L**
- **Human evaluation** on:
  - Contextual relevance  
  - Answer correctness  
  - Distractor plausibility  

---
## 📁 Project Structure

mcqGenX/  
│  
├── README.md  
├── requirements.txt  
│  
├── data/  
│   ├── dataset_raw.jsonl  
│   ├── train.jsonl  
│   ├── val.jsonl  
│   └── test.jsonl  
│  
├── notebooks/  
│   ├── 01_prepare_data.ipynb  
│   ├── 02_few_shot.ipynb  
│   └── 03_fine_tune.ipynb  
│  
├── results/  
│   ├── few_shot_outputs.jsonl  
│   ├── fine_tuned_outputs.jsonl  
│   └── evaluation.json  
│  
└── examples/  
    └── few_shot_examples.jsonl  

---
## ⚙️ Environment Setup

### Python Version
Use **Python 3.10** (recommended for `transformers`, `peft`, and `bitsandbytes`).

### Create Virtual Environment

**macOS / Linux:**
- python3.10 -m venv .venv  
- source .venv/bin/activate  

**Windows:**
- python -m venv .venv  
- .venv\Scripts\activate  

### Install Dependencies
- pip install -r requirements.txt
## 🚀 How to Run the Project

### 1. Prepare the Dataset
Open and run:
**notebooks/01_prepare_data.ipynb**

This notebook:
- Loads `dataset_raw.jsonl`
- Shuffles entries
- Splits into:
  - `train.jsonl`
  - `val.jsonl`
  - `test.jsonl`

---

### 2. Few-Shot MCQ Generation
Run:
**notebooks/02_few_shot.ipynb**

Requirements:
- Claude or OpenAI API key

Output saved to:
- results/few_shot_outputs.jsonl

---

### 3. Fine-Tuning Llama-2-7B (LoRA) — Google Colab
Run:
**notebooks/03_fine_tune.ipynb**

This notebook:
- Loads training data  
- Fine-tunes Llama-2-7B using LoRA  
- Runs entirely on free Colab GPU  

Output saved to:
- results/fine_tuned_outputs.jsonl

---

### 4. Evaluation
Compute ROUGE + human metrics.

Save results in:
- results/evaluation.json
## 🎓 Purpose of the Study

This project helps determine whether educational platforms should rely on:

- **Large general-purpose LLMs** using few-shot prompting  
**or**
- **Smaller, fine-tuned models (LoRA)** trained on curated domain data  

for scalable, high-quality automated MCQ generation.

The findings contribute to research in:
- Educational technology  
- Language model adaptation  
- Assessment automation  
- Cost-efficient AI deployment  

---

## 📚 Reference

Brown, T. et al. (2020).  
*Language Models are Few-Shot Learners.* NeurIPS.
