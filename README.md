# 🧠 Fake News Detection System (ML + RAG + LLM)

An **end-to-end Fake News Detection System implemented in a single notebook**, combining **Machine Learning, Retrieval-Augmented Generation (RAG), and LLM (Gemini)** to provide accurate and explainable predictions.

---

## 🚀 Overview

This project detects whether a news article is **Fake or Real** and enhances predictions using:

* ✅ LSTM-based Deep Learning model
* ✅ RAG pipeline (FAISS + embeddings)
* ✅ Gemini LLM for explanation and validation
* ✅ Confidence calibration for reliability

---

## 🏗️ Pipeline Architecture

```text
User Input
   ↓
LSTM Model → Prediction + Confidence
   ↓
FAISS → Retrieve Similar News (RAG)
   ↓
Gemini → Explanation
   ↓
Gemini → Validation
   ↓
Gemini → Confidence Calibration
   ↓
Final Output
```

---

## ⚙️ Tech Stack

* **Python**
* **PySpark** (data processing)
* **TensorFlow / Keras (LSTM)**
* **FAISS (Vector Search)**
* **Sentence Transformers (Embeddings)**
* **Google Gemini API (LLM)**
* **Matplotlib, Seaborn, WordCloud (Visualization)**

---

## 📓 Notebook Structure

All code is implemented in a **single notebook**, divided into logical sections:

### 1️⃣ Setup & Configuration

* Library installation
* Spark session setup
* Config dictionary

---

### 2️⃣ Data Ingestion (Bronze)

* Load dataset (Fake.csv, True.csv)
* Add labels (Fake = 0, Real = 1)
* Store as parquet

---

### 3️⃣ Data Cleaning (Silver)

* Remove null values
* Merge title + text
* Text preprocessing:

  * Lowercasing
  * Regex cleaning
  * Stopword removal
  * Lemmatization

---

### 4️⃣ Feature Engineering

* Text length
* Word count
* Vocabulary richness
* Stopword ratio
* Visualizations:

  * Histogram
  * Correlation heatmap
  * WordCloud

---

### 5️⃣ Machine Learning Model (LSTM)

* Tokenization & padding
* Bidirectional LSTM model
* Training & evaluation
* Accuracy: **~90–94%**

---

### 6️⃣ RAG Pipeline

* Generate embeddings using SentenceTransformer
* Store embeddings in FAISS
* Retrieve top-k similar documents

---

### 7️⃣ LLM Layer (Gemini)

* Explanation generation
* Prediction validation
* Confidence calibration

---

### 8️⃣ Final Pipeline

```python
result = full_pipeline_advanced("Sample news text")
```

Output includes:

* Prediction
* Confidence
* Explanation
* Validation
* Confidence analysis

---

## 📊 Results

* Accuracy: **~90–94%**
* Improved explainability using RAG + LLM
* More reliable predictions using validation layer

### Example Output:

```text
Prediction: Fake
Confidence: 0.87

Explanation:
The claims contradict verified sources retrieved from dataset...

Validation:
INVALID: The claim is inconsistent with contextual evidence.

Confidence Analysis:
Adjusted Confidence: 0.65
```

---

## 📌 Dataset

Kaggle Fake News Dataset:
https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset

---

## ▶️ How to Run

1. Open the notebook in **Google Colab**
2. Install dependencies:

```bash
pip install pyspark tensorflow langchain faiss-cpu sentence-transformers google-generativeai nltk wordcloud matplotlib seaborn
```

3. Add your Gemini API key:

```python
GENAI_API_KEY = "your_api_key_here"
```

4. Run all cells sequentially

---

## 🌱 Future Improvements

* Deploy on Databricks
* Build API using FastAPI
* Use Transformer models (BERT)
* Improve RAG with advanced vector DB

---

## 🎯 Key Learnings

* End-to-end AI pipeline design
* Integration of ML + RAG + LLM
* Prompt engineering & explainable AI
* Data preprocessing using PySpark

---

## 👤 Author

**Parth Azad**
Aspiring Data Engineer & AI/ML Engineer

---

⭐ Star this repo if you found it useful!
