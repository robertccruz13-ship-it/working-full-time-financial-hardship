# Working Full-Time but Still Struggling to Afford Basic Necessities

## Project Overview

This Social Data Science capstone examines the relationship between personal earnings, housing costs, and housing-cost burden among young adults in the United States.

The study focuses on individuals ages 18–29 who usually work at least 30 hours per week. Using the 2024 American Community Survey Public Use Microdata Sample (ACS PUMS), the project investigates how income, age, weekly work hours, and housing tenure are associated with housing-cost burden.

## Research Question

Among U.S. young adults ages 18–29 who work at least 30 hours per week, how are personal earnings and housing tenure associated with housing-cost burden?

## Research Objectives

- Examine housing-cost burden among young adult renters and homeowners.
- Investigate how personal earnings relate to housing affordability.
- Compare housing-cost burden across housing tenure groups.
- Examine the relationships between age, weekly work hours, income, and housing-cost burden.
- Evaluate these relationships using survey-weighted statistical methods.

## Data Source

**2024 American Community Survey Public Use Microdata Sample (ACS PUMS)**

Source: U.S. Census Bureau

https://www.census.gov/programs-surveys/acs/microdata.html

The analysis combines person-level and housing-level ACS records using household serial numbers.

The analytical sample contains 231,059 eligible observations.

## Methodology

### Data Preparation
- Imported and cleaned ACS person and housing datasets.
- Merged person and housing records using household identifiers.
- Restricted the sample to individuals ages 18–29 working at least 30 hours per week.
- Adjusted personal income using the ACS adjustment factor.
- Constructed a binary housing-cost burden measure.

### Housing-Cost Burden Definition

Housing-cost burden is defined as spending at least 30% of household income on housing costs.

- Renters: Gross rent as a percentage of household income (GRPIP).
- Homeowners: Selected monthly owner costs as a percentage of household income (OCPIP).

### Statistical Analysis

- Weighted descriptive statistics.
- Comparisons across income and housing tenure groups.
- Survey-weighted logistic regression using the R survey package.
- ACS successive-difference replication (SDR) with all 80 replicate weights.
- Multicollinearity and nonlinear relationship diagnostics.
- Sensitivity analysis using a 99th-percentile personal income cap.

The final regression includes income, income squared, age, age squared, weekly work hours, and housing tenure.

## Key Descriptive Findings

Using person-weighted estimates:

- Approximately 37.32% of eligible renters experienced housing-cost burden.
- Approximately 15.44% of eligible homeowners experienced housing-cost burden.

Housing-cost burden was also more prevalent in lower personal-income groups across the housing tenure categories examined.

## Regression Findings

The survey-weighted logistic regression identified statistically significant associations between housing-cost burden and:

- Personal income.
- Age.
- Weekly work hours.
- Housing tenure.

The analysis found evidence of nonlinear relationships involving personal income and age.

Compared with homeowners with a mortgage, renters had substantially higher adjusted odds of housing-cost burden, while homeowners without a mortgage had lower adjusted odds.

A sensitivity analysis capping personal income at the 99th percentile supported the presence of nonlinear income and age relationships.

These findings describe statistical associations and should not be interpreted as causal effects.

## Tools and Technologies

- Python
- R
- Pandas
- NumPy
- Statsmodels
- Survey package for R
- Google Colab
- Jupyter Notebook
- GitHub

## Limitations

- The study uses cross-sectional observational data and cannot establish causation.
- Housing-cost burden is a household-level measure associated with individual records.
- Multiple young adults may belong to the same household.
- Personal income does not represent total household resources.
- The analysis is limited to the selected age and work-hour population.
- Statistical significance does not necessarily indicate practical significance.

## Ethical Considerations

This project uses publicly available, de-identified Census data. Findings are reported in aggregate, and no attempt is made to identify individual respondents.

## Project Status

The primary data preparation, descriptive analysis, survey-weighted regression, model diagnostics, and sensitivity analysis have been completed. Final interpretation and research reporting are in progress.

## Author

Social Data Science Capstone Project
