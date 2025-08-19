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
<img width="940" height="762" alt="image" src="https://github.com/user-attachments/assets/14e5b8c1-ad25-4be0-b0fd-2d40892ce988" />
fmean=df['lifetime_popularity_rank'].fillna(value=df['lifetime_popularity_rank'].mean())
fmean
<img width="741" height="322" alt="image" src="https://github.com/user-attachments/assets/5babfacb-bac9-437e-8666-290420ff5cd1" />
df=pd.read_csv("C:\\Users\\Pandiyan\\Downloads\\SAMPLEIDS.csv")
df
<img width="932" height="823" alt="image" src="https://github.com/user-attachments/assets/4cba89c8-15c7-4082-bad4-085d51554ee8" />
<img width="917" height="277" alt="image" src="https://github.com/user-attachments/assets/c1c488d9-a1c9-4c94-a5f1-b911c82f2c50" />
df.shape
<img width="167" height="55" alt="image" src="https://github.com/user-attachments/assets/6a3a54ca-7a61-450a-ba5b-23654eaf1a8e" />

df.describe()
<img width="871" height="388" alt="image" src="https://github.com/user-attachments/assets/7d5cbf82-ddb1-471c-997d-9adf1b09601f" />
df.info()
<img width="533" height="427" alt="image" src="https://github.com/user-attachments/assets/13e115fc-0fe4-4fd8-be5f-1e3ce0b8f27f" />
df['GENDER'].value_counts()
 <img width="342" height="145" alt="image" src="https://github.com/user-attachments/assets/08aa5eca-eb6c-44ce-bce1-6893c5dc5c69" />
           

df.dropna(how='any').shape
<img width="177" height="75" alt="image" src="https://github.com/user-attachments/assets/e754234f-edd1-42b0-bb12-b0d6e38671ce" />


x1=df.dropna(how='any')
x1
<img width="917" height="742" alt="image" src="https://github.com/user-attachments/assets/ddd21b53-0da8-4b4d-9e26-0987fc270af3" />
res=df.dropna(subset=['M1','M2','M3','M4'],how='any')
res
<img width="937" height="765" alt="image" src="https://github.com/user-attachments/assets/79bd3e3d-a566-4d49-a898-0bf29d8fc9cf" />
m2=df.TOTAL.mean()
m2
<img width="262" height="71" alt="image" src="https://github.com/user-attachments/assets/7141ac47-499d-4d86-bdbb-8b0e35f45305" />
df.isnull()
<img width="893" height="832" alt="image" src="https://github.com/user-attachments/assets/f83d8d7b-cbe8-4afe-879d-d086589d5172" />


df.TOTAL.fillna(m2,inplace=False)
<img width="362" height="512" alt="image" src="https://github.com/user-attachments/assets/5afe7a87-4cfa-4dd1-ba23-bc150a7d63b2" />
import seaborn as sns
sns.heatmap(df.isnull(),yticklables=False,annot=True)
<img width="932" height="611" alt="image" src="https://github.com/user-attachments/assets/1648139e-90d2-4600-ad76-1ac4d10e8fb2" />
sns.heatmap(df.isnull(),yticklables=True,annot=True)
<img width="932" height="611" alt="image" src="https://github.com/user-attachments/assets/6f2a3a35-006a-4f6b-9ef7-e4203f4ba463" />
df.dropna(inplace=True)
sns.heatmap(df.isnull(),yticklables=False,annot=True)
<img width="845" height="558" alt="image" src="https://github.com/user-attachments/assets/431243ca-c56e-4150-b362-63c4cbd10c62" />
import scipy.stats as stats
df=pd.read_csv("C:\\Users\\Pandiyan\\Downloads\\heights.csv")
df
<img width="263" height="645" alt="image" src="https://github.com/user-attachments/assets/350347fa-0213-4fc3-a59d-893d451ff5d7" />
sns.boxplot(data=df)
<img width="737" height="552" alt="image" src="https://github.com/user-attachments/assets/a9d66134-cdb9-4eaf-800f-f25828e1d832" />


sns.scatterplot(data=df)
<img width="772" height="583" alt="image" src="https://github.com/user-attachments/assets/f4f0a04c-b549-4ab3-b8ff-a3e33f0c5e72" />


max=df['height'].quantile(0.75)
min=df['height'].quantile(0.25)
iqr=max-min
iqr 
<img width="376" height="160" alt="image" src="https://github.com/user-attachments/assets/a647cb9c-ee05-4ba9-bf8f-0838d0a25de3" />


lb=min-1.5*iqr
ub=max+1.5*iqr
outliers=df[(df['height']<lb)|(df['height']>ub)]
print("Lower bound:",lb)
print("Upper bound:",ub)
print("Outliers:",outliers)
<img width="353" height="143" alt="image" src="https://github.com/user-attachments/assets/ca17f507-bb1c-4b1e-bdf8-f62a0dd1dcee" />
no_outliers=df[~((df['height']<lb)|(df['height']>ub))]
no_outliers
<img width="397" height="587" alt="image" src="https://github.com/user-attachments/assets/79e31e6d-94a4-4a6c-9446-cee60775ebc9" />
<img width="354" height="404" alt="image" src="https://github.com/user-attachments/assets/b742a9c4-5fc3-4439-a03e-2790bb398fc7" />
<img width="627" height="351" alt="image" src="https://github.com/user-attachments/assets/0b2e53b6-fde2-4af9-af65-1af913210820" />
<img width="676" height="325" alt="image" src="https://github.com/user-attachments/assets/33355254-67b7-4ad7-aac2-75ed8b8f109a" />


# Result
          <<include your Result here>>
