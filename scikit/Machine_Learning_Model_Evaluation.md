# 🤖 Machine Learning Model Evaluation Metrics

Evaluating the results of a machine learning model is as important as building one.

But just like how different problems have different machine learning models, different machine learning models have different evaluation metrics.

Below are some of the most important evaluation metrics you'll want to look into for classification and regression models.

---

## 🎯 Classification Model Evaluation Metrics/Techniques

### Core Metrics

**✅ Accuracy** - The accuracy of the model in decimal form. Perfect accuracy is equal to 1.0.

**🎯 Precision** - Indicates the proportion of positive identifications (model predicted class 1) which were actually correct. A model which produces no false positives has a precision of 1.0.

**🔍 Recall** - Indicates the proportion of actual positives which were correctly classified. A model which produces no false negatives has a recall of 1.0.

**⚖️ F1 Score** - A combination of precision and recall. A perfect model achieves an F1 score of 1.0.

### Visualization & Analysis Tools

**📊 Confusion Matrix** - Compares the predicted values with the true values in a tabular way, if 100% correct, all values in the matrix will be top left to bottom right (diagonal line).

**🔄 Cross-Validation** - Splits your dataset into multiple parts and train and tests your model on each part then evaluates performance as an average.

**📋 Classification Report** - Sklearn has a built-in function called `classification_report()` which returns some of the main classification metrics such as precision, recall and f1-score.

**📈 ROC Curve** - Also known as receiver operating characteristic is a plot of true positive rate versus false-positive rate.

**🏆 Area Under Curve (AUC) Score** - The area underneath the ROC curve. A perfect model achieves an AUC score of 1.0.

---

### 🤔 Which Classification Metric Should You Use?

| Scenario | Recommended Metric |
|----------|-------------------|
| ⚖️ Balanced classes | **Accuracy** - Good starting point when all classes have similar sample sizes |
| ⚠️ Imbalanced classes | **Precision & Recall** - More important when class distribution is skewed |
| 🚫 False positives are costly | **Precision** - Aim higher when false alarms are problematic |
| ❌ False negatives are costly | **Recall** - Aim higher when missing positives is worse |
| 🎯 Balance both concerns | **F1-Score** - Harmonic mean of precision and recall |
| 👁️ Visual understanding | **Confusion Matrix** - Always helpful to see model performance |

---

## 📉 Regression Model Evaluation Metrics/Techniques

**📊 R² (R-squared)** or the coefficient of determination - Compares your model's predictions to the mean of the targets. Values can range from negative infinity (a very poor model) to 1. For example, if all your model does is predict the mean of the targets, its R² value would be 0. And if your model perfectly predicts a range of numbers it's R² va