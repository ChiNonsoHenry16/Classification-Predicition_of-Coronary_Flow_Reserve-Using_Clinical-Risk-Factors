# Using Clinical Risk Factors for either Classfication or Prediction of Coronary Flow Reserve

Coronary flow reserve (CFR), defined as hyperemic or maximal coronary flow divided by resting flow is a physiologic index which interrogates the function of the entire coronary tree, both the larger epicardial coronary vessel and the microvasculature [1]. The dataset used for this study 

This repository contains a complete pipeline for predicting health status (Healthy vs Unhealthy) using various Machine Learning classifiers. It demonstrates: Data preprocessing (scaling + encoding), Training and evaluation of multiple models, Calculation of key classification metrics (Accuracy, Precision, Recall, F1, ROC-AUC) and Visualization of: ROC-AUC curves for all models and Learning curves for training & validation accuracy and Log loss curves for training & validation sets as well as the Confusion matrices for each model. 

# Rule for Classification
The routine described below has a simple rule described below. 
* CFR > 2.5 → Healthy
* CFR ≤ 2.5 → Unhealthy

According to Ref [2], "Values greater than 2 or 2.5 fall within the normal range of coronary flow reserve. Values above 2 or 2.5 indicate good heart health and recovery post-surgical interventions or cardiac events. In other words, it shows that when the heart is under stress or exertion of any sort, there is double the amount of blood flow compared to the contrary flow to the heart when it is at rest. Values less than 2 detect cardiac abnormalities such as epicardial or coronary artery stenosis, which can lead to myocardial ischemia".

📂 Project Structure 
* cfr_simulation_with_health_labels.csv — Sample dataset (should be in your working directory)
* Prediction of Coronary Flow Reserve using Synthetic Data.py or notebook.ipynb — Full Python script
* Classification of Patients using Coronary Flow Reserve (CFR) values.py or notebook.ipynb — Full Python script

⚙️ Key Features - 
* Multiple Models: Logistic Regression, Random Forest, SVM, XGBoost, LightGBM, KNN, Gradient Boosting, Extra Trees, Naive Bayes.
* Explainability with SHAP: Uses TreeExplainer for trees (RF, GB, LGBM), Uses LinearExplainer for logistic regression and Global feature ranking + per-instance explanations. 
* LIME: Explains individual predictions and is Useful for local interpretability. 

⚙️ Pipelines - 
* Uses Scikit-learn Pipeline and ColumnTransformer for clean, reproducible workflows.
* Label Encoding: Handles categorical health labels (Healthy / Unhealthy) robustly.
* Detailed Metrics: Precision, Recall, F1, ROC-AUC plus detailed classification_report.
* Visual Insights: ROC-AUC curves for comparing model performance and Learning & Loss curves for diagnosing under/overfitting.

NOTE: These results are to be submitted to the International Journal of Cardiology. 

# Issues and Limitation 
* Prdictions did not entirely work because while the evaluation metrices are printed after training and testing, the R square values are negative showing the models are not really learning enough. 
* While classifciation worked and printed beautiful accuracies and everything, the SHAP global feature importance plots showed that the risk factors did not fully contribute to the classification.
* The conclusion is that these clinical risk factors have no predictive power for CFR.

Next Steps
* Regenerate the synthetic datasets to have predictive power. 


References 
1. Fearon, William F. (). A link between resting flow, coronary flow reserve and adverse outcomes. International Journal of Cardiology, Volume 309, 25 - 26. 
