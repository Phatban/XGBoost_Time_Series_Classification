# 🧠 Time Series Classification with XGBoost

This project demonstrates how to perform **binary classification** on **univariate time series** using **XGBoost** and other classical machine learning models. The task is based on the [FordA dataset](http://www.timeseriesclassification.com/description.php?Dataset=FordA) from the UCR Time Series Archive.

---

## 📂 Dataset

- **FordA**: Contains time series of length 500 representing engine noise.
- **Goal**: Predict whether an engine has a fault (`1`) or is normal (`-1`).
- **Preprocessing**: Class `-1` is mapped to `0` to fit binary classifiers.

---

## ⚙️ Models Compared

The following models were trained and compared using **5-fold Stratified Cross-Validation**:

- `XGBoost`
- `Random Forest`
- `K-Nearest Neighbors (KNN)`
- `Support Vector Machine (SVM)`
- `Logistic Regression`
- `Gradient Boosting`
- `AdaBoost`
- `MLP Classifier`

Each model uses a reasonable set of hyperparameters and is evaluated using **accuracy score**.

---

## 📊 Visualization

The cross-validation accuracy of all models was visualized in a bar chart:

![Cross-Validated Accuracy](5dd24169-69e4-4c41-ae7b-89662b7046a2.png)

> 📌 Highest performance was achieved by **SVM (~80.98%)**, followed closely by **MLP** and **XGBoost**.

---

## 📌 Conclusion

- Models were evaluated using 5-fold Stratified Cross-Validation.
- **SVM** achieved the highest average accuracy (~80.98%), followed by **MLP (~80.48%)**.
- **XGBoost** performed reasonably well with an accuracy of **77.37%**.
- ⚠️ Test set evaluation is not yet included.

---

## 🔍 XGBoost Analysis

**XGBoost (Extreme Gradient Boosting)** showed solid performance with **77.37%** cross-validated accuracy, though slightly behind SVM and MLP.

### ✅ Advantages:
- Handles high-dimensional input efficiently.
- Fast training, supports parallelization.
- Good baseline with minimal preprocessing.

### ⚠️ Drawbacks:
- Ignores time-dependence between time steps.
- May benefit from feature engineering or hyperparameter optimization.

> 🔍 XGBoost offers a great balance between speed, scalability, and accuracy in time series classification, especially for tabular-style time series.

---

## 🧰 How to Run

1. Clone this repository.
2. Open and run the notebook:
   ```bash
   XGBoost_TimeSeries_Classification.ipynb
   ```

---

## 📌 References

- Dataset: [UCR FordA](http://www.timeseriesclassification.com/description.php?Dataset=FordA)
- Guide inspired by AI Vietnam Course Materials

---

## 🧑‍💻 Author

> Project developed by Tan Phat Nguyen as part of the AIO 2024 program by AI Vietnam.
