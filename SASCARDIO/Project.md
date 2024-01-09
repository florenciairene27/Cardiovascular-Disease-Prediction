# CardioSAS: Predictive Modeling for Cardiovascular Disease Risk Assessment
**Author**: Florencia Irene & Esther Ki
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
In the initial exploratory data analysis (EDA) focusing on categorical variables, it was observed that the gender ratio is similar in the heart disease group and no disease group. There are definitely more people with higher cholesterol in the heart disease group (as you can see the blue is normal and the red and green are high cholesterol groups). On the other hand, minimal visual differences were noted in the distribution of glucose levels, smoking habits, and physical activity between individuals with and without heart disease, suggesting less distinct variations in these factors among the groups.

![eda1](https://github.com/florenciairene27/Irene.github.io/assets/112704355/d430f961-0146-45fa-a0e4-280fa553edb0) ![eda2](https://github.com/florenciairene27/Irene.github.io/assets/112704355/6004b374-9e71-4b24-971d-5891e854d7a5) ![eda3](https://github.com/florenciairene27/Irene.github.io/assets/112704355/36cd1c28-eebe-4c36-9f93-2b7f4f2f1d76)

![eda4](https://github.com/florenciairene27/Irene.github.io/assets/112704355/02f1cfa8-9d62-412d-b5ce-4afdb8d597e4) ![eda5](https://github.com/florenciairene27/Irene.github.io/assets/112704355/11260de6-c31c-49cc-9a99-e01e9c3a5885)

Box plots were generated to explore the numerical variables. In the heart disease group, higher mean ages were observed, along with higher mean values for both systolic and diastolic blood pressure.

![eda7](https://github.com/florenciairene27/Irene.github.io/assets/112704355/f0246988-ab6c-47e3-a984-4f862ae0193e) ![eda8](https://github.com/florenciairene27/Irene.github.io/assets/112704355/349c79d5-fbca-4335-9d41-0351e8c86e8f) ![eda9](https://github.com/florenciairene27/Irene.github.io/assets/112704355/110ad4a1-7c02-440f-986e-432831e5a6cc) <img width="237" alt="eda10" src="https://github.com/florenciairene27/Irene.github.io/assets/112704355/446370b0-7315-42d0-b0cf-6c7e679192fa">

For the height, the distribution looks pretty much similar between the heart disease group and no disease group with similar means, but the heart disease group has higher mean weight. 

![eda11](https://github.com/florenciairene27/Irene.github.io/assets/112704355/6595fa66-114e-4742-8d61-9a250df59fc7) ![eda12](https://github.com/florenciairene27/Irene.github.io/assets/112704355/256822e4-a3ca-4a13-8edd-56b494c2207f)
<img width="401" alt="eda13" src="https://github.com/florenciairene27/Irene.github.io/assets/112704355/5a2e5ff5-7ea6-4204-8b8b-eaebde5c9d0c">

A correlation matrix was also generated, revealing significant correlations among the variables of height, weight, and age, which was an anticipated outcome. Consequently, a new variable, BMI (Body Mass Index), was created, calculated as an individual’s weight in kilograms divided by the square of their height in meters. This combined variable was then assessed to determine its potential to replace height and weight, thereby reducing redundancy.

![eda14](https://github.com/florenciairene27/Irene.github.io/assets/112704355/ca2fbc3f-96c4-407c-8017-933b928e9bd8) 
![eda16](https://github.com/florenciairene27/Irene.github.io/assets/112704355/00b93dfa-21e9-43c8-a324-731920ecd1fa)
![eda17](https://github.com/florenciairene27/Irene.github.io/assets/112704355/0164cb97-adda-4dd1-a3a6-e52abc3d6246)
![eda18](https://github.com/florenciairene27/Irene.github.io/assets/112704355/2e2856de-8c35-47a3-ac74-0caef0ed9d37)

## Research Questions

1. Is there a significant difference in the mean BMI between people with cardiovascular disease and those without disease?
- Compare the results with the height and weight variables in the dataset

2. What factors contribute to the presence of cardiovascular disease? 
- Build a model to assess individual’s risk of cardiovascular disease 

## Results

### Statistical Test
The t-test results of the height, weight, and BMI revealed that there was no significant difference observed in the mean height between the heart disease group and the non-disease group. However, a notable discrepancy was identified in the mean weight and mean BMI, aligning with our expectations derived from the exploratory data analysis (EDA). In medical contexts, BMI is often regarded as a more crucial variable than height and weight due to its standardized approach in assessing overall body composition. Consequently, the decision was made to replace the height and weight variables with BMI to reduce redundancy while retaining all information from the original dataset.

<img width="549" alt="eda19" src="https://github.com/florenciairene27/Irene.github.io/assets/112704355/cc074c1e-c2b7-422b-b729-933df94a0955">

### Training and Test Dataset
The second research question, "What factors contribute to the presence of heart disease?" will be explored by creating a predictive model.
Initially, the dataset was divided, allocating 70% for training and 30% for testing. The proportions of each dataset are presented in the SAS output below:

<img width="262" alt="eda22" src="https://github.com/florenciairene27/Irene.github.io/assets/112704355/64759ced-403c-45da-be81-98f6b5bbf769">

### Modeling

Utilizing a training dataset, a logistic regression model was trained to address the classification problem at hand. Employing all variables within the dataset, the stepwise selection method was utilized to determine relevant predictors. This iterative approach involved initiating an empty model and selectively adding or removing variables based on their respective p-values. The resulting model encompassed all variables, excluding gender and alcohol, indicating their insignificance as predictors. Furthermore, Glucose 3 and smoking variables presented an unexpected scenario; despite their significant p-values, their coefficients were negative. This unexpected observation seemed to suggest a counterintuitive association wherein individuals with higher glucose levels or those who smoked showed a decreased likelihood of developing heart disease, presenting an intriguing and puzzling aspect that requires further investigation.

<img width="402" alt="eda22" src="https://github.com/florenciairene27/Irene.github.io/assets/112704355/47d3fc48-56d5-47f9-8758-6f7403af8026">

Upon assessing the model's performance, an evaluation was conducted using a confusion matrix to measure its predictive capability. An accuracy rate of 72.65% was observed in the model. However, concerns were raised regarding the reliability of estimates associated with Glucose and smoking variables, potentially influencing the model's implications. This prompted the identification of a potential issue: multicollinearity. Suspicions were raised about the potential correlation between smoke and glucose, as well as their possible correlations with other categorical predictors, contributing to this discrepancy. To address this concern, let's explore the potential correlations among variables using chi-square test.

<img width="456" alt="eda24" src="https://github.com/florenciairene27/Irene.github.io/assets/112704355/0167f8d9-c571-4c5f-965c-a8a2b24d8500">

The chi-square tests were performed between all pairs of categorical variables, revealing an association between cholesterol and both glucose and smoke. A decision was made to attempt the removal of glucose and smoke from the model to ascertain if there would be an improvement in accuracy.

<img width="515" alt="eda25" src="https://github.com/florenciairene27/Irene.github.io/assets/112704355/ed618c9e-ac8e-4c8d-a815-ab6f1c1baa67">

The model was then refitted, this time excluding glucose and smoke. The SAS output below displays the estimates of the parameters, revealing significance across all variables, which supports the previous decision.

<img width="251" alt="eda26" src="https://github.com/florenciairene27/Irene.github.io/assets/112704355/734c8ae7-6143-4ff2-b70c-f7690771701b">

For further validation of the decision, an accuracy check was performed on the new model. The accuracy of the new model was measured at 72.30%, indicating a slight decrease. This minor decline in accuracy supports the decision to eliminate these two variables, as their removal only minimally impacts the model's performance. Subsequently, the new model was tested on the testing dataset, revealing that the accuracy remained stable, with a slight improvement.

<img width="449" alt="eda26" src="https://github.com/florenciairene27/Irene.github.io/assets/112704355/527b4654-a920-46c7-9330-28a05e208563">

The Final model and the interpretation are shown in the picture below:

<img width="471" alt="eda27" src="https://github.com/florenciairene27/Irene.github.io/assets/112704355/e03da1c5-e50d-4566-b3b0-7591964952fc">

### Variable Importance 

"Standardized coefficients are coefficients adjusted so that they may be interpreted as having the same, standardized scale and the magnitude of the coefficients can be directly compared (ranked)." (Menard S. 2004)
According to Menard, if coefficients are standardized we can compare the magnitude of it or it means larger absolute value of standardize coeff suggests a more important predictors in terms of it impact on the outcome variable. Based on the model coefficients, here's the variable important rank :

<img width="227" alt="eda28" src="https://github.com/florenciairene27/Irene.github.io/assets/112704355/ea9a0d05-9790-47b8-a401-f3b3108e1cc1">

## Conclusion

In conclusion, the analysis highlighted a significant link between BMI and heart disease, showcasing a distinct difference in BMI values between those with and without the condition. The logistic regression model demonstrated strong performance, accurately predicting heart disease with an impressive 73.23% success rate. Key factors like Ap_hi, age, cholesterol, BMI, Ap_lo, and physical activity emerged as crucial contributors to the likelihood of developing heart disease. These findings shed light on important aspects to consider when understanding how certain factors may predict this medical condition, providing valuable insights for future research and clinical evaluations.

## Limitation

One of the limitation in this study is the nearly equal distribution between individuals with and without heart disease in the dataset, which doesn't entirely mirror the real-world scenario. This poses a challenge when attempting to generalize the analysis and its implications to real-world situations. Additionally, models trained on balanced data might not effectively handle imbalanced data, potentially struggling to make accurate predictions for minority classes. 

Furthermore, relying solely on accuracy as a metric to evaluate the model presents another limitation. Accuracy tends to emphasize the majority classes, with the dominant class significantly impacting the overall accuracy score. This can be problematic, particularly when the focus is on rare classes, as missing even a few cases can have substantial consequences, highlighting the need for additional evaluation metrics beyond accuracy in such scenarios




































