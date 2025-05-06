# 🧠 Analysing COVID-19 Vaccine Tweet Sentiment Using Machine Learning

*Contributors:*  
- Lakshya Jain (23UCS633)  
- Monish Mathur (23UCS648)  
- Naman Khandelwal (23UCS655)

---

## ▶️ Try It Yourself

You can run the project directly using Google Colab:

👉 [Open in Google Colab](https://colab.research.google.com/drive/18oSsL7qsirnIaO7M6R0yBmYIUumG20yC?usp=sharing)

Alternatively, upload the .ipynb notebook manually to [Google Colab](https://colab.research.google.com/), run all cells, and explore the results.

---

## 📌 Introduction

Public sentiment on critical health topics like vaccinations significantly influences public health decisions. In this project, we analyse tweets related to COVID-19 vaccines using machine learning to classify them as *Positive, **Negative, or **Neutral*.

We built a pipeline that:
- Preprocesses tweet data  
- Handles emoji sentiment  
- Trains and evaluates models  
- Visualizes results  

---

## 📂 Dataset Overview

We used the [COVID-19 Vaccination Tweets Dataset](https://www.kaggle.com/datasets) from Kaggle, which contains:
- 🧾 11020 tweets  
- 📆 Metadata like dates, hashtags, user info  
- 📝 Focused on the "text" column for sentiment analysis

---

## 🧹 Step 1: Data Preprocessing

Preprocessing steps included:
- *Cleaning:* Lowercasing, removing URLs, mentions, hashtags, and non-alphanumeric characters  
- *Emoji Handling:* Detected emojis like 😊, 👎 and incorporated their sentiment  
- *Tokenization & Stopword Removal:* Removed common and custom stopwords  
- *Stemming:* Used PorterStemmer to reduce words to root form  
- *Filtering & Deduplication:* Removed empty and duplicate tweets  

---

## 🏷️ Step 2: Sentiment Labelling

If sentiment labels were missing:
- Used TextBlob polarity scores  
- Combined polarity with emoji sentiment  
- Assigned sentiment labels:
  - Positive for score > 0.05  
  - Negative for score < -0.05  
  - Neutral otherwise  

---

## 🤖 Step 3: Text Vectorization & Model Training

- *Vectorization:* TF-IDF (unigrams and bigrams)  
- *Models:*
  - Logistic Regression  
  - Random Forest (selected as best)  
- *Data Split:* 80% training, 20% testing  
- *Hyperparameter Tuning:* Used GridSearchCV with F1-weighted scoring  

---

## 📊 Step 4: Evaluation & Results

- *Metrics Used:*
  - Accuracy  
  - Precision, Recall, F1-score  
  - Confusion Matrix  

- *Model Comparison:*
  - Random Forest outperformed Logistic Regression and was chosen as the final model

- *Feature Importance:*
  - Random Forest: TF-IDF term contributions  
  - Logistic Regression: Feature coefficients

- *Visualizations:*
  - Sentiment distribution  
  - Word clouds per sentiment class  
  - Confusion matrix for best model  

---

## ✅ Conclusion

This project demonstrates the use of machine learning for sentiment analysis of COVID-19 vaccine-related tweets. We built an end-to-end system capable of:
- Cleaning and processing raw tweet text  
- Extracting sentiment from text and emojis  
- Training and evaluating models  
- Visualizing sentiment trends

This system can help health officials, policymakers, and researchers understand public opinion in real time.
