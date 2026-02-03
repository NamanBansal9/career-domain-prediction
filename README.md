# Career Domain Prediction using O*NET and NLP

An end-to-end machine learning project that predicts suitable career domains from occupational skill data using semantic NLP embeddings and ensemble learning techniques.

---

## Overview

Career guidance systems often rely on keyword matching or rigid rules that fail to capture the true semantic relationship between skills, technologies, and professional roles.

This project builds an intelligent career domain prediction pipeline by combining O*NET occupational data, Sentence-BERT embeddings, and multiple machine learning models to generate accurate, interpretable career recommendations.

The system is designed with scalability in mind and can be extended to APIs, chatbots, and real-world career advisory platforms.

---

## Why O*NET?

O*NET (Occupational Information Network) is a standardized occupational database developed by the U.S. Department of Labor. It provides structured, validated, and industry-recognized information about jobs and careers.

O*NET includes:
- Occupational descriptions
- Required skills
- Knowledge areas
- Technologies and tools
- Work activities

Using O*NET ensures that predictions are grounded in real labor-market intelligence rather than synthetic or scraped data. This makes the system reliable, explainable, and aligned with real-world industry standards.

---

## Problem Statement

Given unstructured textual information describing:
- Skills
- Knowledge areas
- Technology exposure

The objective is to predict the most suitable high-level career domain such as:
- Software Engineering
- Data Science
- Cybersecurity
- Digital Marketing

---

## Methodology

### Data Preparation

Occupational data was extracted from O*NET and organized into structured text representations by combining skills, knowledge, and technology information for each role.

Each occupation was manually mapped to a broader career domain to enable supervised learning.

---

### Feature Engineering

Sentence-BERT (SBERT) was used to convert text into dense numerical embeddings.

Unlike traditional vectorization techniques such as TF-IDF, SBERT captures contextual and semantic meaning, enabling the model to understand relationships between skills and career domains rather than relying on keyword overlap.

---

### Model Selection

Multiple machine learning models were trained on SBERT embeddings:

- Logistic Regression for strong baseline performance and interpretability
- Support Vector Machine (RBF kernel) to capture non-linear decision boundaries
- Random Forest to model complex feature interactions

---

### Ensemble Learning

No single model performs optimally across all scenarios. To improve robustness and stability, predictions from all models were combined using an ensemble approach.

The final output is a ranked list of predicted career domains along with confidence scores.

---

## System Flow

O*NET Data  
→ Text Aggregation (Skills + Knowledge + Technology)  
→ Sentence-BERT Embeddings  
→ Multiple ML Models  
→ Ensemble Prediction  
→ Career Domain with Confidence

---

## Technology Stack

- **Programming Language:** Python  
- **Natural Language Processing:** Sentence-BERT (SBERT)  
- **Machine Learning:** Scikit-learn  
- **Data Processing:** Pandas, NumPy  
- **Dataset:** O*NET Occupational Database  
- **Model Serialization:** Pickle / Joblib  
- **Development Environment:** Jupyter Notebook

## Future Enhancements

- Scale the system to the complete O*NET dataset for improved generalization
- Deploy the prediction pipeline as a REST API using FastAPI
- Integrate a conversational career chatbot for interactive guidance
- Enable resume (PDF/text) ingestion and automated skill extraction
- Support fine-grained role-level predictions within career domains
- Build a frontend interface for end-user interaction


## Author

**Naman Bansal**  
Machine Learning & NLP Enthusiast  


