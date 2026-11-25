# 🎬 Movie Review Sentiment Analysis Using Naive Bayes

## 📌 Project Overview

This project uses Natural Language Processing (NLP) and Machine Learning to classify movie reviews into two sentiment categories: **Positive** and **Negative**.

The model learns from labeled movie reviews, processes the text using TF-IDF vectorization, and predicts the sentiment of new reviews using the Multinomial Naive Bayes algorithm.

A simple interactive interface is developed using Gradio to allow users to enter movie reviews and receive sentiment predictions.

## 🎯 Objectives

- Understand and analyze movie review data.
- Perform text preprocessing and cleaning.
- Convert textual data into numerical features using TF-IDF.
- Train and evaluate Naive Bayes classification models.
- Predict sentiment for new, unseen movie reviews.
- Build an interactive application using Gradio.

## 📂 Dataset

**Dataset:** IMDb Movie Reviews Dataset

- Total original records: 50,000
- Features: `review`, `sentiment`
- Target classes: Positive and Negative
- Duplicate reviews identified: 418
- Records after duplicate removal: 49,582
- Missing values: None

## 🛠️ Technologies & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- NLTK / NLP concepts
- Regular Expressions
- Gradio
- Joblib

## ⚙️ Project Workflow

1. **Data Loading:** Imported the IMDb movie review dataset using Pandas.
2. **Exploratory Data Analysis:** Examined dataset structure, missing values, duplicates, and sentiment distribution.
3. **Data Cleaning:** Removed duplicate reviews and cleaned text by:
   - Converting text to lowercase.
   - Decoding HTML entities.
   - Removing HTML tags.
   - Removing URLs.
   - Removing special characters and punctuation.
   - Removing extra whitespace.
4. **Feature Selection:** Separated review text and sentiment labels.
5. **Train-Test Split:** Split the dataset into 80% training and 20% testing data using stratification.
6. **Text Vectorization:** Applied TF-IDF Vectorizer to convert text into numerical features.
7. **Model Training:** Trained and compared three Naive Bayes algorithms:
   - Multinomial Naive Bayes
   - Bernoulli Naive Bayes
   - Complement Naive Bayes
8. **Model Evaluation:** Evaluated the models using accuracy, precision, recall, F1-score, and confusion matrix.
9. **New Review Testing:** Tested the trained model on new movie reviews.
10. **Deployment:** Created an interactive sentiment prediction interface using Gradio.

## 🤖 Model Performance

The following results were obtained using the test dataset.

| Model                   | Accuracy |
| ----------------------- | -------: |
| Multinomial Naive Bayes |   86.29% |
| Bernoulli Naive Bayes   |    \~86% |
| Complement Naive Bayes  |    \~86% |

### Multinomial Naive Bayes Classification Report

| Metric    | Negative | Positive |
| --------- | -------: | -------: |
| Precision |     0.85 |     0.88 |
| Recall    |     0.88 |     0.84 |
| F1-score  |     0.87 |     0.86 |

**Overall Accuracy: 86.29%**

The Multinomial Naive Bayes model was selected for the Gradio application.

## 🚀 Gradio Application

The project includes an interactive application where users can:

- Enter a movie review.
- Submit the review for prediction.
- View the predicted sentiment as Positive or Negative.

## 📁 Project Structure

```text
Movie-Review-Sentiment-Analysis/
│
├── Movie Review Sentiment Analysis Using Naive Bayes.ipynb
├── IMDB Dataset.csv
├── sentiment_model.pkl
├── sentiment_vectorizer.pkl
├── app.py
├── requirements.txt
└── README.md
```

*The structure above describes the intended project files; include the deployment files in the repository when they are ready.*

## 💻 Installation & Usage

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Gradio application

```bash
python app.py
```

Open the local Gradio URL displayed in the terminal to test the application.

## 📚 Key Learnings

- Text preprocessing and cleaning techniques.
- Working with real-world textual datasets.
- TF-IDF feature extraction.
- Understanding and comparing Naive Bayes algorithms.
- Model evaluation and performance interpretation.
- Testing predictions on unseen data.
- Building an interactive ML application using Gradio.

