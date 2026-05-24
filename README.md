# Applied-Predictive-Modelling
# Cyberbullying Detection in Social Media using Machine Learning

## 📌 Overview
This project focuses on detecting cyberbullying and offensive content in social media comments using machine learning and predictive modelling techniques. The system classifies text into:

- Binary Classification: Cyberbullying vs Non-Cyberbullying  
- Multi-Class Classification: Normal, Offensive, Hate Speech  

The project also explores how different demographic groups are targeted in online abuse.

---

## 🎯 Objectives
- Build a model to detect cyberbullying in text data  
- Handle large-scale and imbalanced datasets  
- Compare multiple models (Ridge, Lasso, Logistic Regression)  
- Evaluate performance using standard metrics  

---

## 📊 Datasets
### Dataset 1 (Binary Classification)
- Combined multiple datasets (Twitter, YouTube, Kaggle)
- Total samples: ~225,000+
- Labels:
  - 0 → Non-Cyberbullying  
  - 1 → Cyberbullying  

### Dataset 2 (Multi-Class Classification)
- HateXplain dataset  
- Labels:
  - Normal  
  - Offensive  
  - Hate Speech  
- Includes demographic categories:
  - Race, Religion, Gender, Sexual Orientation  

---

## 🛠️ Technologies Used
- R  
- Machine Learning: `glmnet`, `caret`  
- Text Processing: `tm`, `tidytext`, `SnowballC`  
- Data Manipulation: `dplyr`, `tidyr`  
- Visualisation: `ggplot2`, `wordcloud`  

---

## ⚙️ Methodology

### Data Preprocessing
- Removed duplicates and missing values  
- Cleaned text (URLs, punctuation, numbers)  
- Lowercasing and stopword removal  
- Tokenisation and stemming  

### Feature Engineering
- Document-Term Matrix (DTM)  
- TF-IDF representation  

### Models Used
- Ridge Regression (L2 Regularisation)  
- Lasso Regression (L1 Regularisation)  
- Multinomial Logistic Regression  

### Model Optimisation
- Grid Search  
- 5-Fold Cross Validation  
- Parallel Computing  

---

## 📈 Results

### Binary Classification (Dataset 1)

**Ridge Regression**
- Accuracy: 88.59%  
- Recall: 100%  
- F1-Score: 93.95%  
- AUC: 0.842  

**Lasso Regression**
- Accuracy: 88.74%  
- Recall: 99.67%  
- F1-Score: 94.01%  
- AUC: 0.749  

📌 *Insight:*  
Both models achieved very high recall, meaning they are effective at detecting cyberbullying. However, specificity was low due to class imbalance.

---

### Multi-Class Classification (Dataset 2)

**Multinomial Logistic Regression**
- Accuracy: 13.33%  
- Strong performance in "Offensive" class but weak overall  

**Linear Model**
- Accuracy: 65%  
- Better performance across multiple classes  

📌 *Insight:*  
Multi-class classification is significantly more challenging due to class imbalance and complexity.

---

## 📊 Key Insights
- Cyberbullying comments tend to be shorter  
- Strong class imbalance impacts model performance  
- Feature selection and regularisation are critical  
- Deep learning could improve multi-class performance  

---

## 🚀 Future Improvements
- Apply Deep Learning models (LSTM, BERT)  
- Handle class imbalance using SMOTE or resampling  
- Improve feature representation (word embeddings)  
- Deploy as a real-time moderation system  

---

## ▶️ How to Run

```r
# Install required packages
install.packages(c("tm", "caret", "glmnet", "tidytext", "ggplot2"))

# Run the main script
source("main.R")
