# Risk-Benchmarking-for-LLMs
# 🔍 LLM Risk Benchmarking Toolkit

A practical framework to evaluate the **real-world vulnerabilities of open-source Large Language Models (LLMs)** — developed in collaboration with **Prediction Guard** and presented at **INFORMS 2025**.

---

## 🧠 Objective

LLMs are powerful — but just like people, they’re prone to mistakes under pressure. As these models enter healthcare, finance, and enterprise workflows, it’s no longer enough to just ask *“How accurate is it?”*  

We need to ask:  
**“How safe is it under real-world conditions?”**  
This toolkit is our answer to that.

---

## 🎯 Goals

- Evaluate model sensitivity to prompt variation (spelling errors, tone changes, format shifts)  
- Assess risks related to PII leakage, factual hallucinations, prompt injections, and toxic output  
- Create interpretable metrics like **Prompt Deviation Score (PDS)** and **Semantic Drift**  
- Benchmark the performance and safety tradeoffs between smaller and larger LLMs  
- Provide practical insights for **safer deployment** and **cost-effective model selection**

---

## 🧪 Core Components

### 1. Prompt Robustness Testing
- Synonym swaps & rephrasings  
- Format and tone shifts (formal ↔ casual)  
- Typographical noise (spelling errors)

### 2. Risk Categories Evaluated
- Prompt Sensitivity  
- Prompt Injection Vulnerability  
- Factual Consistency  
- Toxicity & Bias Output  
- PII Leakage (e.g., names, numbers)

### 3. Models Benchmarked
- `Hermes-2-Pro-LLaMA-3-8B`  
- `Hermes-3-LLaMA-3.1-70B`  
Tested using **SQuAD**, **Jigsaw**, and synthetic adversarial sets.

### 4. Custom Metrics Introduced
- **Prompt Deviation Score (PDS)** — how much model behavior changes with prompt tweaks  
- **Cosine Similarity Drift** — semantic shift measured via embeddings  
- **Toxicity Score** — using Google’s Perspective API  
- **Factual Entailment Rate** — judged via LLM-as-a-Judge methodology

---

## ⚙️ Tech Stack

- Python 3.10+  
- Hugging Face Transformers & Datasets  
- SentenceTransformers  
- Databricks / Colab (A100 GPUs recommended)  
- Google Perspective API (toxicity scoring)  
- MLflow (because repeatability is underrated)  
- Optional: OpenAI API for LLM-as-a-Judge evaluations

---

## 💡 Key Insights

- **Smaller is smarter (sometimes):** The 8B model showed better factual reliability and resistance to prompt injection  
- **Semantic tweaks > typos:** Meaningful rewording caused more response drift than misspellings  
- **Efficiency wins:** Open-source models + GPU instances cut evaluation costs by over **90%** vs commercial APIs  
- **Enterprise strategy matters:** Safer models can be tiered for use cases — e.g., Hermes-2 for compliance-sensitive tasks, Hermes-3 for ideation

---

---

## 🛠️ Getting Started

1. Open `SQuAD_Robustness.ipynb` or `Injection_Tests.ipynb`  
2. Choose your LLM(s) and evaluation criteria  
3. Run prompt tests — both original and adversarial  
4. Analyze PDS, similarity drift, and response risk scores  

> ⚡ **Bonus:** Easily runnable on Databricks or Colab — no heavy setup required.

---

## 🔧 Applications

- ✅ AI Governance & Risk Management  
- ✅ Enterprise Model Selection & Audits  
- ✅ AI Trust & Safety Research  
- ✅ Cost-efficient evaluation pipelines for startups  
- ✅ Benchmarking open-source models for regulated domains

---

## 📉 Limitations & Next Steps

- Current focus: English-only prompts and LLaMA-family models  
- Future expansion: Chat-based models (e.g., Mixtral), multilingual evaluation  
- Upcoming feature: Scenario-based red teaming prompts (e.g., healthcare triage, legal disclaimers)

> 💡 Have suggestions or want to collaborate? Open an issue or reach out!

---

## 📌 Acknowledgments

Huge thanks to **Prediction Guard** — especially *Aishwarya Ramasethu* — for mentorship, guidance, and helping us think like red-teamers.  
Thanks to the **open-source LLM community** (Nous, Hugging Face, Teknium), Google’s **Perspective API** team, and **Prof. Matthew Lanham** for his steady academic support.

---

## 📬 Contact

📧 avanti.c@purdue.edu  
💼 Project team: Abhishek Bagepalli, Ramya Polineni, Tsung-Yu Lu, Chan-Yen Hsiung, Jayesh Chaudhari, and Avanti Chandratre  
📍 Purdue University – MSBAIM 2025

