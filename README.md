# Finding-CFR-using-Coronary_Flow_Reserve

Coronary flow reserve (CFR), defined as hyperemic or maximal coronary flow divided by resting flow is a physiologic index which interrogates the function of the entire coronary tree, both the larger epicardial coronary vessel and the microvasculature [1].

This repository contains a complete pipeline for predicting health status (Healthy vs Unhealthy) using various Machine Learning classifiers. It demonstrates: Data preprocessing (scaling + encoding), Training and evaluation of multiple models, Calculation of key classification metrics (Accuracy, Precision, Recall, F1, ROC-AUC) and Visualization of: ROC-AUC curves for all models and Learning curves for training & validation accuracy and Log loss curves for training & validation sets as well as the Confusion matrices for each model. 

📂 Project Structure - cfr_simulation_with_health_labels.csv — Sample dataset (should be in your working directory) and notebook.py or notebook.ipynb — Full Python script or notebook for running the pipeline


⚙️ Key Features - Multiple Models: Logistic Regression, Random Forest, SVM, XGBoost, LightGBM, KNN, Gradient Boosting, Extra Trees, Naive Bayes.

⚙️ Pipelines: Uses Scikit-learn Pipeline and ColumnTransformer for clean, reproducible workflows.

Label Encoding: Handles categorical health labels (Healthy / Unhealthy) robustly.

Detailed Metrics: Precision, Recall, F1, ROC-AUC plus detailed classification_report.

Visual Insights: ROC-AUC curves for comparing model performance and Learning & Loss curves for diagnosing under/overfitting.










References 
1. Fearon, William F. (). A link between resting flow, coronary flow reserve and adverse outcomes. International Journal of Cardiology, Volume 309, 25 - 26. 
