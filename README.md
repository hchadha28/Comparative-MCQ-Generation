# Comparative Analysis of Few-Shot Learning and Fine-Tuning for Automated MCQ Generation

This project is inspired by the influential research paper **“Language Models are Few-Shot Learners” (Brown et al., 2020)**, which introduced the idea that large language models can perform new tasks using only a few examples. Building on this concept, our study investigates whether few-shot prompting alone is sufficient for generating high-quality educational assessments, or whether **fine-tuning a smaller model** offers measurable improvements.

---

## 🎯 Academic Objective

To conduct a systematic comparison between:

1. **Few-Shot Prompting (GPT-4)**
   - No training required  
   - Uses 3–5 example MCQs as demonstrations  

2. **Parameter-Efficient Fine-Tuning (Llama-2-7B with LoRA)**
   - Domain adaptation using 200 geography MCQs  
   - Efficient, low-cost fine-tuning  

---

## 🔍 Research Questions

- Can few-shot prompting alone generate MCQs comparable to those from fine-tuned models?  
- Does fine-tuning give stronger domain-specific control and consistency?  
- What are the trade-offs in **cost**, **accuracy**, and **compute**?

---

## 🧪 Method Overview

- **Dataset**: 400 curated Geography MCQs  
- **Models**:
  - GPT-4 (Few-Shot)
  - Llama-2-7B (LoRA Fine-Tuned)
- **Evaluation**:
  - ROUGE-1 / ROUGE-2 / ROUGE-L  
  - Human evaluation: relevance, correctness, distractor plausibility  

---

## 📘 Project Structure

```text
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
```

---

## 🎓 Purpose of the Study

This academic project explores whether learning platforms should rely on:

- **Large general LLMs with few-shot prompting**, or  
- **Smaller, fine-tuned domain-specific models**

for scalable, automated MCQ generation.

The findings contribute to research in:
- Educational technology  
- Language model adaptation  
- Automated assessment generation  

---

## 📚 Reference

**Brown, T. et al. (2020).** *Language Models are Few-Shot Learners.* NeurIPS.
