# ClaimWise AI

🚀 **Google Cloud BigQuery AI Hackathon Project**


## 🔗 Project Links

* [Live Kaggle Notebook](https://www.kaggle.com/code/nguyennamhongdoan/claimwise-ai-auto-claim-insurance)
* [YouTube Demo]([https://www.youtube.com/watch?v=331wTlPY9IM](https://www.youtube.com/watch?v=0tNLbyQfCr4)
* [Blog Post (Medium)](https://medium.com/@bigqueryteam1/from-hours-to-minutes-how-claimwise-transforms-claims-with-intelligent-automation-7e30b3446f39)

## 📌 Overview

ClaimWise AI is an AI-powered Insurance Claim Assistant that leverages Google Cloud, BigQuery, and Cloud Storage to streamline the traditionally manual and time-consuming claim review process.

Insurance claim adjusters often need to:

* Review lengthy documents and case files
* Analyze photos of damage
* Cross-check information with third-party sources
* Estimate repair costs using rules and past cases

This manual process can be slow, inconsistent, and prone to fraud. ClaimWise AI addresses these challenges by combining document summarization, case retrieval, and image-based fraud detection into a single intelligent assistant.

---

## ✨ Key Features

* **Semantic Claim Retrieval**: BigQuery Vector Search on text embeddings to retrieve similar past cases for faster, more accurate cost estimation
* **Multimodal Fraud Detection**: AI embeddings on crash photos stored in Cloud Storage to detect anomalies and identify potential fraud  
* **Automated Fraud Flagging**: Updates fraud status automatically from duplicated images from historical claims
* **Interactive Analytics**: Rich visualizations and comparative analysis tools

---

## 🛠️ Tech Stack

* **Cloud Platform**: Google Cloud Platform (GCP)
* **Data Storage**: Google Cloud Storage & BigQuery
* **Core Libraries**: Python, Pandas, Matplotlib/Seaborn
* **AI Services**: Google Generative AI (Gemini), BigQuery ML
* **Key Techniques**: Exploratory Data Analysis (EDA), Multimodal Feature Engineering, Similarity Search (Cosine Distance), Classification Modeling, Feature Importance, Prompt Engineering

---

## 📈 Business Impact Metrics

* **Processing Speed**: +95% improvement (minutes vs. days)
* **Fraud Detection**: 95%+ accuracy (detected 3 fraud attempts via duplicate photo recognition)
* **Efficiency Gain**: 70x faster than manual processing (Manual avg: ~60 sec vs. ClaimWise: 0.15 sec per claim)
* **Cost Reduction**: -98% decrease in processing costs
* **Annual Savings**: $815,000+ potential through automation and fraud prevention

---

## 🚀 Quick Start

### Prerequisites

1. **Download raw data**: Get historical claim photos from [Google Drive](https://drive.google.com/drive/folders/1byERaspNHtO7RVL37qY3ytgJjgMtBBdl?usp=sharing) and upload to your Drive
2. **Create BigQuery dataset**: Set up `claimwise_db` dataset in BigQuery
3. **Import claims table**: Create `claims` table using `claims_metadata.xlsx` from BigQuery AI Team/Dataset folder

### Setup Steps

1. **Create GCS bucket**: Set up `claim_medias` bucket in Google Cloud Storage
2. **Upload photos**: Load claim photos into the GCS bucket
3. **Create external table**: Set up `claim_medias` external table in BigQuery with object URIs
4. **Build embedding models**: Create text embedding model for descriptions and multimodal model for photos
5. **Extend claims table**: Add `text_embedding` column to enable semantic similarity search
6. **Run analysis**: Execute the Colab notebook to process claims and detect fraud
---



