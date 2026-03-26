# Analysis and Visualization of Complex Agro-Environmental Data (AVCAD)

**Student:** Danilo III O. Gonzales (29225)  
**Program:** MSc in Green Data Science
**Institution:** Instituto Superior de Agronomia (ISA), Universidade de Lisboa  

---

## About

This repository contains the exercises for the AVCAD course. All exercises use the **EFIplus_medit** dataset — a subset of a database integrating river fish biomonitoring data from Mediterranean countries (Italy, Portugal, and Spain).

---

## Repository Structure

```
greends_avcad_exercises/
├── exercise_01/
├── exercise_02/
├── exercise_03/
│   ├── CaseStudy1_univariate_analysis_visuals.ipynb
│   └── EFIplus_medit.zip
├── exercise_04/
│   └── avcad_exer04_dgonzales.ipynb
├── exercise_05/
│   └── avcad_exer05_dgonzales.ipynb
└── README.md
```

---

## Exercise Summaries

### Exercise 1 — Data Import and Exploration
- Importing and inspecting the EFIplus_medit dataset
- Exploring data types, dimensions, and column names
- Identifying and handling missing values

### Exercise 2 — Data Visualization Evaluation
- Evaluating chart quality using Cairo and Tufte frameworks
- Assessing data-ink ratio, chart junk, and visual clarity
- Critiquing real-world visualizations (e.g., COVID-19 and physician density charts)

### Exercise 3 — Univariate Analysis and Sampling Distributions
- Identifying the **top 4 catchments** by number of fish sampling sites
- Plotting **strip plots**, **histograms** (with KDE, mean/median lines), **boxplots**, and **violin plots** of Annual Mean Temperature (`temp_ann`) in 2×2 grids
- Evaluating **pros and cons** of each plot type as univariate visualizations
- **Challenge:** Demonstrating the Central Limit Theorem by plotting the sampling distribution of mean `temp_ann` across increasing sample sizes (10 to 1500), with a standard error convergence curve and sample size formula derivation

### Exercise 4 — Bivariate Analysis, Normality Testing, and CLT
- **Q1:** Exploring how `temp_ann` affects the presence of *Salmo trutta fario* (Brown Trout) using boxplots and violin plots — trout-present sites are significantly cooler (median ≈ 13.0 °C vs 15.4 °C)
- **Q2:** Comparing the temperature–trout relationship in **Minho** and **Tejo** catchments with Cohen's d effect size analysis — Minho shows a medium effect (d = 0.70) while Tejo shows a large effect (d = 1.84)
- **Q3:** Testing normality of `actual_river_slope` using graphical methods (histogram, Q-Q plot) and the Shapiro-Wilk test — the variable is heavily right-skewed (skewness = 12.76) and not normally distributed
- **Q4:** Demonstrating the CLT by drawing 100 samples of 2000 observations of `actual_river_slope`, showing that sample means are normally distributed despite the original data being highly skewed

### Exercise 5 — Hypothesis Testing
- **Q1:** Testing whether mean `temp_ann` differs between Brown Trout presence and absence sites using **t-test** and **Mann-Whitney U** on both standardized (z-score) and non-standardized values — all tests reject H₀, and results are identical across standardization
- **Q2:** Testing independence of trout presence from country using the **Chi-squared test** — trout presence is strongly associated with country (χ² = 1216.39, p ≈ 0), with Spain having ~93% presence vs Portugal at ~29%
- **Q3:** Testing differences in mean upstream catchment elevation (`Elevation_mean_catch`) among the 8 most sampled catchments using **one-way ANOVA** (F = 157.17, p ≈ 0) and **Tukey HSD** post-hoc pairwise comparisons
- **Q4:** Running the non-parametric equivalent (**Kruskal-Wallis H test**) and comparing with ANOVA — both reach the same conclusion, with pairwise **Mann-Whitney U** tests (Bonferroni-corrected) used as post-hoc

---

## Tools and Libraries

- **Python** (pandas, numpy, seaborn, matplotlib, scipy)
- **Jupyter Notebook** (Google Colab)
- **GitHub** for version control

---

## Dataset

The **EFIplus_medit** dataset contains biomonitoring data from Mediterranean river fish sampling sites across Italy, Portugal, and Spain. Key variables used across exercises include:

| Variable | Description |
|----------|-------------|
| `temp_ann` | Annual Mean Temperature (°C) |
| `temp_jul` | Mean July Temperature (°C) |
| `Actual_river_slope` | River slope at sampling site |
| `Elevation_mean_catch` | Mean elevation of upstream catchment (m) |
| `Salmo trutta fario` | Presence (1) / Absence (0) of Brown Trout |
| `Catchment_name` | Name of the river catchment |
| `Country` | Country (Italy, Portugal, Spain) |
