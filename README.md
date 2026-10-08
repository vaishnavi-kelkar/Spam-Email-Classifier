# Spam Email Classifier — NLP & Machine Learning

## Overview

This project implements a machine learning system to classify text messages as **Spam** or **Ham (Not Spam)** using Natural Language Processing (NLP) techniques.

The project was completed as **Kodbud AI Internship — Task 1**.

## Technologies Used

* Python
* Pandas
* NLTK
* Scikit-learn
* Matplotlib
* Seaborn
* TF-IDF
* Multinomial Naive Bayes
* Logistic Regression

## Dataset

The project uses the `spam.csv` dataset containing labeled messages classified as **ham** or **spam**.

The labels are encoded as:

* `0` → Ham
* `1` → Spam

## Project Workflow

### 1. Data Loading and Cleaning

The dataset is loaded using Pandas and the relevant columns are selected and renamed as:

* `Category`
* `Message`

The dataset is checked for information and missing values.

### 2. Label Encoding

The message categories are converted into numerical labels using `LabelEncoder`.

### 3. Exploratory Data Analysis

The project analyzes:

* Number of characters
* Number of words
* Number of sentences

The distributions of message length and word count are visualized for both ham and spam messages.

### 4. Text Preprocessing

The messages are cleaned using:

* Lowercase conversion
* Tokenization
* Removal of non-alphanumeric tokens
* Stopword removal
* Punctuation filtering
* Porter stemming

### 5. TF-IDF Feature Extraction

The cleaned messages are converted into numerical features using **TF-IDF (Term Frequency–Inverse Document Frequency)**.

A maximum of **3,000 features** is used.

### 6. Train-Test Split

The dataset is divided into:

* **80% training data**
* **20% testing data**

### 7. Machine Learning Models

Two classification models are trained and evaluated:

#### Multinomial Naive Bayes

Used as the primary spam classification model.

#### Logistic Regression

Used as a comparison model to evaluate the performance of another classification approach.

### 8. Model Evaluation

The models are evaluated using:

* Accuracy
* Precision
* Recall
* F1-score

A **confusion matrix** is also generated for the Multinomial Naive Bayes model.

### 9. New Message Prediction

A prediction function is implemented to classify new messages as:

* **Spam**
* **Ham (Not Spam)**

Example messages are tested using the trained Naive Bayes model.

## Project Structure

```text
Spam-Email-Classifier/
│
├── Spam_Email_Classifier.ipynb
└── README.md
```

## How to Run

1. Open `Spam_Email_Classifier.ipynb` in Google Colab or Jupyter Notebook.
2. Make sure the `spam.csv` dataset is available in the working environment.
3. Install the required Python libraries if necessary.
4. Run the notebook cells in order.
5. View the model evaluation results and predictions.

## Results

The notebook evaluates both **Multinomial Naive Bayes** and **Logistic Regression** using accuracy, precision, recall, and F1-score.

The exact numerical results should be taken from the notebook's output.
