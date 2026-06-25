# Conversation-Sentiment-Analysis-in-League-of-Legends-Game-Community

## 🏗️ Data Pipeline & System Architecture

The application (`app.py`) follows a robust data flow from ingestion to visualization:

### 1. Data Ingestion (Extract)
*   **Batch Loading:** Ingests initial historical conversational data from Excel files and loads custom lexicons (`neg_words.txt`, `pos_words.txt`) into memory.
*   **Dynamic Ingestion:** Provides RESTful endpoints via **Flask** to dynamically ingest new user-generated content (Author, Content, Target) from the web UI.

### 2. NLP & Data Transformation (Transform)
*   **Text Cleaning:** Utilizes Regular Expressions (Regex) to strip emojis, special characters, and excess whitespace, ensuring clean data input.
*   **Custom Tokenization:** Employs `PyThaiNLP` with a custom, dynamically updated frozenset vocabulary (incorporating domain-specific toxic and positive words) to accurately tokenize informal Thai text.
*   **Sentiment Feature Engineering:** Computes a `definition_feeling_score` based on a predefined dictionary weighting system, categorizing the data into `pos`, `neg`, or `neu` labels.
*   **AI/ML Readiness:** Implements `CountVectorizer` and trains a `LogisticRegression` model from `scikit-learn` on the transformed tokens, establishing a foundation for predictive analytics.

### 3. Data Serving & Visualization (Load/Serve)
*   **Relational Mapping:** Uses `Pandas` and `collections.Counter` to map source-to-target interactions and aggregate connection weights.
*   **Interactive Graphing:** Generates an interactive HTML-based network graph using `PyVis`, where node connections represent interactions and edge colors represent sentiment (Red = Negative, Green = Positive, Grey = Neutral).
*   **Web Application:** Serves the interactive graphs and data tables through a **Flask** web application, allowing users to filter relationships by sentiment dynamically.

## 🛠️ Tech Stack
*   **Core Logic:** Python, Pandas, Regex
*   **NLP & Machine Learning:** PyThaiNLP, Scikit-learn (CountVectorizer, LogisticRegression)
*   **Web Framework & Serving:** Flask, HTML/CSS
*   **Data Visualization:** PyVis (Network Graphs)

## 🚀 Future Enhancements
*   Integrate data ingestion with a Cloud Storage bucket (e.g., AWS S3 or GCP Cloud Storage).
*   Format output data to be compatible with Vector Databases for Retrieval-Augmented Generation (RAG) architectures.

## ⚙️ How to Run
1. Clone the repository: `git clone https://github.com/ManOfSteel161/lol-community-sentiment-analysis.git`
2. Install dependencies: `pip install -r requirements.txt`
3. Run the main processing script.
