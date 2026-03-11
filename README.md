# Breast Cancer Detection

XGBoost trained to classify breast mass cell nuclei as benign or malignant

Dataset: Breast Cancer Wisconsin (Diagnostic) Dataset from Kaggle https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data

   - 569 samples of breast mass cell nuclei features computed from a digitized image of a fine needle aspirate (FNA)
   
   - 30 features comprised of the Mean, Standard Error, and Worst (mean of 3 largest values) of 10 features computed for each cell nucleus

Dataset was loaded, inspected, and cleaned using Synthetic Minority Oversampling Technique (SMOTE) - Edited Nearest Neighbors (ENN) hybrid resampling to tighten the class distribution

Dataset | Benign Count | Malignant Count
--- | --- | ---
Original Dataset | 357 | 212
Resampled Dataset | 314 | 307

Dataset was shuffled and stratified split into training, validation, and testing sets (60:20:20)

An Optuna study was created to optimize XGBoost hyperparameters based on a binary logistic regression learning objective. Pruning and early stopping callbacks were implemented based on validation logistic loss. Visualizations were created for hyperparameter importances and optimization history

Parameter | Optimal Value
--- | ---
Eta | 0.3592
Gamma | 2.7156e-06
Max Depth | 3
Min Child Weight | 1
Subsample | 0.7881
Column Subsample by Tree | 0.2222
N Estimators | 589

The best XGBoost model was retrained with the combined training and validation sets and evaluated based on Accuracy, Macro Precision, Macro Recall, Macro F1-Score, and Normalized Confusion Matrices

Set | Accuracy | Macro Precision | Macro Recall | Macro F1-Score
--- | --- | --- | --- | ---
Train | 1.0 | 1.0 | 1.0 | 1.0
Test | 1.0 | 1.0 | 1.0 | 1.0
