# Parameter-Optimization-using-SVM

This repository implements an optimized SVM for a multi-class dataset, demonstrating hyperparameter tuning and performance evaluation across multiple randomized samples. The optimization process leverages the Optuna library, and results include detailed accuracy metrics and convergence graphs.

---

## Project Overview

### Objectives:
1. Select a multi-class dataset from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php).
2. Create 10 randomized train-test splits (70-30 split).
3. Optimize SVM hyperparameters (`Kernel`, `Nu`, `Epsilon`) using Optuna.
4. Evaluate the performance for each split and log the results.
5. Plot the convergence graph for the best-performing sample.

---

## Dataset Description
Name: Wine Quality Dataset <br>
Size: ~6,500 rows and 12 features. <br>
Target: Multi-class classification based on wine quality. <br>

---

### 📈 Results

The optimization process was performed on 10 randomized train-test splits (70-30). The best parameters and accuracies for each sample are summarized in the table below:

| Sample | Best Accuracy | Best Parameters (Kernel, Nu, Epsilon)              |
|--------|---------------|----------------------------------------------------|
| S1     | 0.3999        | `{'kernel': 'linear', 'nu': 0.5184, 'epsilon': 0.3022}` |
| S2     | 0.4125        | `{'kernel': 'linear', 'nu': 0.5781, 'epsilon': 0.2297}` |
| S3     | 0.4141        | `{'kernel': 'linear', 'nu': 0.9501, 'epsilon': 0.4421}` |
| S4     | 0.4012        | `{'kernel': 'linear', 'nu': 0.8991, 'epsilon': 0.8751}` |
| S5     | 0.3951        | `{'kernel': 'linear', 'nu': 0.8726, 'epsilon': 0.2339}` |
| S6     | 0.4151        | `{'kernel': 'linear', 'nu': 0.9422, 'epsilon': 0.1709}` |
| S7     | 0.3749        | `{'kernel': 'linear', 'nu': 0.7482, 'epsilon': 0.3088}` |
| S8     | 0.4314        | `{'kernel': 'linear', 'nu': 0.8347, 'epsilon': 0.2412}` |
| S9     | 0.4081        | `{'kernel': 'linear', 'nu': 0.9266, 'epsilon': 0.2594}` |
| S10    | 0.3811        | `{'kernel': 'linear', 'nu': 0.6632, 'epsilon': 0.1050}` |

---

### Best Model Performance

The best performance was achieved on **Sample 8 (S8)** with:
- **Accuracy**: 0.4314
- **Kernel**: Linear
- **Nu**: 0.8347
- **Epsilon**: 0.2412

---

### Convergence Graph

The convergence graph below shows the progression of the optimization process for **Sample 8 (S8)**. It highlights the reduction in Mean Squared Error (MSE) over the optimization iterations:

![Convergence Graph for S8](results/convergence_graph_s8.png)



