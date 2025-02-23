# Smart_mobility

# problem statement

Traffic congestion in Kigali is a growing concern, causing delays, increased fuel consumption, and economic inefficiencies. The lack of predictive models results in poor traffic flow management and inefficient use of road networks. Without data-driven insights, urban planning struggles to address peak-hour congestion effectively.

# DATASET

The dataset contains historical traffic data with vehicle counts (cars, bikes, buses, trucks) recorded at different times, dates, and days of the week. It includes a "Traffic Situation" label, allowing for traffic pattern analysis and machine learning-based congestion prediction.


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

# Discussion of Findings:
The training instances explored different optimization techniques, regularization methods, and hyperparameters to improve traffic situation classification. The results reveal that the SGD optimizer with L2 regularization (Instance 3) yielded the highest accuracy (92.62%), followed closely by Instance 5 (96.81%), which appears to lack details on optimizer and regularization.

Instance 1 (RMSprop + L2 Regularization) achieved 88.42% accuracy, showing that RMSprop effectively adapts the learning rate dynamically but performed slightly lower than SGD.
Instance 2 (Adam + L2 Regularization) scored 86.58% accuracy, confirming Adam’s effectiveness in optimization but slightly underperforming compared to RMSprop.
Instance 3 (SGD + L2 Regularization) obtained the best result among deep learning models (92.62% accuracy), highlighting that SGD with momentum can be effective for this dataset.
Instance 4 (Logistic Regression) resulted in 80.03% accuracy, showing that traditional ML models can still perform reasonably well but may lack deep learning's adaptability.
Instance 5 outperformed all models with 96.81% accuracy, but lacks clarity on its optimization technique, possibly indicating a different architecture or overfitting.
# Best Performing Combination:
Instance 5 yielded the highest accuracy (96.81%)

# Comparison: ML Algorithm vs. Neural Network:
Neural Networks (Instances 1, 2, 3, 5) performed better overall than Logistic Regression (Instance 4).
SGD-based neural network (Instance 3) outperformed Logistic Regression (92.62% vs. 80.03%), showing that deep learning models can better capture complex patterns in the dataset.
Hyperparameters of Logistic Regression: Used the liblinear solver with max_iter=200, showing it was optimized for small datasets but still underperformed compared to neural networks.


video link 
https://youtu.be/C3tdnuEvQ0s 
