# Data-Analysis-in-R
# CYP-GUIDES: Medication Intensity, Race/Ethnicity, and Length of Stay

An exploratory analysis in R of the CYP-GUIDES clinical trial dataset, a randomized trial of genotype-guided psychotropic treatment in hospitalized patients with severe depressive disorders.

## Question

Do patients of different racial and ethnic groups receive different intensities of medication, and does medication intensity relate to hospital length of stay (LOS)?

## Data

- CYP-GUIDES trial dataset (de-identified), available on Kaggle: https://www.kaggle.com/datasets/shashwatwork/clinical-dataset-of-the-cypguides-trial
- The data is not included in this repository. Download it from Kaggle and place `Dataset.csv` in the project folder.

## Methods

- Cleaned and recoded variables (race/ethnicity and gender as factors).
- Counted medication categories received per patient (30 binary category columns, A to AD).
- Defined a high-intensity treatment indicator (2 or more medication categories).
- Summarized LOS, medication intensity, and diagnosis, and visualized patterns with `ggplot2` (histogram, boxplot, proportion plot, heatmap).

## Descriptive findings

- Most patients received a low number of medication categories.
- High-intensity patients tended to have longer LOS.
- The share of high-intensity treatment differed across racial and ethnic groups.
- Severe and recurrent forms of major depressive disorder had the longest stays and highest intensity.

These are descriptive patterns, not causal claims.

## Limitations

- De-identified data with no dosage or timing information.
- Medication categories are simplified.
- LOS is right-skewed and influenced by many factors.
- Formal statistical testing and adjusted models are not yet included.

## Next steps

- Add rank-based tests and a chi-square test for LOS and race by intensity.
- Fit an adjusted model of LOS on intensity, race/ethnicity, diagnosis, and gender.
- Show heatmap values as proportions within each group.

## Files

- `analysis.Rmd`: analysis and slides (R Markdown)
- `README.md`: this file

## Tools

R (tidyverse, ggplot2, knitr, kableExtra, reshape2), R Markdown

## Author

Tashae DeWalt
