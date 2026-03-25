# Hair Fall Risk Factors Analysis

## 📊 Project Overview

This project performs an **exploratory data analysis (EDA)** on a dataset of hair fall risk factors. The goal is to understand whether hair loss is driven by a single factor or by a combination of conditions such as stress, nutritional deficiencies, medical conditions, and lifestyle habits.

**Key question:** Is hair loss multifactorial or dominated by a single risk factor?

## 🎯 Objectives

- Identify the most influential risk factors for hair loss
- Explore interactions between variables (stress × nutrition, age × medical conditions)
- Test statistical assumptions (normality, independence)
- Generate reproducible visualizations and summary tables

## 🛠️ Technologies Used

- **Language:** R 4.x
- **Libraries:** dplyr, ggplot2, readr, openxlsx
- **Tools:** RMarkdown, knitr, RStudio
- **Output formats:** HTML, Markdown, Excel

## 📁 Dataset Description

The dataset contains survey data on individuals with and without hair loss, including:

| Variable | Type | Description |
|----------|------|-------------|
| Age | Numeric | Age in years |
| Stress | Categorical | Low / Moderate / High |
| Nutritional Deficiencies | Categorical | Type of deficiency (e.g., Iron, Zinc, Vitamin D) |
| Medical Conditions | Categorical | e.g., Androgenetic Alopecia, Seborrheic Dermatitis |
| Smoking | Binary | Yes / No |
| Hair Loss | Binary | Outcome variable (0 = No, 1 = Yes) |

*Full variable list available in the analysis.*

## 🔍 Key Findings

1. **Multifactorial nature of hair loss:**  
   No single nutritional deficiency exceeds 55% incidence in hair loss patients. Magnesium (54.8%), Protein (52.2%), and Iron (51.3%) show the highest proportions, but all deficiencies are represented.

2. **Stress interacts with specific nutrients:**  
   Selenium deficiency is highly prevalent under high stress (45%), but nearly absent under low/moderate stress (<2%), suggesting a stress–nutrient interaction.

3. **Medical conditions strongly associated:**  
   Androgenetic Alopecia, Alopecia Areata, and Seborrheic Dermatitis are the most frequent conditions among individuals with hair loss.

4. **Age is not a determining factor:**  
   Age distributions are nearly identical between hair loss and non-hair loss groups. However, age among hair loss individuals is **right-skewed** (peak at 20–25 years), violating normality assumptions.

5. **Stress alone does not determine hair loss:**  
   Proportions of hair loss are similar across Low, Moderate, and High stress groups, though Moderate stress shows a slight increase.

## 📈 Visualizations

The analysis includes:

- Bar plots: stress × hair loss proportions
- Heatmaps: medical conditions × hair loss
- Boxplots: age distribution by hair loss status
- Histograms with density curves (normality assessment)

*See the full RMarkdown document for all figures.*

## 🧪 Statistical Methods

- Contingency tables and proportion tests
- Chi-square tests for categorical associations
- Normality assessment (histograms + theoretical curves)
- Descriptive statistics (mean, median, SD, frequencies)

## 🚀 How to Reproduce

### Prerequisites
- R (≥ 4.0)
- RStudio (recommended)

### Installation
```r
# Install required packages
install.packages(c("dplyr", "ggplot2", "readr", "openxlsx", "knitr"))
