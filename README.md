# DA5401 Assignment 4 — GMM-Based Synthetic Sampling for Imbalanced Data

**Name:** Abesech Inbasekar  
**Roll Number:** ME21B003  

---

## Repository Structure
├── Assignment_4.ipynb # Main Jupyter notebook with code, visualizations, and analysis  
├── README.md # This file – explains project structure and submission details  


- **Assignment_4.ipynb**: Contains the full workflow — data loading, baseline model, GMM sampling, CBU undersampling, model evaluation, and final conclusions.  
- **data/**: If working locally, place the `creditcard.csv` dataset here (from [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud)).  

---

## How to Run

1. Clone the repo and open the notebook in Jupyter/Colab.  
2. Make sure the dataset (`creditcard.csv`) is available in the `data/` folder, or update the path in the notebook.  
3. Run all cells in order.  

The notebook is fully self-contained and produces:  
- Model evaluation metrics (Precision, Recall, F1, Weighted Recall).  
- AIC/BIC plots for selecting the optimal GMM components.  
- Visualizations of class balance before and after resampling.  
- Comparative analysis tables and charts.  

---

## Assignment Components

- **Part A:** Baseline model and data analysis (borrowed from Assignment 3).  
- **Part B:** GMM-based synthetic sampling and clustering-based undersampling (CBU).  
  - Theoretical explanation of GMM vs SMOTE.  
  - Optimal component selection using AIC/BIC.  
  - Synthetic fraud sample generation.  
  - Rebalancing datasets (1:10 ratio, majority capped at 25k).  
- **Part C:** Model training, evaluation, and conclusion.  
  - Logistic Regression on baseline, GMM-only, and CBU+GMM data.  
  - Comparison of Precision, Recall, F1, and **Weighted Recall**.  
  - Final recommendation on oversampling strategy.  

---

## Key Insights

- Baseline model achieves high weighted recall (~0.999) but almost **zero fraud recall** → useless for fraud detection.  
- GMM oversampling raises fraud recall to **~0.90**, with weighted recall still above 0.97.  
- CBU+GMM achieves similar fraud recall but with lower precision and weighted recall.  
- **Final recommendation:** GMM-only oversampling at a **1:10 ratio** offers the best trade-off between catching frauds and minimizing false alarms.  

---

## References

- Dataset: [Credit Card Fraud Detection (Kaggle)](https://www.kaggle.com/mlg-ulb/creditcardfraud)  
- AIC & BIC criteria for model selection: Akaike (1974), Schwarz (1978)  
- Lectures and DA5401 assignment guidelines


