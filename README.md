#  Impact of Occupational Heavy Metal Exposure on Physical Function & Fall Risk — University at Buffalo

### Real-time Public Health Research using NHANES 2011–2016 Data

---

##  Overview

This project investigates how **occupational heavy metal exposure** affects **physical function and fall risk** among U.S. adults using the **NHANES 2011–2016** dataset.  
It applies advanced **survey-weighted regression** and **machine learning models** (Logistic Regression, Random Forest, and XGBoost) to evaluate and predict functional impairment linked to heavy metals such as *lead, cadmium, and manganese*.

The analysis integrates **calibration methods**, **model interpretability**, and **comparative performance evaluation**, forming a reproducible pipeline for public-health analytics.

---

##  Objectives

- Quantify the relationship between heavy metal exposure and functional outcomes.  
- Develop predictive models to classify high-risk individuals.  
- Evaluate model calibration to ensure clinical reliability.  
- Provide insights for **public health policy** and **occupational safety measures**.

---

##  Models Implemented

| Model | Notebook | Description |
|-------|-----------|-------------|
| **Logistic Regression** | `Logistic_only.ipynb` | Baseline model for binary classification of fall risk. |
| **Random Forest (Uncalibrated)** | `Random_forest_only.ipynb` | Tree-based ensemble capturing non-linear relationships. |
| **Random Forest (Calibrated)** | `Randomforest_cal_.ipynb` | Post-calibrated model using isotonic or Platt scaling for improved probability estimates. |
| **XGBoost (Uncalibrated)** | `XGboost_only.ipynb` | Gradient-boosted decision trees optimized for tabular data. |
| **XGBoost (Calibrated)** | `XGBoost_Cal.ipynb` | Probability-calibrated version for more interpretable outputs. |

---

##  Methodology

1. **Data Source** — NHANES 2011–2016 laboratory and questionnaire datasets on heavy metals, physical function, and demographics.  
2. **Data Processing** — Merging, filtering by occupation and age group, handling survey weights.  
3. **Feature Engineering** — Log transformation of metal concentrations, normalization, and binary outcome labeling.  
4. **Modeling** — Implemented in Python (`statsmodels`, `scikit-learn`, `xgboost`).  
5. **Calibration** — Reliability plots and Brier scores to assess predictive probability quality.  
6. **Evaluation Metrics** — Accuracy, ROC-AUC, Precision-Recall, and Calibration Curves.  
7. **Visualization** — Matplotlib/Seaborn visual summaries for interpretability and comparison.

---

##  Results Summary

Key findings from the calibrated models (see `/results/` and `presentation.pptx`):

- **Calibration improved reliability** of probability predictions across all models.  
- **XGBoost with calibration** achieved the best discrimination (highest ROC-AUC).  
- **Random Forest** captured complex exposure–outcome interactions effectively.  
- **Logistic Regression** maintained transparency and interpretability for policy applications.

---

##  Repository Structure

```
 occupational-exposure-nhanes/
 ┣  data/                 # NHANES datasets 
 ┣  notebooks/            # 5 Jupyter notebooks for modeling and calibration
 ┣  results/              # Evaluation metrics, ROC, and calibration plots
 ┣  presentation.pptx     # Slide deck summarizing the findings
 ┗  README.md             # Documentation (this file)
```

---

##  How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/occupational-exposure-nhanes.git
   cd occupational-exposure-nhanes
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run notebooks in Jupyter or Google Colab:
   ```bash
   jupyter notebook notebooks/Random_forest_only.ipynb
   ```

---

## 🧾 Tools & Libraries

- **Python 3.10+**
- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `scikit-learn`, `xgboost`, `statsmodels`
- `scipy`, `imbalanced-learn`
- `jupyter`, `tqdm`

---

## 🎓 Academic Context

This research was conducted as part of the **MPS in Data Science & Applications** program at the **University at Buffalo**, under the supervision of faculty in **Data Analytics and Public Health Research**.  
It demonstrates the integration of data science with epidemiological insights for occupational health monitoring.

---

## 📬 Contact

**Santhakumar Ramesh**  
*MPS in Data Science & Applications, University at Buffalo*  
📧 [santhar1500@gmail.com](mailto:santhar1500@gmail.com)  
🔗 [GitHub](https://github.com/Santhakumarramesh) | [LinkedIn](https://linkedin.com/in/santhakumar-ramesh)

---

⭐ *If you find this project helpful, please star the repo!*
