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

**📊 R² (R-squared)** or the coefficient of determination - Compares your model's predictions to the mean of the targets. Values can range from negative infinity (a very poor model) to 1. For example, if all your model does is predict the mean of the targets, its R² value would be 0. And if your model perfectly predicts a range of numbers it's R² value would be 1.

**📏 Mean Absolute Error (MAE)** - The average of the absolute differences between predictions and actual values. It gives you an idea of how wrong your predictions were.

**📐 Mean Squared Error (MSE)** - The average squared differences between predictions and actual values. Squaring the errors removes negative errors. It also amplifies outliers (samples which have larger errors).

---

### 🤔 Which Regression Metric Should You Use?

**💡 R²** is similar to accuracy. It gives you a quick indication of how well your model might be doing. Generally, the closer your R² value is to 1.0, the better the model. But it doesn't really tell exactly how wrong your model is in terms of how far off each prediction is.

**💡 MAE** gives a better indication of how far off each of your model's predictions are on average.

#### 🏠 Practical Example: House Price Prediction

As for MAE or MSE, because of the way MSE is calculated, squaring the differences between predicted values and actual values, it amplifies larger differences.

| Error Type | When to Use |
|------------|-------------|
| **📏 MAE** | When being $10,000 off is **twice as bad** as being $5,000 off (linear penalty) |
| **📐 MSE** | When being $10,000 off is **more than twice as bad** as being $5,000 off (exponential penalty) |

---

## 📚 Additional Resources

For more resources on evaluating a machine learning model, be sure to check out the following:

- 📖 [Scikit-Learn documentation for metrics and scoring](https://scikit-learn.org/stable/modules/model_evaluation.html) - Quantifying the quality of predictions
- ✍️ [Beyond Accuracy: Precision and Recall](https://towardsdatascience.com/beyond-accuracy-precision-and-recall-3da06bea9f6c) by Will Koehrsen
- 💬 [Stack Overflow: MSE and RMSE explained](https://stackoverflow.com/questions/17197492/is-there-a-library-function-for-root-mean-square-error-rmse-in-python)

---

> 💡 **Pro Tip**: Start with simple metrics like accuracy or R², then dive deeper into specialized metrics based on your specific problem and business requirements!