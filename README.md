# 💬 Airline Sentiment Analysis

> An NLP pipeline that classifies US-airline tweets as positive, negative, or neutral —
> turning unstructured social-media chatter into actionable customer-experience insight.

![status](https://img.shields.io/badge/status-complete-success)
![python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![nlp](https://img.shields.io/badge/NLP-NLTK-green)
![model](https://img.shields.io/badge/best%20model-Random%20Forest%2086.5%25-blue)

## 📌 Business Problem
Airlines compete heavily on customer satisfaction, and much of that sentiment now lives
on social media. Manually reading thousands of tweets is impossible. This project builds
an automatic sentiment classifier so airlines can monitor brand perception at scale,
spot recurring pain points, and respond before issues escalate.

## 🎯 Objectives
1. Classify airline-related tweets into **positive / negative / neutral** sentiment.
2. Surface the operational themes driving negative sentiment.
3. Translate results into recommendations for customer-experience and brand management.

## 🗂️ Data
[Twitter US Airline Sentiment](https://data.world/socialmediadata/twitter-us-airline-sentiment)
— tweets scraped from February 2015 covering several US carriers.

## 🏗️ Workflow
```
Raw tweets → cleaning & preprocessing (tokenization, stemming, stop-word removal)
          → TF-IDF vectorization → model training & comparison → evaluation
```

## ✨ Methods
- Text preprocessing with **NLTK** (tokenization, stemming, stop-word removal)
- **TF-IDF** feature extraction
- Trained and compared multiple classifiers; selected the best by accuracy

## 📊 Results
| Metric | Value |
|---|---|
| **Best model** | Random Forest (untuned) |
| **Accuracy** | **86.5%** |
| Improvement over baseline | ~13 percentage points |

**Key insights**
- Most negative sentiment clusters around **cancelled, delayed, and missed flights**.
- Sentiment is a meaningful signal for customer churn risk in this dataset.
- Class imbalance means the model can lean toward the majority class — a known limitation.

> 📊 *Add a confusion matrix and a top-terms-per-sentiment chart here to make results visual.*

## 💡 Recommendations
- Airlines with high negative-sentiment volume should prioritise the recurring themes
  above (punctuality, baggage handling, customer service).
- Use the classifier for **continuous social-media monitoring** and faster response.
- Personalised outreach and clearer disruption communication can reduce negative sentiment.

## ⚠️ Limitations
- Misclassifies roughly one in seven tweets.
- Class imbalance may bias predictions toward the majority class.

## 🚀 Quickstart
```bash
git clone https://github.com/leokariuki/airline-sentiment-analysis.git
cd airline-sentiment-analysis
pip install -r requirements.txt   # add this file: pandas, scikit-learn, nltk, matplotlib
jupyter lab "group_5 notebook.ipynb"
```

## 🔮 Future Improvements
- Add a transformer baseline (DistilBERT / Hugging Face) and compare to TF-IDF + RF.
- Address class imbalance (resampling / class weights).
- Deploy as a Streamlit app or Hugging Face Space for live tweet scoring.

## 👤 Author
**Leo Kariuki** — [LinkedIn](https://www.linkedin.com/in/leokariuki/) · [Portfolio](https://leokariuki.lovable.app)
