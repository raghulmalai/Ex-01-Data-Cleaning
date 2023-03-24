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
#data_set
```
import pandas as pd
df = pd.read_csv("/content/Data_set.csv")
df.head(5)
df.info()
df.isnull().sum()
#MODE:
df['show_name'] = df['show_name'].fillna(df['show_name']).mode()[0]
df['aired_on'] = df['aired_on'].fillna(df['aired_on']).mode()[0]
df['original_network'] = df['original_network'].fillna(df['original_network']).mode()[0]
#MEAN:
df['rating'] = df['rating'].fillna(df['rating']).mean()
df['current_overall_rank'] = df['current_overall_rank'].fillna(df['current_overall_rank']).mean()
#FORWARD METHOD:
df['watchers'] = df['watchers'].fillna(method='ffill')
df.isnull().sum()
```
```
#loan_data
import pandas as pd
df = pd.read_csv("/content/Loan_data.csv")
df.head(5)
df.info()
df.isnull().sum()
#MODE:
df['Gender'] = df['Gender'].fillna(df['Gender'].mode()[0])
df['Self_Employed'] = df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Dependents'] = df['Dependents'].fillna(df['Dependents'].mode()[0])
#MEAN and MEDIAN:
df['LoanAmount'] = df['LoanAmount'].fillna(df['LoanAmount'].median())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].mean())
df.isnull().sum()
```

# OUPUT
First File:

Data_Set.csv FILE

![Screenshot (16)](https://user-images.githubusercontent.com/118707079/226097653-5b937a1c-5dfd-4135-8d0c-34d771e7dae1.png)
INFO

![Screenshot (19)](https://user-images.githubusercontent.com/118707079/226097909-d032ad30-801e-4cf8-a205-da52a46c26a9.png)

Isnull.().sum() before cleaning

![Screenshot (17)](https://user-images.githubusercontent.com/118707079/226097972-cf6e33ee-0393-4ca9-bc5b-cf0d53b3fb1f.png)

MODE,MEAN and FORWARD METHOD

![Screenshot (20)](https://user-images.githubusercontent.com/118707079/226098096-491bc793-1d37-4e13-9c38-6b1f33616fbc.png)
isnull().sum() after cleaning

![Screenshot (18)](https://user-images.githubusercontent.com/118707079/226098133-6ab056df-ae33-4028-9f5f-bc7b7be00787.png)

Second File:

Loan_Data.csv FILE

![Screenshot (21)](https://user-images.githubusercontent.com/118707079/226098607-c637e069-71c2-4984-954b-32e773235ccd.png)
INFO

![Screenshot (22)](https://user-images.githubusercontent.com/118707079/226098734-38409eb0-d1e7-4c8e-aa9f-6c024bf89b3e.png)

Isnull.().sum() before cleaning

![Screenshot (23)](https://user-images.githubusercontent.com/118707079/226098744-a18a5d18-9e73-4c2a-836b-d626165d3132.png)

MODE,MEAN and MEDIAN

![Screenshot (24)](https://user-images.githubusercontent.com/118707079/226098756-dfe2e54e-e797-4c3b-a846-1ad7797b3686.png)
isnull().sum() after cleaning

![Screenshot (25)](https://user-images.githubusercontent.com/118707079/226098758-9cb68b92-4615-4bbf-ab1b-a8d906c753d4.png)

RESULT:

Thus the given data is read,cleansed and cleaned data is saved into the file.

