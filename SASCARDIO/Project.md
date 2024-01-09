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

![eda7](https://github.com/florenciairene27/Irene.github.io/assets/112704355/f0246988-ab6c-47e3-a984-4f862ae0193e) ![eda8](https://github.com/florenciairene27/Irene.github.io/assets/112704355/349c79d5-fbca-4335-9d41-0351e8c86e8f) ![eda9](https://github.com/florenciairene27/Irene.github.io/assets/112704355/110ad4a1-7c02-440f-986e-432831e5a6cc) <img width="237" alt="eda10" src="https://github.com/florenciairene27/Irene.github.io/assets/112704355/446370b0-7315-42d0-b0cf-6c7e679192fa">

Box plots were generated to explore the numerical variables. In the heart disease group, higher mean ages were observed, along with higher mean values for both systolic and diastolic blood pressure.

![eda11](https://github.com/florenciairene27/Irene.github.io/assets/112704355/6595fa66-114e-4742-8d61-9a250df59fc7) ![eda12](https://github.com/florenciairene27/Irene.github.io/assets/112704355/256822e4-a3ca-4a13-8edd-56b494c2207f)
<img width="401" alt="eda13" src="https://github.com/florenciairene27/Irene.github.io/assets/112704355/5a2e5ff5-7ea6-4204-8b8b-eaebde5c9d0c">

For the height, the distribution looks pretty much similar between the heart disease group and no disease group with similar means, but the heart disease group has higher mean weight. 

![eda14](https://github.com/florenciairene27/Irene.github.io/assets/112704355/ca2fbc3f-96c4-407c-8017-933b928e9bd8) 
![eda16](https://github.com/florenciairene27/Irene.github.io/assets/112704355/00b93dfa-21e9-43c8-a324-731920ecd1fa)
![eda17](https://github.com/florenciairene27/Irene.github.io/assets/112704355/0164cb97-adda-4dd1-a3a6-e52abc3d6246)
![eda18](https://github.com/florenciairene27/Irene.github.io/assets/112704355/2e2856de-8c35-47a3-ac74-0caef0ed9d37)

A correlation matrix was also generated, revealing significant correlations among the variables of height, weight, and age, which was an anticipated outcome. Consequently, a new variable, BMI (Body Mass Index), was created, calculated as an individual’s weight in kilograms divided by the square of their height in meters. This combined variable was then assessed to determine its potential to replace height and weight, thereby reducing redundancy.














