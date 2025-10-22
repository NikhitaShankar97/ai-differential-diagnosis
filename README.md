# AI-Powered Differential Diagnosis Assistant (Industry Capstone)

## 📘 Overview
This project was developed as part of the **Industry Capstone collaboration with Wolters Kluwer Health**, exploring how **Large Language Models (LLMs)** can support clinicians in generating accurate **differential diagnoses** from patient case data.  
The objective was to evaluate whether language models can augment clinical reasoning, reduce diagnostic time, and assist healthcare professionals through structured, explainable AI outputs.

> ⚠️ **Note:** Due to NDA restrictions with Wolters Kluwer Health, the full prototype, datasets, and model outputs cannot be publicly shared. This repository contains the presentation deck and generalized documentation summarizing the methodology and results.

---

## 🎯 Problem Statement
Healthcare professionals often rely on extensive manual reasoning and cross-referencing of patient data to form differential diagnoses.  
The goal of this project was to determine if **LLMs can generate clinically relevant ranked diagnoses** and reasoning summaries based on structured patient history and simulated doctor–patient interactions.

---

## 🔍 Objectives
1. Develop structured **prompt templates** that simulate real patient data for model evaluation.  
2. Compare performance of **OpenAI GPT-4o**, **Google Gemini 2.5 Pro**, and **xAI** models.  
3. Build a **prototype application** allowing clinicians to input patient history and receive ranked diagnostic suggestions with reasoning and red-flag alerts.  
4. Evaluate model accuracy using medical case studies from **New England Journal of Medicine (NEJM)** reports.

---

## 🧩 Data Overview
- **Sources:** 25 NEJM case reports (2024–2025).  
- **Formats Created:**  
  - Short summaries  
  - Full patient histories  
  - Simulated conversational transcripts  
- **Processing:**  
  - Extracted lab results, vitals, and demographics.  
  - Cleaned and structured text for LLM input.  
  - JSON-formatted case data for reproducibility.  

---

## ⚙️ Development Stack
- **LLMs Used:** OpenAI GPT-4o API, Google Gemini 2.5 Pro API  
- **Frameworks:** Python, Streamlit  
- **Environment:** Collaborative notebooks for experimentation  
- **Techniques:** Prompt engineering, “Atom of Thought” reasoning chains, JSON-based structured inputs  

---

## 🧠 Model Evaluation
**Metrics Used:**
- **Top-3 and Top-10 Accuracy** – correctness ranking of generated diagnoses  
- **Mean Reciprocal Rank (MRR)**  
- **Discounted Cumulative Gain (DCG)**  
- **BOND Score (1–5):** measures reasoning overlap with clinical gold standard  

**Key Findings:**
- GPT-4o consistently achieved higher **Top-3 accuracy** and **MRR** across most complexity levels.  
- Structured prompting and “Diagnosis + Confidence + Reasoning + Next Steps” formats reduced hallucination rates.  
- Adding clinical context (age, gender, key symptoms) improved diagnostic precision significantly.  

---

## 🧰 Prototype Overview
Developed an interactive **Streamlit app** where clinicians could:  
- Enter structured or conversational patient histories.  
- View ranked differential diagnoses with confidence scores.  
- Review reasoning and recommended next steps.  
- Receive 🚨 **red-flag alerts** for life-threatening conditions.  
- Export reports as PDFs for clinical reference.

---

## 🌟 Key Outcomes
- Demonstrated that **LLMs can achieve clinically relevant diagnostic reasoning** with proper prompt structure.  
- Established repeatable evaluation metrics for medical LLM benchmarking.  
- Delivered a working prototype to **Wolters Kluwer Health** demonstrating the feasibility of AI-assisted clinical decision support.  

---

## 🚀 Future Enhancements
- Integrate **Retrieval-Augmented Generation (RAG)** using trusted medical literature.  
- Support **real or simulated clinical audio** to enable ambient listening.  
- Develop **multi-agent validation systems** for real-time cross-checking of diagnoses.  
- Implement **live dashboards** for hospital deployment and clinician monitoring.  
- Ensure full compliance with **HIPAA and PHI data privacy** regulations.  

---

## 🛠️ Tools & Technologies
- **Python** (Pandas, Streamlit, JSON, Statsmodels)  
- **OpenAI GPT-4o, Google Gemini 2.5 Pro APIs**  
- **Prompt Engineering & Evaluation Pipelines**  
- **Statistical Ranking Metrics (MRR, DCG, BOND)**  

---

## 👥 Team & Role
Served as **Data Science & AI Consultant**, focusing on:  
- Designing and testing structured prompts for diagnosis generation.  
- Evaluating multi-model outputs using ranking metrics.  
- Developing the prototype interface for demonstration and clinician testing.  
- Presenting results and improvement roadmap to Wolters Kluwer’s health analytics division.  

---

## 📎 File Included
- `/presentation/Wolters_Kluwer_LLM_Differential_Diagnosis.pptx` – client presentation deck summarizing approach, evaluation, and results

