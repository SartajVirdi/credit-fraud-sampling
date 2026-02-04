# Statistical Sampling Approaches for Addressing Class Imbalance in Fraud Detection Systems

**Subject:** UCS654 – Predictive Analytics using Statistics  
**Task:** Assignment 2 (Sampling Techniques)  
**Student:** Sartaj Singh Virdi  
**Registration ID:** 102303259

---

## Introduction

Financial transaction datasets, particularly those involving fraudulent activities, frequently exhibit significant class distribution disparities. This research examines how various statistical sampling methodologies affect the efficacy of different machine learning algorithms when processing an imbalanced credit card transaction dataset.

### Research Goals:

- Address extreme class distribution disparities effectively
- Implement and analyze multiple sampling methodologies
- Assess classifier performance under different sampling conditions
- Determine optimal model-sampling strategy pairings

---

## Addressing Class Distribution Imbalance

Prior to implementing sampling strategies, the dataset underwent balancing through **Random Over Sampling**.

### Rationale for Random Over Sampling:

- Fraudulent cases (minority class) exhibited severe under-representation
- Random under-sampling resulted in substantial loss of majority-class patterns
- Over-sampling retained all authentic transaction records
- Balanced distribution enhanced model training consistency

Following the over-sampling process, equal representation was achieved for both classes, establishing a foundation for controlled experimentation.

---

## Sampling Methodologies Investigated

Post-balancing, five distinct sampling approaches were applied:

1. Simple Random Sampling
2. Systematic Sampling
3. Stratified Sampling
4. Cluster Sampling
5. Bootstrap Sampling

Each methodology generated training subsets for comprehensive model assessment.

---

## Classification Algorithms Employed

Five distinct classification approaches were tested under each sampling methodology:

| Identifier | Algorithm |
|------------|-----------|
| M1 | Gaussian Naive Bayes |
| M2 | Decision Tree Classifier |
| M3 | Random Forest Classifier |
| M4 | K-Nearest Neighbors (KNN) |
| M5 | Support Vector Classifier (SVC) |

---

## Empirical Findings

### Classification Accuracy Results (%)

| Sampling Methodology | Naive Bayes | Decision Tree | Random Forest | KNN | SVC |
|---------------------|-------------|---------------|---------------|-----|-----|
| Simple Random | 77.26 | 99.38 | 100.00 | 97.51 | 97.82 |
| Systematic | 80.79 | 98.25 | 100.00 | 96.51 | 96.94 |
| Stratified | 79.75 | 97.82 | 100.00 | 95.64 | 97.51 |
| Cluster | 100.00 | 99.07 | 100.00 | 92.52 | 97.20 |
| Bootstrap | 85.81 | 99.56 | 100.00 | 98.69 | 98.69 |

---

## Analysis of Results

### Optimal Sampling Strategy by Algorithm

- **Gaussian Naive Bayes:** Cluster Sampling
- **Decision Tree:** Simple Random Sampling / Bootstrap Sampling
- **Random Forest:** All Sampling Methodologies (uniform excellence)
- **KNN:** Bootstrap Sampling
- **SVC:** Bootstrap Sampling

### Summary of Observations

- **Most Effective Sampling Approach:** Cluster Sampling
- **Superior Performing Algorithm:** Random Forest
  - Demonstrated perfect classification accuracy regardless of sampling technique

---

## Principal Observations

- Class imbalance significantly influences predictive model effectiveness
- Random Over Sampling successfully addresses imbalance while preserving information integrity
- Algorithm performance varies substantially across sampling methodologies
- Random Forest demonstrates superior consistency and resilience across conditions

---

## Final Remarks

This investigation underscores the critical importance of integrating class balancing techniques, strategic sampling methodologies, and resilient classification algorithms when analyzing imbalanced datasets. While the exceptionally high accuracy rates—particularly under Cluster and Bootstrap sampling—appear promising, rigorous validation remains essential to prevent overfitting concerns. The findings clearly illustrate that meticulous data preprocessing constitutes a fundamental component of effective fraud detection implementations.
