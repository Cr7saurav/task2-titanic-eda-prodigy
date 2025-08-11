# task2-titanic-eda-prodigy
# Task 2 — Titanic: Data Cleaning & Exploratory Data Analysis (EDA)

## Project Overview
This repository contains the code and notebooks for **Task 2**: performing data cleaning and exploratory data analysis (EDA) on the Titanic dataset (Kaggle). The goal is to inspect data quality, handle missing values, create useful features, visualize distributions and relationships, and summarize insights.

## Dataset
- Source: Kaggle - Titanic: Machine Learning from Disaster  
- Files:
  - `data/raw/train.csv` — training data (contains `Survived` label)
  - Optionally: `data/raw/test.csv` if you want to run predictions

> **Do not** commit large raw datasets or private data. Keep raw files locally or use Git LFS if required.

## What you will find
- `notebooks/01_titanic_eda.ipynb` — interactive notebook with step-by-step EDA
- `scripts/clean_data.py` — reusable cleaning routines
- `plots/` — exported visualizations from the notebook
- `requirements.txt` — python dependencies

## EDA checklist
1. Inspect data shape, dtypes, and missing values.
2. Handle missing values:
   - Fill `Age` (median / predictive imputation)
   - Fill `Embarked` (mode)
   - Drop `Cabin` or encode if you choose
3. Feature engineering:
   - `Title` from `Name`
   - `FamilySize` (`SibSp + Parch + 1`)
   - `IsAlone`
   - `AgeGroup` buckets
4. Univariate analysis: histograms, count plots for `Sex`, `Pclass`, `Embarked`, `Age`, `Fare`.
5. Bivariate analysis: `Survived` vs `Sex`, `Pclass`, `Age`, `Fare`, `Title`.
6. Correlation & heatmap for numeric features.
7. Save plots to `plots/` directory.
8. Optional: quick model (RandomForest) to check feature importances.

## How to run
1. Create a virtual environment:
   ```bash
   python -m venv .venv
   contact  - sauravkumar2484@gmail.com
   source .venv/bin/activate   # macOS / Linux
   .venv\Scripts\activate      # Windows
