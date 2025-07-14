# Marketing-Campaigns-Project
Marketing Campaigns. Exploratory Data Analysis and hypothesis testing 

```markdown
# Marketing Campaign Data Analysis Review

## Executive Summary

This analysis of marketing campaign data employed rigorous statistical methods and exploratory data analysis techniques to understand customer behavior patterns and validate key marketing hypotheses. The analysis addressed data quality issues, performed feature engineering, and conducted multiple statistical tests.

---

## Data Preprocessing and Quality Assessment

### Initial Data Exploration

A custom `summary()` function provided comprehensive insights into:

- Data types and memory usage  
- Unique values and statistical distributions  
- Data quality issues including missing values and whitespace problems  

This systematic approach ensured data integrity before proceeding with the analysis.

### Data Cleaning and Preparation

Several critical data preprocessing steps were implemented:

- **Missing Value Treatment**:  
  Income data was imputed using the average income of customers with similar education and marital status.

- **Data Validation**:  
  Age was calculated using date of birth, with validation to correct inaccuracies. DateTime formats were standardized.

- **Category Consolidation**:  
  Categorical variables were merged into fewer, meaningful categories to reduce dimensionality.

- **Duplicate and Invalid Data Handling**:  
  The dataset was checked for duplicate rows and negative values, which were corrected or removed.

---

## Feature Engineering and Encoding

Encoding strategies were chosen based on variable types:

- **Label Encoding**: Applied to ordinal categorical variables (e.g., education levels)
- **One-Hot Encoding**: Used for nominal categorical variables
- **Feature Creation**:
  - Total number of children
  - Customer age
  - Total spending
  - Total purchases across channels

---

## Exploratory Data Analysis and Visualization

Visualization techniques used `seaborn` and `matplotlib`:

- **Distribution Analysis**:  
  Histograms, KDE plots, and violin plots revealed skewness and distribution patterns.

- **Relationship Exploration**:  
  Scatter plots and correlation matrices identified inter-variable relationships.

- **Categorical Analysis**:  
  Bar plots and pie charts provided insights into category distributions.

- **Outlier Detection**:  
  Box plots highlighted outliers requiring treatment.

---

## Outlier Treatment

A systematic approach included:

- **Winsorization**: Reduced the influence of extreme values.
- **Upper/Lower Bound Thresholds**: Used statistical limits to identify and adjust outliers.

---

## Statistical Analysis Framework

### Normality and Variance Testing

- **68-95-99 Rule**: Visual checks for normal distribution  
- **Levene's Test**: Tested equality of variances  
- **Shapiro-Wilk Test**: Formal test for normality

---

## Hypothesis Testing Results

### Hypothesis 1: Age and Shopping Channel Preference  
> _"Older individuals may not possess the same level of technological proficiency and may, therefore, lean toward traditional in-store shopping preferences."_

- **Methods**: Paired t-test (one-sided), correlation analysis  
- **Result**: **Confirmed** — Older customers show a significant preference for in-store shopping.

---

### Hypothesis 2: Children and Online Shopping Convenience  
> _"Customers with children likely experience time constraints, making online shopping a more convenient option."_

- **Methods**: Mann-Whitney U test, Wilcoxon signed-rank test (one-tailed)  
- **Result**: **Confirmed** — Customers with children made significantly more online purchases.

---

### Hypothesis 3: Channel Cannibalization  
> _"Sales at physical stores may face the risk of cannibalization by alternative distribution channels."_

- **Methods**: Correlation analysis, ANOVA, Tukey’s HSD test  
- **Result**: **Confirmed** — Strong negative correlation between store and web purchases.

---

### Hypothesis 4: US Market Performance  
> _"Does the United States significantly outperform the rest of the world in total purchase volumes?"_

- **Methods**: One-tailed t-test, comparative analysis  
- **Result**: **Confirmed** — US customers had significantly higher total purchase volumes (**p < 0.01**).

---

## Key Findings and Business Implications

### Customer Segmentation Insights

- **Age-Based Preferences**: Generational differences support tailored marketing.  
- **Family Status Impact**: Customers with children form a distinct segment.  
- **Geographic Performance**: US market demonstrates strong performance.

### Revenue Optimization Opportunities

- **Channel Strategy**: Balance traditional vs. digital channels to reduce cannibalization.  
- **Demographic Targeting**: Age and family status predict customer preferences.  
- **Market Expansion**: International markets can grow using US strategy benchmarks.

---

## Statistical Methodology Validation

Both parametric and non-parametric tests were used with appropriate assumptions:

- **Tests Used**:
  - t-tests
  - Mann-Whitney U
  - ANOVA
  - Tukey’s HSD

These methods ensured robust validation across different data distributions and hypothesis types.
---

