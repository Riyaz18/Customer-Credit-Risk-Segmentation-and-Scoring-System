# Customer Credit Risk Segmentation and Scoring System

A data science solution utilizing unsupervised machine learning to segment customers based on financial attributes, thereby developing a synthetic credit scoring system for risk assessment and differentiated financial product offerings.

---

## Project Title & Short Description

**Title:** Customer Credit Risk Segmentation and Scoring System

**Description:** This project implements **K-Means Clustering** to partition a synthetic dataset of customer financial attributes into distinct segments. The segmentation directly informs the development of a proxy **Credit Score** metric, crucial for effective risk management and targeted lending strategies.

---

## Problem Statement / Goal

The primary objective is to categorize the customer base into distinct groups of varying **credit risk levels** (segments). By employing **Unsupervised Learning**, the system automatically identifies patterns in attributes like `Credit Utilization Ratio`, `Payment History`, and `Loan Amount` to assign a quantifiable **Credit Score**, allowing for informed decisions on loan approval and interest rate setting.

---

## Tech Stack / Tools Used

The project is implemented in Python and utilizes key libraries for statistical modeling, data generation, and visualization:

| Category | Tool / Library | Purpose |
| :--- | :--- | :--- |
| **Data Handling** | Pandas NumPy | Data loading cleaning and numerical transformations |
| **Modeling** | Scikit-learn | Core library for clustering algorithms (K-Means) and preprocessing |
| **Statistics** | SciPy | Used for generating realistic truncated normal distributions for synthetic data |
| **Visualization**| Plotly | Interactive visualization of the final customer segments and scores |

---

## Approach / Methodology

1.  **Synthetic Data Generation**: Generated a large, synthetic dataset (`credit_scoring.csv`) using `numpy` and `scipy.stats.truncnorm` to simulate realistic distributions of financial and demographic features.
2.  **Feature Preparation**: Key numerical financial features were selected and preprocessed using a **StandardScaler** to ensure uniform contribution to the clustering process.
3.  **Customer Segmentation**: **K-Means Clustering** was applied to the scaled data to identify natural groupings, ultimately settling on **four optimal clusters**.
4.  **Credit Score Derivation**: A synthetic 'Credit Score' was calculated based on the customers' cluster membership and distance from the cluster center.
5.  **Segment Labeling**: The four clusters were semantically mapped to definitive risk categories: **'Very Low', 'Low', 'Good', and 'Excellent'**.
6.  **Visualization**: The final segmentation and derived credit scores were visualized using an interactive scatter plot via **Plotly Express**.

---

## Results / Key Findings

* The K-Means model successfully identified **four distinct and actionable customer segments** based on their underlying financial profiles.
* The derived 'Credit Score' metric provides a clear, quantitative basis for ranking customer creditworthiness.
* The final segmentation provides immediate strategic value by allowing the business to tailor products and interest rates to customers falling into the **'Good'** and **'Excellent'** segments while managing risk in the **'Low'** and **'Very Low'** segments.

---

## Topic Tags

CreditScoring CustomerSegmentation KMeansClustering UnsupervisedLearning RiskModeling DataScience Python Scikit-learn Plotly SciPy

---

## How to Run the Project

### 1. Install Requirements

Install all necessary packages using the provided `requirements.txt` file:

```bash
pip install -r requirements.txt
