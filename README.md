# UCI Heart Disease Classification ❤️

Binary classification project predicting the presence/absence of heart disease using the classic **UCI Cleveland dataset** (303 samples, 13 features). The project includes EDA, preprocessing pipelines, baseline models, hyperparameter tuning with Optuna, repeated cross-validation, error correlation analysis, and clinical risk stratification.

## Dataset
- 303 patient records with 13 clinical features + target (0 = no disease, 1 = disease present)
- Nearly balanced binary target (~54% healthy vs ~46% diseased)
- Minor missing values (ca and thal, <2%)
- Source:
    - UCI Machine Learning Repository: [Official download page](https://archive.ics.uci.edu/dataset/45/heart+disease)
  
## Key Results
### Best model: CatBoost (tuned)
- Hold-out test set (61 samples):  
  - Accuracy: **90.16%**  
  - Recall: **92.86%**  
  - F1-score: **89.66%**  
  - ROC AUC: **95.24%**  
- Risk stratification:  
  - High-risk group (>70% probability): **81.25%** disease rate  
  - Top 20% highest-risk patients: **91.67%** disease rate

### Other strong performers (tuned)
- Random Forest: **86.89%** accuracy, **86.67%** F1-score  
- AdaBoost: **86.89%** accuracy, **85.19%** F1-score  
- Logistic Regression L2: **85.25%** accuracy, **84.21%** F1-score  
- SVM: **85.25%** accuracy, **83.02%** F1-score  

**Full analysis available in the notebook**:  
exploratory data analysis, preprocessing pipeline, baseline models comparison, hyperparameter tuning with Optuna, repeated stratified cross-validation results (mean / std), error correlation matrix, final model evaluation, risk stratification with probability-based groups, detailed visualizations, and comprehensive commentary after each major step.

## Notebook Structure
The entire project is implemented in a single, well-organized Jupyter Notebook for clarity and reproducibility:
- Clear sectioning with Markdown headers
- Reusable functions defined at the top of each major section and modular pipelines
- Modular design within the notebook - easy to extract into .py files if needed
- Consistent preprocessing across all models
- Detailed EDA with distributions, correlations and statistical tests
- Baseline models + tuning (Optuna, 1000 trials)
- Repeated stratified CV (5×10 folds) and error correlation matrix
- Final model risk stratification + probability distribution plot

## Technologies
- Python, Scikit-learn
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Optuna

## Notebook
Complete pipeline with EDA, modeling, tuning and risk analysis: [View notebook on GitHub](heart_disease_classification.ipynb)

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook heart_disease_classification.ipynb
```
---
⭐ **Star if you like the project!**  

**Author:** Mateusz Zarebski  
[GitHub Profile](https://github.com/mateusz-zarebski) | [Portfolio Overview](https://github.com/mateusz-zarebski/portfolio)



