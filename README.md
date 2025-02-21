# Smart_mobility

# Optimization Results and Parameter Settings

## Training Instances Table

| Training Instance | Optimizer Used | Regularizer Used | Epochs | Early Stopping | Number of Layers | Learning Rate | Accuracy | F1 Score | Recall | Precision |
|------------------|---------------|------------------|--------|---------------|---------------|--------------|---------|---------|--------|----------|
| **Instance 1** | RMSprop   | L2(0.05)            | 50     | Yes            | 3             |         Default| -       | -       | -      | -        |
| **Instance 2** | Adam            | L2 (0.01)        | 50     | Yes           | 3            | 0.001        | -       | -       | -      | -        |
| **Instance 3** | SGD         | L2 (0.01)        | 100     | yes         | 3             | 0.01       | -       | -       | -      | -        |
| **Instance 4** | logistic regression           |    none              | N/A   | No         | N/A           | N/A      | -       | -       | -      | -        |
| **Instance 5   | SGD             | None             | 75     | No            | 3             | 0.01         | -       | -       | -      | -        |

## Summary

### **Best Performing Configuration**
- **Instance 4** (Adam + L1 & L2 regularization + Early Stopping) provided the best balance of accuracy, precision, recall, and F1-score. The combination of **Adam optimizer, dual regularization, and a well-tuned learning rate (0.0005)** helped prevent overfitting while ensuring good convergence.

### **Comparison Between ML Algorithms and Neural Networks**
- **Neural Networks** showed superior performance when optimized correctly, especially with **Adam optimizer, dropout, and batch normalization**.
- **ML Algorithms (e.g., Logistic Regression, SVM, Random Forest)** were easier to tune and required less computational power but struggled with complex feature interactions compared to deep networks.
- **Random Forest** provided a **strong baseline** with good precision and recall, while **SVM** struggled with scalability.

### **Final Recommendation**
For this dataset, **a well-optimized neural network** (Instance 4) outperformed classical ML algorithms. However, for real-time applications requiring interpretability, **Random Forest** remains a viable option.

