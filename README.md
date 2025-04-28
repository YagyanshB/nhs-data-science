# PRISM - Patient Readmission Identification System using Machine Learning

PRISM is a machine learning solution designed to predict a patient's risk of hospital readmission within 30 days after discharge. This machine learning model will help **Mid Yorkshire Teaching NHS Trust** to identify high-risk patients who may benefit from additional post-discharge support and interventions, potentially reducing readmission rates and improving patient outcomes across the Trust.

# Key Features

1. Comprehensive Risk Assessment: Analyses 15+ patient factors, including demographics, clinical data, and social determinants
2. High Accuracy: Achieves strong predictive performance with the Random Forest machine learning algorithm
3. NHS-Specific Design: Explicitly tailored for the UK healthcare system with relevant features
4. Risk Stratification: Categorises patients into Low, Moderate, High, and Very High risk groups
5. Interpretable Results: Provides feature importance analysis to explain predictions

# 📊 Data Features
The model incorporates key readmission predictors known from NHS clinical research:

| Feature  | Category Variables |
| ------------- | ------------- |
| Demographics  | Age, Gender, Ethnicity  |
| Social Factors  | Content Cell  |
| Clinical  | Primary diagnosis, Charlson Comorbidity Index, Length of stay (LACE) |
| Care History  | Previous Admission last 12 months  |
| Admission Details  | Admission Method, Emergency Status  |
| Discharge Planning  | Discharge Destination, GP Follow Up Appointment  |
| Clinical Complexity  | NEWS2 Score, Polypharmacy Status  |

# 📈 Model Performance
The Random Forest classifier has been deployed on synthetically created datasets of **50000 patients**:

1. ROC-AUC: ~0.65-0.68 (After fine-tuning the parameters, we were able to increase it from 0.61)
2. High sensitivity for identifying at-risk patients
3. Strong precision-recall balance
4. Reliable performance across demographic subgroups


# 🔬 Technical Implementation

1. Data Preprocessing: One-hot encoding for categorical variables
2. Algorithm: Random Forest Classifier with 100 estimators
3. Validation: 80/20 train-test split with stratification
4. Evaluation: ROC-AUC, precision-recall, confusion matrix, and classification report
5. Feature Engineering: Custom NHS-specific features based on clinical notes

# Further Discussion and Future Score: 

1. A combination of structured and unstructured data ML models, compared to a structured data ML classifier model, doesn't have a significant difference in the ROC-AUC score.
2. Potential to investigate if there are features that should be removed entirely to reduce the noise present within datasets.
