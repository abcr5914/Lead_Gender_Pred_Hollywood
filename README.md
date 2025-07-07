# 🎬 Gender Bias in Hollywood Dialogue: Classification & Analysis

This project explores **gender dominance in Hollywood movie dialogues** using a classification model that predicts the gender of the lead character based on movie metadata and dialogue statistics. It combines **exploratory data analysis**, **statistical visualization**, and **machine learning** to understand gender trends and their correlation with box office performance.

---

## 📁 Dataset Overview

- Source: Provided `train.csv` and `test.csv` files
- Each row represents one Hollywood movie with fields like:
  - Total words spoken
  - Gender-wise word counts
  - Actor ages
  - Gross revenue
  - Year of release
  - Names and genders of lead actors

---

## 🎯 Objectives

1. **Analyze** gender dominance in speaking roles over time  
2. **Visualize** relationships between gendered dialogue and movie profits  
3. **Predict** the gender of the lead character using interpretable features  

---

## 🛠️ Feature Engineering

New features were created to capture structural gender differences in each movie:

- `Words per Actor` — Dialogues normalized by total number of actors  
- `Words Female %` and `Words Male %` — Relative dialogue distribution  
- `Age Gap Male-Female` — Mean age difference across genders  
- `Age Gap Lead-CoLead` — Age difference between lead and co-lead  
- Several original features (e.g., raw ages) were dropped after transformation

---

## 🤖 Models Used

The project tests six supervised learning algorithms:

| Model                | Reason for Use                                   |
|----------------------|--------------------------------------------------|
| Logistic Regression  | Strong baseline for binary classification        |
| LDA / QDA            | Statistical models to test linear/non-linear separation |
| KNN                  | Simple non-parametric method for local structure |
| Random Forest        | Ensemble of decision trees, good for tabular data |
| Gradient Boosting    | More sensitive boosting-based ensemble method     |

**GridSearchCV** was applied for tuning hyperparameters (where applicable).

---

## 🧪 Evaluation Methodology

- Data split: Training, validation, and held-out test set
- Scaled features using `StandardScaler`
- Accuracy was the main evaluation metric, shown for both validation and test sets

---

## 📈 Key Visual Insights

1. **Male Dialogue Dominance**  
   Pie charts and line plots confirm men dominate most speaking roles across decades.

2. **Changing Trends**  
   Since the 1990s, the share of dialogue spoken by women has gradually increased but rarely crossed 50%.

3. **Revenue vs Dialogue Share**  
   Male-dominant films appear to earn more, but female-dominant films show comparable medians. Profit likely depends on additional factors (franchise, genre, star power).

---

## 🚀 How to Run

1. Load the dataset(train.csv) and run preprocessing blocks
2. Execute feature engineering
3. Train and evaluate models using the provided training-validation split
4. Apply final evaluation on test set
5. Review visual plots and accuracy summaries

---

## ✍️ Author Notes

- Designed for educational and exploratory purposes
- Focused on interpretability and step-by-step analysis
- Could be extended with NLP from raw scripts or advanced ensemble models
