# Sampling Strategies for Imbalanced Credit Card Fraud Detection

**Course:** UCS654 – Predictive Analytics using Statistics  
**Assignment:** Assignment 2 (Sampling Techniques)  
**Author:** Sartaj Singh Virdi  
**Roll Number:** 102303259

## Project Overview

Real-world datasets—especially in domains like credit card fraud detection—are often highly imbalanced. This project investigates how different statistical sampling techniques influence the performance of multiple machine learning classification models when applied to an imbalanced credit card transaction dataset.

### Objectives:
- Handle severe class imbalance effectively
- Apply and compare multiple sampling strategies
- Evaluate model performance across sampling methods
- Identify robust model–sampling combinations

## Class Imbalance Handling

Before applying any sampling techniques, the dataset was first balanced using **Random Over Sampling**.

### Why Random Over Sampling?
- Fraudulent transactions (minority class) were extremely under-represented
- Random under-sampling caused significant loss of majority-class information
- Over-sampling preserved all original legitimate transactions
- Balanced classes improved training stability and fairness

After over-sampling, both classes had equal representation, making the dataset suitable for systematic experimentation.

## Sampling Techniques Evaluated

After balancing, the following five sampling techniques were implemented:

1. Simple Random Sampling
2. Systematic Sampling
3. Stratified Sampling
4. Cluster Sampling
5. Bootstrap Sampling

Each technique was used to generate training subsets for model evaluation.

## Machine Learning Models Used

Five classification algorithms were evaluated under each sampling strategy:

| Code | Model |
|------|-------|
| M1 | Gaussian Naive Bayes |
| M2 | Decision Tree Classifier |
| M3 | Random Forest Classifier |
| M4 | K-Nearest Neighbors (KNN) |
| M5 | Support Vector Classifier (SVC) |

## Experimental Results

### Accuracy Comparison (%)

| Sampling Technique | Naive Bayes | Decision Tree | Random Forest | KNN | SVC |
|-------------------|-------------|---------------|---------------|-----|-----|
| Simple Random | 77.26 | 99.38 | 100.00 | 97.51 | 97.82 |
| Systematic | 80.79 | 98.25 | 100.00 | 96.51 | 96.94 |
| Stratified | 79.75 | 97.82 | 100.00 | 95.64 | 97.51 |
| Cluster | 100.00 | 99.07 | 100.00 | 92.52 | 97.20 |
| Bootstrap | 85.81 | 99.56 | 100.00 | 98.69 | 98.69 |

## Performance Insights

### Best Sampling Technique per Model

- **Gaussian Naive Bayes:** Cluster Sampling
- **Decision Tree:** Simple Random Sampling / Bootstrap Sampling
- **Random Forest:** All Sampling Techniques (consistent performance)
- **KNN:** Bootstrap Sampling
- **SVC:** Bootstrap Sampling

### Overall Findings

- **Best Overall Sampling Technique:** Cluster Sampling
- **Best Overall Model:** Random Forest
  - Achieved perfect accuracy across all sampling strategies

## Key Takeaways

- Class imbalance has a strong impact on predictive performance
- Random Over Sampling effectively mitigates imbalance without data loss
- Different models respond differently to sampling strategies
- Random Forest proves to be the most robust and reliable classifier

## Conclusion

This study highlights the importance of combining class balancing, appropriate sampling techniques, and robust classifiers when working with imbalanced datasets. While extremely high accuracies—especially under Cluster and Bootstrap sampling—are encouraging, they should be validated carefully to avoid overfitting. Overall, the results demonstrate that thoughtful data preparation plays a critical role in successful fraud detection systems.
