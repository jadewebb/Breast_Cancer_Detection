# Breast Cancer Detection

XGBoost trained to classify breast mass cell nuclei as benign or malignant

Dataset: Breast Cancer Wisconsin (Diagnostic) Dataset from Kaggle https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data

     - 569 samples of breast mass cell nuclei features computed from a digitized image of a fine needle aspirate (FNA)
     
     - 30 features comprised of the Mean, Standard Error, and Worst (mean of 3 largest values) of 10 features computed for each cell nucleus

Dataset was loaded, inspected, and cleaned using Synthetic Minority Oversampling Technique (SMOTE) - Edited Nearest Neighbors (ENN) hybrid resampling to tighten the class distribution

   | Benign Count | Malignant Count
  --- | --- | ---
  Original Dataset | 357 | 212
  Resampled Dataset | 314 | 307
