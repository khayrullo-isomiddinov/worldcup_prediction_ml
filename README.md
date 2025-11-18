# World Cup Match Outcome Prediction (Machine Learning Project)

This project implements a complete end-to-end **Machine Learning pipeline** for predicting FIFA World Cup match outcomes. Using historical match data, the model predicts whether a match will end in:

- **Home Win**
- **Away Win**
- **Draw**

The project was developed using a Jupyter Notebook (ml.ipynb) and includes full EDA, feature engineering, model training, hyperparameter tuning, evaluation, and model saving.

---

## What This Project Includes

### **1. Data Loading & Cleaning**
- Loaded the historical World Cup dataset
- Cleaned column names and removed irrelevant fields
- Handled missing/invalid values
- Constructed the target label: **HomeWin / AwayWin / Draw**

### **2. Exploratory Data Analysis (EDA)**
- Summary statistics
- Goals distribution
- Match outcome distribution
- Time-based trends:
  - Total goals per year
  - Average goals per match
  - Attendance trends
  - Matches per World Cup

  ### **3. Feature Engineering**
- Goal difference  
- Total goals  
- Knockout indicator  
- One-hot encoding for:
  - Home team
  - Away team
  - Match stage
  - Team initials

  ### **4. Model Training**
- Train/test split with stratification
- Trained a **Random Forest Classifier**
- Hyperparameter tuning using **GridSearchCV**
- Final model chosen based on **F1-macro score**

### **5. Evaluation**
- Classification report  
- Confusion matrix heatmap  
- Feature importance ranking  
- Multi-class ROC curves (One-vs-Rest)  
- Probability predictions for each outcome 

### **6. Model Saving & Loading**
- Saved final model using `joblib`
- Verified correct loading and inference

This creates a fully reusable, production-ready ML pipeline.

## 🚀 How to Run This Project

### **1. Clone Repository**

```bash
git clone <your-repo-url>
cd <your-repo-folder>

python -m venv .venv

.\.venv\Scripts\activate

pip install -r requirements.txt

jupyter notebook ml.ipynb

import joblib
model = joblib.load("worldcup_match_predictor.pkl")

model.predict(new_X)          
model.predict_proba(new_X)   
```

## Author
Khayrullo “Harry” Isomiddinov
Computer Science @ ELTE
Machine Learning & Full-Stack Developer
