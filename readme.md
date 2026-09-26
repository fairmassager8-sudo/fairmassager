# FairMassager: Artifact and Supplementary Material

This repository contains the implementation and supplementary artifacts for **FairMassager**.

## Source Code

The complete implementation of **FairMassager** is available at:

**Google Drive:**  
https://drive.google.com/drive/folders/18dfoTHx-2fT7ZDmwySMtLVl-rX5wMC7l?usp=sharing

---

## Ablation Study Results
To examine the individual contribution of each stage of FairMassager, we conduct an ablation study by separately evaluating the situation-testing and label-mitigation stages. The results indicate that both stages contribute to improving fairness, while their combination provides the overall benefit of FairMassager.
https://docs.google.com/spreadsheets/d/1v24kDxrBTopvubpnzQHXbEVgTFhP9kSpc2uGaiXuZ2w/edit?gid=830016659#gid=830016659 



## Supplementary results of FairMassager are available at:

**Google Drive:**  
https://drive.google.com/drive/folders/18dfoTHx-2fT7ZDmwySMtLVl-rX5wMC7l?usp=sharing


# Table 1. Overview of the Datasets Used in This Study

| Dataset | Description | Protected Attribute(s) | Size | # Features |
|----------|-------------|------------------------|-----:|-----------:|
| Adult [1] | U.S. 1994 Census dataset used for predicting individual income. | Sex, Race | 48,842 | 8 |
| COMPAS [2] | Defendants' criminal records used to predict the likelihood of future offenses. | Sex, Race | 7,214 | 6 |
| German [3] | Personal details utilized to assess whether a person qualifies for good or bad credit. | Sex | 1,000 | 7 |
| Heart [4] | Medical records from the Cleveland Database used to predict the likelihood of heart disease. | Age | 297 | 14 |
| Student [5] | Student academic records used to predict the likelihood of achieving high grades. | Sex | 1,044 | 25 |
| Default [7] | Financial records of Taiwanese customers used to predict the risk of payment default. | Sex | 30,000 | 24 |
| MEPS15 [8] | Survey records from a 2015 U.S. study collecting information about households and associated healthcare providers. | Race | 15,830 | 139 |
| MEPS16 [8] | Survey records from a 2016 U.S. study collecting information about households and associated healthcare providers. | Race | 15,675 | 139 |

---

# Table 2. Fairness and Performance Metrics Used in This Study

**Note:**  
- **FPR = FP / (TN + FP)**
- **TPR = TP / (TP + FN)**

| Fairness Metric | Definition | Ideal Value | Performance Metric | Definition | Ideal Value |
|-----------------|------------|------------:|--------------------|------------|------------:|
| **Average Odds Difference (AOD)** | Average disparity in TPR and FPR between unprivileged (U) and privileged (P) groups.<br><br>**AOD = ½[(TPR<sub>U</sub> − TPR<sub>P</sub>) + (FPR<sub>U</sub> − FPR<sub>P</sub>)]** | 0 | **Recall** | TP / (TP + FN) | 1 |
| **Equal Opportunity Difference (EOD)** | Difference in TPR between unprivileged and privileged groups.<br><br>**EOD = TPR<sub>U</sub> − TPR<sub>P</sub>** | 0 | **Accuracy** | (TP + TN) / (TP + TN + FP + FN) | 1 |
| **Statistical Parity Difference (SPD)** | Difference in probability of favorable outcome between groups.<br><br>**SPD = P(Ŷ = 1 \| a = 0) − P(Ŷ = 1 \| a = 1)** | 0 | **Precision** | TP / (TP + FP) | 1 |

---

# References

**[1]** UCI Adult Dataset (1994)  
http://mlr.cs.umass.edu/ml/datasets/Adult

**[2]** COMPAS Analysis (ProPublica) (2015)  
https://github.com/propublica/compas-analysis

**[3]** UCI Statlog (German Credit Data) (2000)  
https://archive.ics.uci.edu/ml/datasets/Statlog+(German+Credit+Data)

**[4]** UCI Heart Disease Dataset (2001)  
https://archive.ics.uci.edu/ml/datasets/Heart+Disease

**[5]** UCI Student Performance Dataset (2014)  
https://archive.ics.uci.edu/ml/datasets/Student+Performance

**[6]** Bank Marketing (UCI / Kaggle) (2017)  
https://www.kaggle.com/c/bank-marketing-uci

**[7]** UCI Default of Credit Card Clients Dataset (2016)  
https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients

**[8]** Medical Expenditure Panel Survey (MEPS) (2015–2016)  
https://meps.ahrq.gov/mepsweb/
