# 🌍 Topic Modeling on Restaurant Reviews

This project applies topic modeling using **BERTopic** and **UMAP** to extract key insights from Yelp restaurant reviews in Arizona. It uncovers themes, visualizes trends over time, and contrasts customer sentiment patterns to inform business strategies.

---

## 📌 Overview

- **Author:** Tsai-Yun Hsieh  
- **Date:** 2025-02-27  
- **Tech Stack:** Python, BERTopic, UMAP, SentenceTransformers, Matplotlib, Seaborn, Pandas

---

## ⚙️ Workflow

### 1. Data Preparation
- Load 5,000 restaurant reviews from `restaurant_reviews_az.csv`
- Compute and visualize review lengths

### 2. Embedding & Dimensionality Reduction
- Encode reviews using `all-MiniLM-L6-v2` model
- Reduce dimensions using UMAP (5D space, cosine similarity)

### 3. Topic Modeling with BERTopic
- Apply BERTopic with UMAP + precomputed embeddings
- Extract top 6 topics (excluding outliers)
- Print keywords and representative documents

### 4. Topic Visualization
- Bar chart of top keywords per topic
- Intertopic distance map
- Topic hierarchy tree
- Topic distribution for a single review

### 5. Time-Series Topic Trend (2020–2021)
- Aggregate monthly topic frequency
- Plot bar chart showing topic shifts over time

### 6. Compare Topics in 1-Star vs 5-Star Reviews
- Classify topics in negative (1-star) and positive (5-star) reviews
- Plot grouped bar chart for visual comparison

---

## 🔍 Topic Interpretations

| Topic | Description                              |
|-------|------------------------------------------|
| 0     | Food quality – taste, freshness, plating |
| 1     | Service experience – staff, wait times   |
| 2     | Environment – ambiance, decor            |
| 3     | Price/value – cost, portion size         |
| 4     | Location/access – parking, convenience   |
| 5     | Specific dishes and unique experiences   |

---

## 📊 Key Visualizations

- `visualize_barchart()` – Top keywords per topic  
- `visualize_topics()` – Topic distance map  
- `visualize_hierarchy()` – Topic grouping tree  
- `visualize_distribution()` – Topic prob. for single doc  
- Time series plot – Monthly frequency (2020-2021)  
- Grouped bar chart – Topic freq. by review rating

---

## 📈 Business Insights

### Temporal Trends:
- Topics fluctuate by month (seasonal and event-based)
- Breakfast and ambiance topics rise in colder seasons
- Useful for planning promotions and menus

### Sentiment-Based Differences:
- 5⭐ reviews emphasize food & service quality
- 1⭐ reviews focus on problems like bad service or disappointing food
- Businesses can:
  - Improve based on 1-star topics
  - Promote strengths from 5-star highlights

---

## 📂 Dataset

- **File:** `restaurant_reviews_az.csv`  
- **Columns:** `text`, `stars`, `date`

---

## 🛠️ Installation

pip install bertopic umap-learn sentence-transformers pandas matplotlib seaborn

## ▶️ How to Run

Topic Modeling with BERT.ipynb

Make sure to place restaurant_reviews_az.csv in the correct path or update the file path accordingly.

## 📁 Output
Keyword bar charts for top topics

Interactive topic visualizations (Plotly)

Monthly topic frequency chart

1⭐ vs 5⭐ topic distribution chart

## 🙌 Acknowledgements
This project enhanced my understanding of unsupervised NLP techniques like BERTopic and UMAP. Through customer-driven topic clustering, visual analysis, and sentiment separation, we can extract meaningful insights from unstructured data for actionable restaurant strategy.
