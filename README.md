# Smoking Prevalence in England: HSE 1999 vs HSE 2019

## Project Overview

This project investigates whether smoking prevalence in England decreased between 1999 and 2019. It uses data from two independent cross-sectional surveys: the **Health Survey for England (HSE) 1999** and **Health Survey for England (HSE) 2019**.

The analysis examines overall smoking prevalence, gender differences and the statistical significance of changes in smoking patterns over the 20-year period.

## Research Question

**Has smoking prevalence in England decreased between 1999 and 2019?**

## Datasets

| Dataset  | Description                                      |
| -------- | ------------------------------------------------ |
| HSE 1999 | Health Survey for England data collected in 1999 |
| HSE 2019 | Health Survey for England data collected in 2019 |

- Data source: Health Survey of England
- Data access link: https://digital.nhs.uk/data-and-information/publications/statistical/health-survey-for-england
- Sample size (1999): (10259, 1699)
- Sample size (2019): (10299, 1841)
- Combined analytical sample: 14,907 observations

## Project Structure

```text
project/
│
├── figures/
│
│
├── .gitignore
│
├── 01_data_mining.ipynb
├── 02_descriptive_statistical_analysis.ipynb
├── 03_hypothesis_testing.ipynb
└── 04_figures.ipynb
├── README.md
├── requirements.txt
```

## Methodology

The project follows four main stages:

1. **Data Mining:** Loading, exploring, cleaning and harmonising variables across the two survey years.
2. **Descriptive Statistical Analysis:** Examining smoking prevalence overall and by gender.
3. **Hypothesis Testing:** Applying two-proportion Z-tests, chi-square tests of independence and binary logistic regression.
4. **Visualisation:** Presenting the findings using charts and figures.

The binary outcome for regression was defined as:

- 1 = Current smoker
- 0 = Non-current smoker (former and never smokers)

## Key Findings

### 1. Overall Smoking Prevalence

| Measure            |                 Result |
| ------------------ | ---------------------: |
| Prevalence in 1999 |                 22.47% |
| Prevalence in 2019 |                 15.39% |
| Absolute decrease  | 7.08 percentage points |
| Relative decrease  |                 31.52% |

Overall smoking prevalence declined by approximately 31.52% between 1999 and 2019.

### 2. Smoking Prevalence by Gender

| Gender |   1999 |   2019 | Absolute change |
| ------ | -----: | -----: | --------------: |
| Male   | 31.72% | 16.79% |       -14.92 pp |
| Female | 14.56% | 14.26% |        -0.30 pp |

The results indicate that:

- Male smoking prevalence decreased substantially, by approximately 47.05% relative to its 1999 level.
- Female smoking prevalence remained relatively stable, declining by approximately 2.06%.
- The gender gap in smoking prevalence narrowed from 17.16 percentage points in 1999 to 2.54 percentage points in 2019.

The overall decline in smoking prevalence was therefore much more pronounced among males than females.

### 3. Hypothesis Testing

**1. Two-proportion Z-test**

- Z-statistic: 11.06446
- P-value: 9.32894 × 10⁻²⁹

**2. Chi-square Test of Independence**

- Chi-square statistic: 121.95496
- Degrees of freedom: 1
- P-value: 2.36139 × 10⁻²⁸

Both tests indicate a statistically significant difference in smoking patterns between the two survey years (p < 0.001).

### 4. Binary Logistic Regression

A logistic regression model was fitted using smoking status as the dependent variable and survey year, gender and their interaction as explanatory variables.

- Observations: 14,907
- Pseudo R-squared: 0.02914
- Likelihood ratio test p-value: 3.885 × 10⁻⁹⁰

| Predictor          | Coefficient | P-value |
| ------------------ | ----------: | ------: |
| Intercept          |     -0.7667 | < 0.001 |
| Survey year (2019) |     -0.8335 | < 0.001 |
| Gender (Female)    |     -1.0031 | < 0.001 |
| Year × Gender      |      0.8092 | < 0.001 |

The statistically significant year-by-gender interaction indicates that the change in smoking odds between 1999 and 2019 differed significantly between males and females.

The estimated odds of current smoking decreased by approximately 56.6% among males and 2.4% among females.

## Conclusion

The findings provide strong statistical evidence that smoking prevalence in England decreased between 1999 and 2019. Overall prevalence declined from 22.47% to 15.39%, representing a relative reduction of approximately 31.52%.

Gender comparisons revealed that the decline was substantially greater among males than females. Logistic regression further identified a statistically significant interaction between survey year and gender, suggesting that the change in smoking patterns differed significantly by gender.

Overall, the results demonstrate a considerable reduction in smoking prevalence, particularly among males, over the 20-year period.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Pyreadstat
- Matplotlib
- Seaborn
- SciPy
- statsmodel
- Jupyter Notebook

## Limitations

- The surveys are independent cross-sectional samples, not longitudinal observations of the same individuals.
- Differences in survey design, variable definitions and population characteristics may affect comparability.
- The reported logistic regression uses conventional non-robust standard errors and does not account for the complex HSE survey design.
- Survey weights, strata, clustering and age-standardisation should be considered in further analysis.
- The gender interaction describes differences in odds, which are not identical to differences in prevalence.

## How to Run the Project

1. Clone or download this repository.
2. Install the required Python libraries (use the requirement.txt file).
3. Open the notebooks using Jupyter Notebook or JupyterLab.
4. Run the notebooks in numerical order, from `01_data_mining.ipynb` to `04_figures.ipynb`.

Installation command:

```bash
pip install -r requirements.txt
```

## Project Information

- **Author:** Fedelis Verolian
- **Date:** 03/11/2026
- **Repository:** Case-study-mc
