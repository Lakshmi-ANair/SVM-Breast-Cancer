# Breast Cancer Classification using SVM

This project demonstrates how to use **Support Vector Machines (SVM)** to classify breast cancer tumors as **malignant (M)** or **benign (B)** using the Breast Cancer Wisconsin dataset. Both **linear** and **non-linear (RBF kernel)** models are explored, including **hyperparameter tuning** and **decision boundary visualization**.

---

## Objective

- To understand the theory and implementation of **SVM classifiers**.
- Apply **linear** and **RBF kernel SVMs** to a real-world dataset.
- Evaluate and visualize their performance.
- Practice **hyperparameter tuning** and **model validation**.

---

## Dataset: Breast Cancer Wisconsin (Diagnostic)

- 569 samples, 30 numeric features, and a binary target (`M` = 1, `B` = 0).
- Features describe characteristics of the cell nuclei present in the image.
- Available from UCI ML Repository or `sklearn.datasets`.

---

## Technologies Used

- Python 3
- scikit-learn
- pandas, numpy
- matplotlib, seaborn
- Jupyter Notebook
- VS Code

---

## Models Implemented

| Model         | Kernel Type | Accuracy | Notes |
|---------------|-------------|----------|-------|
| SVM (Linear)  | Linear      | ~92-95%  | Fast, interpretable |
| SVM (RBF)     | RBF (non-linear) | ~96-98% | Better with complex data |

---

## 📉 Visualizations

- Decision boundaries after applying **PCA (2D)**.
- RBF kernel handles complex boundaries better than linear.

---

##  Questions Explained

### 1. What is a **support vector**?

Support vectors are **data points closest to the decision boundary (hyperplane)**. These are the **most important points** in SVM — removing them would change the decision boundary. They "support" the optimal margin.

---

### 2. What does the **C parameter** do?

- **C** controls the **trade-off between maximizing the margin and minimizing classification errors**.
- A **low C** encourages a larger margin with some misclassifications (more generalization).
- A **high C** tries to classify all training examples correctly (may overfit).

---

### 3. What are **kernels** in SVM?

Kernels are functions that **transform input data into higher-dimensional spaces** where it may become linearly separable.

- Examples:
  - **Linear kernel**: No transformation.
  - **Polynomial kernel**: Captures polynomial boundaries.
  - **RBF kernel**: Gaussian transformation for complex shapes.

---

### 4. Difference between **Linear** and **RBF** kernel?

| Feature       | Linear Kernel            | RBF Kernel                    |
|---------------|--------------------------|-------------------------------|
| Data type     | Linearly separable       | Non-linear patterns           |
| Speed         | Faster                   | Slower but more powerful      |
| Accuracy      | Lower (on complex data)  | Higher (with tuning)          |
| Use case      | High-dimensional sparse  | Complex relationships         |

---

### 5. Advantages of SVM

- Works well in **high-dimensional** space.
- Effective with clear margin separation.
- Versatile with different **kernel functions**.
- Memory efficient (uses only support vectors).

---

### 6. Can SVMs be used for **regression**?

Yes! It's called **SVR (Support Vector Regression)**. It tries to fit the best line within a **margin of tolerance** rather than predicting exact values.

---

### 7. What happens when data is **not linearly separable**?

SVM applies the **kernel trick** (e.g., RBF) to **map data into a higher-dimensional space** where it becomes linearly separable. This allows SVM to find non-linear decision boundaries.

---

### 8. How is **overfitting handled** in SVM?

Overfitting is handled by:
- Choosing the right **C value** (not too high).
- Selecting proper **kernel and parameters (gamma, degree)**.
- Using **cross-validation** to evaluate performance.
- Feature scaling (standardization) before training.

---

## What You'll Learn

- How SVM finds **maximum margin hyperplanes**.
- Importance of **support vectors**.
- Use of **kernel trick** for non-linear data.
- Performing **hyperparameter tuning** with GridSearchCV.
- Evaluating using **accuracy, classification report, cross-validation**.
- Visualizing decision boundaries using PCA.

---

## How to Run This Project

1. Open `breast_cancer.ipynb` in VS Code.
2. Ensure Jupyter extension is installed and Python kernel is selected.
3. Run cells one by one (`Shift + Enter`).
4. View plots and accuracy results.
5. Optionally tweak `C` and `gamma` values to see changes.

---

## Future Improvements

- Try SVM with other kernels (Polynomial, Sigmoid).
- Try on other datasets (Iris, MNIST).
- Implement Support Vector Regression (SVR).

---

