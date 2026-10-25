# 🚢 Titanic Survival Prediction

A complete binary classification project predicting passenger survival on the Titanic dataset, implementing a full data science workflow from Exploratory Data Analysis (EDA) to feature engineering, model training, and evaluation.

---

## 📊 Project Overview
The sinking of the Titanic is one of the most infamous shipwrecks in history. This project builds and evaluates machine learning models to predict whether a passenger survived based on demographic and socioeconomic features (e.g., age, sex, ticket class, and fare).

---

## 🛠️ Tech Stack & Tools
* **Language:** Python 3.10+
* **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn
* **Environment:** Jupyter Notebook / VS Code

---

## ⚙️ Workflow & Methodology
1. **Exploratory Data Analysis (EDA):** Inspected data distributions and identified missing values in `Age`, `Cabin`, and `Embarked`.
2. **Data Cleaning & Imputation:** 
   * Filled missing `Age` values using feature medians.
   * Filled missing `Embarked` values with the mode.
3. **Feature Engineering:**
   * **`Has_Cabin`**: Binary flag indicating whether a passenger had a recorded cabin.
   * **`FamilySize`**: Combined `SibSp` and `Parch` to represent total family members on board.
   * **One-Hot Encoding**: Converted categorical variables (`Sex`, `Embarked`) into numerical format.
4. **Model Training & Validation:** Trained and benchmarked both **Logistic Regression** and **Random Forest Classifier**, achieving a validation accuracy of **82.12%**.

---

## 📈 Results & Evaluation

### Confusion Matrix
The Random Forest model was evaluated on a validation split (20% of the training data):
![Confusion Matrix](./images/confusion_matrix.png)

### Feature Importance Analysis
The model's feature importance weights highlight which attributes heavily influenced survival probability:
![Feature Importance](./images/feature_importance.png)

* **Key Takeaway:** Being female (`Sex_male` having a negative weight inverse) and paying a higher ticket price (`Fare`) or traveling in a higher class (`Pclass`) were strong indicators of survival priority (women and children first).

---

## 🚀 How to Run Locally
1. Clone the repository:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/machine-learning-foundations.git](https://github.com/ahmed-idmachiche/machine-learning-foundations.git)