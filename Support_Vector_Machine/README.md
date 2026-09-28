# Support Vector Machine (SVM)

> *Learning SVM from first principles—understanding the mathematics before relying on libraries.*

This folder documents my journey of understanding **Support Vector Machines** beyond `sklearn.SVC()`. Instead of stopping at using a library, I explored how SVMs work mathematically, why kernels exist, and how nonlinear decision boundaries are created.

The goal of these notebooks was not only to build working models, but also to understand the reasoning behind concepts like **hinge loss**, **support vectors**, **Lagrange multipliers (`α`)**, **kernel functions**, and **Sequential Minimal Optimization (SMO)**.

## What I Learned

- Why maximizing the margin improves classification.
- How hinge loss trains a Linear SVM.
- Why Support Vectors alone define the decision boundary.
- How the **Kernel Trick** creates nonlinear boundaries without explicitly generating new features.
- The difference between **Polynomial** and **RBF** kernels.
- How **SMO** optimizes two Lagrange multipliers at a time while satisfying SVM constraints.
- How changing the kernel changes the definition of similarity instead of changing the optimization algorithm.

## Learning Progression

| Notebook | Focus |
|----------|-------|
| `SVM_using_Sklearn.ipynb` | Understanding the basics of SVM |
| `Linear_SVM_from_Scratch.ipynb` | Hinge Loss and SGD |
| `Polynomial_SVM_using_Sklearn.ipynb` | Polynomial Kernel |
| `Polynomial_SVM_from_Scratch.ipynb` | SMO and Lagrange Multipliers |
| `RBF_SVM_using_Sklearn.ipynb` | Gaussian Kernel |
| `RBF_SVM_from_Scratch.ipynb` | Custom RBF Kernel with SMO |

## Implementations

### Linear SVM
- Implemented from scratch using NumPy.
- Built hinge-loss optimization with Stochastic Gradient Descent.
- Visualized the decision boundary.

### Polynomial SVM
- Explored the Polynomial Kernel using Scikit-learn.
- Implemented a complete Polynomial Kernel SVM from scratch.
- Learned how SMO updates `α` values instead of directly learning weights.

### RBF SVM
- Compared different `gamma` values using Scikit-learn.
- Implemented the Gaussian Kernel and SMO from scratch.
- Observed how only a subset of training points became Support Vectors.

## Results

| Model | Training | Test |
|-------|---------:|-----:|
| Linear SVM (Scratch) | **86.67%** | — |
| Polynomial SVM (Scratch) | **99.58%** | **96.67%** |
| RBF SVM (Scratch) | **98.33%** | **98.33%** |

The RBF implementation achieved **98.33%** accuracy while requiring only **46 Support Vectors** to define the nonlinear decision boundary.

## Dataset

All notebooks use the **Two Moons** dataset because it clearly demonstrates why kernel methods are needed when a straight line is not enough.

## Tech Stack

- Python
- NumPy
- Matplotlib
- Scikit-learn (dataset generation, preprocessing, train-test split, and evaluation)
