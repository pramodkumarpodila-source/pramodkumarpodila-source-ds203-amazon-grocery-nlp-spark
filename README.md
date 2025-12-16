# pramodkumarpodila-source-ds203-amazon-grocery-nlp-spark
Big data project using Spark and NLP on Amazon Grocery reviews to analyze customer sentiment and product performance.
# Analyzing 14.3M Amazon Grocery Reviews with PySpark & NLP

**DS203 Big Data – Final Project**  
**Team:** Geny, Majd, Sai Pramod  
**Institution:** Cornerstone College, Vancouver, BC

---

## Overview

End-to-end big data pipeline using **Apache Spark** and **PySpark** to analyze **14.3 million Amazon Grocery reviews** (2000–2023) and build an NLP sentiment classifier.

**Key Results:**
- 🤖 **83.2% accuracy** sentiment model (0.895 AUC)
- 📊 **480× review growth** from 2000 to 2021
- ✅ Verified buyers rate **5.5% higher** than non-verified

---

## Repository Structure


├── notebooks/
│ ├── 01_data_prep.ipynb # Data cleaning & feature engineering
│ ├── 02_analysis.ipynb # Exploratory analysis & PySpark queries
│ └── 03_nlp_sentiment.ipynb # NLP pipeline & sentiment model
├── models/
│ └── grocery_sentiment_lr/ # Saved Spark ML model
└── README.md

---

## Dataset

**Source:** Amazon Reviews 2023 – Grocery & Gourmet Food  
**Link:** https://amazon-reviews-2023.github.io

**⚠️ Dataset NOT included in repo** (too large for GitHub, added to `.gitignore`)

### How to Get the Data

1. Download from [Amazon Reviews 2023](https://amazon-reviews-2023.github.io) (Grocery & Gourmet Food category)
2. Place files in a `data/` folder in repo root
3. Update paths in `01_data_prep.ipynb` if needed

**Stats:** 14,318,520 reviews · 10 fields · ~1.4 GB

---

## Quick Start

Clone repo
git clone https://github.com/pramodkumarpodila-source/pramodkumarpodila-source-ds203-amazon-grocery-nlp-spark.git
cd pramodkumarpodila-source-ds203-amazon-grocery-nlp-spark

Install dependencies
pip install pyspark jupyter pandas matplotlib seaborn

Download dataset (see above), then run notebooks in order
jupyter notebook

---

## What Each Notebook Does

### 1. Data Preparation
- Loads 14.3M reviews from JSONL into Spark
- Cleans data (99.9955% completeness)
- Engineers `review_length` and `is_positive` features
- Partitions into 3 CSVs (~4.77M rows each)

### 2. Analysis & Exploration
- PySpark queries: filtering, grouping, joins, window functions
- Key findings:
  - Review volume grew 480× (2000–2021)
  - Ratings dropped from 4.8 → 4.05 stars
  - Verified: 4.14 stars vs Non-verified: 3.93 stars
  - Top products hold perfect 5.0 ratings

### 3. NLP Sentiment Model
- Spark ML pipeline: Tokenizer → StopWords → HashingTF → IDF → Logistic Regression
- 10% stratified sample (~1.43M reviews)
- **Results:** 83.2% accuracy, 0.895 AUC

---

## DS203 Requirements Met

✅ Dataset ~1.4 GB, 14.3M rows  
✅ Filtering (5+ queries)  
✅ Aggregations (avg, sum, min, max)  
✅ Grouping, sorting, joins (self-join)  
✅ Window functions (rank, lag, lead)  
✅ Aggregate windows (running totals)  
✅ New columns (`review_length`, `is_positive`)  
✅ Documentation & visualizations  

---

## Tech Stack

Apache Spark 4.x · PySpark · Python 3.13+ · Jupyter · Spark MLlib

---

## Team

Geny · Majd · Sai Pramod  
Cornerstone College, Vancouver, BC · December 2025

---

## License

Educational project for DS203 Big Data course.

