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
![Screenshot_20230323_011354](https://user-images.githubusercontent.com/121166004/227136904-b6d12793-2bc1-42f4-97b5-3ad8315bc31f.png)


### NON NULL BEFORE:

### df.info:
![Screenshot_20230323_011409](https://user-images.githubusercontent.com/121166004/227136996-5e995a3e-f4a9-4542-9d07-f03e4711f7eb.png)


### MODE:
![Screenshot_20230323_011441](https://user-images.githubusercontent.com/121166004/227137087-7bf2ea58-d750-4586-9374-00e0949a0042.png)

### MEAN:
![Screenshot_20230323_011454](https://user-images.githubusercontent.com/121166004/227137205-9799a902-9242-4126-86b5-096596dd296a.png)


### MEDIAN:
![Screenshot_20230323_011503](https://user-images.githubusercontent.com/121166004/227137288-b32162c1-422d-4727-9ec2-444d12e9a590.png)

### NON NULL AFTER:

### df.info:
![Screenshot_20230323_011522](https://user-images.githubusercontent.com/121166004/227137789-420b9897-a9f9-4267-856f-4843a9866b2c.png)


### df.isnull().sum():
![Screenshot_20230323_011533](https://user-images.githubusercontent.com/121166004/227137734-1de760dc-0403-4d74-9cc2-7c41c2898b07.png)


RESULT:

Thus,the given data is read,cleared and the cleaned data is saved into the file.

