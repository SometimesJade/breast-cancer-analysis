# Breast Cancer Data Analysis

A statistical analysis project investigating the characteristics of breast cancer diagnoses. This project explores the relationship between patient attributes (such as Age and Tumor Size) and the diagnosis result (Benign vs. Malignant) using Python.

## Project Overview

The goal of this analysis is to identify significant differences between benign and malignant cases. The project utilizes **Exploratory Data Analysis (EDA)** and **Statistical Hypothesis Testing** (Mann-Whitney U test) to validate findings.

**Key Questions Analyzed:**
* Is there a significant difference in the **age** of patients with benign vs. malignant tumors?
* How does **tumor size** correlate with the diagnosis result?
* What are the statistical effect sizes of these differences?

## Dataset

The data contains records of female patients with the following features:
* **Target:** `Diagnosis Result` (Benign / Malignant)
* **Features:** `Year`, `Age`, `Menopause`, `Tumor Size (cm)`, `Inv-Nodes` (Involvement of lymph nodes), `Breast` (Left/Right), `Metastasis`, `Breast Quadrant`, `History`.

*Original Source: [Kaggle - Breast Cancer Prediction Dataset](https://www.kaggle.com/datasets/fatemehmehrparvar/breast-cancer-prediction)*

## Technologies & Libraries

* **Python 3.x**
* **Pandas & NumPy:** Data manipulation and cleaning.
* **Matplotlib & Seaborn:** Data visualization (Histograms, KDE plots).
* **SciPy (stats):** Statistical testing (Chi2, Mann-Whitney U).

## Data Cleaning Process

The raw data required specific preprocessing steps documented in the notebook:
1.  **Handling Missing Values:** Identified and removed rows containing the placeholder `'#'`.
2.  **Data Typing:** Converted string columns (e.g., `Tumor Size`, `Age`) to integers.
3.  **Error Correction:** Removed invalid entries in the `Inv-Nodes` column (specifically the erroneous value `'3'`).
4.  **Subset Creation:** Split data into `benign_total` and `malignant_total` for comparative analysis.

## Key Findings & Results

The analysis produced the following statistical insights:

### 1. Age Factor
* **Observation:** Malignant tumors occur more frequently in older patients compared to benign tumors.
* **Result:** The difference is statistically significant ($p < 0.0001$).
* **Effect Size:** $r_{rb} = 0.638$ (Large effect).

### 2. Tumor Size
* **Observation:** Malignant tumors are significantly larger on average than benign tumors.
* **Result:** The difference is statistically significant ($p < 0.0001$).
* **Effect Size:** $r_{rb} = 0.832$ (Very large effect).

## How to Run

1.  Clone the repository.
2.  Install dependencies:
    ```bash
    pip install pandas numpy matplotlib seaborn scipy notebook
    ```
3.  Launch the Jupyter Notebook:
    ```bash
    jupyter notebook "Breast Cancer Analysis.ipynb"
    ```

