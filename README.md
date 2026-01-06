# Debug Effort Estimation System

## 📌 Overview
The Debug Effort Estimation System is a machine learning project designed to analyze software error logs and estimate the level of effort required to resolve them.  
The project combines Natural Language Processing (NLP) with structured data features to provide meaningful insights into debugging complexity.

This project is built as a real-world, developer-focused ML use case rather than a traditional academic dataset.

---

## 🎯 Problem Statement
Not all software errors require the same amount of debugging effort.  
Some errors are resolved instantly, while others consume significant developer time.

This project aims to:
- Classify errors into **Low, Medium, and High** debugging effort
- Analyze patterns in error messages and metadata
- Provide an interpretable ML solution for developer productivity analysis

---

## 🗂 Dataset Description
The dataset consists of manually curated error logs with the following features:

- `error_message` – Raw error message text (used for NLP)
- `error_type` – Category of error (Syntax, Runtime, Import, IO)
- `language` – Programming language
- `file_type` – Source file type
- `line_number` – Line where the error occurred
- `time_to_fix` – Time taken to resolve the error (in minutes)
- `effort_level` – Debug effort class (Low / Medium / High)

### Effort Level Definition
Effort levels are derived objectively from resolution time:
- **Low**: < 10 minutes
- **Medium**: 10–30 minutes
- **High**: > 30 minutes

---

## 🔍 Exploratory Data Analysis (EDA)
EDA was performed to understand:
- Distribution of debug effort levels
- Error types vs resolution time
- Patterns in frequently occurring errors

This helped validate labeling logic and guide feature selection.

---

## 🧠 Machine Learning Approach

### Classification
- **Model**: Logistic Regression
- **Text Processing**: TF-IDF Vectorization on error messages
- **Additional Features**: Encoded categorical variables and line numbers

### Evaluation Metrics
- Precision
- Recall
- F1-score
- Confusion Matrix

Due to the small dataset size, certain classes may be underrepresented in the test split. This limitation is acknowledged and discussed.

---

## ⚠️ Limitations
- Small, manually curated dataset
- Class imbalance due to limited samples
- Performance expected to improve with larger real-world error logs

---

## 🚀 Future Improvements
- Regression model to predict exact resolution time
- Larger dataset from real developer logs
- Deployment as a developer support tool or dashboard

---

## 🛠 Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn

---

## 👤 Author
Jagadheesan
