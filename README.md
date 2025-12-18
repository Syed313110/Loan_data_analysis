# Loan Approval/Rejection Analysis Project

![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

## Project Overview

This project analyses a loan approval dataset sourced from Kaggle to identify patterns and factors that influence whether a loan application is approved or rejected. The project uses Python-based data analysis techniques to explore applicant demographics, financial characteristics, and credit history, with the aim of generating insights that could support decision-making in the financial services industry.

The analysis focuses on exploratory data analysis (EDA) and visualisation to uncover relationships between variables such as income, loan amount, credit history, and loan status.

---

## Dataset Content

The dataset used in this project is the **Loan Approval Classification Dataset** obtained from Kaggle:

https://www.kaggle.com/datasets/taweilo/loan-approval-classification-data

The dataset contains loan application records with the following types of variables:

- Applicant demographics (e.g. gender, marital status, education)
- Financial information (e.g. applicant income, co-applicant income, loan amount)
- Loan characteristics (e.g. loan term, property area)
- Credit history
- Target variable indicating whether the loan was approved or not

The dataset is of a manageable size and suitable for exploratory analysis and visualisation within the project constraints.

---

## Business Requirements

The primary business requirements for this project are:

1. Identify key factors associated with loan approval decisions.
2. Understand how applicant income and loan amount relate to approval outcomes.
3. Explore whether demographic or categorical variables influence loan approval rates.
4. Present insights in a clear and interpretable way for both technical and non-technical stakeholders.

---

## Hypotheses and Validation

The following hypotheses guide the analysis:

1. Applicants with a positive credit history are more likely to have their loans approved.
2. Applicants with higher income relative to requested loan amounts have a higher likelihood of approval.
3. Young applicants or those with short employment history might be less likely to get approved.
4. Home ownership status may impact loan approval.

These hypotheses are validated through:
- Descriptive statistics
- Grouped comparisons
- Data visualisations (histograms, bar charts, scatter plots, and box plots)

---

## Project Plan

### High-Level Steps
1. Load and inspect the dataset.
2. Clean and preprocess the data (handling missing values and data types).
3. Perform exploratory data analysis (EDA).
4. Visualise key relationships relevant to business questions.
5. Interpret results and summarise insights.

### Data Management
- Data was extracted from a CSV file.
- Cleaning steps included handling missing values and ensuring correct data types.
- Data transformations were applied where necessary to support analysis and visualisation.

### Methodology Rationale
Exploratory data analysis was chosen to allow flexible investigation of patterns and relationships without making strong modelling assumptions. Visual analysis supports clearer communication of insights to business stakeholders.

---

## Mapping Business Requirements to Visualisations

| Business Requirement | Visualisation Used | Rationale |
|---------------------|------------------|-----------|
| Income vs loan approval | Box plots, scatter plots | Compare distributions across approval outcomes |
| Loan amount patterns | Histograms | Understand typical loan sizes |
| Categorical impacts | Bar charts | Compare approval rates across categories |
| Credit history impact | Grouped bar charts | Highlight approval differences clearly |

---

## Analysis Techniques Used

- Descriptive statistics using Pandas
- Grouped aggregations
- Exploratory visualisations using Matplotlib and Seaborn

### Limitations and Alternatives
- The dataset is observational and does not imply causation.
- No predictive modelling was performed; future work could include classification models.
- Some missing values could limit the completeness of certain analyses.

### Use of Generative AI
Generative AI tools were used to:
- Support ideation for business questions
- Improve code readability and structure
- Assist with documentation clarity

All outputs were reviewed and adapted to ensure understanding and originality.

---

## Ethical Considerations

- The dataset contains anonymised data and does not include personally identifiable information.
- Potential bias may exist in historical loan approval decisions.
- Results are interpreted cautiously to avoid reinforcing unfair or discriminatory conclusions.

---

## Dashboard Design

This project focuses on notebook-based visualisation rather than a deployed dashboard.

Planned visual elements can include but not limited to:
- Histograms for numeric distributions
- Bar charts for categorical comparisons
- Scatter plots for relationship analysis
- Box plots for outcome comparison

Insights are communicated using clear visualisations supported by written explanations for both technical and non-technical audiences.

---

## Unfixed Bugs

- Some missing values remain where imputation could introduce bias.
- Certain categorical variables have imbalanced classes, limiting comparison depth.

These issues were documented and considered during interpretation.

---

## Development Roadmap

### Challenges Faced
- Handling missing data without distorting distributions
- Selecting visualisations that best support business questions

### Future Improvements
- Build a predictive loan approval model
- Perform feature importance analysis
- Expand analysis with additional datasets

---

## Deployment

This project was not deployed as a live application, as the focus was on exploratory data analysis rather than application development.

---

## Main Data Analysis Libraries

- **Pandas**: Data loading, cleaning, and analysis
- **NumPy**: Numerical operations
- **Matplotlib**: Core plotting library
- **Seaborn**: Enhanced statistical visualisations

Example:
```python
import pandas as pd
import seaborn as sns

df = pd.read_csv("loan_data.csv")
sns.boxplot(data=df, x="Loan_Status", y="LoanAmount")

