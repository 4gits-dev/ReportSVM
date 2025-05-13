# ReportSVM
# Sentiment Analysis using SVM

This project applies **Support Vector Machine (SVM)** to perform sentiment analysis on movie or product reviews. The goal is to classify reviews as **positive** or **negative**.

---

## 📂 Dataset

- Dataset used is from [Kaggle UMICH SI650](https://www.kaggle.com/c/si650winter11/data)
- The data is in **TSV (Tab-Separated Values)** format.
- Each line consists of:
  - **Label**: `1` for positive sentiment, `0` for negative sentiment.
  - **Text**: the actual review.

> Example:
```tsv
1   I loved the Da Vinci Code.
0   The movie was boring and too long.
