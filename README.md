# Predicting COVID-19 Severity using Bayesian Networks in WiseR

This project was developed as part of the **NTU Winter Immersion Programme 2024** under the guidance of faculty at **Nanyang Technological University (NTU), Singapore**. As part of the group assignment, we were permitted to reproduce and personalize existing open-source repositories to explore a healthcare-focused machine learning problem.

## Objective
The goal of this project is to utilize **Bayesian Networks** via the [WiseR](https://arxiv.org/abs/2108.07046) tool to model and predict the severity of COVID-19 in patients. Specifically, we studied the relationship between various biomarkers and severe disease outcomes, with a focus on **S100A12**, a key inflammatory marker.

## Problem Statement
We aimed to validate research suggesting that biomarkers such as **S100A12** correlate with high COVID-19 severity. Our task included reproducing, modifying, and interpreting code to support this hypothesis using a provided dataset.

## Dataset
We used `data.csv` (shared as part of the assignment), which includes:
- Demographics
- Clinical variables
- Protein and metabolome features

Preprocessing involved:
- Dimensionality reduction using PCA
- Discretization of variables for compatibility with Bayesian modeling

## Methodology
- **Structure Learning**: Hill Climbing algorithm with AIC scoring
- **Parameter Estimation**: Bayesian estimation with imaginary sample size
- **Blacklist Rules**: To prevent biologically implausible edges
- **Inference**: S100A12 set as evidence to evaluate impact on COVID-19 severity (WHO Ordinal Scale)

## Modifications Made
- Customized the structure learning configuration for better model performance
- Tuned parameters to improve robustness under sparse data
- Performed detailed inference across different ranges of S100A12 levels

## Results
- High S100A12 levels were strongly associated with severe COVID-19 cases
- Bayesian inference clearly differentiated mild, moderate, and severe outcome probabilities
- The modified model provided a more interpretable and data-efficient structure than the baseline

## Presentation & Demo
Final deliverables included a detailed presentation and demo, covering:
- Topic selection and medical relevance
- Network structure and key associations
- Modifications and inference insights
- Future scope: adding biomarkers and external validation

##  References
- Gallo Marin et al. (2021), “Predictors of COVID-19 severity: A literature review”
- Maheshwari et al. (2021), “WiseR: An end-to-end structure learning and deployment framework for causal graphical models”


---

**Disclaimer**: This repository is released for educational purposes and to document the project conducted during the NTU Winter Programme 2024. Reuse and further experimentation are encouraged with credit.
