# Intelligent Community Complaint Classification System

**An Artificial Intelligence project to automate the sorting of citizen complaints using Natural Language Processing (NLP) and Hybrid Classification logic.**

---

## 👤 Author Details
- **Name:** Muhammad Affan Kabir  
- **SAP ID:** 65139  
- **Course:** Artificial Intelligence  
- **Institution:** Riphah International University  

---

## 📌 Project Summary

Civic authorities receive thousands of unstructured text complaints daily. Manually routing these to the correct department (e.g., Water vs. Electricity) is inefficient.

This project implements a **Hybrid AI Classifier** that categorizes complaints into four specific departments:

1. **Cleaning** – e.g., “Garbage is piling up”
2. **Water** – e.g., “The main pipe is leaking”
3. **Electricity** – e.g., “Voltage fluctuation detected”
4. **Inflation** – e.g., “Prices of essential goods are too high”

### Key Features
- **Hybrid Logic:** Combines **Deterministic Rules** (keyword overrides) with **Probabilistic Machine Learning** (Naive Bayes).
- **Noise Filtering:** Identifies irrelevant inputs and categorizes them as **“Others”**.
- **Self-Contained Dataset:** Generates **500 synthetic samples** with shared context for improved generalization.

---

## 🛠️ Proposed Methodology

The system processes each complaint through:

1. **TF-IDF Vectorization** – Converts text into numerical form.  
2. **Model Training** – Multinomial Naive Bayes classifier.  
3. **Three-Layer Prediction System:**  
   - **Layer 1 — Rule-Based Overrides** for critical keywords.  
   - **Layer 2 — Machine Learning Prediction** using probability scores.  
   - **Layer 3 — Safety Net**: Low confidence (<45%) → **“Others”**.

---

## 💻 Dependencies & Requirements

Install the needed Python libraries:

```bash
pip install pandas scikit-learn matplotlib seaborn


# 🚀 Execution Instructions

This project runs via **AI_Semester_Project.ipynb** in Google Colab or any Notebook environment.

---

## 1. Clone the Repository

```bash
git clone https://github.com/YourUsername/Smart-Complaint-System.git
```

---

## Implementation
### Open the Project

Use any of the following:

* **Google Colab**
* **Jupyter Notebook**
* **VS Code**

---

### Run All Cells

* **Steps 1 & 2:** Generate dataset + train model
* **Step 3:** Display Confusion Matrix + Accuracy
* **Step 4:** Launch **Live Prediction Demo**

---

# 📝 Example Usage

### **Scenario 1 — AI Prediction**

**Input:**

> “The bills are becoming very expensive these days”

**Output:**
`Inflation (AI Confidence: 78.5%)`

---

### **Scenario 2 — Keyword Override**

**Input:**

> “There is a severe blackout in my area”

**Output:**
`Electricity (Guaranteed by Keyword)`

---

### **Scenario 3 — Noise Filtering**

**Input:**

> “I am going to watch a cricket match”

**Output:**
`Others (Detected as Irrelevant/Low Confidence)`

---

# 📂 Repository Structure

```
AI_Semester_Project.ipynb   →  Source code  
Project_Report.pdf          →  Academic documentation  
README.md                   →  Setup guide (this file)
```

---

*Submitted as the Semester Project for the Faculty of Computing.*
