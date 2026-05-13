# 🏠 Flat Price Prediction

## Multi-Class Classification of Real Estate Prices

---

## 📌 Overview

This project predicts **property price categories (Low/Medium/High)** based on residential flat features. A comparative study of three machine learning algorithms — Logistic Regression, K-Nearest Neighbors, and Neural Networks — is performed on a dataset of 1200 properties.

---

## 📊 Dataset

| Aspect | Details |
|--------|---------|
| **Samples** | 1200 rows |
| **Features** | 12 (6 numerical, 6 categorical) |
| **Target** | Price_Category (Low / Medium / High) |
| **Class Distribution** | Medium (34.4%), Low (33.5%), High (32.1%) — well-balanced |

### Features
- **Location** — City Center / Suburbs / Countryside
- **Size_sqft** — Area in square feet
- **Num_Bedrooms** / **Num_Bathrooms**
- **Has_Balcony** — Yes/No
- **Floor_Number**
- **Building_Age_Years**
- **Parking_Available** — Yes/No
- **Nearby_Schools** — Few/Many
- **Distance_to_CityCenter_km**
- **Security_Level** — Low/Medium/High

---

## 🧠 Models Evaluated

| Model | Key Parameters | Accuracy |
|-------|---------------|----------|
| **Logistic Regression** | solver='lbfgs', max_iter=2000 | 36.11% |
| **K-Nearest Neighbors** | n_neighbors=5, euclidean | 31.67% |
| **Neural Network (MLP)** | hidden layers (128,64), relu, adam | 35.00% |

---

## 🔧 Preprocessing Steps

1. **Missing Value Imputation**
   - Numerical → Median imputation
   - Categorical → Mode imputation
2. **Encoding** — One-hot encoding for categorical features
3. **Scaling** — StandardScaler (LogReg, KNN) / MinMaxScaler (Neural Network)
4. **Train-Test Split** — 70/30 random split

---

## 📈 Results Summary
Logistic Regression : 36.11% accuracy
Neural Network : 35.00% accuracy
KNN : 31.67% accuracy
