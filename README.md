---
editor_options: 
  markdown: 
    wrap: 72
---

# Leyi-and-Ella-Project

Project Repository for Longitudinal Data Analysis Practical 25/26.

This project prepares the UCL cohorts COVID-19 survey Waves 1-3 for a
longitudinal analysis of depressive symptoms, loneliness, and social
support.

## Title

Loneliness, Social Support, and Depressive Symptoms During COVID-19: A
Three-Wave Longitudinal Analysis of UK Cohort Data

## Background Note

The COVID-19 survey collected information on participants' physical and
mental health, wellbeing, family/relationships, education, and work
across three pandemic waves. Wave 1 was May 2020, Wave 2 was
September/October 2020, and Wave 3 was February/March 2021 during the
third UK lockdown.

## Main Research Question

How did depressive symptoms change across three waves of the COVID-19
pandemic, and were loneliness and social support associated with
depressive symptoms over time?

## Hypotheses

H1: Depressive symptoms will differ across waves, with higher depressive
symptoms expected at Wave 3 compared with Wave 1.

H2: Higher loneliness will be associated with higher depressive symptoms
across waves.

H3: Lower perceived social support will be associated with higher
depressive symptoms across waves.

H4: Social support may moderate the loneliness-depression association,
such that the association between loneliness and depressive symptoms is
weaker among people reporting stronger social support.

## Read This Repository In Order

1.  `analysis/01_data_cleaning.Rmd` reads the raw files from
    `data/raw/`, creates participant keys, recodes documented
    missing-value codes, creates provisional scores, validates ranges,
    and writes `data/processed/analysis_long.rds`.

2.  `analysis/02_data_exploration.Rmd` reads
    `data/processed/analysis_long.rds`, checks structure, missingness,
    attrition, and descriptive distributions, then saves figures to
    `figures/`.

3.  `analysis/03_mixed_effects_analysis.Rmd` reads
    `data/processed/analysis_long.rds`, prepares the modelling dataset,
    fits random-intercept mixed-effects models, compares model fit,
    tests the hypotheses, and saves model figures and tables.

## Project Structure

``` text
Leyi-and-Ella-Project/
├── Leyi-and-Ella-Project.Rproj
├── README.md
├── .gitignore
├── analysis/
│   ├── 01_data_cleaning.Rmd
│   ├── 02_data_exploration.Rmd
│   └── 03_mixed_effects_analysis.Rmd
├── data/
│   ├── raw/
│   └── processed/
│       └── analysis_long.rds
├── figures/
│   ├── depression_histogram.png
│   ├── loneliness_histogram.png
│   ├── score_boxplots.png
│   ├── model_estimated_depression_by_wave.png
│   └── loneliness_social_support_interaction.png
└── outputs/
    ├── model_sample_table.csv
    ├── icc_table.csv
    ├── model_comparison.csv
    ├── wave_comparisons.csv
    └── moderation_check.csv
```

## Summary of Findings

The mixed-effects analysis found that depressive symptoms differed
across waves, with Wave 3 significantly higher than Wave 1. Loneliness
was positively associated with depressive symptoms, while social support
was negatively associated with depressive symptoms. Social support also
slightly weakened the association between loneliness and depressive
symptoms.

For the full analysis, see
`analysis/03_mixed_effects_analysis.Rmd`.

## Figures

### Estimated Depressive Symptoms Across Waves

![Estimated depressive symptoms across
waves](figures/model_estimated_depression_by_wave.png)

### Loneliness And Depressive Symptoms By Social Support

![Loneliness and depressive symptoms by social
support](figures/loneliness_social_support_interaction.png)
