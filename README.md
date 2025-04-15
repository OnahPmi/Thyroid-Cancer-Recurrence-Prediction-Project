# Differentiated Thyroid Cancer (DTC) Recurrence Prediction Project

**This Repository contains the code base of our study titled: `Optimizing Unsupervised Feature Engineering and Predictive Models for Thyroid Cancer Recurrence Prediction.`**

**The code base is divided into two scripts.**
1. **`EDA dimensionality reduction Exploration`**, where we explored the various dimensionality reduction techniques to find the optimal ones for the modelling pipeline. 
2. **`Hyperparameter Tuning and Initial Classification Pipelines Evaluation`**, where we performed hyperparameter optimization of the classification pipelines using the best-performing dimentionality reduction techniques and performed initial evaluations.
3. **`Classification Pipelines' Evaluation Evaluation (AUC, ROC Curve, DET Curve & 95% CI)`**, where we evaluated the classification pipelines using AUC, ROC $ DET Curves and computing the 95% Confidence Intervals (CIs).
4. **`Classification Pipelines' Evaluation Evaluation (Other Metrics, 95% CI)`**, where we evaluated the classification pipelines on other metrics like balanced accuracy, F-1 score, sensitivity, specificity and precision, including their 95% CIs.
5. **`Classification Pipelines' Evaluation Comparison`**, where we perfomed statistical tests such as Wilcoxon Signed-Rank Test to compare the performances of the classification pipelines.
6. **`Classification Pipelines' Subgroups Consistency Evaluation`**, where we performed the stratified subgroup evaluation of the best-performing classification pipeline.
7. **`Plotting Confusion Matrix`**, whhere we plotted the confusion matrices of the classification pipelines.
8. **`Classification Pipelines' Evaluation Explanability with SHAP`**, where we performed the explainability of the best-performing classification pipeline using SHAP analysis.
9. **`Workflow Diagram`**, were we created the flow diagram for the study methodology.

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
