# Hospital Readmission Prediction using PCA and Random Forest

This project predicts hospital readmission for diabetic patients using **machine learning**.  
We use **Logistic Regression** and **Random Forest** models, with **PCA visualization** and **SMOTE** for handling class imbalance.

## Dataset
- Source: https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008
- Size: 101,766 patient encounters, ~50 variables (after initial inspection)
- Key target: `readmitted` (binary classification after preprocessing)

## Project Structure
- data/ — Raw & processed data (contains `diabetic_data.csv`)
- notebooks/ — Jupyter/Colab notebooks
  - `01_data_cleaning_eda.ipynb` — data cleaning & EDA
  - `02_feature_engineering_scaling_pca.ipynb` — encoding, scaling, PCA
  - `03_modeling_logistic_random_forest.ipynb` — modeling and evaluation
- results/ — Plots, PCA graphs, confusion matrices
- requirements.txt — Python packages used
- .gitignore — files & folders to ignore

## Project Workflow
1. **Data Import & Cleaning**
   - Replace or impute missing values
   - Convert categorical variables to appropriate types
   - Map age ranges to numeric values where required
2. **Exploratory Data Analysis (EDA)**
   - Distribution of age, gender, race
   - Readmission rates and class imbalance checks
   - PCA for dimensionality reduction and visualization
3. **Feature Engineering & Scaling**
   - One-hot encoding for categorical variables
   - StandardScaler applied to numeric features
4. **Model Training**
   - Logistic Regression
   - Random Forest
   - Handle class imbalance with SMOTE (or other resampling)
5. **Evaluation**
   - Accuracy, Precision, Recall, F1-Score
   - Confusion Matrix & Heatmap
   - ROC Curve & AUC

## Notebooks (open in Google Colab)
- Data Cleaning & EDA: https://colab.research.google.com/github/Abhishekupca/Hospital-Readmission-Prediction-using-PCA-and-RF/blob/main/notebooks/01_data_cleaning_eda.ipynb
- Feature Engineering & PCA: https://colab.research.google.com/github/Abhishekupca/Hospital-Readmission-Prediction-using-PCA-and-RF/blob/main/notebooks/02_feature_engineering_scaling_pca.ipynb
- Modeling & Evaluation: https://colab.research.google.com/github/Abhishekupca/Hospital-Readmission-Prediction-using-PCA-and-RF/blob/main/notebooks/03_modeling_logistic_random_forest.ipynb

## Requirements
Install all dependencies with:

pip install -r requirements.txt

## Notes
- The dataset `diabetic_data.csv` is expected in the `data/` folder. If the dataset is large and you prefer not to keep it in the repo, move it to an external storage and add to `.gitignore`.
- Replace placeholder notebooks with the full notebooks or push your existing notebooks to `notebooks/`.