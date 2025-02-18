# Advance Machine Learning 

## Overview
This project applies various machine learning algorithms to the Pima Diabetes dataset and the Wine Quality dataset. The objective is to evaluate and compare the performance of Boosting methods and Neural Networks in both classification and regression tasks.

## Datasets
- **Pima Diabetes Dataset**: Used for classification tasks to predict diabetes.
- **Wine Quality Dataset**: Used for both regression and classification tasks to predict wine quality.

## Implemented Algorithms
- Gradient Boosting Classifier & Regressor
- AdaBoost Classifier & Regressor
- MLP (Multi-Layer Perceptron) Classifier & Regressor

## Performance Evaluation Metrics
- **Classification**: Accuracy, AUC (Area Under the Curve)
- **Regression**: RMSE (Root Mean Squared Error), Explained Variance
- **Computational Efficiency**: Cross-validation (CV) runtime

## Key Findings
### Pima Diabetes Dataset (Classification)
- Gradient Boosting and AdaBoost performed similarly (~0.76 accuracy, ~0.82-0.83 AUC).
- MLP Classifier had lower accuracy (0.70) and AUC (0.73) with higher computational cost.
- Feature selection improved performance slightly while reducing runtime.

### Wine Quality Dataset (Regression & Classification)
- Gradient Boosting Regressor had the best RMSE (0.64) and explained variance (0.34), outperforming AdaBoost and MLP.
- MLP Regressor had the longest runtime (~9 seconds) compared to boosting methods (~2 seconds).
- Classification models performed better with binning.
- Normalizing the target variable had no significant effect on classification performance.

## Feature Selection Insights
- **Pima Diabetes Dataset**: Blood glucose, BMI, and age were the most important features.
- **Wine Quality Dataset**: Volatile acidity, sulphates, and alcohol were key predictors. Total sulfur dioxide was also important for classification.

## Comparison with Previous Methods
- Boosting methods outperformed decision trees.
- Random forests had similar accuracy but slightly lower AUC.
- Neural networks required more computation but didn’t always outperform tree-based methods.

## Practical Implications
- For diabetes screening, **blood glucose and BMI** are key indicators.
- In wine quality prediction, **volatile acidity and sulphates** are significant features.
- Feature selection improves efficiency while maintaining performance.

## Running the Code
1. Ensure Python and dependencies are installed:
   ```bash
   pip install -r requirements.txt
   ```
2. Run the training script:
   ```bash
   python train_models.py
   ```
3. Evaluate the models based on the output metrics.

## Conclusion
Boosting techniques provide a good balance between performance and computational efficiency. MLP models need further tuning to match the efficiency of tree-based methods. Feature selection enhances model efficiency without significant performance loss.

---
**Author**: Umme Athiya  
**Course**: Advanced Machine Learning  
**Institution**: DePaul University
