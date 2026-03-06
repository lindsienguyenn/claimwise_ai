# ClaimWise AI - Google Cloud BigQuery AI Hackathon Project



## 🔗 Project Links

* Watch the video demo here — [YouTube Demo](https://www.youtube.com/watch?v=0tNLbyQfCr4) 
* View  the Architecture diagram & code — [Live Kaggle Notebook](https://www.kaggle.com/code/nguyennamhongdoan/claimwise-ai-auto-claim-insurance)
* Read the Blog Post —  [Medium Post](https://medium.com/@bigqueryteam1/from-hours-to-minutes-how-claimwise-transforms-claims-with-intelligent-automation-7e30b3446f39)

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
### Setup

**1. Configure Google Cloud**
```bash
# Create storage bucket
gsutil mb gs://claim_medias

# Upload claim photos
gsutil -m cp -r ./photos/* gs://claim_medias/
```

**2. Set Up BigQuery**
- Create `claimwise_db` dataset
- Import `claims` table from `claims_metadata.xlsx`
- Create external table `claim_medias` with GCS URIs

**3. Build Embedding Models**
- Generate text embeddings for claim descriptions
- Create multimodal embeddings for damage photos
- Add `text_embedding` column to claims table

**4. Run Analysis**
- Execute the [Kaggle notebook](https://www.kaggle.com/code/nguyennamhongdoan/claimwise-ai-auto-claim-insurance)
- Review fraud flags and similarity scores
- Export results for business review

---

## Results

ClaimWise AI successfully processed 100+ test claims, detecting 3 fraud attempts through duplicate image recognition while reducing average processing time from 60 seconds to 0.15 seconds per claim.




