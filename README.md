<H3>ENTER YOUR NAME: Pochi reddy </H3>
<H3>ENTER YOUR REGISTER NO: 212223240115</H3>
<H3>EX. NO.1</H3>
<H3>DATE</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
~~~
import numpy as np
import pandas as pd
from  sklearn.preprocessing   import MinMaxScaler
from sklearn.model_selection import train_test_split
df = pd.read_csv('Crop_recommendation_expanded.csv')
df.head()
df.info()
df.describe()
df.isnull().sum()
df.duplicated()
df  = df.drop(columns = ['label'])
scalar = MinMaxScaler()
df1 = pd.DataFrame(scalar.fit_transform(df))
df1.head()
X = df1.iloc[:,:-1]
Y = df1.iloc[:,-1]
x_train,x_test,y_train,y_test =train_test_split(X, Y, test_size=0.2, random_state=42)


~~~


## OUTPUT:
![image](https://github.com/user-attachments/assets/0074ce92-7adf-406f-9a51-c57487face49)
![image](https://github.com/user-attachments/assets/9248d85b-
![image](https://github.com/user-attachments/assets/c891d30d-5193-49a5-b40b-8b8e96ac663f)

![image](https://github.com/user-attachments/assets/24613e4f-c957-430f-820c-7594d0f8fa07)




## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


