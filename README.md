# Identifying-biomarkers-of-depression
Uses the National Health and Nutrition Examination Survey to identify biomarkers of depression

  Depression is a common mood disorder with potentially severe ramifcations for physical and mental well-being. Despite pharmacological treatments being available, much about the biology underlying how these treatments work, and about the condition itself, remains unknown. 

The National Health and Nutrition Examination Survey collects comprehensive demographic, nutritional, physical and mental health data from a representative demographic cross-section of the US public. Two features of this dataset make the NHANES an excellent source into the biological basis of depression.  Firstly, blood and urine samples are collected and levels of an extensive and diverse set of markers are measured. Additionally, as part of the survey the PHQ-9 questionnaire is administered, which assesses depressive state on the basis of answers to nine questions. Each question is scored on a Likert scale of 0 (0 days/week) to 3 (every day), and the total scored is classified on the folowing ordinal scale: 0-4: Not depressed, 5-9: 'Mildly dperessed, 10-14: moderately depressed, 15-29: moderately severely dperessed, 20+: severely depressed. The coexistence of both sets of data makes the NHANES an excellent dataset to study the association between particular markers and depression level.

This project utilizes data from 14 years (2005-2018) to identify potential biomarkers of depression based on PHQ-9 scores and blood/urine samples. The basic outline/conclusions of this project are as follows:

  -Reduce the dataset to subjects with complete lab tests and PHQ-9 questionnaire responses
  -Perform EDA on all biomarkers to visualize relationships with PHQ-9 score
  -Use a multivariable ordinal logistic regression to identify markers that increase or decrease the odds of being depressed:

![image](https://user-images.githubusercontent.com/89553765/195697909-7105c57a-9a61-4f50-9b89-7291a54d44ec.png)
