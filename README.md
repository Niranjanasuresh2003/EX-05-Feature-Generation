# EX-05-Feature-Generation


## AIM

To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation

Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 

# ALGORITHM

### STEP 1

Read the given Data

### STEP 2

Clean the Data Set using Data Cleaning Process

### STEP 3

Apply Feature Generation techniques to all the feature of the data set

### STEP 4
Save the data to the file


# CODE
~~~
data.csv
import pandas as pd   
import seaborn as sbn 
df=pd.read_csv("/content/data.csv") 
df.info() 
df.isnull().sum()
from sklearn.preprocessing import LabelEncoder 
le = LabelEncoder() 
df['Ord_2'] = le.fit_transform(df['Ord_2']) 
sbn.set(style ="darkgrid") 
sbn.countplot(df['Ord_2'])
from sklearn.preprocessing import OneHotEncoder 
enc = OneHotEncoder() 
enc = enc.fit_transform(df[['City']]).toarray() 
encoded_colm = pd.DataFrame(enc) 
df = pd.concat([df, encoded_colm], axis=1) 
df = df.drop(['City'], axis=1) 
df.head(10) 
df = pd.get_dummies(df, prefix=['Ord_2'], columns=['Ord_2']) 
df.head(10) 
df = pd.get_dummies(df, prefix=['Ord_1'], columns=['Ord_1']) 
df.head(10)
~~~
# encoding.csv
~~~
import pandas as pd 
import seaborn as sbn 
data=pd.read_csv("/content/Encoding Data.csv") 
data.info() 
data.isnull().sum() from sklearn.preprocessing import LabelEncoder 
le = LabelEncoder() data['ord_2'] = le.fit_transform(data['ord_2']) 
sbn.set(style ="darkgrid") 
sbn.countplot(data['ord_2']) from sklearn.preprocessing import OneHotEncoder 
en = OneHotEncoder() 
en = en.fit_transform(data[['nom_0']]).toarray() 
encoded_colm = pd.DataFrame(en) 
data= pd.concat([data, encoded_colm], axis=1) 
data= data.drop(['nom_0'], axis=1) 
data.head(10) 
data = pd.get_dummies(df, prefix=['bin_2'], columns=['bin_2']) 
data.head(10)
~~~
# titanic.csv
~~~
import pandas as pd 
import seaborn as sbn 
dt=pd.read_csv("/content/titanic_dataset.csv") 
dt.info() 
dt.isnull().sum() 
dt['Age']=dt['Age'] . fillna(dt ['Age'].mean()) 
dt ['Cabin']=dt['Cabin']. fillna(dt['Cabin']. mode() [0]) 
dt ['Embarked']=dt['Embarked'] . fillna(df ['Embarked'].mode( )[0]) 
dt.isnull().sum( ) from sklearn.preprocessing import LabelEncoder 
lc = LabelEncoder() 
df['Sex'] = lc.fit_transform(df['Sex']) 
sbn.set(style ="darkgrid") 
sbn.countplot(df['Sex']) from sklearn.preprocessing import OneHotEncoder 
enc= OneHotEncoder() 
enc= enc.fit_transform(dt[['Name']]).toarray() 
encoded_colm = pd.DataFrame(enc) 
dt= pd.concat([dt, encoded_colm], axis=1) 
dt= dt.drop(['Name'], axis=1) 
dt.head(10) 
dt = pd.get_dummies(dt, prefix=['Ticket'] ,columns=['Ticket']) 
df.head(10) 
dt = pd.get_dummies(dt, prefix=['Embarked'] ,columns=['Embarked']) 
df.head(10)
~~~

# OUPUT

# Data.csv

![image](https://user-images.githubusercontent.com/129851738/232754878-c1b1ac80-2180-43cd-9da8-369514288729.png)


![image](https://user-images.githubusercontent.com/129851738/232754982-6d9c8a13-d3a4-47a6-ac63-77742332bddf.png)


![image](https://user-images.githubusercontent.com/129851738/232755061-2eeba20c-0a64-4011-82a8-fdf114636668.png)

![image](https://user-images.githubusercontent.com/129851738/232755142-8a2f6df2-3900-46ce-8b83-c785e9f602bf.png)

![image](https://user-images.githubusercontent.com/129851738/232755229-9077990b-b98d-4953-bfe3-0f6d8bb8667b.png)

# Encoding.csv

![image](https://user-images.githubusercontent.com/129851738/232755352-5e2c37b6-269a-4a72-835b-b60dea4a38a4.png)

![image](https://user-images.githubusercontent.com/129851738/232755415-c1e7d49b-ca55-411c-88eb-e3e1b5e03c37.png)

![image](https://user-images.githubusercontent.com/129851738/232755460-a22b4d45-015f-450d-8631-d99a0f79ea84.png)

![image](https://user-images.githubusercontent.com/129851738/232755504-91239857-e900-45a3-850a-911d33e6332f.png)


# Titanic.csv

![image](https://user-images.githubusercontent.com/129851738/232755610-9a6dbfcf-69ec-4f53-9bd6-cbbffc0a0c24.png)

![image](https://user-images.githubusercontent.com/129851738/232755670-9f2d0f05-0fc8-4373-bca1-016c6e7fa3d4.png)

![image](https://user-images.githubusercontent.com/129851738/232755722-5b741a61-f8df-4fd8-97c2-2701368b6ecf.png)

![image](https://user-images.githubusercontent.com/129851738/232755753-a70b3c2a-fbe0-45df-bf1d-8e96ea19bf50.png)

![image](https://user-images.githubusercontent.com/129851738/232755795-c25b0f57-fc62-4545-9735-6c25b63adf70.png)
![image](https://user-images.githubusercontent.com/129851738/232755831-69efe4c1-11e5-4d8e-a268-3abec3586595.png)

# RESULT:

Thus the program for Feature Generation is executed successfully.
