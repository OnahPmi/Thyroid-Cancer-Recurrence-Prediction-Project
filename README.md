# Well-Differentiated Thyroid Cancer Recurrence Prediction Project

**This Repository contains the code base of our study titled: `Optimizing Unsupervised Feature Engineering and Predictive Models for Thyroid Cancer Recurrence Prediction.`**

**The code base is divided into two scripts.**
1. **`EDA dimensionality reduction Exploration`**, where we explored the various dimensionality reduction techniques to find the optimal ones for the modelling pipeline. 
2. **`Predictive model building`**, where we built the models using the optimal dimensionality reduction techniques identified in (1).

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
