## Sampling Techniques for Machine Learning Models

## Overview
This project applies **five different sampling techniques** to balance an imbalanced credit card dataset and evaluates their impact on **five machine learning models**. The goal is to determine which sampling technique yields the highest accuracy for each model.

## Dataset
The dataset used is the **Credit Card Fraud Detection Dataset**, downloaded from the following GitHub repository:
[Creditcard_data.csv](https://github.com/AnjulaMehto/Sampling_Assignment/blob/main/Creditcard_data.csv)

### Steps Involved:
1. Download and **preprocess** the dataset.
2. **Balance** the dataset using various resampling techniques.
3. Determine **sample sizes** using the formula discussed in class.
4. Generate five samples using the following **techniques**:
   - Simple Random Sampling
   - Stratified Sampling
   - Systematic Sampling
   - Cluster Sampling
   - Bootstrap Sampling
5. Train five machine learning models on the sampled datasets:
   - Logistic Regression
   - Decision Tree
   - Random Forest
   - XGBoost
   - SVM
6. Evaluate accuracy and determine the best sampling technique for each model.

---

## Results

| Sampling Technique  | Logistic Regression | Decision Tree | Random Forest | XGBoost | SVM |
|---------------------|---------------------|---------------|---------------|---------|-----|
| Simple Random      | 0.883117            | 0.922078      | 0.974026      | 0.948052| 0.909091 |
| Stratified        | 0.922078            | 0.961039      | 0.974026      | 0.974026| 0.980519 |
| Systematic        | 0.83871             | 0.903226      | **1.000000**      | 0.903226| 0.83871 |
| Cluster           | **0.978159**        | **1.000000**  | **1.000000**  | **1.000000** | **1.000000** |
| Bootstrap         | 0.918301            | 0.973856      | 0.996732      | 0.993464| 0.98366 |

### Best Sampling Technique for Each Model:
- **Logistic Regression:** Cluster Sampling
- **Decision Tree:** Cluster Sampling
- **Random Forest:** Systematic Sampling
- **XGBoost:** Cluster Sampling
- **SVM:** Cluster Sampling

---

## How to Run the Code
### Prerequisites:
Install the following lobraries:
```bash
pip install numpy pandas scikit-learn xgboost
```

### Steps:
1. Clone the repository:
   ```bash
   git clone <your-github-repo-link>
   cd <repo-folder>
   ```
2. Run the Python script:
   ```bash
   python sampling_assignment.py
   ```
3. View results in the console and generated output files.

---

## Discussion

The results show that **Cluster Sampling** consistently performs well across multiple models. **Random Forest**, however, achieves perfect accuracy with both **Systematic Sampling** and **Cluster Sampling**. These findings suggest that the choice of sampling technique has a significant impact on model performance.

---
## License

This project is released under the MIT License.

---
## Contributors
- Rishika Mathur

For any queries, feel free to open an issue in the repository!

---
