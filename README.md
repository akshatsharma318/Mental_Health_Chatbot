# 🧠 Mental Health Chatbot + Stress Analyzer – Mann-o-meter
Mann-o-meter is an AI-powered web application offering:

A responsive mental health chatbot driven by advanced Information Retrieval (IR) techniques.

A stress prediction system powered by Machine Learning (ML) for personalized wellness insights.

Interactive dashboards for visualizing health trends and stress patterns.

# 🚀 Features
## 🗣️ 1. IR-Based Mental Health Chatbot
Crisis Keyword Detection: Flags emergency terms like “suicide”, “want to die” and shows Indian mental health helpline info.

Hybrid Retrieval Logic:

Uses TF-IDF, BM25, and BERT embeddings (via sentence-transformers) to understand user queries.

Ranks responses using a custom fusion of scores.

Evaluation: Measured using NDCG (Normalized Discounted Cumulative Gain) for retrieval performance.

## 🤖 2. Stress Level Analyzer (ML-Based)
Inputs: Age, Sleep Time, Physical Activity, Heart Rate, Blood Pressure

Predictions:

Numeric Stress Level (0-10) → RandomForestRegressor

Stress Category (Low, Medium, High) → RandomForestClassifier

Model Metrics:

Regression: MAE, R² Score

Classification: Accuracy, Classification Report

## 📊 3. Visual Health Dashboard
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

# 🤖 Machine Learning
Models: RandomForestRegressor, RandomForestClassifier

Data Processing:

Parsing Blood Pressure, encoding gender

Handling missing fields with DummyRegressor/DummyClassifier

Evaluation:

Regression: MAE, R²

Classification: Confusion Matrix, Precision, Recall, F1

# 📂 Datasets
Mental_Health_FAQ.csv: Pre-curated mental health Q&A pairs for chatbot

Sleep_health_and_lifestyle_dataset.csv: User health data (Age, BP, Sleep, etc.)

# 🛠️ Tech Stack
Component:	Tools/Libraries

Backend	:Flask, Python

ML/IR	: scikit-learn, sentence-transformers, rank_bm25

NLP :	NLTK

Data Handling	: pandas, numpy

Visualization :	matplotlib

# Deployment : Ready for platforms like Render, Heroku, etc.

### 📍 Chatbot Interface
### 📍 Stress Input Form
### 📍 Radar Chart for Health Metrics
### 📍 Age vs Stress Bar Chart

---
<img src="https://github.com/user-attachments/assets/d45b0aab-6317-4689-a637-262994cb9d67" width="600"/>
<img src="https://github.com/user-attachments/assets/ae9dc69a-5a83-46c4-8700-28714ae85535" width="200"/>
<img src="https://github.com/user-attachments/assets/7bc86a58-78a7-4b69-b3d4-015b70f5f5a7" width="400"/>
<img src="https://github.com/user-attachments/assets/9719a01a-e794-4eaa-bfee-2cb836170783" width="400"/>
<img src="https://github.com/user-attachments/assets/3620a070-2339-49db-833e-7ab42e7bc77b" width="400"/>
<img src="https://github.com/user-attachments/assets/d9a05e79-d5b9-4f0b-bfc2-2cbea99e42c2" width="400"/>

---

#### Other teammates : 
Sansriti Mishra   : https://github.com/Cyberpunk-San

Aditya Dec Sharma : https://github.com/Aditya12D

Advik Rajvansh    :

Upanshi Mittal    :

## ✅ How to Run

```bash
git clone https://github.com/akshatsharma318/Mental_Health_Chatbot.git
cd IR
cd mental-health
pip install -r requirements.txt
python app.py  # Flask entry point

