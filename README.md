# Comparative Analysis of Few-Shot Learning and Fine-Tuning for Automated MCQ Generation

This project is inspired by the influential research paper **“Language Models are Few-Shot Learners” (Brown et al., 2020)**, which introduced the idea that large language models can perform new tasks using only a small number of examples. Building upon this concept, our study examines whether few-shot prompting alone is sufficient for generating high-quality educational assessments, or whether **fine-tuning a smaller model** offers measurable improvements.

---

## 🎯 Academic Objective

To conduct a systematic comparison between:

1. **Few-Shot Prompting (GPT-4)**  
   - No training required  
   - Uses 3–5 example MCQs as demonstrations  

2. **Parameter-Efficient Fine-Tuning (Llama-2-7B with LoRA)**  
   - Domain adaptation using 200 geography MCQs  
   - Efficient, low-cost fine-tuning

Our goal is to determine which method is more effective for **automated MCQ generation** in terms of quality, relevance, and distractor plausibility.

---

## 🔍 Research Questions

- Can few-shot prompting alone generate MCQs of comparable quality to those produced by fine-tuned models?  
- Does fine-tuning provide stronger domain-specific control and consistency?  
- What are the trade-offs in **cost**, **accuracy**, and **computational requirements** between the two approaches?

---

## 🧪 Method Overview

- **Dataset**: 250 curated Geography MCQs (balanced by topic and difficulty)  
- **Models**:
  - GPT-4 (Few-Shot)
  - Llama-2-7B (Fine-Tuned with LoRA)
- **Evaluation Metrics**:
  - ROUGE-1 / ROUGE-2 / ROUGE-L  
  - Human evaluation:  
    - Contextual relevance  
    - Answer correctness  
    - Distractor plausibility  

---

## 📘 Project Structure

mcqGenX/
│
├── README.md
├── requirements.txt
│
├── data/
│ ├── dataset_raw.jsonl
│ ├── train.jsonl
│ ├── val.jsonl
│ └── test.jsonl
│
├── notebooks/
│ ├── 01_prepare_data.ipynb
│ ├── 02_few_shot.ipynb
│ └── 03_fine_tune.ipynb
│
├── results/
│ ├── few_shot_outputs.jsonl
│ ├── fine_tuned_outputs.jsonl
│ └── evaluation.json
│
└── examples/
└── few_shot_examples.jsonl


---

## 🎓 Purpose of the Study

This academic project aims to explore whether educational institutions and learning platforms should rely on:

- **Large general-purpose LLMs with few-shot prompting**, or  
- **Smaller, fine-tuned models specialized through domain data**

for scalable, automated MCQ generation.

Our findings will contribute to ongoing research in:
- Educational technology  
- Language model adaptation  
- Automated assessment generation  

---

## 📚 Reference

**Brown, T. et al. (2020).** *Language Models are Few-Shot Learners.* NeurIPS.

---
