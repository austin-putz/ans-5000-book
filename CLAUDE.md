# Introduction to Data Science & Statistics Course Plan
## AnS 500 - Fall 2025 (16 Weeks Total: 8 Weeks Data Science + 8 Weeks Statistics)

---

## Course Overview

**Duration**: 16 weeks total (8 weeks Part 1 + 8 weeks Part 2)
**Format**: 2 hours lecture per week + 1 homework assignment
**Tools**: R + Quarto exclusively
**Prerequisites**: None (Part 1 starts from basics)

---

# PART 1: INTRODUCTION TO DATA SCIENCE (Weeks 1-8)

## Part 1 Overview

This first half of the course introduces students to data science fundamentals using R, RStudio, and Quarto. Students will learn modern data manipulation and visualization techniques using the tidyverse ecosystem. By the end of Part 1, students will be able to import, clean, transform, visualize, and report on data using reproducible workflows.

**Philosophy**: Tidyverse-first approach, real-world animal science datasets, reproducible research from day one.

---

## Part 1: 8-Week Course Outline

### Week 1: Foundations of Data Science & Best Practices
**Topics**:
- What is data science? Definition, scope, and the data science workflow
- Why statistics matters (preview of Part 2)
- Observational vs experimental design (brief intro)
- Programming languages for data science: R, Python, Julia
- Why avoid Excel for analysis (when it's okay, when it's not)
- Project organization: folder structure, file naming conventions
- Data best practices: column naming, file formats (CSV, Excel), metadata
- Database fundamentals: relational structure, long vs wide format
- Version control basics: Git and GitHub
- Introduction to R, RStudio, and Quarto
- What does it take to be a data scientist?

**R/Quarto Focus**: Installing R/RStudio, first Quarto document, project setup, basic R as a calculator

**Homework**: Install R/RStudio/Quarto, set up a project with proper folder structure, write reflection on data science

