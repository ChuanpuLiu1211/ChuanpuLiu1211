# KNN Classification with Cross-Validation Project

This project implements a K-Nearest Neighbors (KNN) classifier with hyperparameter tuning through cross-validation.

## Environment Requirements

### Python Version
- Python 3.8+

### Dependencies
```
numpy==1.21.0
pandas==1.3.0
scikit-learn==1.0.2
matplotlib==3.4.2
seaborn==0.11.2
jupyter==1.0.0
```

## Project Overview

The project includes the following main features:

1. Data preprocessing and distribution analysis
2. KNN model hyperparameter tuning
3. Model evaluation using cross-validation
4. Detailed classification performance metrics analysis
5. Visualization of results

## Main Features

### Data Processing

- Loading and preprocessing raw data
- Analysis and visualization of label distribution
- Dataset splitting (training, validation, test sets)

### Model Training and Tuning

- Implementation of an Enhanced KNN classifier
- Grid search for hyperparameters:
  - n_neighbors: K value selection
  - weights: distance weighting
  - metric: distance measurement method
- Parameter optimization using cross-validation

### Best Parameters

The best parameters found through grid search:
```
{
    'n_neighbors': 3,
    'weights': 'distance',
    'metric': 'manhattan'
}
```

Cross-validation accuracy: 0.8873

### Model Evaluation

Main performance metrics on the test set:

- Accuracy: 0.8604
- F1 Score (weighted): 0.8603
- F1 Score (macro): 0.3478
- Recall (weighted): 0.8604
- Recall (macro): 0.3788
- Precision (weighted): 0.8612
- Precision (macro): 0.3406

Detailed performance by class:

| Class | Precision | Recall | F1 Score | Support |
|-------|-----------|--------|-----------|---------|
| 1     | 0.92      | 0.93   | 0.92      | 5539    |
| 2     | 0.13      | 0.32   | 0.18      | 25      |
| 3     | 0.01      | 0.03   | 0.02      | 36      |
| 4     | 0.30      | 0.24   | 0.27      | 518     |

## Visualization Results

The project generates two main visualization outputs:

1. KNN hyperparameter tuning results (enhanced.png)
2. Confusion matrix (matrix.png)

## Project Structure

```
.
├── README_EN.md
├── Group13_KNN_Cross_Val.ipynb    # Main Jupyter notebook file
├── enhanced.png        # Parameter tuning visualization
└── matrix.png           # Confusion matrix visualization
```

## Conclusions

1. The model performs well on the majority class (Class 1) with precision and recall both above 0.92
2. Performance on minority classes (Classes 2, 3, 4) is poor, likely due to class imbalance
3. Overall accuracy reaches 0.86, but low macro-average metrics indicate room for improvement in handling imbalanced data

