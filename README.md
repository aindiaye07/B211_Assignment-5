# B211_Assignment-5

Purpose of Program:
- The purpose of this project is to build and evaluate three different machine learning classification models to predict whether a breast tumor is malignant or benign based on features extracted from digitized images.
- Goal is to compare model performance to determine the most effective classifier for early detection.

Dataset:
- Source: `sklearn.datasets.load_breast_cancer`
- Samples: 569
- Features: 30 (mean radius, texture, perimeter, area, etc.)
- Target: Binary classification (0: Malignant, 1: Benign)

Implementation:
- Data Preprocessing (Was split into 80% training and 20% testing using a stratified split to maintain class balance ('random_state=42')
- Scaling = 'StandardScaler' was applied to features for SVM and Logistic Regression to ensure proper convergence.
- Model 1 (SVM) = Linear nature of data features.
- Model 2 (Random Forest) = Able to handle feature importance.
- Model 3 (Logistic Regression) = Robust linear model.

Evaluation Metrics:
- Accuracy
- Precision
- Recall
- F-1 Score

Limitations:
- 569 samples are sufficient for a benchmark, but small for deep learning, but suitable for traditional ML
- While Random Forest and Logistic Regression provide insights, complex can be black boxes
- Data is really clean; Real-world data requires handling missing values and outliers

Pros and Cons of Models:

SVM:
- Pros: High precision in detecting malignancies; Good for high-dimensional data
- Con: Less interpretable than trees

Logistic Regression
- Pros: High accuracy, fast to tain, and provides probability scores
- Cons: Can be sensitive to outliers

Random Forest:
- Pros: Handles non-linear data well; Robust againt overfitting.
- Cons: Has lower accuracy compared to SVM


Conclusion:
- The SVM model generally performed best by maximizing the recall for the malignant class, ensuring the highest possible dectection rate.
- In context of cancer detection, maximizing recall is more important than overall accuracy because missing a diagnosis (False Negative) is more dangerous than a false alarm (False Positive).
- Frequently produces highest recall and lowest false negative, meaning it rarely misses maligant cases.
- Was highly effective at finding the margin from benign to malignant tumors.
