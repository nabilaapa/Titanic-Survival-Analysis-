# Titanic-Survival-Analysis
---
*Tools : Python, Jupyter Lab, Git, Numpy, Pandas, Scipy, Matplotlib, Seaborn, Scikit-Learn*

Data Source : [Titanic - Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic)

    On April 15, 1912, during her maiden voyage, the widely considered “unsinkable” RMS Titanic sank after colliding with an iceberg. Unfortunately, there weren’t enough lifeboats for everyone onboard, resulting in the death of 1502 out of 2224 passengers and crew.

    In the Hollywood blockbuster that was modelled on this tragedy, it seemed to be the case that upper-class people, women and children were more likely to survive than others. But did these properties (socio-economic status, sex and age) really influence one's survival chances?

    Based on data of a subset of 891 passengers on the Titanic, I will make a model that can be used to predict survival of other Titanic passengers.

    Build a predictive model that answers the question: “what sorts of people were more likely to survive?” using passenger data (ie name, age, gender, socio-economic class, etc).

## Project Background
---
Currently, the survival rate of passengers on the Titanic dataset is only 38.38% for the whole period recorded. However, we aim to increase the survival rate to 50% and improve the overall performance of our predictive model in 2023 by:

- Utilizing predictive modeling techniques to accurately predict whether a passenger will survive or not based on various factors.
- Conducting in-depth analysis to identify the key factors that significantly influence the chances of survival. By understanding these factors, we can implement targeted strategies to improve the overall survival rate.

## Exploratory Data Analysis
---
We have some interesting assumptions based on the problem description noted earlier:
1. Women (Sex=female) were more likely to have survived.
2. Children (Age<?) were more likely to have survived.
3. The upper-class passengers (Pclass=1) were more likely to have survived.

## Feature Engineering
---
1. create a new feature called Family size based on Parch and SibSp to get total count of family members on board.
2. engineer the Name feature to extract Title as a new feature.
3. create a new feature called Family type with labels=['Solo', 'Small', 'Big', 'Very big'])
4. create a Fare class feature if it helps our analysis.

## Data Preprocessing
---
- Handling Missing Value
- Handling Duplicated Value
- Handling Outliers
- Feature Transformation
- Feature Encoding
- Feature Selection
- Imbalance Target Handling

## Modeling
---
10 models were evaluated using ROC AUC as the evaluation metric to measure the models' performance in predicting the positive class. It was found that the `Gradient Boosting Classifier - Hyperparameter Tuning model with SMOTE dataset` achieved the highest ROC AUC score of 91% when considering all classes with consideration of not underfitting or overfitting. This model demonstrated exceptional predictive power in distinguishing between the positive and negative classes by obtaining the top 3 predictors namely Title_MR, Pclass, and Sex based on the results of the SHAP Value.

## Insights & Recommendation
---

Recommendations:
1. Increase awareness and safety measures for adult male passengers (identified with the title "Mr."). Training and awareness campaigns about evacuation safety and prioritizing vulnerable groups during emergencies could enhance the survival chances of adult male passengers.
2. Improve facilities and lifeboats for passengers in lower classes (pclass=2 or pclass=3) to enhance the safety of passengers in lower classes who have a lower chance of survival.
3. Continue to adhere to the "Women and Children First" policy and ensure its enforcement during emergencies or evacuations.

By understanding the above factors, further actions can be taken to improve the safety and survival chances of passengers in the future.


---
