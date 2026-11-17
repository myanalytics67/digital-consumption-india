# Mapping the E-Consumer: An Empirical Analysis of MPCE and Digital Spend

An empirical study of household consumption expenditure and online spending patterns in India using the **Household Consumption Expenditure Survey (HCES) 2023–24** and R.

## Overview

India's digital economy has expanded rapidly, but participation in online consumption may differ across socioeconomic groups. This project examines how the share of household consumption expenditure spent online varies across rural and urban households, employment groups and living-standard levels.

The study investigates whether these differences persist after accounting for household size and state-level variation.

## Research Questions

- How does the share of household consumption spent online differ between rural and urban households?
- How does online spending vary across employment groups?
- Does the rural–urban difference vary across employment categories?
- Is household living standard, measured through Monthly Per Capita Consumption Expenditure (MPCE), associated with online spending?
- Do these relationships persist when the explanatory factors are considered jointly?

## Data

**Source:** Household Consumption Expenditure Survey (HCES) 2023–24, National Statistics Office (NSO), Ministry of Statistics and Programme Implementation (MoSPI), Government of India.

The analysis uses household-level information from multiple HCES data levels:

- **Level 15:** Household characteristics, sector, state, survey weights and expenditure information.
- **Level 3:** Main household income activity, used to classify employment groups.
- **Levels 5, 6, 8, 9, 10, 12 and 13:** Item-level expenditure data used to construct MPCE.

The datasets were combined using household identifiers constructed from the survey's identification variables.

## Methodology

The analysis was conducted in R and involved:

1. Data cleaning, preparation and merging across HCES data levels.
2. Construction of household MPCE using expenditure components and their respective recall periods.
3. Calculation of online spending as a percentage of monthly household consumption expenditure.
4. Classification of households by rural/urban sector and employment group.
5. Survey-weighted descriptive statistics.
6. Weighted linear regression models with state fixed effects.
7. Weighted two-way ANOVA to examine employment-group differences and sector–employment interactions.
8. A joint regression examining sector, employment group, log MPCE and household size.

Survey weights were calculated using the survey multiplier divided by 100.

## Key Findings

- The weighted average online spending share was **2.84% for rural households**, compared with **8.85% for urban households**.
- Regular wage/salary households recorded a higher weighted average online spending share (**8.64%**) than self-employed households (**4.47%**) and casual-labour households (**1.71%**).
- The rural–urban difference was also visible across employment groups.
- Higher household living standards, measured through MPCE, were positively associated with online spending.
- The rural–urban gap became smaller after accounting for employment, MPCE, household size and state, but remained statistically significant.

## Limitations

- The analysis uses cross-sectional data from a single survey year and therefore cannot establish causal relationships.
- Missing online expenditure observations are excluded; if these represent zero spending, the estimated average online spending share may be overstated.
- Variables such as education, age, internet access and banking access are not included in the models.
- The analysis is conducted at the household level and does not capture differences between individual household members.

## Tools and Technologies

- **R**
- Tidyverse
- Data.table
- ggplot2
- Weighted statistical analysis
- Linear regression and ANOVA

## Project Report

The knitted HTML report is available in this repository:

[`report.html`](report.html)

Open the file to view the complete analysis, methodology, statistical outputs and visualisations.

## Project Type

**Collaborative Academic Group Project**

A group research project involving collaborative data preparation, statistical analysis, interpretation of findings and report writing.
