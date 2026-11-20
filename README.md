# Data Science on Brazilian E-Commerce
### Python & R Implementations | Jupyter Notebook, R Markdown, and Quarto

Data Science project using the Brazilian E-Commerce Public Dataset by Olist. This repository provides three implementations of the same analytical workflow across Python and R ecosystems.

The project covers the complete Data Science pipeline, including data acquisition, data understanding, preprocessing, exploratory data analysis, statistical analysis, feature engineering, and machine learning-based delivery delay prediction.

## Project Implementations

This repository provides three different ways to explore and execute the project:

| File | Language | Framework | Description |
|---|---|---|---|
| `Data_Science.ipynb` | Python | Jupyter Notebook | Interactive Python-based analysis |
| `Data_Science.rmd` | R | R Markdown | Reproducible statistical analysis and modeling |
| `Data_Science.qmd` | Python | Quarto | Python-based analytical report |

## Project Overview

E-commerce logistics is a critical component of customer satisfaction and operational efficiency. Delivery delays can negatively affect customer experience, business performance, and customer retention.

This project explores the Olist Brazilian E-Commerce dataset to investigate transaction patterns, delivery performance, customer behavior, and factors associated with late deliveries.

The primary predictive modeling task is to develop a binary classification model to identify orders that are delivered later than their estimated delivery dates.

## Objectives

- Understand the structure and quality of the Olist dataset.
- Perform data cleaning and preprocessing.
- Conduct exploratory data analysis (EDA).
- Investigate statistical relationships and patterns.
- Develop meaningful features from transactional and delivery data.
- Perform customer segmentation using RFM analysis.
- Build a machine learning model for delivery delay classification.
- Evaluate predictive performance using multiple classification metrics.
- Compare analytical implementations across Python and R.

## Dataset

**Brazilian E-Commerce Public Dataset by Olist**

Source: [Kaggle - Olist Brazilian E-Commerce Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

The dataset contains anonymized information about Brazilian e-commerce transactions, including:

- Orders
- Customers
- Order items
- Products
- Sellers
- Payments
- Reviews
- Product category translations

The original dataset is not included in this repository. Users must obtain it from Kaggle before running the project.

## Analytical Workflow

### 1. Data Acquisition
- Retrieve the dataset from Kaggle.
- Load individual CSV files.
- Inspect dataset structures and dimensions.

### 2. Data Understanding and Quality Assessment
- Examine data types and descriptive statistics.
- Identify missing values and duplicate records.
- Investigate relationships between datasets.
- Understand table relationships and analytical granularity.

### 3. Data Preprocessing and Feature Engineering
- Convert date columns into datetime formats.
- Create delivery-related variables.
- Calculate delivery, approval, and shipping durations.
- Construct calendar-based features.
- Aggregate transaction-level information.
- Handle missing values and duplicates.
- Apply Isolation Forest for outlier screening.

### 4. Exploratory Data Analysis
- Analyze numerical distributions and correlations.
- Investigate monthly order trends.
- Examine delivery performance.
- Analyze customer purchasing behavior.
- Perform RFM analysis.
- Compare weekday and weekend delivery durations using the Mann–Whitney U test.

### 5. Predictive Modeling: Delivery Delay Classification

Develop a binary classification model to predict late deliveries.

**Target variable:**
- `is_late = 1`: Actual delivery date is later than the estimated delivery date.
- `is_late = 0`: Actual delivery date is on or before the estimated delivery date.

Modeling methodology:
- Order-level feature aggregation.
- Chronological train-test split.
- Numerical and categorical preprocessing.
- Dummy classifier as a baseline.
- Random Forest classification.
- Classification threshold analysis.
- Feature importance analysis.

Features that would only become available after delivery are excluded to reduce target leakage.

**Evaluation metrics:**
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Average Precision

### 6. Conclusion and Further Work
- Summarize analytical findings.
- Evaluate model performance.
- Discuss methodological limitations.
- Identify opportunities for future improvements.

## Technologies and Tools

### Python
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Scikit-learn
- KaggleHub
- Jupyter Notebook
- Quarto

### R
- R
- Tidyverse
- Lubridate
- Janitor
- Skimr
- Naniar
- GGally
- Broom
- Scales
- Tidymodels
- Ranger
- Isotree
- R Markdown

## Repository Structure

```text
Olist-Dataset-Prediction/
│
├── code/
|   ├── Data_Science.ipynb
|   ├── Data_Science.Rmd
|   └── Data_Science.qmd
│
├── README.md
├── LICENSE
├── .gitignore
│
└── data/
```

## How to Run

### Option 1: Jupyter Notebook

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn kagglehub jupyter
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open `Data_Science.ipynb` and execute the cells sequentially.

### Option 2: R Markdown

Install the required R packages:

```r
install.packages(c(
  "tidyverse", "lubridate", "janitor", "skimr",
  "naniar", "GGally", "broom", "scales",
  "tidymodels", "ranger", "isotree",
  "rmarkdown", "knitr"
))
```

Open `Data_Science.Rmd` in RStudio and use the **Knit** function to render the report.

### Option 3: Quarto

Install the required Python libraries and [Quarto](https://quarto.org/).

Render the document:

```bash
quarto render Data_Science.qmd
```

## Important Notes

- The three files represent alternative implementations of the project.
- The Python and R implementations may produce different numerical results due to differences in libraries, preprocessing behavior, and model configurations.
- The dataset must be obtained separately from Kaggle.
- Predictive features should reflect information available at the intended prediction time.
- Model evaluation should consider class imbalance and the operational consequences of false predictions.

## Acknowledgements
Thanks to Olist for providing the Brazilian E-Commerce Public Dataset for educational and analytical purposes.

---
