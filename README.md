#  Problem Analysis Workshop 4  

**Notebook:** `DR_Workshop_04.ipynb`  
**Author:** Sabrina Ronnie George Karippatt
**Date:** 11 November 2025  

---

##  Objective

This workshop builds upon the previous *Dimensionality Reduction Workshop* by shifting the focus from **variance analysis** to **data transformation and readiness**.  
The goal was to make the dataset statistically consistent and model-ready by applying five key transformations required in **Unit 6**.

---

##  Dataset

- **Source:** World Bank API — Consumer Price Index (CPI) dataset  
  *File:* `API_FP.CPI.TOTL.ZG_DS2_en_csv_v2_23195.csv`  
- **Scope:** Annual CPI growth rates for Canada (1960–2024)  
- **Purpose:** To analyze inflation trends and prepare data for dimensionality reduction techniques such as PCA.

---

##  Workflow Summary

The notebook performs the following major steps:

1. **Environment Setup & Verification**  
   - Displays Python, OS, and library versions.  
   - Uses relative paths for reproducibility.

2. **Data Loading & Inspection**  
   - Reads the CPI dataset (`.csv`) and converts it into a tidy long format.  
   - Focuses on Canadian CPI data and validates date ranges and completeness.

3. **Data Transformations**  
   The following transformations were applied sequentially:
   -  *Converting factor variables to numeric*  
   -  *Converting calendar dates to Julian & Ordinal values*  
   -  *Encoding categorical variables to dummies*  
   -  *Performing Box–Cox transformations* for positive numeric features  
   -  *Applying Tukey’s Ladder (p = 0.5)* to handle remaining skewed values  

4. **Validation & Visualization**  
   - Numerical and visual validation of skewness reduction.  
   - Histogram comparison before and after **Box–Cox transformation** confirms normalization.  

5. **Export & Reproducibility**  
   - Saves processed output as  
     `data/processed/API_FP.CPI.TOTL.ZG_DS2_en_csv_v2_23195_transformed.csv`  
   - Generates `requirements.txt` using `pip freeze` for full reproducibility.

---

##  Results

- Skewness in the main variable (`Value`) reduced from **1.37 → 0.01** after Box–Cox transformation.  
- Transformed dataset now exhibits **stable variance and near-normal distribution**.  
- All five required transformations completed successfully with proper markdown documentation.  
- Histogram validation demonstrates visible improvement in distribution symmetry.

---

##  Techniques Covered

- **Principal Component Analysis (PCA)** – linear dimensionality reduction (from previous workshop)  
- **Feature Selection / Factor Analysis** – identifying influential predictors  
- **Box–Cox & Tukey’s Ladder** – variance stabilization and normalization  

These techniques align with **Unit 6 learning outcomes** on preparing, transforming, and validating data for dimensionality reduction.

---

##  Deliverables

| File | Description |
|------|--------------|
| `notebooks/DR_Workshop_04.ipynb` | Main analysis notebook with transformations, plots, and summary |
| `data/API_FP.CPI.TOTL.ZG_DS2_en_csv_v2_23195.csv` | Original CPI dataset |
| `data/processed/API_FP.CPI.TOTL.ZG_DS2_en_csv_v2_23195_transformed.csv` | Processed output dataset |
| `requirements.txt` | Environment dependency list |
| `README.md` | Project summary and reproducibility documentation |

---

##  Conclusion

This workshop successfully bridges the gap between **dimensionality reduction** and **data readiness**.  
The CPI dataset has been fully transformed, validated, and exported for downstream analytical tasks, ensuring that future PCA or feature selection analyses are statistically valid and reproducible.

---

##  References

- World Bank Open Data — [https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG](https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG)  
- Course Material — Unit 6, *Dimensionality Reduction & Data Transformation*, PROG8431  
- Conestoga College Applied AI & Machine Learning Curriculum  
