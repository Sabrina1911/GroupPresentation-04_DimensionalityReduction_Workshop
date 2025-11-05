# Dimensionality Reduction Workshop

## Project Overview
This project analyzes World Bank Consumer Price Index (CPI) data (2017-2024) for Canada and global regions, focusing on dimensionality reduction techniques for inflation analysis. The project demonstrates systematic preprocessing, feature selection, and dimensionality reduction methods through an object-oriented programming approach.

## Contributors
- Jatinder Pal Singh (9083762) - Missing Values Ratio + Low Variance Filter
- Andrew Silveira (5077086) - High Correlation Filter + PCA
- Rohit Krishnamurthy (8993045) - Random Forest Importance + Forward Selection
- Sabrina Ronnie George Karippatt (8991911) - Backward Selection + Transformations (Box–Cox & Tukey)

## Data Sources
- World Bank CPI Dataset (2017-2024)
- Location: `data/API_FP.CPI.TOTL.ZG_DS2_en_csv_v2_23195.csv`

## Hypothesis
**Null Hypothesis (H₀):** Changes in the Consumer Price Index (CPI) show no statistically significant trend, pattern, or structural shift during 2017-2024.

**Alternative Hypothesis (H₁):** The CPI series exhibits a significant temporal or structural pattern, indicating measurable inflationary pressure or trend behavior.

## Key Features

### 1. Data Preprocessing
- Missing Values Filter (threshold: 0.4)
- Low Variance Filter (threshold: 0.01)
- High Correlation Filter (cutoff: 0.90)

### 2. Feature Selection & Dimensionality Reduction
- Principal Component Analysis (PCA)
- Random Forest Feature Importance
- Sequential Feature Selection (Forward and Backward)

### 3. Data Transformations
- Box-Cox Transformation for strictly positive features
- Tukey's Ladder (signed power transform) for features with zeros/negatives

## Technical Implementation
- Object-Oriented Programming approach
- Python libraries: NumPy, Pandas, Matplotlib, SciPy, scikit-learn
- Custom utility classes for data processing and analysis

## Project Structure
```
GroupPresentation_4/
├── data/
│   └── API_FP.CPI.TOTL.ZG_DS2_en_csv_v2_23195.csv
├── notebooks/
│   └── DimensionalityReduction_Workshop.ipynb
└── README.md
```

## Requirements
The project requires the following Python packages:
- numpy
- pandas
- matplotlib
- scipy
- scikit-learn

## Usage
1. Load and preprocess the CPI dataset using the `DataIngest` class
2. Apply feature filtering using the preprocessing utilities
3. Analyze correlations through visualization
4. Perform dimensionality reduction using PCA
5. Extract feature importance using Random Forest
6. Apply sequential feature selection
7. Transform features using Box-Cox and Tukey methods

## Analysis Workflow
1. Data Ingestion and Cleaning
2. Feature Preprocessing and Filtering
3. Correlation Analysis
4. Principal Component Analysis
5. Feature Importance Ranking
6. Sequential Feature Selection
7. Distribution Transformation and Normalization

## Results
The analysis provides insights into:
- Feature correlations in CPI data
- Principal components explaining variance
- Most important features through Random Forest
- Optimal feature subsets through sequential selection
- Normalized feature distributions after transformations

