# Bank Marketing Classification using Machine Learning

## Project Overview

This project aims to predict whether a bank client will subscribe to a term deposit based on marketing campaign data.

It is a binary classification problem where:

* 1 → Client subscribes
* 0 → Client does not subscribe

The project evaluates the impact of dimensionality reduction techniques on model performance.

---

## Dataset Description

* Dataset: Bank Marketing Dataset
* Total Records: 45,211
* Train/Test Split: 80% / 20%
* Test Samples: 9,043

### Class Distribution

* No (0): ~88%
* Yes (1): ~12%

This indicates a highly imbalanced dataset.

---

## Data Preprocessing

* Replaced missing values ("unknown")
* Applied median imputation for numerical features
* Applied mode imputation for categorical features
* Converted target variable (y) to binary
* Applied one-hot encoding for categorical variables
* Feature scaling using StandardScaler

---

## Models Used

### Random Forest

* Ensemble model based on decision trees
* Handles non-linear relationships
* Provides feature importance
* Uses class_weight="balanced" for imbalanced data

### XGBoost

* Gradient boosting algorithm
* High performance and efficiency
* Handles non-linear relationships
* Uses scale_pos_weight to address class imbalance

---

## Dimensionality Reduction

### Principal Component Analysis (PCA)

* Retains 95% of the dataset variance
* Reduces dimensionality while preserving important information

### Feature Selection

* Applied using SelectFromModel with Random Forest
* Removes less important features based on importance scores

---

## Model Performance

### XGBoost Results

| Model         | Accuracy | F1 Score |
| ------------- | -------- | -------- |
| XGBoost       | 0.8876   | 0.8964   |
| XGBoost + PCA | 0.8911   | 0.8945   |

### Random Forest Results

| Model                  | Accuracy | F1 Score |
| ---------------------- | -------- | -------- |
| Random Forest          | 0.8657   | ~0.88    |
| RF + PCA               | 0.8687   | ~0.88    |
| RF + Feature Selection | 0.8607   | ~0.88    |

---

## Evaluation Metrics

* Accuracy
* Recall
* F1-score
* Confusion Matrix

---

## Visualizations

* Accuracy comparison (bar chart)
* F1-score comparison
* Confusion matrix heatmaps
* Hyperparameter tuning heatmap

---

## Hyperparameter Tuning

* Applied using GridSearchCV
* Tuned parameters:

  * n_estimators
  * max_depth

A heatmap was used to visualize model performance across parameter combinations.

---

## Key Insights

* XGBoost outperformed Random Forest
* PCA slightly improved accuracy for both models
* Feature selection did not significantly improve performance
* Class imbalance affects minority class prediction

---

## Conclusion

* Best performing model: XGBoost with PCA
* PCA reduced dimensionality while maintaining performance
* Model selection and preprocessing play a critical role in performance

---

## Technologies Used

* Python
* Pandas, NumPy
* Scikit-learn
* XGBoost
* Matplotlib, Seaborn

---

## Team Members

* Moustafa
* Yousef
* Ahmed Masry
* Mohamed
* Ahmed Salah

---

## Notes

This project was developed as part of the Pattern Recognition course under the supervision of Dr. Yasmine.
