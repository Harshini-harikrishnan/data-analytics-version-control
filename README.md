🧠 Neuro-Behavioral Fatigue and Risk Assessment Framework (NFAM)
An Explainable Mathematical Framework for Cognitive Fatigue, Digital Overload, and Sleep Efficiency Modeling
📘 Overview

The Neuro-Behavioral Fatigue Assessment Model (NFAM) is a computational framework designed to quantify, interpret, and visualize student mental fatigue and cognitive risk through behavioral, digital, and lifestyle indicators.
Unlike traditional psychological assessments, NFAM integrates mathematical modeling, machine learning, and explainable AI (XAI) techniques to provide data-driven insights into fatigue, sleep efficiency, and digital overload patterns.

The system introduces three novel composite behavioral metrics:

🧩 CFI (Cognitive Fatigue Index) – models mental exhaustion from distraction, daytime sleepiness, and screen exposure

💻 DOM (Digital Overload Multiplier) – captures digital and attention-related strain

🌙 SEM (Sleep Efficiency Model) – quantifies restorative potential using behavioral correlates

⚙️ NFAM Composite Index – integrates all three metrics to predict overall cognitive risk levels

🔬 Theoretical Basis
1️⃣ Cognitive Fatigue Index (CFI)
CFI=w1Dr′+w2Sd′+w3Ts′+w4(1−Hs′)+w5Psleep

Where:
Dr′: Normalized distraction rate
Sd′: Daytime sleepiness
Ts′: Screen exposure
Hs′: Study hour consistency
Psleep: Binary sleep penalty (activated if sleep < 7 hours)

Purpose: Captures cognitive fatigue by integrating attention, digital exposure, and sleep deprivation indicators.

2️⃣ Digital Overload Multiplier (DOM)
DOM=Ts′×Sm′Hs′+ε

Where:
Ts′: Screen exposure
Sm′: Social media engagement
Hs′: Study hour consistency
ε: Small constant for normalization

Purpose: Measures the intensity of digital strain relative to productive engagement.

3️⃣ Sleep Efficiency Model (SEM)
SEM=αEr′+β(1−Ts′)+γSd′+δCm′

Where:
Er′: Normalized exercise regularity
Ts′: Screen exposure (inverse)
Sd′: Daytime sleepiness
Cm′: Commute time

Purpose: Estimates sleep quality using behavioral correlates instead of physiological data.

4️⃣ NFAM Composite Risk Model
NFAM=0.40(CFI)+0.35(DOMnorm)+0.25(1−SEMnorm)

Purpose: Aggregates fatigue, digital load, and recovery potential to classify cognitive risk into:

Low Risk
Moderate Risk
High Risk
Critical Risk

🧩 Implementation Flow

Data Loading & Preprocessing
Import raw academic and behavioral dataset (Excel/CSV)
Normalize all variables to [0,1] scale
Handle missing values and derive features
Metric Computation
Calculate CFI, DOM, and SEM using defined formulas
Normalize and standardize composite values
NFAM Composite Formation
Integrate indices using weighted mathematical composition
Behavioral Archetype Clustering
Use K-Means clustering to identify student behavioral groups:
Balanced Achiever
Digitally Overwhelmed
Burnt-Out Striver
Moderate Risk Learner
Predictive Modeling
Apply Random Forest and XGBoost classifiers
Train on CFI, DOM, and SEM to predict risk categories
Evaluate with accuracy, confusion matrices, and CV-scores
Explainable AI Analysis
Use LIME (Local Interpretable Model-agnostic Explanations) and Permutation Importance
Generate human-readable justifications for predicted risk levels
Visualization

CFI Analysis
<img width="1749" height="490" alt="image" src="https://github.com/user-attachments/assets/a9b2abe8-70a5-4db0-9486-57923e48e76e" />

DOM Analysis
<img width="1375" height="989" alt="image" src="https://github.com/user-attachments/assets/b69aa60e-30e2-4b74-971a-8e9ad4a91187" />

SEM Analysis
<img width="1389" height="989" alt="image" src="https://github.com/user-attachments/assets/40146a42-7c87-43cb-9016-a9133d0848db" />

NFAM Composite Distribution
<img width="1300" height="1119" alt="image" src="https://github.com/user-attachments/assets/d021175e-b9d4-44ae-883c-49fd43a65983" />

Behavioral Archetype Visualization
<img width="1354" height="1120" alt="image" src="https://github.com/user-attachments/assets/f26fc0e1-d73f-47e7-bbc3-ee7d1ee9d1dd" />

Predictive Model Comparison
<img width="1390" height="989" alt="image" src="https://github.com/user-attachments/assets/a99def0e-5135-4430-aa0e-e24017627d81" />

Comprehensive Summary Dashboard
<img width="1458" height="1120" alt="image" src="https://github.com/user-attachments/assets/3d7aa28c-57bf-4c7d-a1b5-c0482819ee9c" />


📊 Outputs

All visualizations are auto-saved in the working directory:

File Name	Description
cfi_analysis.png	Cognitive Fatigue Index distribution and categories
dom_analysis.png	Digital overload metrics and correlations
sem_analysis.png	Sleep efficiency modeling and regression plots
nfam_composite_analysis.png	Composite index and risk distribution
behavioral_archetypes.png	K-means clustering of behavioral groups
predictive_model_analysis.png	Random Forest & XGBoost performance comparison
nfam_comprehensive_summary.png	Complete visual dashboard summary
