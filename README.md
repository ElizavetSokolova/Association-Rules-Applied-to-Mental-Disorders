# Association Rules Analysis for Mental Health Diagnostics

Analysis of mental disorder diagnostic patterns using association rules mining on psychological survey data.
The results of analysis can be found in RPubs: https://rpubs.com/Sokolova/1397991

## About

Association rules is an unsupervised learning algorithm which is sharpened for the purpose of finding patterns in data such as market basket analysis or customer preferences to create recommendation systems.

Despite the fact that those are the most popular applications, this study shows how the association rules algorithms may help to analyze survey data, and namely, psychological and behavioral questionnaires for mental disorder diagnosis. The current dataset is collected from a private psychology clinic. This dataset comprised 30 samples for each of the Normal, Mania Bipolar Disorder, Depressive Bipolar Disorder, and Major Depressive Disorder categories summing up to 120 patiants. The dataset contains the 17 essential symptoms psychiatrists use to diagnose the described disorders.

Source of dataset: https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/0FNET5

This implementation may help to better understand the causalities between the patients’ characteristics and symptom patterns, extending beyond simple correlation analysis.

Step-by-step, the work will look as follows:

Loading and inspecting data
Feature preprocessing (discretization of rating scales)
Frequency inspection of symptoms
Discovering symptom patterns and diagnostic rules
Visualization and clinical interpretation

## Dataset

**Source:** Mental Disorders Diagnostic Survey  
**Size:** 120 patients (30 per diagnostic category)  
**Features:** 17 symptoms + 1 diagnosis variable  
**Diagnoses:** Bipolar Type-1, Bipolar Type-2, Major Depressive Disorder, Normal

**Symptom types:**
- Categorical (Seldom, Sometimes, Usually, Most-Often, YES, NO)
- Rating scales (1-10, discretized to Low/Medium/High)

## Files
```
├── Mental_Disorders_AR.Rmd       # R Markdown analysis
├── Mental_Disorders_AR.pdf       # Generated report
├── Dataset-Mental-Disorders.csv  # Survey data
└── README.md                     # This file
```

## How to Run

### Prerequisites

Install required R packages:
```r
install.packages(c("arules", "arulesViz", "tidyverse", "knitr", "RColorBrewer"))
```

### Generate Report

**Option 1: RStudio (recommended)**
1. Open `Mental_Disorders_AR.Rmd` in RStudio
2. Click **Knit** → **Knit to PDF**
3. The PDF will be generated automatically

**Option 2: Command line**
```r
rmarkdown::render("Mental_Disorders_AR.Rmd")
```

### View Report

Simply open `Mental_Disorders_AR.pdf` to see the complete analysis with visualizations.

---

**Author:** Elizaveta Sokolova  
**Date:** February 2026