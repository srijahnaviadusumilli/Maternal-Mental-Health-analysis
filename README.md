# Maternal Mental Health During COVID-19: EPDS Assessment Analysis
This repository contains materials for the project "Maternal Mental Health During COVID-19: EPDS Assessment Analysis", which investigates the relationship between demographic and obstetric factors and maternal mental health during the COVID-19 pandemic. Using standard machine learning models and statistical analysis, the project identifies key predictors of depression risk in pregnant women and develops tools for early intervention.
This study investigates the relationship between demographic and obstetric factors and maternal mental health during the COVID-19 pandemic.

## Project Overview

- **Objective**:  Analyze the impact of demographic and obstetric factors on maternal mental health during COVID-19, using EPDS scores to assess depression severity and develop predictive models for clinical screening.

- **Data Source**: Pregnancy During the COVID-19 Pandemic (PdP) Study - Canadian cohort data collected from April 2020 to April 2021 (https://www.kaggle.com/datasets/yeganehbavafa/mental-health-in-the-pregnancy-during-the-covid-19).

- **Sample Size**: 10,772 pregnant women from Canada.

- **Approach**:
Comprehensive exploratory data analysis with advanced visualization techniques.
Statistical analysis using non-parametric methods (Chi-square, Mann-Whitney U tests).
Machine learning implementation with XGBoost, Random Forest, Logistic Regression, and K-Nearest Neighbors.
SMOTE technique applied to address class imbalance in depression severity categories.

## Key Findings
- **Depression Prevalence**
72.2% of pregnant women experienced some degree of depression symptoms during the pandemic
27.4% reported moderate-to-severe symptoms (substantially higher than pre-pandemic rates of 10-15%)
Distribution: Mild depression (44.8%), None/minimal (27.7%), Moderate (21.8%), Severe (5.6%)

- **Machine Learning Performance**
XGBoost: Achieved highest accuracy (89.46%) for multi-class depression prediction
Random Forest: Exceptional performance for severe depression detection (AUC = 0.99)
Cross-validation: 5-fold validation ensured robust model evaluation

## Files in the Repository

- **maternal-mental-health-analysis.ipynb-**: Jupyter Notebook containing complete analysis pipeline including data preprocessing, statistical tests, and machine learning models.
- **maternal-mental-health-report.pdf-**: Comprehensive research report with methodology, results, and clinical implications.
- **maternal-mental-health-presentation.pptx-**: Slide deck summarizing key findings, methodology, and clinical relevance.

## Methodology

- **Data Collection & Preprocessing**
  - Eligibility Criteria: Age ≥18 years, pregnancy ≤35 weeks gestation, Canadian residence, English/French proficiency  
  - Variable Selection: 7 clinically relevant variables based on perinatal depression literature  
  - Data Quality: Complete case analysis, outlier detection using IQR method, categorical encoding for income and education levels  
  - Missing Data Handling: Robust statistical methods maintaining data integrity  

- **Statistical Analysis Framework**
  - Distribution Assessment: Shapiro-Wilk tests revealed non-normal distributions, leading to non-parametric approach  
  - Correlation Analysis: Multicollinearity assessment identified strong correlation (r=0.74) between threat perception variables  

- **Inferential Statistics**
  - Chi-square tests for categorical associations (income/education with EPDS categories)  
  - Mann-Whitney U tests for continuous variable relationships  
  - Monte Carlo simulation for enhanced statistical power  

- **Machine Learning Pipeline**
  - Feature Engineering: RobustScaler standardization, stratified train-test split (80%/20%)  
  - Class Imbalance: SMOTE implementation creating balanced training data (13,716 samples total)  
  - Model Evaluation: 5-fold cross-validation, accuracy metrics, AUC-ROC analysis  
  - Performance Metrics: Sensitivity (84-97%), Precision (81-96%), F1-scores (82-97%) for XGBoost  

- **Clinical Validation**
  - EPDS Categorization: Validated thresholds - None/minimal (0-6), Mild (7-13), Moderate (14-19), Severe (20-30)  
  - Risk Stratification: Models effectively rank depression severity for clinical screening priorities  
  - Feature Importance: Random Forest analysis quantified relative predictor contributions  

- **Key Statistical Results - Demographic Associations**
  - Age: Mean 32.4 years (SD=4.7), significant association with depression severity (p<0.001)  
  - Income: Higher income protective - >$150K group: 42.3% no/minimal depression vs. <$40K group: 15.6%  
  - Education: Significant protective effect of higher education (χ²=152.73, p<0.001)  

- **Psychological Measures**
  - Anxiety Scores: Strong correlation with EPDS (Spearman's ρ=0.63), mean=19.3 (SD=6.2)  
  - Threat Perception: Multimodal distribution in COVID-19 concerns, mean danger score=51.8 (SD=24.6)  


- **Model Performance Comparison**

  | Model           | Accuracy | Severe Depression AUC |
  |-----------------|----------|------------------------|
  | XGBoost         | 89.46%   | 0.98                   |
  | Random Forest   | 77.62%   | 0.99                   |
  | K-Nearest Neighbors | 65.59%   | 0.98                   |

## Clinical Applications

  - Real-time telehealth screening with six-variable model  
  - Enables early intervention and targeted support    
  - Informs evidence-based policy development for maternal mental healthcare  
  - Quick pre-visit risk assessments with minimal training  
  - Seamless integration with existing infrastructure  
  - Real-time stratification for timely identification of high-risk cases

## Limitations

- **Cross-sectional Design**: Cannot establish causal relationships between risk factors and depression
- **Geographic Restriction**: Canadian sample limits generalizability to other cultural contexts
- **Self-reported Measures**: Potential response bias in mental health assessments
- **Variable Selection**: Focused analysis may have overlooked other relevant factors (pre-existing conditions, pregnancy complications)
- **Sampling Bias**: Digital recruitment may underrepresent individuals with limited technology access

## Future Research Directions
Future research should focus on tracking mental health from pregnancy through postpartum, testing targeted interventions for high-risk groups, and expanding predictive models with biological, genetic, and psychosocial factors. Comparing results across cultures and healthcare systems will improve generalizability, while assessing model accuracy will ensure reliable predictions. Importantly, implementation studies are needed to integrate these models into routine care, especially through telehealth, where our six-variable model can provide quick, low-burden risk screening to support timely mental health care.

## International Relevance
Despite being conducted in Canada, findings show consistency with international research:

- **Iran**: Similar age-anxiety associations and education-social dysfunction links (Sayahi et al., 2023)
- **California**: Comparable depression rates (22% vs. our 21.8% moderate range) (Phipps et al., 2023)
- **Europe**: Aligned depression prevalence during pandemic waves (Tauqeer et al., 2023)

## Contributors

- **Jamesetta Quiqui**
- **Nigama Pervala**
- **Saptashi Purkayastha**
- **Shruti Chaitanya**
- **Sri Jahnavi Adusumilli**

## Contact

For questions or suggestions, please contact:  
Sri Jahnavi Adusumilli - [srijadus@iu.edu](mailto:srijadus@iu.edu)
