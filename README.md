# Machine Learning Final Project - Santander
**Final Project (Grade 95, M.Sc. Data Science, HIT). An advanced binary classification project focused on predicting future customer transactions for the [Banco Santander Kaggle Competition](https://www.kaggle.com/competitions/santander-customer-transaction-prediction/overview). This project was defended in an oral exam and achieved a high score for its complexity and analytical depth.**
## Overview
The goal of this project is to identify which customers will make a specific transaction in the future, irrespective of the amount. The challenge involves dealing with anonymous numerical features and a highly imbalanced dataset (only 10% target rate), requiring sophisticated feature engineering and robust model evaluation.
## Key Features
- **Extensive Feature Engineering:** Expanded the original 200 features by adding **217 new statistical features** (mean, std, skew, kurtosis, etc.). Performed feature selection to create a "Lean Model" using the 65 most impactful features, reducing noise and improving inference speed.
- **Advanced Modeling with CatBoost:** Selected **CatBoost** as the primary algorithm, outperforming Logistic Regression due to its superior handling of the dataset's unique structure.
- **Imbalanced Data Strategy:** Focused on **AUC-ROC** as the primary metric (instead of simple accuracy) to effectively capture the minority class.
- **Model Explainability:** Analysis of feature importance to provide insights into what drives customer transactions.
## Tech Stack
- **Language:** Python
- **Libraries:** CatBoost, Scikit-learn, Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Metric:** AUC-ROC (Area Under the ROC Curve)
## Repository Structure
- `Santander_Transaction_Prediction_Final.ipynb`: Full end-to-end implementation (EDA, Feature Engineering, Modeling, Evaluation).
- `train.csv` / `test.csv`: The raw competition datasets (stored via Git LFS).
- `Final_Project_Instructions.pdf`: The official project requirements and guidelines.
- `submission_santander.csv`: Final predictions submitted for evaluation.
- `sample_submission.csv`: Reference format for Kaggle submissions.
- `kaggle_score.png`: Screenshot of the model's evaluation score.
## Dataset
The raw `train.csv` and `test.csv` files (~288MB each) are included in this repository, stored via **Git LFS** (Large File Storage) due to their size. To fetch them after cloning, make sure Git LFS is installed (`git lfs install`) and run `git lfs pull`.

The dataset originates from the [Santander Customer Transaction Prediction](https://www.kaggle.com/competitions/santander-customer-transaction-prediction/data) Kaggle competition, where it can also be downloaded directly.
