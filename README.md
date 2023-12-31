# Fetal-Health-Project

## Motivation:

### Problem statement:

- Under-five mortality is greatly influenced by the death of children in the first month of their life. Perinatal mortality is largely caused by intrapartum complications. However, Cardiotocograms (CTGs), which are simple and affordable, can serve as a monitoring tool to assess fetal health and identify high-risk women during labor.

### Project importance:

- To help achieve the MDG 4 goal of globally reducing under-five mortality by two-thirds. Additionally, to reduce maternal mortality, which accounts for 295,000 deaths during pregnancy and childbirth, with 94% occurring in low-resource settings, many of which are preventable.

### Dataset description:

- Our dataset consists of 2126 CTG exam records of pregnant women in their third trimester. It includes 22 features, with Fetal Health classified into three classes (Normal as 1, Suspect as 2, and Pathological as 3) by expert obstetricians.

### Project objectives:
1. To identify the most significant features for detecting high-risk fetal health conditions.
2. To analyze the precision of CTG model algorithms in correctly classifying instances.
3. Based on the model evaluation result, propose the global scale-up of CTG usage, with a focus on regions burdened by high newborn and maternal mortality.

### Approach:

![**Alt text**](classification_approach.jpg)

#### Steps:

##### Preprocess/ Clean data studying dataframe
1. Cleaned data by dropping null values. (Decided no further cleaning needed since the dataset appeared clean)
2. Studied the columns and what they represent as well as how many data are in each category of fetal health

##### EDA (1)
1. Created pairplot with all the features of the dataset to have a general idea about the dataset
2. Correlation heatmap was created using all the feature to recognize any correlation

##### OLS Model (1)
1. OLS Regression model was done to identify the significant features in recognizing patterns

##### Feature Selection
1. New dataframe created with significant features

##### EDA (2)
1. Pairplot created to further analyze significant features
2. Created separate datasets according to fetal health category
3. Different Types of plots were created in python and Tablaeu (Graphs and Dashboard) to see the relationship between fetal health versus each feature
4. T-tests done for each feature to identify if there are any significant differences between their averages and fetal health.

##### OLS Model (2)
1. OLS model generated for significant features

##### EDA (3)
1. Created correlation heatmap for significant features to identify the correlation with each other
2. Scatterplots were generated for features with high correlation to analyze them further

##### Predictions 
1. Model evaluation done after balancing data to identify the precision of the model

## Results:
- Significant features that affect the fetal health are:
    - Baseline value
    - Uterine contractions 
    - Severe Decelerations
    - Prolongued Decelerations
    - Abnormal short term variability 
    - Percentage of time with abnormal long term variability
    (identified using the p-value of OLS Regression model)

##### T-test results:
- Since the p-value is >0.05 when comparing severe decelerations of normal and suspect, we do not reject the null hypothesis that the averages are equal. Therefore, we would conclude that there is not enough evidence to conclude that there is a significant difference between the averages of severe decelerations between normal and suspect.
- For all other comparisons, we reject the null hypothesis that the averages are equal. Therefore, we would conclude that the averages of all the other comparisons done are significantly different.

##### Model Evaluation results:
- Our model with significant features has approximately 70% accuracy when introduced to a new dataset.

## Conclusion:
 The model exhibits a 70% accuracy rate, indicating its proficient ability to classify various classes. As a result, it is highly recommended for adoption by health systems, especially in developing nations, for use during prenatal checks, particularly prior to or during labor in the third trimester. This implementation can effectively aid in reducing newborn and maternal mortality rates.