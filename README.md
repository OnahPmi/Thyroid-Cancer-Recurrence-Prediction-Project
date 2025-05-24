# [Differentiated Thyroid Cancer (DTC) Recurrence Prediction Project](https://pmc.ncbi.nlm.nih.gov/articles/PMC12070754/)

**This Repository contains the code base of our study titled: `Optimizing Unsupervised Feature Engineering and Classification Pipelines for Differentiated Thyroid Cancer (DTC) Recurrence Prediction`**, which has been pulished in _BMC Medical Informatics and Decision Making_ (Link ⟶ [Click to view](https://pmc.ncbi.nlm.nih.gov/articles/PMC12070754/)).

# Abstract
**Background:** Differentiated thyroid cancer (DTC) is a common endocrine malignancy with rising incidence and frequent recurrence, despite a generally favorable prognosis. Accurate recurrence prediction is critical for guiding post-treatment strategies. This study aimed to enhance predictive performance by refining feature engineering and evaluating a diverse ensemble of machine learning models using the UCI DTC dataset.

**Methods:** Unsupervised data engineering—specifically dimensionality reduction and clustering—was used to improve feature quality. Principal Component Analysis (PCA) and Truncated Singular Value Decomposition (t-SVD) were selected based on superior clustering metrics: adjusted Rand Index (ARI > 0.55) and V-measure (> 0.45). These were integrated into classification pipelines using Logistic Regression (LR), Support Vector Machine (SVM), Random Forest (RF), K-Nearest Neighbors (KNN), Feedforward Neural Network (FNN), and Gradient Boosting (GB). Model performance was evaluated through bootstrapping on an independent test set, stratified 10-fold cross-validation (CV), and subgroup analyses. Metrics included balanced accuracy, F1 score, AUC, sensitivity, specificity, and precision, each reported with 95% confidence intervals (CIs). SHAP analysis supported model interpretability.

**Results:** The PCA-based LR pipeline achieved the best test set performance: balanced accuracy of 0.95 (95% CI: 0.90–0.99), AUC of 0.99 (95% CI: 0.97–1.00), and sensitivity of 0.94 (95% CI: 0.84–1.00). In stratified CV, it maintained strong results (balanced accuracy: 0.86; AUC: 0.97; sensitivity: 0.80), with consistent performance across clinically relevant subgroups. The t-SVD-based LR pipeline showed comparable performance on both test and CV sets. SVM and FNN pipelines also performed robustly (test AUCs > 0.99; CV AUCs > 0.96). RF and KNN had high specificity but slightly lower sensitivity (test: ~0.87; CV: 0.77–0.80). GB pipelines showed the lowest overall performance (test balanced accuracy: 0.86–0.88; CV: 0.85–0.88).

**Conclusions:** Dimensionality reduction via PCA and t-SVD significantly improved model performance, particularly for LR, SVM, FNN, RF and KNN classifiers. The PCA-based LR pipeline showed the best generalizability, supporting its potential integration into clinical decision-support tools for personalized DTC management.

## The code base is divided into 9 scripts for easy accessibility.
1. **`1. EDA dimensionality reduction Exploration`**, where we explored the various dimensionality reduction techniques to find the optimal ones for the modelling pipeline. 
2. **`2. Hyperparameter Tuning and Initial Classification Pipelines Evaluation`**, where we performed hyperparameter optimization of the classification pipelines using the best-performing dimentionality reduction techniques and performed initial evaluations.
3. **`3a. Classification Pipelines' Evaluation Evaluation (AUC, ROC Curve, DET Curve & 95% CI)`**, where we evaluated the classification pipelines using AUC, ROC $ DET Curves and computing the 95% Confidence Intervals (CIs).
4. **`3b. Classification Pipelines' Evaluation Evaluation (Other Metrics, 95% CI)`**, where we evaluated the classification pipelines on other metrics like balanced accuracy, F-1 score, sensitivity, specificity and precision, including their 95% CIs.
5. **`3c. Classification Pipelines' Evaluation Comparison`**, where we perfomed statistical tests such as Wilcoxon Signed-Rank Test to compare the performances of the classification pipelines.
6. **`3d. Classification Pipelines' Subgroups Consistency Evaluation`**, where we performed the stratified subgroup evaluation of the best-performing classification pipeline.
7. **`4. Plotting Confusion Matrix`**, whhere we plotted the confusion matrices of the classification pipelines.
8. **`5. Classification Pipelines' Evaluation Explanability with SHAP`**, where we performed the explainability of the best-performing classification pipeline using SHAP analysis.
9. **`6. Workflow Diagram`**, were we created the flow diagram for the study methodology.

### In order to successfully run the notebooks 

**Create a new virtual (conda) environment and install the following:**  
`python==3.8.18 or above`  
`numpy==1.24.4`  
`scipy==1.10.1`  
`scikit-learn==1.3.2`  
`pandas==2.0.4`  
`seaborn==0.12.2`  
`matplotlib==3.7.2`  
`umap-learn==0.5.6`  
`prince==0.13.0`    
`shap==0.47.1`  
`graphviz==0.20.3`  

- For each one, try using conda:

```bash
conda install <package_name>
```

- If it's not available on conda, try conda-forge:

```bash
conda install -c conda-forge <package_name>
```

- If this still fails, then ultimately use pip:

```bash
pip install <package_name>
```
