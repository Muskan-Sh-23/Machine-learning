# Logistic Regression – From Scratch & Scikit-Learn

This project demonstrates **Logistic Regression** on the **Breast Cancer Wisconsin (Diagnostic) dataset**.  
It includes **from-scratch implementation** using Python & NumPy, as well as **scikit-learn’s implementation**.  
The goal is to classify tumors as **benign (0)** or **malignant (1)**.

---

## **Dataset**
- 569 samples, 30 features  
- Target: 0 = Benign, 1 = Malignant
- Features include: mean radius, mean texture, mean smoothness, etc.  

---

## **1. From Scratch Implementation**
**File:** `01_Logistic_Regression_From_Scratch_Breast_Cancer.ipynb`  

### **What’s done**
- Implemented **sigmoid function** for probability mapping  
- Performed **binary classification** using a threshold (0.5 default)  
- **Gradient descent** for updating weights  
- Added **L2 regularization** to prevent overfitting  
- Applied **feature scaling** for faster and stable convergence  

### **Highlights**
- Achieved **98.77% accuracy** on the full dataset  
- Visualized **loss curve**  to track training convergence  
- Explored how **thresholds and regularization** affect classification  

### **Workflow**
1. Initialize weights and bias  
2. Compute linear combination of features  
3. Apply sigmoid → predicted probabilities  
4. Convert probabilities to class labels using threshold  
5. Compute **regularized loss**  
6. Compute gradients and update weights  
7. Repeat for 5000 iterations  
8. Plot loss curve for visualization  

---

## **2. Scikit-Learn Implementation**
**File:** `02_Logistic_Regression_Sklearn_Breast_Cancer.ipynb`  

### **What’s done**
- Used `sklearn.linear_model.LogisticRegression` with:  
  - penalty='l2' → L2 regularization  
  - C=10 → inverse of regularization strength  
  - solver='lbfgs' → optimization method  
  - max_iter=5000 → ensure convergence  

- **Train-test split** applied (80%-20%) with random_state=42 for reproducibility  
- Feature scaling applied to ensure proper convergence  

### **Results**
- Accuracy: **97.37%** on test set  
- Confusion matrix and classification report provided  
- Histogram of predicted probabilities shows model confidence:
  - Peaks near 0 → confident benign predictions  
  - Peaks near 1 → confident malignant predictions  

---

## **3. Visualizations**
- **Loss Curve** – shows training convergence (from scratch model)  
- **Probability Histogram** – shows confidence of predictions for each class (sklearn model)  

---

## **4. Key Learnings**
- From scratch implementation reinforces **deep understanding of logistic regression**  
- Gradient descent, L2 regularization, thresholds, and feature scaling are **critical for performance**  
- Comparison with sklearn demonstrates **algorithm vs library abstraction**  
- Visualizations make results **interpretable and easy to communicate**  

---

## **5. Folder Structure**
```text
Logistic_Regression/
├─ 01_Logistic_Regression_From_Scratch_Breast_Cancer.ipynb
├─ 02_Logistic_Regression_Sklearn_Breast_Cancer.ipynb
└─ README.md
```

## **6.Common Pitfalls & Learnings**

1. **Feature Scaling Matters**  
   - Gradient descent may **fail or converge slowly** if features are on different scales.  
   - Always scale **training and test data** consistently.

2. **Train vs Test Fit**  
   - Never fit the scaler on test data.  
   - Use fit on training data, then transform test data to **prevent data leakage**.

3. **Threshold Choice**  
   - Default 0.5 works in most cases, but **changing threshold** affects accuracy, sensitivity, and specificity.  
   - Visualize predictions to see the effect.

4. **Numerical Stability in Sigmoid**  
   - Sigmoid output may reach exactly 0 or 1 → can cause **log(0) errors**.  
   - Use np.clip(y_pred, 1e-10, 1-1e-10) to **avoid NaNs**.

5. **Regularization**  
   - Forgetting L2 term in gradient update or loss can lead to **overfitting**.  
   - Proper λ (C in sklearn) balances **accuracy vs weight magnitude**.

6. **Iterations / Convergence**  
   - Too few iterations → model **may not converge**.  
   - Always check **loss curve**; increase max_iter if needed.

7. **Debugging Tips**  
   - Print first few y_pred and y_class to verify **thresholding logic**.  
   - Plot **loss curves** to check gradient descent behavior.  
   - Compare scratch vs sklearn results for sanity check.


*This project demonstrates Logistic Regression both from scratch and with scikit-learn.  
It helped understand gradient descent, regularization, thresholds, and feature scaling deeply.  
The visualizations and results make the model interpretable.*

