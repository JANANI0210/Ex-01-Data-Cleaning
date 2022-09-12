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
#01

import pandas as pd

df = pd.read_csv("/content/Data_set.csv")

print(df)

df.head(10)

#02

df.info()

#03

df.isnull()

#04

df.isnull().sum()

#05

df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])


df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])


df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])


df.head()

#06

df['rating']=df['rating'].fillna(df['rating'].mean())


df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())


df.head()

#07

df['watchers']=df['watchers'].fillna(df['watchers'].median())


df.head()

#08

df.info()

#09

df.isnull().sum()




# OUPUT

![1sc](https://user-images.githubusercontent.com/86832944/189711321-6922b693-822a-4772-888b-c9f96e47cf16.png)

![2sc](https://user-images.githubusercontent.com/86832944/189711448-0b91f2a0-a762-4dcd-9631-8f8a33a5c7ce.png)

![3sc](https://user-images.githubusercontent.com/86832944/189711612-4c67e1b6-3047-4bfc-a9bf-5c1a4ff6109e.png)

![4sc](https://user-images.githubusercontent.com/86832944/189711859-29f88542-915c-498a-9991-79f65bf56b05.png)

![5sc](https://user-images.githubusercontent.com/86832944/189711916-9d3c2a06-dc86-4001-a805-4a6124191a8e.png)

![6sc](https://user-images.githubusercontent.com/86832944/189712102-81a892fc-de8e-49e0-b639-efe815815185.png)

![7sc](https://user-images.githubusercontent.com/86832944/189712194-5c6c7c34-6cc2-437a-af85-b25849728e82.png)


## RESULT

Thus, the given data is read cleaned and the cleaned data is saved to a file.

