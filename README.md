# Visual-Data-Analysis-with-Python
# Visual Data Analysis with Python

**Project Period:** June 2025 – August 2025  
**Project Type:** Exploratory Data Analysis (EDA) and Unsupervised Analysis  
**Language:** Python

An end-to-end visual data analysis project exploring feature distributions, relationships, unusual observations, and dimensionality reduction using a reproducible synthetic dataset.

## Project Overview

This project analyzes a dataset containing **1,200 observations and 12 numeric features**. It applies univariate, bivariate, and multivariate visualization techniques, uses Isolation Forest for anomaly detection, and applies Principal Component Analysis (PCA) to create a two-dimensional representation of the feature space.

The dataset is synthetically generated and includes three latent feature groups and injected anomalies. It is intended as a reproducible portfolio case study, not as real customer, financial, medical, or operational data.

## Objectives

- Explore individual feature distributions and identify unusual values.
- Examine relationships and correlations between numeric variables.
- Detect potential outliers using an unsupervised learning algorithm.
- Reduce the 12-dimensional feature space to two principal components.
- Visualize the data and interpret PCA feature loadings.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- Scikit-learn
- Jupyter Notebook

## Repository Structure

```text
Visual-Data-Analysis-with-Python/
│
├── Visual_Data_Analysis_with_Python.ipynb
├── visual_analysis_dataset.csv
├── dataset_metrics.json
├── requirements.txt
└── README.md
```

## Analysis Workflow

### 1. Data Loading and Preprocessing
- Load the dataset using Pandas.
- Inspect dataset dimensions and data types.
- Generate descriptive statistics.
- Check for missing values and duplicate records.

### 2. Univariate Analysis
- Analyze individual feature distributions.
- Generate histograms and density plots.
- Use box plots to identify potential outliers.
- Examine feature variability and distribution patterns.

### 3. Bivariate and Multivariate Analysis
- Calculate pairwise correlation coefficients.
- Generate correlation heatmaps.
- Use Plotly scatter matrices to explore feature relationships.
- Identify strongly correlated variables and patterns.

### 4. Outlier Detection

Apply the **Isolation Forest algorithm** to identify anomalous observations.

- Standardize the 12 numeric features.
- Configure Isolation Forest with `contamination=0.12`.
- Identify observations predicted as outliers.
- Compare predictions with synthetic anomaly labels for validation.

### 5. Principal Component Analysis (PCA)

Apply PCA to reduce dimensionality and visualize the dataset.

- Standardize numeric features.
- Calculate explained variance ratios.
- Reduce 12 features to 2 principal components.
- Visualize the resulting two-dimensional feature space.
- Analyze PCA loadings to understand feature contributions.

## Results and Findings

| Metric | Result |
|---|---:|
| Total observations | 1,200 |
| Numeric features | 12 |
| Injected anomaly rate | 12.0% |
| Isolation Forest detected outlier rate | 12.0% |
| Maximum absolute correlation | 0.624 |
| PCA variance explained (2 components) | 52.51% |
| Segment silhouette score | 0.183 |

### Key Insights

- Isolation Forest detected 12% of observations as outliers.
- The maximum absolute pairwise correlation was approximately 0.624.
- PCA reduced the original 12-dimensional feature space to two components.
- The first two principal components preserved approximately 52.51% of the total variance.
- The silhouette score of 0.183 indicates weak separation between the supplied segment labels.

**Note:** Matching the injected anomaly rate does not necessarily mean every injected anomaly was correctly detected. The two-component PCA projection also does not preserve 85% of the variance.

## Installation and Setup

### Prerequisites

- Python 3.9 or later
- pip
- Jupyter Notebook

### 1. Clone the Repository

```bash
git clone <repository-url>
cd Visual-Data-Analysis-with-Python
```

### 2. Create a Virtual Environment

**Windows:**

```bash
python -m venv .venv
.venv\Scripts\activate
```

**macOS/Linux:**

```bash
python -m venv .venv
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook Visual_Data_Analysis_with_Python.ipynb
```

Run all notebook cells sequentially to reproduce the analysis.

## Google Colab

You can also execute this project using Google Colab:

1. Upload the Jupyter Notebook.
2. Upload `visual_analysis_dataset.csv`.
3. Install the required dependencies if necessary.
4. Execute all notebook cells sequentially.

## Reproducibility

- The dataset contains 1,200 synthetic observations and 12 numeric features.
- Random-state settings are used to make key analysis steps reproducible.
- The notebook calculates the analysis metrics.
- `dataset_metrics.json` stores a snapshot of the reported metrics.
- The synthetic anomaly label is reserved for validation and is excluded from model input features.

## Limitations

- The dataset is synthetic and may not represent real-world complexity.
- Isolation Forest results depend partly on the configured contamination parameter.
- Two PCA components explain approximately 52.51% of total variance.
- The low silhouette score does not demonstrate strong cluster separation.

## Future Improvements

- Compare Isolation Forest with Local Outlier Factor.
- Experiment with K-Means and DBSCAN clustering.
- Explore additional feature engineering techniques.
- Compare PCA with alternative dimensionality-reduction methods.
- Apply the workflow to real-world datasets.

## Author

**Srishti Mishra**
