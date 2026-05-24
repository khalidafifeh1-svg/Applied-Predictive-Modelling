# Applied-Predictive-Modelling
# Cyberbullying Detection in Social Media using Machine Learning

##  Overview
This project focuses on detecting cyberbullying and offensive content in social media comments using machine learning and predictive modelling techniques. The system classifies text into:

- Binary Classification: Cyberbullying vs Non-Cyberbullying  
- Multi-Class Classification: Normal, Offensive, Hate Speech  

The project also explores how different demographic groups are targeted in online abuse.

---

##  Objectives
- Build a model to detect cyberbullying in text data  
- Handle large-scale and imbalanced datasets  
- Compare multiple models (Ridge, Lasso, Logistic Regression)  
- Evaluate performance using standard metrics  

---

##  Datasets
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

## Technologies Used
- R  
- Machine Learning: `glmnet`, `caret`  
- Text Processing: `tm`, `tidytext`, `SnowballC`  
- Data Manipulation: `dplyr`, `tidyr`  
- Visualisation: `ggplot2`, `wordcloud`  

---

##  Methodology

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

##  Results

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

 *Insight:*  
Both models achieved very high recall, meaning they are effective at detecting cyberbullying. However, specificity was low due to class imbalance.

---

### Multi-Class Classification (Dataset 2)

**Multinomial Logistic Regression**
- Accuracy: 13.33%  
- Strong performance in "Offensive" class but weak overall  

**Linear Model**
- Accuracy: 65%  
- Better performance across multiple classes  

 *Insight:*  
Multi-class classification is significantly more challenging due to class imbalance and complexity.

---

## Key Insights
- Cyberbullying comments tend to be shorter  
- Strong class imbalance impacts model performance  
- Feature selection and regularisation are critical  
- Deep learning could improve multi-class performance  

---

##  Future Improvements
- Apply Deep Learning models (LSTM, BERT)  
- Handle class imbalance using SMOTE or resampling  
- Improve feature representation (word embeddings)  
- Deploy as a real-time moderation system  

---
<img width="1344" height="960" alt="download" src="https://github.com/user-attachments/assets/057e2083-f8bd-4a76-9083-4a3cf866635d" />
<img width="1344" height="960" alt="download" src="https://github.com/user-attachments/assets/d4892aec-be19-444a-bf33-074683eb960a" />
<img width="1344" height="960" alt="download" src="https://github.com/user-attachments/assets/91bba04d-fc9d-4819-8e20-763c47458751" />
<img width="1344" height="960" alt="download" src="https://github.com/user-attachments/assets/7f6d3f8e-f42c-4042-a933-2b6106e8a53d" />
<img width="1344" height="960" alt="download" src="https://github.com/user-attachments/assets/6603e942-8339-4da4-8713-e74d93b905f9" />
<img width="1344" height="960" alt="download" src="https://github.com/user-attachments/assets/d773e413-3d90-44a7-a91b-90f12e0bc70b" />
<img width="1344" height="960" alt="download" src="https://github.com/user-attachments/assets/b0f8cdef-989d-4f5c-b373-d9b6484354de" />
<img width="1344" height="960" alt="download" src="https://github.com/user-attachments/assets/2fc28a08-5c33-434b-bca8-17d481ddf4db" />
<img width="1344" height="960" alt="download" src="https://github.com/user-attachments/assets/d2a8b891-5ef3-4419-a9bc-5eecf12cfe9e" />
<img width="1344" height="960" alt="download" src="https://github.com/user-attachments/assets/273e7e41-c0b5-4da4-9d08-65370ef4d2de" />


```r
