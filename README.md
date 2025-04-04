
# 🧠 Sentiment Analysis on Threads App Reviews (USA - English)

## 📌 Project Overview

This repository contains a complete sentiment analysis pipeline to **predict sentiment labels from app reviews** of the **Threads application** scraped from the **Google Play Store**, specifically from **users in the United States using English language**.

The project involves:

- Web scraping Play Store reviews
- Text preprocessing & slang word handling
- Labeling using the VADER lexicon
- Data visualization (Polarity Distribution & WordCloud)
- Feature extraction using TF-IDF
- Model training with:
  - Support Vector Machine (SVM)
  - Random Forest
  - Deep Learning

---

## 📂 Project Structure

```
.
├── Proyek_Analisis_Sentimen_Dicoding_Oman.ipynb
├── README.md
├── /data
│   └── threads_reviews_en_us.csv
└── /visuals
    ├── polarity_distribution.png
    └── wordcloud_positive_negative.png
```

---

## 🛠️ Technologies Used

- Python (Pandas, Scikit-learn, Matplotlib, Seaborn, TensorFlow/Keras)
- Natural Language Processing (NLP)
- VADER Sentiment Analyzer
- TF-IDF Vectorizer
- Machine Learning Models: SVM, Random Forest
- Deep Learning (Dense Neural Networks)
- Jupyter Notebook

---

## 🔍 Workflow Breakdown

### 1. 📥 Scraping Reviews
Collected user reviews of Threads from the **Google Play Store** using the `google-play-scraper` targeting **US region** and **English language**.

---

### 2. 🧹 Preprocessing
Text cleaning includes:
- Lowercasing
- Removing punctuation, numbers, and stopwords
- Custom function to replace **slang words**

> Example: `"u"` → `"you"`, `"idk"` → `"I don't know"`

---

### 3. 🏷️ Sentiment Labeling (VADER Lexicon)
Using **VADER** to assign:
- `Positive` (compound ≥ 0.05)
- `Neutral` (compound > -0.05 and < 0.05)
- `Negative` (compound ≤ -0.05)

---

### 4. 📊 Data Visualization

#### 📈 Polarity Distribution
Visualized the polarity score distribution across reviews.

#### ☁️ WordCloud Exploration
- Word clouds generated to highlight dominant terms in **positive** and **negative** reviews.

---

## 🤖 Modeling

### 🔢 Feature Extraction
Used **TF-IDF vectorization** to convert text into numerical format.

---

### ✅ Models Implemented

| Model            | Split Ratio | Description                          |
|------------------|-------------|--------------------------------------|
| **SVM**          | 80/20       | Support Vector Machine classifier    |
| **Random Forest**| 70/30       | Ensemble-based classification        |
| **Deep Learning**| Custom      | Fully connected layers with ReLU + Dropout |

---

## 📈 Results
Each model's performance is evaluated using:
- Accuracy
- Confusion Matrix
- Classification Report

(📌 *Metrics are available in the notebook output.*)

---

## 🚀 How to Run

1. Clone the repo:
```bash
git clone https://github.com/your-username/threads-sentiment-analysis.git
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Open the notebook:
```bash
jupyter notebook Proyek_Analisis_Sentimen_Dicoding_Oman.ipynb
```

---

## 📚 Future Improvements

- Include multilingual support
- Real-time streaming review analysis
- Integration with dashboard (Streamlit / Flask)

---

## 🙌 Acknowledgement

This project was completed as part of **Dicoding's Data Science Path**, focusing on real-world text sentiment analysis in the app ecosystem.
