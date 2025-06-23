# Web-Based-Analysis-of-Women-Hormonal-Health-Challenges-using-Data-Mining-and-NLP-Techniques

## Project Overview  
Empathy Engine is a unified analysis system designed to explore and address the **emotional and psychological challenges** faced by women dealing with **Polycystic Ovary Syndrome (PCOS)** and **Thyroid disorders**. By combining **web mining**, **sentiment & emotion detection**, and **machine learning**, this project transforms **Reddit conversations** and **trusted medical sources** into actionable support recommendations.

The system not only detects emotions like *sadness*, *anger*, and *fear* from user-generated content but also **matches them with remedies** sourced from **Mayo Clinic**, **Healthline**, and **WebMD**, offering holistic insights that bridge emotional and clinical support.

---

## Datasets Used

| Source         | Type                 | Purpose                              |
|----------------|----------------------|--------------------------------------|
| Reddit (r/PCOS, r/thyroidhealth) | User-generated content | Real stories, symptoms, emotional struggles |
| Mayo Clinic, Healthline, WebMD | Clinical content        | Evidence-based remedies & advice     |

---

## Data Preprocessing

- Cleaned and normalized Reddit text
- Removed emojis, URLs, punctuation
- Applied tokenization, lowercasing, and TF-IDF vectorization
- Used `ast.literal_eval` for list parsing in scraped data
- Handled class imbalance using **SMOTE**

---

## 🧠 Algorithms & Models

| Module              | Methodology                       | Outcome                                   |
|---------------------|-----------------------------------|-------------------------------------------|
| Sentiment Analysis  | VADER (NLTK)                      | Classifies as Positive / Neutral / Negative |
| Emotion Detection   | DistilRoBERTa (Hugging Face)      | Detects Joy, Sadness, Anger, Fear, etc.   |
| ML Classification   | Logistic Regression, SVC, XGBoost | Best: SVC with **86% accuracy**           |
| Remedy Matching     | Keyword Extraction + Mapping      | Emotion-to-remedy recommendations         |

---

## Key Results

**Sentiment Analysis**

| Condition | Positive | Negative | Neutral |
|-----------|----------|----------|---------|
| PCOS      | 40%      | 45%      | 15%     |
| Thyroid   | 35%      | 50%      | 15%     |

**Emotion Detection**

| Emotion   | PCOS (%) | Thyroid (%) |
|-----------|----------|-------------|
| Sadness   | 40       | 45          |
| Anger     | 20       | 25          |
| Fear      | 15       | 10          |
| Joy       | 15       | 10          |

---

## Tech Stack

- **Language**: Python 3.9  
- **Libraries**: NLTK, Transformers, scikit-learn, imbalanced-learn  
- **Scraping**: asyncpraw, BeautifulSoup  
- **Visualization**: seaborn, matplotlib  
- **ML Models**: Logistic Regression, SVC, XGBoost  
- **Text Vectors**: TF-IDF  

---

## Future Scope

- Integrate GPT for contextual emotion-aware chatbot responses  
- Expand support to other hormonal conditions (e.g., endometriosis)  
- Include multimedia data (voice, videos) from vlogs/forums  
- Build a feedback-enabled recommender system  
- Add XAI for interpretability and explainability in predictions  

> 💡 “Data can heal—when it listens.”

---

