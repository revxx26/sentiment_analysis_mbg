# Sentiment Analysis of the Free Nutritious Meal Program (MBG) Using Naive Bayes

This project analyzes public sentiment toward Indonesia's Free Nutritious Meal Program (Makan Bergizi Gratis / MBG) using Natural Language Processing (NLP), text mining, TF-IDF, and the Naive Bayes classification algorithm.

The project uses public opinion data from social media X obtained through Kaggle to identify whether public responses toward the MBG program are positive or negative.

---

## Project Overview

The Free Nutritious Meal Program (MBG) has generated various responses from the public, including support and criticism regarding its benefits, budget, distribution, and implementation.

Due to the large amount of public opinion shared through social media, manual analysis can be inefficient. Therefore, this project applies sentiment analysis and machine learning techniques to automatically classify public opinion.

The main objective of this project is to build a sentiment classification model using Naive Bayes and evaluate its performance in identifying positive and negative sentiment.

---

## Objectives

The objectives of this project are:

- Analyze public sentiment toward the MBG program.
- Process and clean textual data from social media.
- Classify public opinion into positive and negative sentiment.
- Transform text data into numerical features using TF-IDF.
- Build a sentiment classification model using Naive Bayes.
- Evaluate model performance using Accuracy, Precision, Recall, and F1-Score.
- Visualize frequently occurring words using Word Cloud.

---

## Dataset

The dataset used in this project was obtained from Kaggle and contains public opinion data collected from social media X.

Dataset information:

- Source: Kaggle
- Platform: X (Twitter)
- Initial dataset: 3,459 records
- Final dataset after removing neutral sentiment: 1,868 records
- Sentiment classes:
  - Positive
  - Negative

### Sentiment Distribution

- Positive: 69.6%
- Negative: 30.4%

The majority of public opinion in the processed dataset was classified as positive sentiment.

---

## Project Workflow

The project follows the following workflow:

1. Problem Identification
2. Data Collection
3. Text Preprocessing
4. Sentiment Labeling
5. TF-IDF Feature Extraction
6. Word Cloud Visualization
7. Data Splitting
8. Naive Bayes Classification
9. Model Evaluation
10. Conclusion

---

## Text Preprocessing

Before being used for machine learning, the raw text data goes through several preprocessing stages.

### Cleaning

Removes unnecessary elements from the text such as:

- URLs
- Mentions
- Emojis
- Numbers
- Special characters
- Irrelevant symbols

### Case Folding

Converts all text into lowercase to ensure that words with different capitalization are treated as the same word.

### Tokenization

Splits sentences into individual words or tokens for further processing.

### Stopword Removal

Removes common words that do not provide significant information for sentiment classification.

### Stemming

Transforms words into their base forms by removing prefixes, suffixes, or other affixes.

---

## Sentiment Labeling

Sentiment labeling is performed automatically using a lexicon-based approach.

The sentiment of each text is determined based on the accumulated weight of positive and negative words contained in the text.

The sentiment classes used in this project are:

- Positive
- Negative

Neutral sentiment data was removed to allow the classification model to focus on distinguishing positive and negative opinions.

After removing neutral sentiment, 1,868 records were used for further analysis.

---

## Feature Extraction

Text data cannot be directly processed by most machine learning algorithms.

Therefore, this project uses:

### TF-IDF

TF-IDF stands for:

**Term Frequency - Inverse Document Frequency**

TF-IDF transforms textual data into numerical feature vectors based on the importance of each word within the dataset.

The resulting TF-IDF matrix is used as input for the Naive Bayes classification model.

---

## Machine Learning Model

This project uses the:

### Naive Bayes Classifier

Naive Bayes is a probabilistic machine learning algorithm commonly used for text classification and sentiment analysis.

The model classifies public opinion into:

- Positive sentiment
- Negative sentiment

---

## Train-Test Split

The processed dataset is divided using an 80:20 ratio.

- Training data: 1,494 records
- Testing data: 374 records

The training data is used to train the Naive Bayes model, while the testing data is used to evaluate its performance.

---

## Model Evaluation

The model is evaluated using several classification metrics:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

### Model Accuracy

The Naive Bayes model achieved:

**90.11% Accuracy**

### Classification Report

| Sentiment | Precision | Recall | F1-Score |
|------------|-----------|--------|----------|
| Negative | 0.99 | 0.66 | 0.79 |
| Positive | 0.88 | 1.00 | 0.94 |
| Macro Average | 0.93 | 0.83 | 0.86 |
| Weighted Average | 0.91 | 0.90 | 0.89 |

The model achieved a recall score of 1.00 for positive sentiment, meaning that all positive samples in the testing data were successfully identified.

The negative sentiment class achieved a precision score of 0.99.

---

## Data Visualization

### Sentiment Distribution

The sentiment distribution shows that:

- 69.6% of the analyzed opinions are positive.
- 30.4% of the analyzed opinions are negative.

### Word Cloud

Word Cloud visualization is used to identify frequently occurring words in positive and negative sentiment.

Positive sentiment commonly includes words related to the perceived benefits of the program.

Negative sentiment contains discussions related to concerns such as:

- Budget
- Implementation
- Distribution
- Potential misuse

### Confusion Matrix

A Confusion Matrix is used to analyze the number of correct and incorrect predictions produced by the classification model.

The results show that the model successfully classified most testing data correctly.

---

## Technologies and Tools

The technologies and tools used in this project include:

- Python
- Google Colab
- Pandas
- Natural Language Processing (NLP)
- Text Mining
- TF-IDF
- Naive Bayes
- Machine Learning
- Matplotlib
- WordCloud
- Scikit-learn

---

## Repository Structure

```text
sentiment_analysis_mbg/
│
├── Sentiment_Analysis_MBG.ipynb
│
├── README.md
│
├── dataset/
│   └── dataset.csv
│
└── paper/
    └── Sentiment_Analysis_MBG.pdf
```

The Jupyter Notebook contains the complete data processing, sentiment analysis, machine learning, visualization, and model evaluation workflow.

---

## Research Paper

This project is also documented in the research paper:

**"Analisis Sentimen Terhadap Program Makan Bergizi Gratis Menggunakan Metode Naive Bayes"**

### Authors

- Avandi Wardana
- Azhra Chandatya
- Moh. Fakih Erwansyah
- Revaldy Arrahman

Information Systems Study Program  
Universitas Bina Sarana Informatika

---

## Conclusion

This project demonstrates the implementation of an end-to-end sentiment analysis workflow for analyzing public opinion toward the Free Nutritious Meal Program (MBG).

The workflow includes:

- Data collection
- Text preprocessing
- Sentiment labeling
- TF-IDF feature extraction
- Data visualization
- Naive Bayes classification
- Model evaluation

From the processed dataset, positive sentiment represents 69.6% of the analyzed opinions, while negative sentiment represents 30.4%.

The Naive Bayes classification model achieved an accuracy of **90.11%**, demonstrating strong performance in classifying public sentiment within the dataset used in this project.

---

## Author

**Revaldy Arrahman**

Information Systems Student  
Universitas Bina Sarana Informatika

Interested in:

- Data Analytics
- Data Engineering
- Machine Learning
- Data Visualization
