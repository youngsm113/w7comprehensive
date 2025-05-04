# Predicting Disease Progression with Linear Regression  
  
## Overview    
I used the UCI Diabetes dataset (via `sklearn.datasets`) to model the one-year disease progression measure as a function of 10 baseline clinical variables.    
  
## Contents    
- `q5-compprehensive.ipynb`: step-by-step exploration, training, and evaluation.        
  
## Process & Reflection    
1. **Exploration**: No missing values; distributions roughly Gaussian.    
2. **Model**: Simple Ordinary Least Squares (Linear Regression)    
3. **Evaluation**:    
   Mean Squared Error on test set: 2900.194.
   - I added RMSE to help interpret the results. Target values range from 25 to 346, so with an RMSE of approximately 54, the model's predictions are off by about 54 units from the actual value. 
   - Scatter plot showed predictions roughly along the diagonal, indicating a reasonable fit but room for improvement.
4. **Reflection**   
   This model may offer insights for general trend prediction or risk grouping. However, in a clinical or high-stakes setting, this error level may be too large to base decisions on. Enhancing the model to include feature importance may offer insights into which features most influence disease progression. Furthermore, I suggest adding cross-validation to obtain a more reliable performance estimate. 
5. **Next Steps**:    
   - Try regularized models (Ridge/Lasso) to reduce variance. The model captures some signal in the data, but not with high precision.    
   - Engineer new features (e.g. interaction terms) or try non-linear models (Decision Trees, SVR).    
  
## How to run    
1. Clone this repo    
2. Install required packages (e.g., `pip install pandas numpy scikit-learn seaborn matplotlib`)    
3. Launch `q5-comprehensive.ipynb` in Jupyter    
 
