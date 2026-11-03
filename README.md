# Smoking Prevalence in England: A Comparative Analysis of HSE 1999 and HSE 2019

## Project Overview

This project investigates whether smoking prevalence in England decreased between 1999 and 2019. It uses data from two independent cross-sectional surveys: the **Health Survey for England (HSE) 1999** and **Health Survey for England (HSE) 2019**.

The analysis uses Python to explore the data, compare smoking prevalence across the two survey years, and conduct statistical hypothesis tests.

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

The project is organised into four stages:

1. **Data Mining:** Data loading, exploration, cleaning, and harmonisation of variables across survey years.
2. **Descriptive Statistical Analysis:** Examination of smoking patterns and prevalence in 1999 and 2019.
3. **Hypothesis Testing:** Application of statistical tests to assess differences in smoking prevalence and the association between smoking status and survey year.
4. **Visualisation:** Presentation of findings through charts and figures.

## Key Findings

| Measure                   |                          Result |
| ------------------------- | ------------------------------: |
| Smoking prevalence (1999) |                          22.47% |
| Smoking prevalence (2019) |                          15.39% |
| Absolute change           | 7.08 percentage points decrease |
| Relative change           |                 31.52% decrease |

### Statistical Tests

**1. Two-proportion Z-test**

- Z-statistic: 11.06446
- P-value: 9.32894 × 10⁻²⁹

**2. Chi-square Test of Independence**

- Chi-square statistic: 121.95496
- Degrees of freedom: 1
- P-value: 2.36139 × 10⁻²⁸

Both tests indicate a statistically significant difference in smoking patterns between the two survey years (p < 0.001).

## Conclusion

The analysis provides strong statistical evidence that smoking prevalence in England decreased between 1999 and 2019. Prevalence fell from 22.47% to 15.39%, representing a relative reduction of approximately 31.52%.

The findings demonstrate a significant change in smoking patterns over the 20-year period.

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

- The datasets are independent cross-sectional surveys, not longitudinal observations of the same individuals.
- Differences in survey design, variable definitions, and population characteristics may affect comparability.
- Survey weights and complex sampling design should be considered when interpreting population-level estimates and statistical tests.

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
- **Institution:** ****\_\_****
- **Date:** 03/11/2026
- **Repository:** Case-study-mc
