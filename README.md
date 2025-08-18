# 🖱️ Click-Through Rate (CTR) Prediction Model

This project focuses on predicting whether a user will **click on an online advertisement (CTR prediction)** using **machine learning** techniques.  
It involves **data preprocessing, feature engineering, text processing, and model evaluation** to build a robust prediction pipeline.  

---

## 📌 Project Overview

- **Goal:** Predict the probability of a user clicking an advertisement.  
- **Dataset:** Contains user demographics, online behavior, and ad content (e.g., *Daily Time Spent on Site*, *Age*, *Ad Topic Line*, *City*, *Country*).  
- **Models Used:**  
  - Logistic Regression (baseline)  
  - Decision Tree / Random Forest (experimental)  -->To Be Applied
  - XGBoost / LightGBM (planned)  -->To Be Applied
- **Key Techniques:**  
  - Exploratory Data Analysis (EDA)  
  - Categorical Encoding (LabelEncoder, CountEncoder, OneHotEncoder)  
  - Text Preprocessing (NLTK + TF-IDF)  -->NLTK to be applied
  - Feature Engineering & Scaling  
  - Model Evaluation with ROC-AUC, Precision-Recall  

---

## 📂 Project Structure


---

## ⚙️ Workflow

### 1. Data Loading  
- Load dataset with Pandas.  
- Inspect columns: numeric, categorical, and text-based features.  

### 2. Exploratory Data Analysis (EDA)  
- Visualize distributions of numeric features.  
- Check correlations with target (`Clicked on Ad`).  
- Analyze categorical balance (City, Gender, Country).  

### 3. Preprocessing  
- Handle missing values and duplicates.  
- **Categorical Encoding:** OneHot, Count, or Target encoding.  
- **Text Cleaning:** Tokenization, stopword removal, lemmatization (NLTK).  
- **Vectorization:** TF-IDF on `Ad Topic Line`.  
- **Scaling:** Normalize numeric features if needed.  

### 4. Feature Engineering  
- Extract keywords from ad content.  
- Create interaction features (e.g., *Daily Internet Usage × Age*).  
- Dimensionality reduction for text vectors (TruncatedSVD).  

### 5. Model Training  
- Train Logistic Regression (baseline).  
- Compare with Random Forest, XGBoost, LightGBM.  
- Apply cross-validation.  

### 6. Model Evaluation  
- Accuracy, Precision, Recall, F1-score.  
- ROC-AUC and PR curve.  
- Confusion matrix visualization.  

### 7. Experiments & Notes  
- Baseline LR → ROC-AUC: `0.xx`.  
- Added TF-IDF (`Ad Topic Line`) → ROC-AUC improved to `0.xx`.  
- Encoding strategies tested: OneHot vs. CountEncoder.  

---

## 📊 Results (Sample)

| Model                | Accuracy | ROC-AUC | Notes                          |
|-----------------------|----------|---------|--------------------------------|
| Logistic Regression   | 0.84     | 0.78    | Baseline numeric + categorical |
| TF-IDF + LR           | 0.87     | 0.81    | Added Ad Topic Line            |
| Random Forest         | 0.89     | 0.83    | Better handling of categories  |

---

## 🔧 Requirements

Install dependencies:

```bash
pip install -r requirements.txt