**External Links to Include**:
- [The R Project](https://www.r-project.org/)
- [RStudio/Posit](https://posit.co/downloads/)
- [Quarto](https://quarto.org/)
- [Python](https://www.python.org/)
- [Julia Language](https://julialang.org/)
- [Git](https://git-scm.com/)
- [GitHub](https://github.com/)
- [R for Data Science (2e)](https://r4ds.hadley.nz/)

---

### Week 2: Getting Started with R, RStudio, and Reading Data
**Topics**:
- RStudio interface: Console, Scripts, Environment, Files, Plots, Help
- R Projects and working directories (`here` package)
- Installing and loading packages: `install.packages()`, `library()`
- Quarto documents: YAML headers, markdown syntax, code chunks, rendering
- Reading CSV files: `readr::read_csv()`
- Reading Excel files: `readxl::read_excel()`
- First look at data: `head()`, `tail()`, `glimpse()`, `str()`, `summary()`
- Basic data structures: vectors, data frames, tibbles
- R help system: `?function`, `??search term`, package documentation

**R/Quarto Focus**: Create first analysis with imported data, render to HTML/PDF

**Homework**: Import CSV and Excel datasets, explore structure, create Quarto report with observations

**External Links**:
- [readr documentation](https://readr.tidyverse.org/)
- [readxl documentation](https://readxl.tidyverse.org/)
- [Tidyverse](https://www.tidyverse.org/)

---

### Week 3: Data Types, Strings, and Introduction to dplyr
**Topics**:
- R data types: numeric, integer, character, factor, logical, Date/POSIXct
- Type checking: `class()`, `typeof()`, `is.numeric()`, etc.
- Type coercion: `as.numeric()`, `as.character()`, `as.factor()`
- Working with factors: `forcats` package basics
- String manipulation with `stringr`:
  - `str_detect()`, `str_replace()`, `str_replace_all()`
  - `str_to_lower()`, `str_to_upper()`, `str_trim()`
  - `str_split()`, `str_c()`, `str_subset()`
- Regular expressions (regex) basics
- Introduction to the pipe: `%>%` (magrittr) and `|>` (native pipe)
- First dplyr verbs: `select()`, `filter()`

**R/Quarto Focus**: Cleaning messy data, string operations, filtering datasets

**Homework**: Clean dataset with messy strings/column names, apply filters, document process in Quarto

**External Links**:
- [stringr documentation](https://stringr.tidyverse.org/)
- [forcats documentation](https://forcats.tidyverse.org/)
- [Regular expressions cheat sheet](https://www.rstudio.com/wp-content/uploads/2016/09/RegExCheatsheet.pdf)

---

### Week 4: Data Manipulation with dplyr
**Topics**:
- Core dplyr verbs in depth:
  - `mutate()`: Create and modify variables
  - `arrange()`: Sort rows by one or more columns
  - `group_by()` + `summarise()`: Grouped aggregations
  - `count()` and `tally()`: Frequency tables
  - `rename()`: Rename columns
  - `relocate()`: Reorder columns
- The power of the pipe: chaining operations
- Working across multiple columns: `across()` function
- Conditional operations:
  - `if_else()`: Vectorized if-else
  - `case_when()`: Multiple condition logic
- Handling missing data:
  - `is.na()`, `drop_na()`, `replace_na()`
  - `coalesce()`: Replace NAs with values
- Window functions: `lag()`, `lead()`, `cumsum()`, `row_number()`

**R/Quarto Focus**: Complex multi-step transformations, grouped summaries, dealing with NAs

**Homework**: Multi-step data transformation challenge using animal science dataset

**External Links**:
- [dplyr documentation](https://dplyr.tidyverse.org/)
- [dplyr cheat sheet](https://github.com/rstudio/cheatsheets/blob/main/data-transformation.pdf)

---

### Week 5: Introduction to Data Visualization with ggplot2
**Topics**:
- The Grammar of Graphics philosophy
- ggplot2 basic structure: `data` + `aes()` + `geom_*()`
- Essential geometries:
  - `geom_point()`: Scatter plots
  - `geom_line()`: Line plots
  - `geom_col()` / `geom_bar()`: Bar charts
  - `geom_histogram()`: Distributions
  - `geom_boxplot()`: Box plots
  - `geom_violin()`: Violin plots
- Aesthetic mappings: `x`, `y`, `color`, `fill`, `size`, `shape`, `alpha`
- Scales: continuous and discrete
- Coordinate systems: `coord_cartesian()`, `coord_flip()`
- Labels and titles: `labs(title, subtitle, x, y, caption)`
- Themes: `theme_minimal()`, `theme_classic()`, `theme_bw()`
- Saving plots: `ggsave()`

**R/Quarto Focus**: Create publication-ready plots, understand when to use each geom

**Homework**: Create 5 different plot types from dataset, properly labeled and themed

**External Links**:
- [ggplot2 documentation](https://ggplot2.tidyverse.org/)
- [ggplot2 cheat sheet](https://github.com/rstudio/cheatsheets/blob/main/data-visualization.pdf)
- [R Graph Gallery](https://r-graph-gallery.com/)

---

### Week 6: Advanced ggplot2 and Multi-Panel Plots
**Topics**:
- Faceting for small multiples:
  - `facet_wrap()`: Wrap panels by one variable
  - `facet_grid()`: Grid of panels by two variables
- Statistical layers:
  - `geom_smooth()`: Add trend lines (lm, loess, gam)
  - `stat_summary()`: Summarize y for each x
  - Error bars: `geom_errorbar()`, `geom_pointrange()`
- Customizing themes:
  - `theme()`: Fine-tune plot appearance
  - Creating custom themes
  - Modifying legends, axes, grid lines
- Color palettes:
  - `scale_color_brewer()`, `scale_fill_brewer()`
  - `scale_color_viridis_c()` / `_d()`: Colorblind-friendly
  - Custom color scales
- Text and annotations:
  - `geom_text()`, `geom_label()`: Add text to plots
  - `annotate()`: Add annotations
- Combining plots:
  - `cowplot` package: `plot_grid()`
  - `patchwork` package: `+`, `/`, `|` operators
- Final polish for publications

**R/Quarto Focus**: Complex multi-panel figures, publication-ready output

**Homework**: Replicate a published figure from a journal article

**External Links**:
- [cowplot documentation](https://wilkelab.org/cowplot/)
- [patchwork documentation](https://patchwork.data-imaginist.com/)
- [Color Brewer](https://colorbrewer2.org/)

---

### Week 7: Data Reshaping, Joining, and Iteration
**Topics**:
- Tidy data principles (Hadley Wickham)
- Reshaping with `tidyr`:
  - `pivot_longer()`: Wide to long format
  - `pivot_wider()`: Long to wide format
  - `separate()`: Split one column into many
  - `unite()`: Combine columns
- Joining datasets (SQL-style joins):
  - `left_join()`: Keep all rows from left table
  - `right_join()`: Keep all rows from right table
  - `inner_join()`: Keep only matching rows
  - `full_join()`: Keep all rows from both tables
  - `anti_join()`, `semi_join()`: Filtering joins
- Binding datasets:
  - `bind_rows()`: Stack datasets vertically
  - `bind_cols()`: Attach datasets horizontally
- When to use loops (and when NOT to)
- Functional programming with `purrr`:
  - `map()`: Apply function, return list
  - `map_dbl()`, `map_chr()`: Return vectors
  - `map_df()`: Return data frame
  - `map2()`, `pmap()`: Multiple inputs
- List columns and nested data frames

**R/Quarto Focus**: Complex reshaping, merging multiple datasets, iteration

**Homework**: Merge multiple related datasets, reshape from wide to long, summarize with iteration

**External Links**:
- [tidyr documentation](https://tidyr.tidyverse.org/)
- [purrr documentation](https://purrr.tidyverse.org/)
- [Tidy data paper](https://www.jstatsoft.org/article/view/v059i10)

---

### Week 8: Special Data Formats, Integration, and Course Wrap-up
**Topics**:
- Reading data from other statistical software:
  - `haven` package: SAS (`.sas7bdat`), SPSS (`.sav`), Stata (`.dta`)
  - Why you might need this, how to handle labels
- Working with Excel files:
  - `readxl`: Reading Excel (simple)
  - `writexl`: Writing Excel files
  - `openxlsx`: Advanced Excel operations (formatting, multiple sheets)
- Other useful packages:
  - `janitor`: Cleaning column names, removing duplicates, `tabyl()`
  - `lubridate`: Date and time manipulation
  - `glue`: String interpolation
- Review: The complete data science workflow
- Reproducibility and best practices checklist
- Transitioning to Part 2: How data science enables statistics
- Resources for continued learning
- Career paths in data science

**R/Quarto Focus**: Import from various formats, complete pipeline from raw data to report

**Homework**: **Final Part 1 Project** - Import messy multi-source data, clean, transform, visualize, present in professional Quarto report

**External Links**:
- [haven documentation](https://haven.tidyverse.org/)
- [writexl documentation](https://docs.ropensci.org/writexl/)
- [janitor documentation](https://sfirke.github.io/janitor/)
- [lubridate documentation](https://lubridate.tidyverse.org/)

---

## Part 1 Teaching Notes

### Package Installation - Week 1
Recommend students install all necessary packages at the start:

```r
# Core tidyverse (includes dplyr, ggplot2, tidyr, readr, purrr, stringr, forcats, tibble)
install.packages("tidyverse")

# Additional packages for Part 1
install.packages(c(
  "readxl",      # Read Excel files
  "writexl",     # Write Excel files
  "haven",       # Read SAS/SPSS/Stata files
  "janitor",     # Data cleaning
  "lubridate",   # Date/time manipulation
  "cowplot",     # Combining plots
  "patchwork",   # Combining plots (alternative)
  "here",        # Project-relative paths
  "glue"         # String interpolation
))
```

### Recommended Quarto YAML for Part 1 Assignments

```yaml
---
title: "Week X Homework: [Topic]"
author: "Your Name"
date: today
format:
  html:
    toc: true
    toc-depth: 2
    code-fold: false
    code-tools: true
    theme: cosmo
    embed-resources: true
execute:
  warning: false
  message: false
---
```

### Teaching Philosophy for Part 1

1. **Tidyverse-first**: No base R subsetting (`df$col`, `df[,1]`), use dplyr/tidyr exclusively
2. **Pipe-forward**: Encourage `|>` or `%>%` for readable code flow
3. **Real data**: Use actual animal science datasets with real messiness
4. **Reproducibility**: Every analysis in Quarto from Week 1
5. **Best practices early**: Teach project organization, naming conventions, documentation from the start
6. **Build incrementally**: Each week builds directly on previous weeks
7. **Show, don't tell**: Live coding demonstrations, not just slides

### Common Student Challenges (Part 1)

1. **Path issues**: Teach R Projects and `here::here()` early
2. **Package loading**: Distinguish `install.packages()` (once) vs `library()` (every session)
3. **Pipe confusion**: Practice reading pipes as "and then"
4. **ggplot layering**: Use `+` not `%>%` between ggplot layers
5. **Join confusion**: Draw Venn diagrams for different join types
6. **Forgetting `group_by()` before `summarise()`

---

---

# PART 2: INTRODUCTION TO STATISTICS (Weeks 9-16)

## Part 2 Overview

The second half builds on Part 1's data manipulation and visualization skills to conduct statistical analyses. Students will learn frequentist statistical inference, hypothesis testing, and regression modeling.

**Prerequisites**: Completion of Part 1 (or equivalent R/tidyverse experience)

---

## Part 2: 8-Week Course Outline

### Week 1: Statistical Foundations & Study Design
**Topics**:
- Big picture: What is statistics?
- Frequentist vs Bayesian frameworks
- Understanding p-values and statistical significance
- Observational vs Experimental studies
- Randomized Controlled Trials (RCTs)
- Confounding variables and causation vs correlation

**R/Quarto Focus**: Setting up statistical analysis workflows, basic visualization of distributions

**Homework**: Critique a published study (observational vs experimental), identify potential confounders

---

### Week 2: Descriptive Statistics & Exploratory Data Analysis
**Topics**:
- Measures of central tendency (mean, median, mode)
- Measures of variability (variance, SD, IQR, range)
- Data visualization principles
- Distribution shapes (normal, skewed, bimodal)
- Outlier detection
- Summary statistics in context

**R/Quarto Focus**: `dplyr::summarise()`, `ggplot2` for EDA, creating publication-ready tables with `gt` or `knitr::kable()`

**Homework**: Complete EDA on a provided dataset with Quarto report

---

### Week 3: Probability Distributions & Introduction to Inference
**Topics**:
- Normal distribution and properties
- Central Limit Theorem
- Sampling distributions
- Standard error vs standard deviation
- Confidence intervals (concept and calculation)
- Introduction to z-scores and standardization

**R/Quarto Focus**: `rnorm()`, `pnorm()`, `qnorm()`, simulations to demonstrate CLT, visualization of sampling distributions

**Homework**: Simulation exercise demonstrating CLT with different sample sizes

---

### Week 4: Hypothesis Testing Fundamentals
**Topics**:
- Null and alternative hypotheses
- Type I and Type II errors
- Statistical power
- One-sample t-tests
- Two-sample t-tests (independent samples)
- Paired t-tests
- Assumptions and diagnostics

**R/Quarto Focus**: `t.test()`, checking assumptions (normality tests, QQ plots), effect sizes with `effsize` package

**Homework**: Conduct and interpret t-tests on agricultural/animal science datasets

---

### Week 5: Analysis of Variance (ANOVA)
**Topics**:
- When to use ANOVA vs t-tests
- One-way ANOVA
- ANOVA assumptions (normality, homogeneity of variance, independence)
- Post-hoc tests (Tukey HSD, Bonferroni)
- Multiple comparisons problem
- Effect sizes (eta-squared, omega-squared)

**R/Quarto Focus**: `aov()`, `TukeyHSD()`, `car::leveneTest()`, visualization of group differences with boxplots and interaction plots

**Homework**: Complete one-way ANOVA analysis with post-hoc comparisons

---

### Week 6: Categorical Data Analysis
**Topics**:
- Chi-square goodness of fit test
- Chi-square test of independence
- Fisher's exact test
- Risk ratios and odds ratios
- 2x2 contingency tables
- Interpretation in biological contexts

**R/Quarto Focus**: `chisq.test()`, `fisher.test()`, `table()`, `prop.test()`, mosaic plots with `ggplot2`

**Homework**: Analyze categorical data from a veterinary or animal breeding study

---

### Week 7: Simple Linear Regression
**Topics**:
- Correlation vs regression
- Pearson correlation coefficient
- Simple linear regression model
- Least squares estimation
- Interpretation of coefficients (slope, intercept)
- R-squared and model fit
- Residual diagnostics
- Prediction and confidence intervals

**R/Quarto Focus**: `lm()`, `cor()`, diagnostic plots (`plot(model)`), `broom::tidy()` and `broom::glance()`, `ggplot2::geom_smooth()`

**Homework**: Build and interpret a simple linear regression model

---

### Week 8: Multiple Regression & Course Integration
**Topics**:
- Multiple regression basics
- Interpreting multiple predictors
- Categorical predictors (dummy variables)
- Model comparison (AIC, adjusted R-squared)
- Variable selection considerations
- Course synthesis: choosing the right statistical test
- Review of key concepts
- Path forward: next steps in statistical learning

**R/Quarto Focus**: `lm()` with multiple predictors, `step()`, model comparison, creating comprehensive analysis reports in Quarto

**Homework**: Final project - complete analysis from EDA through regression with written interpretation

---

## General Course Guidelines

### Quarto Workflow
- Each lecture will include a `.qmd` file with code examples
- Students will submit homework as rendered Quarto documents (HTML or PDF)
- Emphasize reproducible research practices
- YAML header templates will be provided

### Recommended R Packages
Core packages to install at the start of the course:
```r
install.packages(c(
  "tidyverse",      # Data manipulation and visualization
  "broom",          # Tidy statistical output
  "car",            # Companion to Applied Regression
  "effsize",        # Effect size calculations
  "ggpubr",         # Publication-ready plots
  "rstatix",        # Pipe-friendly statistical tests
  "gt",             # Grammar of Tables
  "patchwork",      # Combining plots
  "emmeans"         # Estimated marginal means
))
```

### Assessment Philosophy
- Focus on interpretation over calculation
- Emphasize assumptions and diagnostics
- Real-world datasets from animal/agricultural sciences
- Build statistical thinking, not just button-pushing

### Teaching Approach
- Start with questions, not tests
- Use simulation to build intuition
- Connect to previous R/data management skills
- Emphasize visualization before testing
- Discuss common pitfalls and misinterpretations

---

## Week 1 Detailed Lecture Outline

### Learning Objectives
By the end of Week 1, students will be able to:
1. Distinguish between frequentist and Bayesian statistical philosophies
2. Correctly interpret p-values and identify common misinterpretations
3. Differentiate observational studies from experimental studies
4. Explain the key features and benefits of Randomized Controlled Trials (RCTs)
5. Understand the relationship between study design and causal inference
6. Identify confounding variables in research scenarios

---

### Lecture Structure (2 hours)

#### Part 1: What is Statistics? (20 minutes)

**Key Questions**:
- Why do we need statistics?
- What can statistics tell us? What can't it tell us?
- The role of uncertainty and variability

**Discussion Points**:
- Statistics as a tool for making decisions under uncertainty
- Difference between descriptive and inferential statistics
- Preview of the course: building a statistical toolkit

**R Example**:
```r
# Demonstrate variability with a simple example
library(tidyverse)

# Simulate two groups of cattle weights
set.seed(123)
group_a <- rnorm(30, mean = 500, sd = 50)  # Treatment A
group_b <- rnorm(30, mean = 520, sd = 50)  # Treatment B

# Visualize
tibble(
  weight = c(group_a, group_b),
  treatment = rep(c("A", "B"), each = 30)
) %>%
  ggplot(aes(x = treatment, y = weight)) +
  geom_boxplot() +
  geom_jitter(width = 0.1, alpha = 0.5) +
  labs(title = "Do treatments differ?",
       y = "Weight (kg)",
       x = "Treatment") +
  theme_minimal()
```

**Key Question for Students**: *How confident are we that Treatment B is actually better?*

---

#### Part 2: Frequentist vs Bayesian Frameworks (25 minutes)

**Frequentist Approach**:
- Probability = long-run frequency
- Parameters are fixed but unknown
- Focus on what would happen if we repeated the experiment many times
- P-values and confidence intervals
- "What is the probability of observing data this extreme, given the null hypothesis is true?"

**Bayesian Approach**:
- Probability = degree of belief
- Parameters are uncertain (have distributions)
- Incorporates prior knowledge
- Posterior distributions and credible intervals
- "What is the probability that the hypothesis is true, given the data?"

**Key Differences Table**:

| Aspect | Frequentist | Bayesian |
|--------|-------------|----------|
| Probability | Long-run frequency | Degree of belief |
| Parameters | Fixed, unknown | Random variables with distributions |
| Prior knowledge | Not formally incorporated | Explicitly incorporated via priors |
| Output | p-values, confidence intervals | Posterior distributions, credible intervals |
| Interpretation | "If null is true, how likely is this data?" | "Given the data, how likely is the hypothesis?" |

**Note**: This course will focus primarily on frequentist methods (most common in animal/agricultural sciences), but awareness of Bayesian thinking is valuable.

**Discussion**: Why is the frequentist approach dominant in scientific publishing?

---

#### Part 3: Understanding P-Values (30 minutes)

**Definition**:
A p-value is the probability of obtaining results at least as extreme as the observed results, assuming the null hypothesis is true.

**What p-values ARE**:
- A measure of compatibility between data and the null hypothesis
- Continuous measure (not binary)
- Dependent on sample size
- A probability about the data, not about the hypothesis

**What p-values ARE NOT**:
- ❌ The probability that the null hypothesis is true
- ❌ The probability that the result occurred by chance
- ❌ The probability of making a wrong decision
- ❌ Evidence for the alternative hypothesis
- ❌ The magnitude or importance of an effect

**Common Misinterpretations**:
1. "p = 0.03 means there's a 3% chance the null is true" → **WRONG**
2. "p = 0.06 means there's no effect" → **WRONG** (absence of evidence ≠ evidence of absence)
3. "p = 0.001 means a large effect" → **WRONG** (statistical significance ≠ practical significance)

**The p < 0.05 Threshold**:
- Arbitrary convention proposed by R.A. Fisher
- Not a bright line between "true" and "false"
- Many fields are moving away from rigid thresholds
- Focus should be on effect sizes and confidence intervals

**R Simulation to Build Intuition**:
```r
# Simulate what p-values mean
set.seed(456)

# Generate data where null hypothesis is TRUE (no difference)
simulate_null_true <- function() {
  group1 <- rnorm(20, mean = 100, sd = 15)
  group2 <- rnorm(20, mean = 100, sd = 15)  # Same mean!
  t.test(group1, group2)$p.value
}

# Run simulation 1000 times
p_values <- replicate(1000, simulate_null_true())

# Visualize
tibble(p_value = p_values) %>%
  ggplot(aes(x = p_value)) +
  geom_histogram(bins = 20, fill = "steelblue", alpha = 0.7) +
  geom_vline(xintercept = 0.05, color = "red", linetype = "dashed", size = 1) +
  labs(title = "Distribution of p-values when null is TRUE",
       subtitle = "~5% of p-values are below 0.05 by chance alone",
       x = "P-value",
       y = "Count") +
  theme_minimal()

# What proportion are "significant"?
mean(p_values < 0.05)  # Should be close to 0.05
```

**Key Insight**: When the null hypothesis is true, we still get p < 0.05 about 5% of the time. This is Type I error.

---

#### Part 4: Observational vs Experimental Studies (30 minutes)

**Observational Studies**:
- Researcher observes without manipulating
- Cannot control for confounding variables
- Examples: surveys, cohort studies, case-control studies
- Can show associations but not causation

**Experimental Studies**:
- Researcher actively manipulates variables (treatments)
- Controls conditions
- Randomization helps balance confounders
- Can establish causation (under proper design)

**Key Concept: Confounding**

A confounder is a variable that:
1. Is associated with the exposure/treatment
2. Independently affects the outcome
3. Is not on the causal pathway

**Classic Example: Ice Cream and Drowning**
- Observational data shows ice cream sales correlate with drowning deaths
- Confounder: Temperature/Season
- Ice cream doesn't cause drowning!

**Agricultural Example: Pasture Type and Weight Gain**
```r
# Simulated example showing confounding
set.seed(789)

farm_data <- tibble(
  farm = rep(1:20, each = 10),
  pasture_type = rep(c("A", "B"), each = 100),
  # Farm quality is a confounder (better farms choose pasture A)
  farm_quality = rep(rnorm(20, mean = 50, sd = 10), each = 10),
  # Weight gain depends on farm quality, NOT pasture type
  weight_gain = farm_quality + rnorm(200, mean = 0, sd = 5)
)

# Naive analysis (ignoring confounding)
farm_data %>%
  group_by(pasture_type) %>%
  summarise(mean_gain = mean(weight_gain))

# Appears that pasture A is better!
# But it's because better farms chose pasture A

# Visualization
farm_data %>%
  ggplot(aes(x = farm_quality, y = weight_gain, color = pasture_type)) +
  geom_point(alpha = 0.6) +
  geom_smooth(method = "lm", se = FALSE) +
  labs(title = "Confounding Example: Farm Quality affects both pasture choice and outcome",
       x = "Farm Quality Score",
       y = "Weight Gain (kg)",
       color = "Pasture Type") +
  theme_minimal()
```

**Discussion**: How can we address confounding?
- Randomization (experimental studies)
- Statistical adjustment (observational studies)
- Matching
- Stratification

---

#### Part 5: Randomized Controlled Trials (RCTs) (15 minutes)

**Definition**: An experiment where participants are randomly assigned to treatment or control groups.

**Key Features of RCTs**:
1. **Randomization**: Ensures groups are balanced on both known and unknown confounders
2. **Control group**: Provides a comparison baseline
3. **Blinding** (when possible): Reduces bias
   - Single-blind: Participants don't know their group
   - Double-blind: Neither participants nor researchers know
4. **Standardization**: All other conditions kept as similar as possible

**Why Randomization Works**:
- Balances confounders across groups (on average)
- Allows causal inference
- Known probability distribution (enables statistical testing)

**Agricultural/Animal Science Examples**:
- Feed trial: Randomly assign calves to different diets
- Drug efficacy: Randomly assign pigs to antibiotic vs placebo
- Breeding trial: Randomly assign mating pairs

**Limitations of RCTs**:
- Can be expensive
- May not be ethical (e.g., can't randomly assign animals to disease exposure)
- May not be practical (long-term outcomes, rare events)
- Results may not generalize to real-world conditions

**R Simulation: Demonstrating the Power of Randomization**:
```r
# Show that randomization balances confounders
set.seed(2024)

# Population of 100 animals with various characteristics
population <- tibble(
  animal_id = 1:100,
  age = runif(100, min = 1, max = 5),
  baseline_weight = rnorm(100, mean = 300, sd = 50),
  farm = sample(c("North", "South", "East", "West"), 100, replace = TRUE),
  sex = sample(c("M", "F"), 100, replace = TRUE)
)

# Randomly assign to treatment
population <- population %>%
  mutate(treatment = sample(rep(c("Control", "Treatment"), each = 50)))

# Check balance
population %>%
  group_by(treatment) %>%
  summarise(
    mean_age = mean(age),
    mean_weight = mean(baseline_weight),
    prop_male = mean(sex == "M"),
    .groups = 'drop'
  )

# Should be similar between groups!
```

---

### Wrap-up & Preview (10 minutes)

**Key Takeaways**:
1. Statistics helps us make decisions under uncertainty
2. Frequentist approach: focus on long-run properties
3. P-values are widely misunderstood—they tell us about data, not hypotheses
4. Study design matters: observational vs experimental
5. Randomization is powerful for causal inference
6. Next week: We'll start quantifying data with descriptive statistics

**Questions to Ponder**:
- When you read research papers, can you identify the study design?
- Are the conclusions justified by the design?
- What confounders might be present?

---

## Week 1 Homework Assignment

### Assignment: Study Design Critique & P-value Interpretation

**Part 1: Study Design Analysis (50 points)**

You will be provided with 3 short abstracts from published animal science studies. For each study:

1. Identify whether it is observational or experimental
2. If experimental, describe the randomization procedure
3. List potential confounding variables
4. Assess whether the conclusions about causation are justified
5. Suggest improvements to the study design (if any)

**Part 2: P-value Simulation (30 points)**

Using R and Quarto:

1. Generate two groups of simulated data where the null hypothesis is FALSE (means are actually different: 100 vs 110, n=25 each, SD=15)
2. Run a t-test and report the p-value
3. Repeat this process 100 times (using a loop or `replicate()`)
4. Create a histogram of the p-values
5. Calculate what proportion of p-values are < 0.05
6. Write a brief interpretation: What is this proportion called? What does it depend on?

**Part 3: Reflection (20 points)**

In 200-300 words, reflect on:
- One common p-value misinterpretation that surprised you
- How you will think differently about statistical significance going forward
- A real-world example from your field where confounding might be an issue

**Submission**:
- Render your Quarto document to HTML
- Submit both the `.qmd` and `.html` files

**Grading Rubric**:
- Correct identification and justification (Part 1): 50%
- Code correctness and visualization (Part 2): 30%
- Thoughtfulness of reflection (Part 3): 20%

---

## Additional Resources for Week 1

### Required Reading
- ASA Statement on P-values and Statistical Significance (2016)
- "The Earth Is Round (p < .05)" by Cohen (1994) - sections on p-value interpretation

### Optional Reading
- Ioannidis (2005) "Why Most Published Research Findings Are False"
- Greenland et al. (2016) "Statistical tests, P values, confidence intervals, and power: a guide to misinterpretations"

### R Resources
- R for Data Science (2e): Chapters on data visualization and transformation (review)
- Quarto documentation: https://quarto.org/docs/get-started/hello/rstudio.html

### Videos/Tutorials
- "Dance of the p-values" (YouTube) - visual demonstration of p-value distributions
- StatQuest: "P-values, clearly explained" by Josh Starmer

---

## Notes for Instructor

### Timing Recommendations
- Spend more time on p-values (students struggle most with this)
- Interactive elements: Have students guess if differences are "significant" before revealing p-values
- Use real datasets from animal science journals for discussion

### Common Student Misconceptions to Address
1. "p = 0.05 is the cutoff" (rigid thinking)
2. "Significant means important" (conflating statistical and practical significance)
3. "Randomization means we assign treatments randomly to humans/animals we encounter" (no—we randomly assign within the study participants)
4. "Observational studies are bad" (no—they're necessary when experiments aren't feasible)

### Engagement Strategies
- Poll: "What % of studies do you trust based on p < 0.05 alone?"
- Think-pair-share: Identify confounders in a provided scenario
- Live coding: Simulate p-value distributions together

### Assessment Notes
- Grade homework holistically, not just on correctness
- Look for statistical thinking, not perfect answers
- Provide detailed feedback on p-value interpretation (this is foundational)

---

## Appendix: Sample Quarto Setup for Course

### Recommended YAML Header for Student Assignments
```yaml
---
title: "Week 1 Homework: Study Design & P-values"
author: "Your Name"
date: today
format:
  html:
    toc: true
    toc-depth: 2
    code-fold: false
    theme: cosmo
    embed-resources: true
execute:
  warning: false
  message: false
---
```

### Setup Chunk for Course
```r
# Load packages
library(tidyverse)
library(broom)

# Set theme for all plots
theme_set(theme_minimal())

# Set seed for reproducibility
set.seed(123)
```

---

*End of Week 1 Plan*
