# Identifying-biomarkers-of-depression
Uses the National Health and Nutrition Examination Survey to identify biomarkers of depression

Data used: The National Health and Nutrition Examination Survey (NHANES), years 2005-2018
Libraries used:Pandas, atplotlib, Seaborn, Scikit-Learn,
Techniques used: Data cleaning, data imputation, data visualization, random forest regression

PROBLEM STATEMENT

  Depression is a common mood disorder with potentially severe ramifcations for physical and mental well-being. Despite pharmacological treatments being available, much about the biology underlying how these treatments work, and about the condition itself, remains unknown. Identifying biomarkers is an important step towards improving our understanding and treatment of depression. 

The National Health and Nutrition Examination Survey (NHANES) collects comprehensive demographic, nutritional, physical and mental health data from a representative demographic cross-section of the US public. Two features make the NHANES an excellent dataset for uncovering biomarkers of depression.  Firstly, blood and urine samples are collected and levels of an extensive and diverse set of markers are measured. Secondly, as part of the survey the PHQ-9 questionnaire is administered, which assesses depressive state on the basis of answers to nine questions. Each question is scored on a Likert scale of 0 (0 days/week) to 3 (every day), and the total scored is calculated on a scale of 0-27. 

This project utilizes data from 14 years (2005-2018) to 1) identify potential biomarkers of depression based on PHQ-9 scores and blood/urine samples, and 2) evaluate the usefulness of this data for modeling PHQ-9 score.


RESULTS

The distribution of PHQ-9 scores from 19,268 subjects is heavily right-skewed:

![image](https://user-images.githubusercontent.com/89553765/219124972-a907fbb3-e2f1-448b-a60a-3fa70a9bddf0.png)

The variables span major blood cell types, and a variety of metabolic markers:

![image](https://user-images.githubusercontent.com/89553765/220649139-8a5b0ac2-8a0f-4e30-a0a1-af2db1c1126d.png)

Without exception, the variables showed very weak or no correlation with PHQ-9 score. The following are some of the variables that showed the strongest correlations, as quantified by Kendall's tau, a non-parametric  correlation coefficient:

![image](https://user-images.githubusercontent.com/89553765/220647284-92d187fb-2134-4b50-ae74-e8d32a50c1bc.png)

And the coefficients of all of the variables showing the strongest trends with PHQ-9 score: 

![image](https://user-images.githubusercontent.com/89553765/220649900-7d7a5a18-8b05-4b7e-b692-9bfc4cc16e0e.png)

To deterine whether common lab test features could be used to predict PHQ-9 score, I built a random forest regression model using all 40 variables as features. Examining the model's performance metrics reveals that it explains a minimal amount of variance, with and R2 value of 0.008. Moreover, the model has worse predictive utility than a constant model using the mean PHQ-9 score.

![image](https://user-images.githubusercontent.com/89553765/220473796-eca2d3a9-5056-4cfb-9dbd-e6822aa5eac5.png)




