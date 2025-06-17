# Salary-Prediction

Objective: 
Predict the salary based on every features in the dataset.

Overview:
These project is divided into three phases.

First Phase:
Data exploration and data cleaning

Second Phase:
Advance statistics and EDA before training the model

Third Phase:
Model traning and making future predicitions and visualize it by making dashboard 

These project is currently in evolution phase.

**Data Structure**
There are 6704 data points (rows) and 6 features (attributes)
The data is messy need to clean it before further process

Before cleaning the data need to be first explore the data and analysing it with some basic methods.

1. Understand the attributes
   Age: The age of the particular employee
   Gender: The gender identification of the employee
   Education: The educational background of the employee
   Job Title: The domain of the current job of the employee
   Years of Experience: The experience in the particular job domain
   Salary: The Current salary of the employee

   The data type of the attributes are in float and object
   float: Age, Years of Experience, and Salary
   object: Gender, Education level, and Job Title

2. To get the count of the unique values per column by using **nunique()** method.
   Toget the actual unique values **unique()** method can be use, but to get for all features   **for loop**, the **unique()** method can be useful only for **single pandas series** not for **DataFrame**

3. Obeseravtion to note, the **nunique()** method doesn't include the NaN values, there might be some missing values.
4. Where as in the **unique()** method the NaN will display with the unique values of the particular feature.
5. The feature "Education Level" contain data points with same background but different identification, "Bachelor's" and "Bachelor's Degree" are the similar in terms of qulification.

**Exploratory Data Analysis (Inital stage)**
1. Summarized statistics using describe() method the summary of the numeric feature displays include "count, mean, std, min, 25%, 50%, 75% , and max". The main focus was on count, min, and max to get idea of missing values and the maximum and minimum data points from each features.
2. Summarized the categorical data using value_counts() method, count the unique values of every data points. Can aso incluse NaN to count number of null values inside the feature.

**Handling missing value**
1. To handle the missing value, first need to identify the dependency between the features.
   Key Observation:
   Age <-> Years of Experience
   Years of Experience deponds on Age and possibly Job Title
   Years of Experience <-> Salary
   Salary depends on Years of Experience and possibly Education Level

2. GroupBy method used to explore the relationship with different feature

   

