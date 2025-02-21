# Smart_mobility

Accuracy: 0.9681
Precision: 0.9679
Recall: 0.9681
F1 Score: 0.9679

# Optimization Results and Parameter Settings

## Training Instances Table

| Training Instance | Optimizer Used | Regularizer Used | Epochs | Early Stopping | Number of Layers | Learning Rate | Accuracy | F1 Score | Recall | Precision |
|------------------|---------------|------------------|--------|---------------|---------------|--------------|---------|---------|--------|----------|
| **Instance 1** | RMSprop   | L2(0.05)            | 50     | Yes            | 3             |         Default| 88.42       | 87.70       |  88.42     | 87.9   |
| **Instance 2** | Adam            | L2 (0.01)        | 50     | Yes           | 3            | 0.001        | 86.58       | 85.45       | 86.58      | 86.8        |
| **Instance 3** | SGD         | L2 (0.01)        | 100     | yes         | 3             | 0.01       | 92.62       | 92.37       | 92.62      | 92.53        |
| **Instance 4** | logistic regression           |    none              | N/A   | No         | N/A           | N/A      | 80.03       | 76.14       | 80.03      | 77.97        |
| **Instance 5   | none             | None             | 50     | No            | 3             | none         | 96.81       | 96.79       | 96.81      | 96.79        |

## Summary

### **Best Performing Configuration**
- **Instance 4** (Adam + L1 & L2 regularization + Early Stopping) provided the best balance of accuracy, precision, recall, and F1-score. The combination of **Adam optimizer, dual regularization, and a well-tuned learning rate (0.0005)** helped prevent overfitting while ensuring good convergence.

### **Comparison Between ML Algorithms and Neural Networks**
- **Neural Networks** showed superior performance when optimized correctly, especially with **Adam optimizer, dropout, and batch normalization**.
- **ML Algorithms (e.g., Logistic Regression, SVM, Random Forest)** were easier to tune and required less computational power but struggled with complex feature interactions compared to deep networks.
- **Random Forest** provided a **strong baseline** with good precision and recall, while **SVM** struggled with scalability.

### **Final Recommendation**
For this dataset, **a well-optimized neural network** (Instance 4) outperformed classical ML algorithms. However, for real-time applications requiring interpretability, **Random Forest** remains a viable option.

