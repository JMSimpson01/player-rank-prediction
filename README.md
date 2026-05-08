# Chess Player Skill Prediction Using Machine Learning

## Project Overview

This project shows how machine learning can be used to predict chess player skill ratings based on gameplay stats from online chess matches.

This project reviews chess match data and trains classification models in order to determine whether or not a player belongs to one of the following skill levels:

- Beginner
- Intermediate
- Advanced
- Expert

The project was completed for the CS 2100 Introduction to Machine Learning final project.

---

# Research Question

Can machine learning predict a chess player’s skill rating using only gameplay stats and match information?

---

# Dataset

Dataset Source:
- Kaggle Chess Games Dataset

Dataset Link:
https://www.kaggle.com/datasets/datasnaek/chess

The dataset contains information about thousands of online chess matches, including:

- Number of turns
- Opening used
- Match type
- Match result
- Player ratings

---

# Technologies Used

- Python
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Joblib
- Jupyter Notebook
- Visual Studio Code

---

# Project Structure

player-rank-prediction/

├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_EDA.ipynb
│   ├── 02_Preprocessing.ipynb
│   ├── 03_Baseline_Model.ipynb
│   └── 04_Final_Model.ipynb
│
├── models/
│   └── random_forest_model.pkl
│
├── reports/
│   └── figures/
│
├── presentation/
│
├── requirements.txt
├── README.md
└── .gitignore

---

# Exploratory Data Analysis

The project includes exploratory data analysis to examine:

- Skill level distribution
- Feature relationships
- Correlations between gameplay statistics
- Dataset structure and missing values

Visualizations include:

- Skill distribution bar chart
- Correlation heatmap
- Confusion matrix
- Feature importance graph

---

# Feature Engineering

The following features were used for prediction:

- turns
- opening_ply
- rated
- opening_name_encoded

Player ELO ratings were converted into skill categories:

| ELO Range | Skill Category |
|---|---|
| Below 1000 | Beginner |
| 1000–1399 | Intermediate |
| 1400–1799 | Advanced |
| 1800+ | Expert |

---

# Machine Learning Models

## Baseline Model
- Logistic Regression

## Final Model
- Random Forest Classifier

The Random Forest model was able to achieve higher accuracy and better classification performance than the baseline model.

---

# Evaluation Metrics

The models were evaluated using:

- Accuracy
- Classification Report
- Confusion Matrix

These metrics were used to analyze model performance and prediction quality.

---

# Results

The Random Forest model was able to outperform the Logistic Regression baseline model.

Important findings:
- Opening selection influenced skill prediction
- Certain skill categories was easier to classify than others
- Additional feature engineering improved the models performance

---

# Saved Model

The final trained model was saved using Joblib:

models/random_forest_model.pkl

---

# How to Run the Project

## 1. Install Dependencies

```bash
pip install -r requirements.txt

