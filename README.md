# WHO Nigeria Hypertension Analysis

## Project Overview

This project analyzes WHO hypertension prevalence estimates for Nigeria to examine changes over time, differences by sex, and uncertainty in reported estimates.

The analysis applies an end-to-end healthcare data analytics workflow, from data preparation and exploratory analysis to statistical testing, visualization, and interpretation of findings.

## Research Questions

This project addresses the following questions:

- How has hypertension prevalence in Nigeria changed over time?
- How do reported estimates differ between females and males?
- How has uncertainty around the estimates changed over time?
- Are there statistically significant trends in the reported estimates?

## Objectives

- Analyze temporal trends in hypertension prevalence estimates.
- Compare reported estimates between females and males.
- Examine uncertainty around the estimates.
- Apply statistical methods to assess trends over time.
- Present findings through clear healthcare data visualizations.

## Dataset

The dataset was obtained from the World Health Organization (WHO) and contains hypertension prevalence estimates for Nigeria.

**Coverage:**
- **Country:** Nigeria
- **Years:** 1990–2018
- **Sex:** Female, Male, Total
- **Observations:** 34
- **Main measure:** Hypertension prevalence rate per 100 population

The analysis also derived an uncertainty-width variable:

`uncertainty_width = RATE_PER_100_NU - RATE_PER_100_NL`

This represents the width between the reported upper and lower uncertainty bounds.

## Methods

The analysis included:

1. Data extraction and loading
2. Data cleaning and quality checks
3. Descriptive statistics
4. Temporal trend analysis
5. Female–male comparison
6. Uncertainty analysis
7. Spearman rank correlation analysis
8. Data visualization
9. Interpretation of findings

## Tools

- Python
- Pandas
- NumPy
- Matplotlib
- SciPy
- Google Colab

## Key Findings

### Overall

The overall mean reported hypertension prevalence estimate was approximately **36.26 per 100 population**.

### Sex differences

The mean reported estimates were:

| Sex | Mean estimate |
|---|---:|
| Female | 37.19 |
| Male | 34.11 |
| Total | 35.74 |

Across overlapping observation years, female estimates were consistently higher than male estimates.

### Change over time

Among the available observations:

- **Female:** 35.9 in 1990 → 38.8 in 2017
- **Male:** 34.1 in 1990 → 33.6 in 2015
- **Total:** 35.1 in 1990 → 36.1 in 2018

The female estimate therefore showed the clearest increase over the observed period.

### Uncertainty

The average uncertainty width for female estimates decreased from approximately **24.23** during 1990–1999 to **12.23** from 2000 onward, representing an approximately **49.5% reduction**.

### Statistical trend analysis

Spearman rank correlation was used to assess monotonic trends over time.

| Sex | Spearman ρ | p-value |
|---|---:|---:|
| Female | 0.997 | <0.001 |
| Male | -0.396 | 0.379 |
| Total | 0.655 | 0.110 |

The female series showed a strong statistically significant positive trend, while the male and total series did not demonstrate statistically significant trends at the conventional 0.05 significance level.

## Limitations

- The dataset contains a relatively small number of observations.
- Observation years differ across sex categories.
- The analysis is descriptive and does not establish causal relationships.
- Reported prevalence estimates may reflect differences in data availability, estimation methods, or uncertainty over time.
- The analysis does not account for additional factors such as age, geographic variation, socioeconomic characteristics, or healthcare access.

## Conclusion

This analysis demonstrates an end-to-end approach to examining population health data using Python.

The findings indicate a clear upward trend in reported female hypertension prevalence estimates over the observed period, while male and total estimates showed less pronounced trends. The reduction in uncertainty width over time also suggests changes in the precision of reported estimates.

The project demonstrates how statistical analysis and data visualization can be used to identify patterns and communicate insights from healthcare data.

## Repository Contents

```text
who-nigeria-hypertension-analysis/
│
├── README.md
│
└── WHO_Nigeria_Hypertension_Analysis_portfolio_cleaned.ipynb
```

## Reproducibility

The complete analysis workflow is available in the Jupyter Notebook included in this repository.

The notebook contains the data preparation, analysis, statistical testing, visualization, and interpretation steps used in this project.

## Author

**Chidera Obi**

Medical Laboratory Scientist | Healthcare Data Analytics | Health Data Science

---

*This project was developed as part of a healthcare data analytics and research portfolio.*
