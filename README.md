# Digit Classification: SVM vs MLP

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Completed-green)

## 📌 Project Overview
This project explores and compares two supervised learning approaches for classifying handwritten digits (0-9) using the **MNIST** subset provided by Scikit-Learn. 
The goal was to analyze the impact of dimensionality reduction (**PCA**) on model performance and to visualize decision boundaries for:
1.  **Support Vector Machines (SVM)** with various kernels.
2.  **Multi-Layer Perceptrons (MLP)** with different architectures.

This analysis was conducted as part of a Machine Learning laboratory course.

## 🛠️ Technical Approach

### 1. Data Preprocessing
* **Normalization:** Used `MinMaxScaler` to scale pixel intensities between 0 and 1.
* **Dimensionality Reduction:** Applied **PCA (Principal Component Analysis)** to reduce the 64-dimensional feature space to 2 components, enabling 2D visualization of decision regions.
* **Stratified Split:** Ensured class balance in train/test sets.

### 2. Models Implemented
* **SVM:** Tested Linear, RBF, and Polynomial kernels. Analyzed the impact of the regularization parameter `C` and gamma.
* **MLP:** Experimented with hidden layer structures (e.g., `(100,)`, `(50,30)`), activation functions (`relu`, `tanh`), and optimizers (`adam`, `sgd`).

### 3. Visualization
Extensive use of `mlxtend` to plot **decision boundaries**, providing visual insight into how each model partitions the feature space.

## 📊 Results Summary

| Model | Configuration | Accuracy (Test) |
|-------|---------------|-----------------|
| **SVM** | RBF Kernel, C=1.0 | **~65%** |
| **MLP** | (100,) units, Adam | ~66% |

*Note: The accuracy is constrained by the aggressive reduction to only 2 principal components for visualization purposes. Using all 64 features yields significantly higher accuracy (>95%).*

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/wekt2k04/digits-classification-svm-mlp.git](https://github.com/wekt2k04/digits-classification-svm-mlp.git)
2. Install requirements
   ```bash
   pip install -r requirements.txt
3. Run the notebook
   ````bash
   jupyter notebook notebooks/Handwritten_Digits_Classification_SVM_vs_MLP.ipynb
