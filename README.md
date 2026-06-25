# Conversation-Sentiment-Analysis-in-League-of-Legends-Game-Community

## 📌 Project Overview
This project demonstrates an end-to-end data processing workflow designed to handle **unstructured text data** from Thai gaming communities (League of Legends). The primary objective is to transform raw, noisy conversation data into structured, actionable insights using Natural Language Processing (NLP) and graph analysis.

This repository serves as a foundational example of **AI Data Readiness**, showcasing how unstructured text can be extracted, cleaned, and modeled to support machine learning workloads and advanced analytics.

## 🏗️ Data Pipeline Architecture

*   **1. Data Extraction:**
    *   Gathered and ingested raw, unstructured community conversation logs and forum data.
*   **2. Data Transformation & AI Readiness:**
    *   Performed rigorous text cleaning and preprocessing tailored for informal Thai language nuances.
    *   Integrated **Transformers** to process the text and classify sentiment metrics (Positive/Negative/Neutral).
    *   Modeled social interaction patterns and conversational networks using **NetworkX**, creating structured relationship data from raw text.
*   **3. Data Loading & Output:**
    *   Structured the final NLP and graph outputs into clean datasets, making them fully accessible for downstream analytics, dashboards, or future machine learning models.

## 🛠️ Key Technologies
*   **Language:** Python
*   **Data Processing:** Pandas, NumPy
*   **NLP & Machine Learning:** HuggingFace Transformers
*   **Graph Analytics:** NetworkX

## 🚀 Future Enhancements
*   Integrate data ingestion with a Cloud Storage bucket (e.g., AWS S3 or GCP Cloud Storage).
*   Format output data to be compatible with Vector Databases for Retrieval-Augmented Generation (RAG) architectures.

## ⚙️ How to Run
1. Clone the repository: `git clone https://github.com/ManOfSteel161/lol-community-sentiment-analysis.git`
2. Install dependencies: `pip install -r requirements.txt`
3. Run the main processing script.
