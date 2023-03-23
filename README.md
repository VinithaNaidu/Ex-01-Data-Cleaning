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
df.isnull()
df.isnull().sum()
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
### DATA:
![1](https://user-images.githubusercontent.com/121166004/227132657-40e1a821-bdf5-4f63-8d24-4dec52e2b478.png)

### NON NULL BEFORE:

### df.info:
![2](https://user-images.githubusercontent.com/121166004/227133414-caec4d2e-5c8d-4174-a09e-6a6aa563f83c.png)

### MODE:
![2](https://user-images.githubusercontent.com/121166004/227133786-e98dd67e-f16a-4af7-9a57-b7a9790ae457.png)


### MEAN:
![2](https://user-images.githubusercontent.com/121166004/227133999-bf300e34-035c-4fdc-9a96-f67bca58a76f.png)

### MEDIAN:
![Screenshot_20230323_010815](https://user-images.githubusercontent.com/121166004/227135723-26c5d9f7-af3c-403d-b16f-bd37e47f52ce.png)


### NON NULL AFTER:

### df.info:
![2](https://user-images.githubusercontent.com/121166004/227134267-e0095a3f-c232-4f4e-958e-7c00e85faee2.png)

### df.isnull().sum():
![2](https://user-images.githubusercontent.com/121166004/227134476-e7e4d6af-ba34-4cf8-a949-5296790c4339.png)

RESULT:

Thus,the given data is read,cleared and the cleaned data is saved into the file.

