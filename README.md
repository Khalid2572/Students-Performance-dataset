# Student Performance Prediction 🎓📊

This project uses the [Students Performance dataset](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams) to predict whether a student is a high performer or not based on features like gender, parental education, lunch type, and test preparation course.

---

## 📁 Dataset
- Source: Kaggle (StudentsPerformance.csv)
- Total rows: 1000
- Features include:
  - Gender
  - Race/ethnicity
  - Parental level of education
  - Lunch type
  - Test preparation course
  - Math, Reading, and Writing scores

---

## 🎯 Objective
Predict if a student is a **high performer** using their background and test preparation features.

- High Performer: `1` (Average score ≥ 80)
- Not High Performer: `0` (Average score < 80)

---

## 🧹 Data Preprocessing
- Created `average_score` column
- Created binary label `High_Performance` from `average_score`
- Dropped unused columns (`math score`, `reading score`, `writing score`, `average_score`)
- Applied `LabelEncoder` to categorical columns

---

## 📊 Exploratory Data Analysis (EDA)
Used **Seaborn** visualizations to analyze:
- Gender vs High Performance
- Parental education level impact
- Lunch type differences
- Effect of test preparation course

Key Insights:
- Students who completed test prep had higher performance
- Higher parental education generally led to better scores
- Males and females had slightly different performance distributions

---

## ⚙️ Models Used
- **Logistic Regression** with `class_weight='balanced'`
- **Decision Tree Classifier**
- **Random Forest Classifier**

---

## 🧪 Evaluation Metrics
Used:
- Accuracy
- Classification report (Precision, Recall, F1-score)
- Confusion Matrix

---

## 🏁 Results
- **Logistic Regression** (balanced): Decent baseline
- **Random Forest**: Highest accuracy
- All models improved after correcting for class imbalance and using encoding properly

---

## 📌 What I Learned
- How to handle binary classification with imbalanced data
- Feature encoding with LabelEncoder
- Model evaluation and performance comparison
- Visual data storytelling through EDA
- Class balancing using `class_weight='balanced'`

---

## 🧾 How to Run
1. Clone this repository
2. Download the dataset: `StudentsPerformance.csv`
3. Open and run the notebook: `Student_Performance_Prediction.ipynb`

---

## 🚀 Future Improvements
- Try one-hot encoding instead of label encoding
- Add `Family Support`, `Study Time`, or `Free Time` features if available (other datasets)
- Experiment with boosting models like `XGBoost` or `CatBoost`
- Try 3-class classification (low / medium / high)

---

## 🔗 Dataset Source
- [Students Performance Dataset](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)
