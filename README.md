# 🧠 Mental Health Chatbot + Stress Analyzer – Mann-o-meter
Mann-o-meter is an AI-powered web application offering:

A responsive mental health chatbot driven by advanced Information Retrieval (IR) techniques.

A stress prediction system powered by Machine Learning (ML) for personalized wellness insights.

Interactive dashboards for visualizing health trends and stress patterns.

# 🚀 Features
🗣️ 1. IR-Based Mental Health Chatbot
Crisis Keyword Detection: Flags emergency terms like “suicide”, “want to die” and shows Indian mental health helpline info.

Hybrid Retrieval Logic:

Uses TF-IDF, BM25, and BERT embeddings (via sentence-transformers) to understand user queries.

Ranks responses using a custom fusion of scores.

Evaluation: Measured using NDCG (Normalized Discounted Cumulative Gain) for retrieval performance.

🤖 2. Stress Level Analyzer (ML-Based)
Inputs: Age, Sleep Time, Physical Activity, Heart Rate, Blood Pressure

Predictions:

Numeric Stress Level (0-10) → RandomForestRegressor

Stress Category (Low, Medium, High) → RandomForestClassifier

Model Metrics:

Regression: MAE, R² Score

Classification: Accuracy, Classification Report

# 📊 3. Visual Health Dashboard
User-wise Stress Visualization: Personal metrics in radar and bar charts

Population Trends:

Stress distribution across age groups

Average stress per health indicator

🧠 Core Technologies Used
🔍 Information Retrieval
Text cleaning via NLTK: Tokenization, Stopwords, Lemmatization

Representations:

Sparse: TF-IDF, BM25Okapi

Dense: Sentence-BERT

Score Fusion Strategy: Weighted hybrid of sparse + dense scores

Ranking Evaluation: ndcg_score

🤖 Machine Learning
Models: RandomForestRegressor, RandomForestClassifier

Data Processing:

Parsing Blood Pressure, encoding gender

Handling missing fields with DummyRegressor/DummyClassifier

Evaluation:

Regression: MAE, R²

Classification: Confusion Matrix, Precision, Recall, F1

📂 Datasets
Mental_Health_FAQ.csv: Pre-curated mental health Q&A pairs for chatbot

Sleep_health_and_lifestyle_dataset.csv: User health data (Age, BP, Sleep, etc.)

