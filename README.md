# Biosignal Analysis for Smoking Prediction
This project focuses on analyzing biosignal and health-related data to predict smoking habits using **machine learning algorithms**. The dataset (`smoking.csv`) contains demographic, physiological, and clinical features of individuals, and the goal is to classify whether a person is a smoker or non-smoker.

---

## Project Structure

```
├── smoking.csv                # Dataset
├── smoking_analysis.ipynb     # Main analysis & model training script
├── README.md                  # Project documentation
```

---

## Dataset

* **Source:** Provided `smoking.csv` file
* **Shape:** `(#rows, #columns)` after preprocessing
* **Dropped Columns:** `ID`, `oral` (irrelevant for prediction)
* **Target Variable:** `smoking` (Binary: 0 = Non-Smoker, 1 = Smoker)

**Features include:**

* Demographic: `gender`, `age`, `height(cm)`, `weight(kg)`
* Clinical: `hemoglobin`, `triglyceride`, `HDL`, `LDL`, `serum creatinine`, `ALT`, `fasting blood sugar`, etc.
* Lifestyle/Indicators: `tartar`, `dental caries`, `waist(cm)`, `systolic`, `relaxation`, `Gtp`

---

## Workflow

1. **Exploratory Data Analysis (EDA):**

   * Visualizations using `matplotlib` & `seaborn` (histograms, barplots, pie charts, boxplots).
   * Class distribution check (`smoking` column).

2. **Data Preprocessing:**

   * Dropped irrelevant columns (`ID`, `oral`).
   * Label Encoding for categorical variables (`gender`, `tartar`, `dental caries`).
   * Standardization (`StandardScaler`) for numerical features.

3. **Feature Importance:**

   * Used `ExtraTreesClassifier` to evaluate top contributing features.

4. **Model Training & Evaluation:**

   * **Logistic Regression**
   * **Decision Tree Classifier**
   * **Bagging Classifier (with Decision Trees)**
   * **Extra Trees Classifier**
   * **Random Forest Classifier**

   Metrics used: **Accuracy, Precision, Recall, F1-Score** (via `classification_report`).

---

## Results

* **Logistic Regression:** Baseline linear model performance.
* **Decision Tree:** Simple non-linear classification.
* **Bagging Classifier:** Improved stability & reduced variance with 1000 estimators.
* **Extra Trees & Random Forest:** Ensemble methods for high accuracy and feature importance extraction.


---

## Tech Stack

* **Languages:** Python
* **Libraries:**

  * `numpy`, `pandas` → Data handling
  * `matplotlib`, `seaborn` → Data visualization
  * `scikit-learn` → Preprocessing, ML models, metrics

---

