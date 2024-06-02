Graduate Admission Chance Prediction Project
Project Overview
The goal of this project is to predict the likelihood of a student being admitted to a graduate program based on several key factors such as GRE scores, TOEFL scores, university ratings, statement of purpose strength, letter of recommendation strength, undergraduate CGPA, and research experience. By utilizing linear regression, we aim to develop a predictive model that can help prospective students estimate their chances of admission.

Data Description
The dataset used in this project contains 400 observations with the following features:

Serial No: Identifier for each student (not used in prediction)
GRE Score: Graduate Record Examination scores (290 to 340)
TOEFL Score: Test of English as a Foreign Language scores (92 to 120)
University Rating: Rating of the university (1 to 5)
SOP: Strength of the Statement of Purpose (1 to 5)
LOR: Strength of the Letter of Recommendation (1 to 5)
CGPA: Undergraduate Cumulative Grade Point Average (6.8 to 9.92)
Research: Research experience (0 or 1)
Chance of Admit: Probability of admission (0.34 to 0.97)
Steps Involved
Data Import and Exploration:

Imported the dataset and explored its structure using methods like .info() and .describe().
Ensured all columns are properly typed and no missing values are present.
Data Preparation:

Defined the target variable y (Chance of Admit) and features X (all other relevant columns excluding Serial No).
Split the data into training and testing sets using a 70-30 split to ensure that the model's performance can be evaluated on unseen data.
Model Selection and Training:

Chose Linear Regression as the model due to its simplicity and effectiveness for regression tasks.
Trained the model on the training data using model.fit(X_train, y_train).
Model Prediction:

Made predictions on the test set using model.predict(X_test).
Examined the coefficients and intercept of the linear regression model to understand the influence of each feature.
Model Evaluation:

Evaluated the model's performance using metrics like Mean Absolute Error (MAE), Mean Absolute Percentage Error (MAPE), and Mean Squared Error (MSE).
Achieved an MAE of 0.044, a MAPE of 7.57%, and an MSE of 0.0040, indicating that the model performs reasonably well in predicting admission chances.
Model Coefficients
The coefficients from the trained model indicate how each feature impacts the admission chances:

GRE Score: 0.0020
TOEFL Score: 0.0029
University Rating: 0.0057
SOP: -0.0038
LOR: 0.0197
CGPA: 0.1131
Research: 0.0206
The intercept of the model is -1.2831. Positive coefficients suggest that higher values of these features increase the chance of admission, while the negative coefficient for SOP indicates a slight decrease in admission chances with higher SOP scores, which might require further investigation.

Conclusion
This project demonstrates how linear regression can be effectively used to predict the likelihood of admission to graduate programs based on several academic and extracurricular factors. The model's predictions can serve as a useful tool for students to assess their chances and potentially improve their profiles before applying. The relatively low error metrics indicate that the model is quite accurate, though further refinement and exploration of more complex models could potentially improve predictions.
