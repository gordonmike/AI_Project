# Intelligent Community Complaint Classification System

**An Artificial Intelligence project to automate the sorting of citizen complaints using Natural Language Processing (NLP) and Hybrid Classification logic.**

---

## 👤 Author Details
* **Name:** Muhammad Affan Kabir
* **SAP ID:** 65139
* **Course:** Artificial Intelligence
* **Institution:** Riphah International University

---

## 📌 Project Summary
Civic authorities receive thousands of unstructured text complaints daily. Manually routing these to the correct department (e.g., Water vs. Electricity) is inefficient.

This project implements a **Hybrid AI Classifier** that categorizes complaints into four specific departments:
1.  **Cleaning** (e.g., "Garbage is piling up")
2.  **Water** (e.g., "The main pipe is leaking")
3.  **Electricity** (e.g., "Voltage fluctuation detected")
4.  **Inflation** (e.g., "Prices of essential goods are too high")

### Key Features
* **Hybrid Logic:** Combines **Deterministic Rules** (keyword overrides for 100% accuracy on critical terms) with **Probabilistic Machine Learning** (Naive Bayes) for complex sentence understanding.
* **Noise Filtering:** Intelligent detection of **"Irrelevant"** inputs (e.g., sports, casual chat), classifying them as **"Others"** instead of generating false tickets.
* **Self-Contained Dataset:** Includes a built-in module that generates 500 robust synthetic samples with shared contexts to prevent overfitting.

---

## 🛠️ Proposed Methodology
The system processes text through three distinct layers:
1.  **Feature Extraction:** Converts raw text into numerical vectors using **TF-IDF** (Term Frequency-Inverse Document Frequency).
2.  **Model Training:** Trains a **Multinomial Naive Bayes (MNB)** classifier on the generated dataset.
3.  **Prediction Pipeline:**
    * **Layer 1 (Rules):** Checks for high-priority keywords (e.g., "blackout"). If found -> **Guaranteed Category**.
    * **Layer 2 (AI):** If no keywords found, the AI model predicts the probability.
    * **Layer 3 (Safety):** If confidence is low (< 45%) or the content is detected as irrelevant -> **Classified as "Others"**.

---

## 💻 Dependencies & Requirements
To run this project, you need Python installed along with the following libraries:

* `pandas` (Data Manipulation)
* `scikit-learn` (Machine Learning & Metrics)
* `matplotlib` & `seaborn` (Data Visualization)

**Installation Command:**
```bash
pip install pandas scikit-learn matplotlib seaborn
