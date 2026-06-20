Parkinson's Disease Prediction using Biomedical Voice Features
📌 Project Objective
The goal of this project is to develop a high-precision machine learning model to predict whether a person has Parkinson’s disease based on non-invasive health metrics and vocal features. Approximately 90% of people with Parkinson's disease exhibit vocal impairments (dysarthria) in the early stages. By training classification algorithms on biomedical voice measurements, this project offers an automated screening approach with high diagnostic sensitivity.
🛠️ Tech Stack & Environment
Environment: Python (Jupyter Notebook)
Data Manipulation: Pandas, NumPy
Data Visualization: Matplotlib, Seaborn
Machine Learning: Scikit-Learn (Support Vector Machine, Random Forest, Logistic Regression, StandardScaler, train_test_split, Classification Metrics), XGBoost, Imbalanced-Learn (SMOTE)
📊 Dataset
The project utilizes biomedical voice measurements from patients (parkinsons.csv), encompassing various acoustic risk features:  
Frequencies: MDVP:Fo(Hz), MDVP:Fhi(Hz), MDVP:Flo(Hz) (Average, high, and low fundamental vocal frequencies)   
Acoustic Variations: Jitter (frequency absolute/percentage shifts) and Shimmer (amplitude/loudness variations)   
Noise Ratios & Non-linear Metrics: NHR, HNR (Noise-to-harmonic ratios), RPDE, DFA, spread1, spread2, D2, PPE (Complex non-linear vocal dynamics)   
Target: status (1 = Parkinson's Disease, 0 = Healthy) 
⚙️ MethodologyData Preprocessing: 
Dropped unique uninformative identifiers (name). Handled missing vectors, addressed target class imbalance using SMOTE strictly on the training partition to prevent data leakage, and standardized numerical metrics using StandardScaler across a stratified 80/20 train-test split.  
Exploratory Data Analysis (EDA): Visualized feature behaviors using histograms and boxplots to catch outlier boundaries, mapped feature interactions via correlation heatmaps, and isolated nonlinear markers (like PPE and spread1) as primary determinants of the disease.
Model Training: Built and optimized four distinct binary classification architectures: Logistic Regression, Support Vector Machine (SVM), Random Forest, and XGBoost (Extreme Gradient Boosting).
Evaluation: Assessed comparative performance across all models using Accuracy, Precision, Recall (critical for minimizing medical False Negatives), and F1-Score, followed by detailed Confusion Matrix and ROC-AUC curve validation for the top performer.
📈 Results
Top Performing Model: XGBoost Classifier
Overall Accuracy: 94.87%
Precision / Recall / F1-Score: 96.55% / 96.55% / 96.55%
The XGBoost model demonstrates exceptional diagnostic capability, capturing complex non-linear acoustic signatures to safely minimize False Negatives and serve as a highly reliable baseline for non-invasive Parkinson's screening.

<img width="322" height="250" alt="Screenshot 2026-06-19 222722" src="https://github.com/user-attachments/assets/c585d161-71c9-445e-9308-d29b795680e7" />
