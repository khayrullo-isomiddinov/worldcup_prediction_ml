# World Cup Match Outcome Prediction (Machine Learning Project)

Welcome to my not-so-scientific-but-kinda-scientific attempt to predict FIFA World Cup match outcomes using Machine Learning.  I took a bunch of historical matches and shook them up in a Random Forest. Now the model predicts:

- **Home Win**  
- **Away Win**  
- **Draw**

Basically, if football was predictable (it’s not), this model would be a genius.  

Also, **I believe Spain will be champions next time**. Don’t argue. I said what I said. 🇪🇸.

---

## What’s Inside This Project

### **1. Data Loading & Cleaning**
- Loaded World Cup match data  
- Removed random messy columns (referee names… why were they even there?)  
- Cleaned everything until pandas stopped complaining  
- Made the main label: **HomeWin / AwayWin / Draw**

---

### **2. Exploratory Data Analysis (EDA)**  
Mostly me looking at plots and pretending I understand football statistics.

- Goals distribution  
- Match outcomes  
- Trends by year:
  - Total goals
  - Average goals
  - Attendance
  - Match count  

**Preview Plot:**  
![Goals Over The Years](https://static.independent.co.uk/2022/12/18/15/SEI137980520-1.jpg)


---

### **3. Feature Engineering**
- Goal difference (shocking: scoring more goals helps win matches)  
- Total goals  
- “Is Knockout” flag  
- One-hot encoding for:
  - Home team  
  - Away team  
  - Stage  
  - Team initials  

My notebook now has like 300+ columns. Probably not healthy.

---

### **4. Model Training**
- Train/test split  
- Trained a **Random Forest Classifier**  
- Did **GridSearchCV**, because why not torture my CPU  
- Picked best model based on F1 score

---

### **5. Evaluation**
- Classification report  
- Confusion matrix  
- Feature importance  
- Multi-class ROC curves  
- Probability predictions (so the model can say “I think Spain wins, but like 63% sure”)  

**Some cool visual:**  
![Confusion Matrix](https://images.mlssoccer.com/image/private/t_editorial_landscape_12_desktop/mls-lag-prd/jua6trkfwsccfydfm02f.jpg)

---

### **6. Saving & Loading the Model**
- Saved using `joblib`  
- Loaded it back  
- It actually worked (rare W)

---

## How To Run This Project (quick version)

```bash
git clone <your-repo-url>
cd <your-repo-folder>

python -m venv .venv
.\.venv\Scripts\activate  # Windows

pip install -r requirements.txt
```


jupyter notebook ml.ipynb
