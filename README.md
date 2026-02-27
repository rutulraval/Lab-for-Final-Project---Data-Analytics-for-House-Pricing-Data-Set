<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=3,9,15&height=200&section=header&text=House%20Pricing%20Data%20Analytics&fontSize=36&fontColor=ffffff&animation=fadeIn&fontAlignY=40&desc=Linear%20Regression%20%7C%20EDA%20%7C%20Ridge%20%7C%20Pipeline%20%7C%20King%20County%2C%20USA&descAlignY=62&descSize=15" width="100%"/>

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white"/>
  <img src="https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white"/>
  <img src="https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/IBM-052FAD?style=for-the-badge&logo=ibm&logoColor=white"/>
</p>

</div>

---

## 📋 Project Overview

This repository contains a **data analytics and machine learning capstone project** completed as part of the IBM Data Science Professional Certificate programme. It performs a comprehensive end-to-end analytical workflow on the **King County, USA house sales dataset** — covering exploratory data analysis (EDA), data wrangling, statistical visualisation, and predictive modelling using regression techniques.

The project demonstrates the full data science pipeline: from raw data ingestion and cleaning, through visual correlation analysis, to model training, evaluation, and regularisation — resulting in quantified predictive performance metrics for house price estimation.

---

## 🎯 Analytical Objectives

The project addresses 10 structured analytical questions (`Q1`–`Q10`) that progressively deepen the analytical complexity:

| Question | Focus Area | Technique |
|:---|:---|:---|
| Q1 | Dataset structure & types | `df.dtypes`, `df.describe()` |
| Q2 | Data cleaning | Drop irrelevant columns (`id`, `Unnamed: 0`), null inspection |
| Q3 | Unique value distributions | `.value_counts().to_frame()` — floors, bedrooms, waterfront |
| Q4 | Waterfront impact on price | Box plot — price vs waterfront attribute |
| Q5 | Price vs square footage | Regression plot (`sns.regplot`) — `sqft_above` vs `price` |
| Q6 | Simple linear regression | `LinearRegression` on `sqft_living` → R² score |
| Q7 | Multiple linear regression | Multi-feature model — bedrooms, bathrooms, floors, sqft, condition, grade |
| Q8 | Scikit-learn Pipeline | `StandardScaler` + `PolynomialFeatures` + `LinearRegression` via `Pipeline` |
| Q9 | Ridge Regression | `Ridge(alpha=0.1)` — regularised model fit and evaluation |
| Q10 | Regularisation comparison | Second-order polynomial + Ridge → R² improvement quantified |

---

## 🛠️ Technology Stack

| Technology | Role |
|:---|:---|
| **Python 3.x** | Core language |
| **Jupyter Notebook** | Interactive analysis environment |
| **Pandas** | Data loading, cleaning, transformation, groupby |
| **NumPy** | Numerical operations and array handling |
| **Matplotlib** | Base plotting library |
| **Seaborn** | Statistical visualisation (`regplot`, `boxplot`) |
| **Scikit-learn** | `LinearRegression`, `Ridge`, `Pipeline`, `PolynomialFeatures`, `StandardScaler`, `train_test_split` |

**Notebook composition:**

```
Python / Jupyter cells (EDA + modelling)   ████████████████████  ~70%
Visual evidence (question screenshots)     ████████░░░░░░░░░░░░  ~25%
Markdown documentation                     ██░░░░░░░░░░░░░░░░░░   ~5%
```

---

## 📁 Repository Contents

| File | Description |
|:---|:---|
| `House_Sales_in_King_Count_USA.ipynb` | Main Jupyter Notebook — all 10 analytical questions |
| `dtypes.jpg` | Q1 output: dataset column types snapshot |
| `q2 drop and describe.jpg` | Q2 output: post-clean `.describe()` statistics |
| `q3 explaratory to_frame method.jpg` | Q3 output: `.value_counts().to_frame()` result |
| `q4 boxplot waterfront price.jpg` | Q4 output: waterfront vs price box plot |
| `q5 regplot price sqft.jpg` | Q5 output: regression plot — `sqft_above` vs `price` |
| `q6 r2 linear regression.jpg` | Q6 output: R² score for simple linear regression |
| `q7 linear regression other features.jpg` | Q7 output: multi-feature linear regression results |
| `q8 pipeline fit.jpg` | Q8 output: Pipeline fit with polynomial + scaling |
| `q9 ridge fit.jpg` | Q9 output: Ridge regression model R² |
| `q10 regularisation.jpg` | Q10 output: improved R² via polynomial Ridge regularisation |

---

## 📊 Dataset Summary

| Attribute | Value |
|:---|:---|
| **Dataset** | King County House Sales (USA) |
| **Source** | IBM Skills Network / Kaggle variant |
| **Records** | ~21,613 house sale transactions |
| **Features** | 21 (bedrooms, bathrooms, sqft_living, sqft_lot, floors, waterfront, view, condition, grade, sqft_above, sqft_basement, yr_built, yr_renovated, zipcode, lat, long, sqft_living15, sqft_lot15) |
| **Target variable** | `price` (house sale price in USD) |
| **Date range** | May 2014 – May 2015 |

---

## 🔬 Modelling Pipeline Detail

```
1. Data Ingestion
   └── pd.read_csv() → DataFrame

2. Data Wrangling
   ├── Drop: ['id', 'Unnamed: 0']
   ├── Null check & removal
   └── dtypes inspection

3. Exploratory Data Analysis
   ├── value_counts() → categorical distributions
   ├── sns.boxplot() → price vs waterfront
   └── sns.regplot() → price vs sqft_above

4. Modelling
   ├── Simple LR:   LinearRegression(sqft_living) → R²
   ├── Multiple LR: LinearRegression(7 features)  → R²
   ├── Pipeline:    StandardScaler + PolynomialFeatures(2) + LR → R²
   └── Ridge:       Ridge(alpha=0.1) + Polynomial(2) → R² (best)

5. Evaluation
   └── R² score comparison across all 4 models
```

---

## 🚀 Running the Notebook

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Launch

```bash
jupyter notebook "House_Sales_in_King_Count_USA.ipynb"
```

Execute all cells sequentially (`Cell → Run All`) to reproduce the full analysis and model evaluation pipeline.

---

## 📚 Course Context

| Detail | Value |
|:---|:---|
| Course | Data Analysis with Python |
| Provider | IBM / Coursera |
| Certificate | IBM Data Science Professional Certificate |
| Assignment | Final Capstone Lab |
| Dataset | King County House Sales, USA |

---

<div align="center">

**👤 Author: [Rutul Raval](https://github.com/rutulraval)** · IBM Data Science Certified · SDET

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=3,9,15&height=100&section=footer" width="100%"/>

</div>
