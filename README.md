# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
```
import pandas as pd
df=pd.read_csv("/content/Loan_data (1).csv")
print(df)
df.head(10)
df.info()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()

df.info()
df.isnull().sum()
```
# OUPUT
# DATA

![DATA](https://user-images.githubusercontent.com/128909895/227720080-92c22d70-dd19-4947-9dd6-b86526b8da64.png)
# NON NULL BEFORE
## df.info
![NON NULL BEFORE](https://user-images.githubusercontent.com/128909895/227720168-57c41db6-b65e-4cf7-bfbb-6cc541cb4b3a.png)
## Mode

![mode](https://user-images.githubusercontent.com/128909895/227720313-d287869f-d14c-49ae-9e39-c3dc201e8eae.png)

## Mean

![mean](https://user-images.githubusercontent.com/128909895/227720377-951947d6-8d23-4959-ab2a-925fab5e49c1.png)
## Median
![median](https://user-images.githubusercontent.com/128909895/227720407-d8d54010-fa7c-4a70-8f2b-05c20308fea2.png)
# NON NULL AFTER
## df.info()

![DFINFO](https://user-images.githubusercontent.com/128909895/227720495-3977bd3b-ff3d-4c44-9103-6b6d8bc4fd0b.png)
## df.isnull().sum()

![isnull](https://user-images.githubusercontent.com/128909895/227720560-ab703a2e-7928-4166-b657-6bc9ff6a78f0.png)
# Result
Thus,the given data is read,cleansed and the cleaned data is saved into the file.
