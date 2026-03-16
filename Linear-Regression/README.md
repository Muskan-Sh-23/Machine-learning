# Linear Regression
This folder contains my practice implementations and experiments with Linear Regression while learning Machine Learning.

The goal of these notebooks is to understand the Algorithm both mathematically and practically by implementing it from scratch and comparing it with library implementations.

# Experiments in this Folder

   ### 1. Imperfect First Implementation
   

This notebook contains my first attempt at implementing linear regression while learning the fundamentals of the algorithm.

In this experiment, I explored several variations including:

* **Simple Linear Regression**
* **Multiple Linear Regression**
* **Polynomial Regression**

The model did not perform well and produced an R² score close to -2. However, this implementation was intentionally kept in the repository because it represents the early stage of the learning process and highlights the challenges involved in correctly implementing machine learning algorithms.

Through this experiment, I learned several important lessons:

* The importance of correctly preparing and scaling input features
* How model complexity increases when moving from simple to multiple and polynomial regression
* How incorrect parameter estimation or feature handling can significantly affect model performance
* The importance of debugging and validating machine learning implementations

Although the results were imperfect, this notebook played an important role in building an intuitive understanding of regression models and how they behave with different feature representations.

### 2. Linear Regression on Height vs Weight Dataset


In this notebook, linear regression was implemented from scratch using a dataset relating human height and weight.

The purpose of this experiment was to apply the regression algorithm to a simple real-world relationship and observe how the model fits the data. Visualizing the regression line helped understand how the model predicts continuous values.

Key insights:

* Linear regression models relationships between continuous variables.
* Visualization helps interpret the behavior of the model.
* Even simple datasets can illustrate the fundamental idea of regression.

---

### 3. Linear Regression using Gradient Descent


In this experiment, the parameters of the regression model were optimized using gradient descent.

Instead of solving the model analytically, gradient descent iteratively updates the model parameters by minimizing the cost function.

Through this implementation I explored:

* how the cost function behaves during optimization
* how learning rate affects convergence
* how iterative updates gradually improve the model

Key insights:

* Gradient descent is a powerful optimization technique used widely in machine learning.
* Proper choice of learning rate is important for stable convergence.

---

### 4. Linear Regression using Closed Form Solution


This notebook implements linear regression using the closed-form solution, commonly known as the Normal Equation.

Instead of iterative optimization, the parameters are calculated directly using matrix operations.

This experiment helped compare two different approaches to solving linear regression:

* analytical solution (closed form)
* iterative optimization (gradient descent)

Key insights:

* Closed-form solutions are computationally efficient for small datasets.
* However, they may become expensive for very large datasets.

---

### 5. Linear Regression using scikit-learn


In this notebook, linear regression was implemented using the machine learning library scikit-learn.

The goal was to understand how machine learning libraries simplify model training and evaluation. By comparing results with my manual implementations, I could verify the correctness of my understanding of the algorithm.

Key insights:

* Machine learning libraries provide optimized implementations.
* Understanding the algorithm from scratch helps interpret the behavior of library models.

---

### 6. Linear Regression using scikit-learn on Additional Dataset


In this experiment, the regression algorithm was applied to another dataset using my own implementation.

The purpose was to observe how the model behaves when the data distribution changes and to verify that the implementation works consistently across different datasets.

Key insights:

* Model performance depends strongly on the characteristics of the dataset.
* Testing on multiple datasets improves confidence in the implementation.

---

## Overall Learning from These Experiments


Working through multiple implementations of linear regression helped build a deeper understanding of how regression models function both mathematically and computationally.

Instead of relying only on machine learning libraries, implementing the algorithm from scratch made it possible to understand the internal mechanics of the model, including how parameters are updated and how prediction errors are minimized.

Several important insights emerged from these experiments:

**Understanding the algorithm from first principles**


Implementing linear regression manually clarified how the regression line is derived, how model parameters influence predictions, and how the cost function measures model performance.

**Role of optimization techniques**


Through the gradient descent implementation, it became clear how iterative optimization methods gradually reduce error and converge toward optimal parameter values.

**Comparison of analytical and iterative solutions**


The closed form solution demonstrated how linear regression can be solved directly using matrix operations, while gradient descent showed a more scalable approach used in many machine learning algorithms.

**Impact of dataset characteristics**


Running the same algorithm on multiple datasets showed how model performance depends on the structure, distribution, and scale of the data.

**Importance of experimentation and debugging**


Even the imperfect first implementation played an important role in the learning process by highlighting common mistakes and encouraging deeper investigation into the algorithm.

Overall, these experiments helped transform linear regression from a theoretical concept into a practical tool that can be implemented, analyzed, and applied to real datasets.
