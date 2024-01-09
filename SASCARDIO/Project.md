# CardioSAS: Predictive Modeling for Cardiovascular Disease Risk Assessment

## Introduction
Cardiovascular disease is a disorder that affects the heart and blood vessels. It is the leading cause of death globally, accounting for 31% of all deaths, and 17.7 million people die every year. Common types of CVDs are Coronary Artery Disease, Heart Attack, Storke, and Heart Failure. Since early detection and management are necessary and patients’ awareness of risk factors are important, building a model to predict cardiovascular disease is essential

## Data Description 
**Source** : [https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset/data]

**There are 3 types of input features:**

1. Objective: factual information;
2. Examination: results of medical examination;
3. Subjective: information given by the patient.

**Features:**

1. Age | Objective Feature | age | int (days)
2. Height | Objective Feature | height | int (cm) |
3. Weight | Objective Feature | weight | float (kg) |
4. Gender | Objective Feature | gender | categorical code |
5. Systolic blood pressure | Examination Feature | ap_hi | int |
6. Diastolic blood pressure | Examination Feature | ap_lo | int |
7. Cholesterol | Examination Feature | cholesterol | 1: normal, 2: above normal, 3: well above normal |
8. Glucose | Examination Feature | gluc | 1: normal, 2: above normal, 3: well above normal |
9. Smoking | Subjective Feature | smoke | binary |
10. Alcohol intake | Subjective Feature | alco | binary |
11. Physical activity | Subjective Feature | active | binary |
12. Presence or absence of cardiovascular disease | Target Variable | cardio | binary |
13. All of the dataset values were collected at the moment of medical examination.

## Exploratory Data Analysis
![eda1](https://github.com/florenciairene27/Irene.github.io/assets/112704355/d430f961-0146-45fa-a0e4-280fa553edb0) ![eda2](https://github.com/florenciairene27/Irene.github.io/assets/112704355/6004b374-9e71-4b24-971d-5891e854d7a5) ![eda3](https://github.com/florenciairene27/Irene.github.io/assets/112704355/36cd1c28-eebe-4c36-9f93-2b7f4f2f1d76)

![eda4](https://github.com/florenciairene27/Irene.github.io/assets/112704355/02f1cfa8-9d62-412d-b5ce-4afdb8d597e4) ![eda5](https://github.com/florenciairene27/Irene.github.io/assets/112704355/11260de6-c31c-49cc-9a99-e01e9c3a5885)

In the initial exploratory data analysis (EDA) focusing on categorical variables, it was observed that the gender ratio is similar in the heart disease group and no disease group. There are definitely more people with higher cholesterol in the heart disease group (as you can see the blue is normal and the red and green are high cholesterol groups). On the other hand, minimal visual differences were noted in the distribution of glucose levels, smoking habits, and physical activity between individuals with and without heart disease, suggesting less distinct variations in these factors among the groups.










