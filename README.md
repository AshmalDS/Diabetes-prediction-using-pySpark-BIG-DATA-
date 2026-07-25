Diabetes Prediction using PySpark (Big Data)
📌 Project Overview

This project predicts whether a person has diabetes based on their medical information, using PySpark and Spark MLlib. Unlike typical pandas/sklearn projects, this pipeline is built to handle data at scale using Spark's distributed processing tools — from data loading to model training and evaluation.

The dataset contains 95,724 rows of patient health records, with the goal of classifying each patient as diabetic (1) or non-diabetic (0).

🗂️ Dataset Description

Each row represents a patient, and each column represents a health-related feature.

Column	Description
gender	Gender of the person (Male/Female)
age	Age of the person
hypertension	High blood pressure (0 = No, 1 = Yes)
heart_disease	Whether the person has heart disease
smoking_history	Smoking behavior of the person
bmi	Body Mass Index (health indicator)
HbA1c_level	Average blood sugar level over time
blood_glucose_level	Current glucose level in blood
diabetes	Target variable (0 = No diabetes, 1 = Diabetes)
🛠️ Tools & Technologies
PySpark (Spark SQL, Spark MLlib)
StringIndexer — encoding categorical features
VectorAssembler — combining features into a single vector
Logistic Regression — classification model
🔄 Workflow
Created a Spark session and loaded the dataset
Performed exploratory data analysis (EDA)
Preprocessing: handled missing values (dropping/filling), encoded categorical columns with StringIndexer
Assembled features into a single vector using VectorAssembler
Split data into train/test sets
Trained a Logistic Regression model
Generated predictions and evaluated performance
📊 Results
Accuracy: 0.961

Note: This dataset is imbalanced (far fewer diabetic cases than non-diabetic). Accuracy alone can be misleading in this scenario — precision, recall, and F1-score for the diabetic class give a more complete picture and will be added in a future update.

🚀 Future Improvements
Evaluate precision/recall/F1-score (not just accuracy) due to class imbalance

👤 Author

Built by AYESHA ASHMAL as part of a data science / big data learning portfolio.
Try other models (Random Forest, Gradient Boosted Trees) available in Spark MLlib
Handle class imbalance (e.g., class weighting)
Deploy as a simple prediction app
