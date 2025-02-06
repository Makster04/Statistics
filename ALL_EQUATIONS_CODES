# Hypothesis Testing Symbols and Terminology Explained

This document explains the key symbols and terms used in hypothesis testing along with their definitions, equations, and Python implementations where applicable.

---

## Table of Contents
1. [Hypothesis Testing Basics](#hypothesis-testing-basics)
2. [Symbols and Their Meanings](#symbols-and-their-meanings)
3. [Types of Hypothesis Tests](#types-of-hypothesis-tests)
4. [Python Examples](#python-examples)

---

## Hypothesis Testing Basics
Hypothesis testing is a statistical method used to determine whether there is enough evidence in a sample of data to infer that a certain condition is true for the entire population.

### Key Concepts:
- **Null Hypothesis (H₀)**: The default assumption or claim.
- **Alternative Hypothesis (H₁ or Ha)**: The claim we want to test.
- **Significance Level (α)**: The probability of rejecting the null hypothesis when it is true.
- **p-value**: The probability of obtaining test results at least as extreme as the observed results, assuming the null hypothesis is true.

---

## Symbols and Their Meanings

| Symbol          | Meaning                               | Equation / Explanation                                  |
|----------------|---------------------------------------|--------------------------------------------------------|
| **H₀**         | Null Hypothesis                      | The hypothesis we aim to test (e.g., \( \mu = 100 \))  |
| **H₁ or Ha**   | Alternative Hypothesis               | The opposite of the null hypothesis                    |
| **α (alpha)**  | Significance Level                   | Common values: 0.05, 0.01                              |
| **p-value**    | Probability Value                    | The smaller the p-value, the stronger the evidence     |
| **t**          | t-statistic                          | Used in t-tests                                        |
| **χ²**         | Chi-square statistic                 | Used in chi-square tests                               |
| **F**          | F-statistic                          | Used in ANOVA                                          |
| **Z**          | Z-score                              | Used in Z-tests                                        |
| **n**          | Sample Size                          | Number of observations in the sample                   |
| **s**          | Sample Standard Deviation            | Measures the dispersion of the sample                  |

---

## Types of Hypothesis Tests

### 1. **Z-Test**
Used when the sample size is large (\( n > 30 \)) and the population standard deviation is known.

### 2. **t-Test**
Used when the sample size is small (\( n \leq 30 \)) or the population standard deviation is unknown.
- **One-Sample t-Test**: Tests if the sample mean differs from a known population mean.
- **Two-Sample t-Test**: Compares the means of two independent samples.

### 3. **Chi-Square Test**
Used for categorical data to test the independence between two variables.

### 4. **ANOVA (Analysis of Variance)**
Used to compare the means of three or more groups.

---

## Python Examples
### 1. **One-Sample t-Test**
```python
import numpy as np
from scipy import stats

# Generate sample data
data = np.random.normal(100, 10, 30)
population_mean = 100

# Perform one-sample t-test
t_stat, p_value = stats.ttest_1samp(data, population_mean)
print(f"t-statistic: {t_stat:.2f}, p-value: {p_value:.4f}")
```

### 2. **Two-Sample t-Test**
```python
# Generate data for two groups
group1 = np.random.normal(100, 15, 30)
group2 = np.random.normal(105, 15, 30)

# Perform two-sample t-test
t_stat, p_value = stats.ttest_ind(group1, group2)
print(f"t-statistic: {t_stat:.2f}, p-value: {p_value:.4f}")
```

### 3. **Chi-Square Test**
```python
observed = np.array([[10, 20, 30], [6, 9, 17]])
chi2, p_value, dof, expected = stats.chi2_contingency(observed)
print(f"Chi-square statistic: {chi2:.2f}, p-value: {p_value:.4f}")
```

---

## Conclusion
This document provides a detailed explanation of the symbols and terms in hypothesis testing along with Python examples. By understanding these key concepts and symbols, you can perform various statistical tests and interpret the results effectively.

# Hypothesis Testing Guide with Python Visualizations

This guide explains the key symbols, terms, and types of hypothesis tests along with Python examples using libraries such as `numpy`, `scipy`, `matplotlib`, and `seaborn`. Each test is accompanied by a code example and a visualization.

---

## Table of Contents
1. [One-Sample t-test](#one-sample-t-test)
2. [Two-Sample t-test](#two-sample-t-test)
3. [Chi-Square Test](#chi-square-test-for-independence)
4. [ANOVA (Analysis of Variance)](#anova-analysis-of-variance)
5. [Confidence Interval](#confidence-interval)

---

## One-Sample t-test
Used to determine if the mean of a sample differs significantly from a known population mean.

### **Equation**
The test statistic is calculated as:
\[
t = \frac{\bar{x} - \mu}{\frac{s}{\sqrt{n}}} \text{, where:}
\]
- \( \bar{x} \) = sample mean
- \( \mu \) = population mean
- \( s \) = sample standard deviation
- \( n \) = sample size

### **Python Code with Visualization**:
```python
import numpy as np
import matplotlib.pyplot as plt
from scipy import stats

# Generate sample data
data = np.random.normal(102, 10, 100)
population_mean = 100

# Perform t-test
t_stat, p_value = stats.ttest_1samp(data, population_mean)

# Plot
plt.figure(figsize=(10, 6))
plt.hist(data, bins=20, alpha=0.7, label='Sample Data')
plt.axvline(np.mean(data), color='red', linestyle='--', label=f'Sample Mean: {np.mean(data):.2f}')
plt.axvline(population_mean, color='blue', linestyle='-', label=f'Population Mean: {population_mean}')
plt.title('One-Sample t-test Visualization')
plt.xlabel('Value')
plt.ylabel('Frequency')
plt.legend()
plt.show()
```

---

## Two-Sample t-test
Used to compare the means of two independent samples.

### **Equation**
The test statistic is calculated as:
\[
t = \frac{\bar{x}_1 - \bar{x}_2}{\sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}}
\]
- \( \bar{x}_1, \bar{x}_2 \) = sample means
- \( s_1, s_2 \) = sample standard deviations
- \( n_1, n_2 \) = sample sizes

### **Python Code with Visualization**:
```python
# Generate data for two groups
group1 = np.random.normal(100, 15, 50)
group2 = np.random.normal(105, 15, 50)

# Perform two-sample t-test
t_stat, p_value = stats.ttest_ind(group1, group2)

# Plot
plt.figure(figsize=(12, 6))
plt.hist(group1, bins=20, alpha=0.7, label='Group 1')
plt.hist(group2, bins=20, alpha=0.7, label='Group 2')
plt.axvline(np.mean(group1), color='red', linestyle='--', label=f'Group 1 Mean: {np.mean(group1):.2f}')
plt.axvline(np.mean(group2), color='blue', linestyle='--', label=f'Group 2 Mean: {np.mean(group2):.2f}')
plt.title('Two-Sample t-test Visualization')
plt.xlabel('Value')
plt.ylabel('Frequency')
plt.legend()
plt.show()
```

---

## Chi-Square Test for Independence
Used to test the independence between two categorical variables.

### **Equation**
\[
\chi^2 = \sum \frac{(O - E)^2}{E}
\]
- \( O \) = observed frequency
- \( E \) = expected frequency

### **Python Code with Visualization**:
```python
import seaborn as sns

# Observed data (contingency table)
observed = np.array([[10, 20, 30], [6, 9, 17]])
chi2, p_value, dof, expected = stats.chi2_contingency(observed)

# Plot observed and expected frequencies
fig, ax = plt.subplots(1, 2, figsize=(12, 6))
sns.heatmap(observed, annot=True, fmt="d", ax=ax[0], cmap="Blues")
ax[0].set_title("Observed Frequencies")
sns.heatmap(expected, annot=True, fmt=".2f", ax=ax[1], cmap="Reds")
ax[1].set_title("Expected Frequencies")
plt.show()
```

---

## ANOVA (Analysis of Variance)
Used to compare the means of three or more groups.

### **Equation**
The F-statistic is calculated as:
\[
F = \frac{\text{Between-group variance}}{\text{Within-group variance}}
\]

### **Python Code with Visualization**:
```python
# Generate data for three groups
group1 = np.random.normal(100, 15, 30)
group2 = np.random.normal(105, 15, 30)
group3 = np.random.normal(110, 15, 30)

# Perform one-way ANOVA
f_stat, p_value = stats.f_oneway(group1, group2, group3)

# Plot
plt.figure(figsize=(12, 6))
sns.boxplot(data=[group1, group2, group3], palette="Set2")
plt.xticks([0, 1, 2], ['Group 1', 'Group 2', 'Group 3'])
plt.title('ANOVA: Group Comparison')
plt.ylabel('Value')
plt.show()
```

---

## Confidence Interval
Used to estimate the range of values that contains the population parameter with a certain level of confidence.

### **Equation**
\[
CI = \bar{x} \pm Z \left( \frac{s}{\sqrt{n}} \right)
\]
- \( \bar{x} \) = sample mean
- \( Z \) = Z-score for the confidence level
- \( s \) = sample standard deviation
- \( n \) = sample size

### **Python Code with Visualization**:
```python
mean = np.mean(data)
std_err = stats.sem(data)
conf_interval = stats.t.interval(0.95, len(data)-1, loc=mean, scale=std_err)

# Plot
plt.figure(figsize=(10, 6))
plt.hist(data, bins=20, alpha=0.7, label='Sample Data')
plt.axvline(conf_interval[0], color='green', linestyle='--', label=f'95% CI Lower: {conf_interval[0]:.2f}')
plt.axvline(conf_interval[1], color='green', linestyle='--', label=f'95% CI Upper: {conf_interval[1]:.2f}')
plt.axvline(mean, color='red', linestyle='-', label=f'Sample Mean: {mean:.2f}')
plt.title('Confidence Interval Visualization')
plt.xlabel('Value')
plt.ylabel('Frequency')
plt.legend()
plt.show()
```

---

## Conclusion
This guide provides an overview of common hypothesis tests with Python implementations and visualizations. You can modify and extend these examples to fit your own data and analysis needs.

# Z-Test and t-Test Guide

This document provides an overview of Z-tests and t-tests, including their purposes, assumptions, formulas, and Python implementations.

---

## Table of Contents
1. [Overview](#overview)
2. [Z-Test](#z-test)
    - [When to Use](#when-to-use-z-test)
    - [Formula](#z-test-formula)
    - [Python Implementation](#z-test-python-implementation)
3. [t-Test](#t-test)
    - [When to Use](#when-to-use-t-test)
    - [Types of t-Tests](#types-of-t-tests)
    - [Python Implementation](#t-test-python-implementation)
4. [Comparison of Z-Test and t-Test](#comparison-of-z-test-and-t-test)

---

## Overview
Z-tests and t-tests are used in hypothesis testing to determine whether there is a significant difference between means or proportions.

| Test  | Purpose                                  | Sample Size | Population SD Known? |
|-------|------------------------------------------|-------------|---------------------|
| Z-Test | Compare sample mean to population mean   | Large (n > 30) | Yes                  |
| t-Test | Compare means between groups or samples | Small (n ≤ 30) | No                   |

---

## Z-Test

### When to Use Z-Test
- Sample size is large (n > 30)
- Population standard deviation (σ) is known

### Z-Test Formula
\[
Z = \frac{\bar{X} - \mu}{\frac{\sigma}{\sqrt{n}}}
\]
Where:
- \( \bar{X} \): Sample mean
- \( \mu \): Population mean
- \( \sigma \): Population standard deviation
- \( n \): Sample size

### Z-Test Python Implementation
```python
import numpy as np
from scipy import stats

# Sample data
sample_data = np.random.normal(100, 15, 50)  # mean=100, std=15, n=50
population_mean = 100
population_std = 15
n = len(sample_data)

# Z-test calculation
z_stat = (np.mean(sample_data) - population_mean) / (population_std / np.sqrt(n))
p_value = 2 * (1 - stats.norm.cdf(abs(z_stat)))

print(f"Z-statistic: {z_stat:.2f}, p-value: {p_value:.4f}")
```

---

## t-Test

### When to Use t-Test
- Sample size is small (n ≤ 30)
- Population standard deviation is unknown

### Types of t-Tests
1. **One-Sample t-Test**: Tests if the sample mean differs from a known population mean.
2. **Two-Sample t-Test**: Compares the means of two independent samples.
3. **Paired t-Test**: Compares means from the same group at different times.

### t-Test Formula (One-Sample)
\[
t = \frac{\bar{X} - \mu}{\frac{s}{\sqrt{n}}}
\]
Where:
- \( \bar{X} \): Sample mean
- \( \mu \): Population mean
- \( s \): Sample standard deviation
- \( n \): Sample size

### t-Test Python Implementation
#### One-Sample t-Test
```python
import numpy as np
from scipy import stats

# Sample data
data = np.random.normal(100, 10, 25)
population_mean = 100

# Perform one-sample t-test
t_stat, p_value = stats.ttest_1samp(data, population_mean)
print(f"t-statistic: {t_stat:.2f}, p-value: {p_value:.4f}")
```

#### Two-Sample t-Test
```python
# Generate data for two groups
group1 = np.random.normal(100, 12, 30)
group2 = np.random.normal(105, 12, 30)

# Perform two-sample t-test
t_stat, p_value = stats.ttest_ind(group1, group2)
print(f"t-statistic: {t_stat:.2f}, p-value: {p_value:.4f}")
```

---

## Comparison of Z-Test and t-Test

| Feature       | Z-Test                            | t-Test                       |
|---------------|-----------------------------------|------------------------------|
| Sample Size   | Large (n > 30)                   | Small (n ≤ 30)               |
| Population SD | Known                            | Unknown                      |
| Distribution  | Normal                           | t-distribution (approaches normal as n increases) |

---

## Conclusion
Z-tests and t-tests are essential tools for hypothesis testing. The choice between them depends on sample size and whether the population standard deviation is known. This guide provides formulas and Python examples to help implement these tests in practice.


