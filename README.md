# 📊 Machine Learning-Based Prediction of Maximum Von Mises Stress

A machine learning project focused on predicting the **maximum Von Mises stress** in a cantilever beam using its thickness distribution. The project explores the effectiveness of dimensionality reduction techniques and neural networks for engineering design prediction.

---

## 📖 Overview

Finite Element Analysis (FEA) is widely used to evaluate stress distributions in engineering structures but can be computationally expensive for large-scale design studies. This project investigates whether machine learning models can accurately predict the **maximum Von Mises stress** directly from beam thickness distributions, reducing computational effort.

Two different approaches were developed and compared:

1. **Direct Neural Network (MLP)**
2. **PCA + Neural Network (Dimensionality Reduction + MLP)**

---

## 🎯 Objectives

* Predict maximum Von Mises stress from beam thickness data.
* Compare the performance of direct feature learning and PCA-based dimensionality reduction.
* Improve model generalization through preprocessing and optimization techniques.
* Explore the applicability of machine learning in engineering design and analysis.

---

## 🛠️ Technologies Used

* Python
* NumPy
* Pandas
* Scikit-Learn
* TensorFlow / Keras
* Matplotlib

---

## 📂 Methodology

### Approach 1: Direct Neural Network

```text
226 Thickness Features
          │
          ▼
MLP (512 → 256 → 128 → 64 → 1)
          │
          ▼
Maximum Von Mises Stress
```

### Approach 2: PCA + Neural Network

```text
226 Thickness Features
          │
          ▼
PCA (226 → 208 Features)
          │
          ▼
MLP (256 → 128 → 64 → 1)
          │
          ▼
Maximum Von Mises Stress
```

---

## ⚙️ Data Preprocessing & Optimization

The following techniques were implemented to improve model performance:

* Feature standardization
* Log transformation using log(1+y) to reduce output skewness
* Quantile transformation for improved target distribution
* Early stopping to prevent overfitting
* Learning rate scheduling
* Dropout regularization
* Swish activation function
* Huber loss function
* K-Fold Cross Validation

---

## 📈 Key Findings

* PCA-assisted models performed better when training data was limited.
* Dimensionality reduction reduced model complexity and improved generalization.
* Direct neural networks benefited from larger datasets by utilizing all available information.
* Rare high-stress samples remained the most challenging predictions due to dataset imbalance.

---

## 🚀 Results

The project successfully demonstrated that machine learning models can predict structural stress with reasonable accuracy while significantly reducing computational requirements compared to repeated simulation-based evaluations.

The comparison between PCA-assisted and direct neural network architectures provided valuable insights into the trade-off between model complexity and predictive performance.

---

## 📚 Learning Outcomes

* Neural Network Design and Training
* Dimensionality Reduction using PCA
* Regression Modelling
* Model Optimization and Regularization
* Engineering Applications of Machine Learning
* Data Preprocessing and Feature Engineering

---

## 🔮 Future Work

* Physics-Informed Neural Networks (PINNs)
* Surrogate modelling for CFD and FEA applications
* Larger datasets and advanced architectures
* Uncertainty quantification and model explainability
* Integration of machine learning with computational engineering workflows

---

## 👨‍💻 Author

**Srajan Sijariya**
Mechanical Engineering Undergraduate, IIT Ropar

Interested in:

* Computational Fluid Dynamics (CFD)
* Machine Learning
* Scientific Computing
* Engineering Simulations

