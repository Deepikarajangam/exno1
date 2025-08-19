# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
import pandas as pd
df=pd.read_csv("C:\\Users\\Pandiyan\\Downloads\\Data_set.csv")
df
<img width="961" height="792" alt="image" src="https://github.com/user-attachments/assets/ca380590-18bf-46c2-a054-df7a9ee73768" />

df.info()
<img width="610" height="362" alt="image" src="https://github.com/user-attachments/assets/799f9e0b-5db2-4043-8e4c-f394311eaec4" />
df.describe()

<img width="927" height="397" alt="image" src="https://github.com/user-attachments/assets/6fa1f793-2d5f-420b-8dfa-252cd459e6cb" />
df.head(10)
<img width="927" height="721" alt="image" src="https://github.com/user-attachments/assets/f7013665-4bb0-4d72-beae-6ab18f6d54ac" />
df.tail(5)
<img width="906" height="420" alt="image" src="https://github.com/user-attachments/assets/c67094c2-e470-4906-a85c-db8e9d49af71" />

df.shape
<img width="186" height="57" alt="image" src="https://github.com/user-attachments/assets/0932f564-e454-4732-8080-365b143bfe25" />
df.isnull()
<img width="943" height="510" alt="image" src="https://github.com/user-attachments/assets/786a51fc-ab13-43de-842f-031ca49e328d" />
df.notnull()
<img width="922" height="530" alt="image" src="https://github.com/user-attachments/assets/85be4649-63bd-4b5f-88e7-6a838cd5d789" />
df.isnull().sum()
<img width="513" height="308" alt="image" src="https://github.com/user-attachments/assets/63933a3d-b8e5-433d-a60b-f7ead2c4197f" />
df.dropna(axis=0)
<img width="928" height="806" alt="image" src="https://github.com/user-attachments/assets/73125af9-5226-4681-8e25-992819d8e1cc" />
df.dropna(axis=1)
<img width="702" height="565" alt="image" src="https://github.com/user-attachments/assets/2bd40260-c71c-4949-bd1c-0c68a11d244a" />
dfs=df[df['num_episodes']>20]
dfs
<img width="901" height="821" alt="image" src="https://github.com/user-attachments/assets/bdcaf639-8dde-4b82-b228-e337c1656b57" />
<img width="872" height="267" alt="image" src="https://github.com/user-attachments/assets/2fe84529-737d-456c-bb3b-96eb0ad8ff42" />
df.fillna(0)
<img width="922" height="761" alt="image" src="https://github.com/user-attachments/assets/a6669521-7445-4675-bf0b-6dd4eb528c69" />
dfs=df[df['show_name'].str.startswith(('A','F'))&(df['num_episodes']>25)]
dfs
<img width="903" height="223" alt="image" src="https://github.com/user-attachments/assets/4539f553-c527-4d7b-b832-36150f73e542" />
df.iloc[:3]
<img width="923" height="256" alt="image" src="https://github.com/user-attachments/assets/caccc4fc-84a7-46d2-95da-727e9b4430fb" />
df.iloc[:4]
<img width="932" height="360" alt="image" src="https://github.com/user-attachments/assets/7d522a59-ac7f-488f-8ae4-dcdbcb7956b4" />


df.iloc[[1,3,5],[1,3,5]]
<img width="500" height="208" alt="image" src="https://github.com/user-attachments/assets/d739bd85-7056-4471-a1b7-9f9e45dac466" />
df.fillna('sample value')
<img width="947" height="740" alt="image" src="https://github.com/user-attachments/assets/56d4383a-cea7-4411-a802-1c9d4cad07cf" />
ffil=df.fillna(method='ffill')
ffil
<img width="907" height="771" alt="image" src="https://github.com/user-attachments/assets/d8777a41-643e-4403-82bf-32e6d5cab67f" />
bfil=df.fillna(method='bfill')
bfil
<img width="918" height="757" alt="image" src="https://github.com/user-attachments/assets/e500a996-8135-442f-b596-91af7bcf8451" />
m=df.num_episodes.mean()
m
<img width="210" height="62" alt="image" src="https://github.com/user-attachments/assets/8f8a1b1d-cc71-4d2a-bb6e-bba983099f74" />
m=df.fillna(df['num_episodes'].mean())
m

            



           
# Result
          <<include your Result here>>
