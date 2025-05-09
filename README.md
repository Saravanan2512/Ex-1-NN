<H3>ENTER YOUR NAME : Saravanan G</H3>
<H3>ENTER YOUR REGISTER NO : 212223230194</H3>
<H3>EX. NO.1</H3>
<H3>DATE:10/03/2025</H3>
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
### DATASET:
```
import pandas as pd                                               
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
df=pd.read_csv("Churn_Modelling.csv",index_col="RowNumber")        
df.head()

```
### NULL VALUES:
```
df.isnull().sum()
```
### NORMALIZED DATA:

```
df=df.drop(['Surname', 'Geography','Gender'], axis=1)              
scaler=StandardScaler()                                             
df=pd.DataFrame(scaler.fit_transform(df))
df.head()
```

### DATA SPLITTING:
```
X,Y=df.iloc[:,:-1].values ,df.iloc[:,-1].values                     
print('Input:\n',X,'\nOutput:\n',Y)
```

### TRAIN AND TEST DATA:
```
Xtrain,Xtest,Ytrain,Ytest = train_test_split(X, Y, test_size=0.2)  
print("Xtrain:\n" ,Xtrain, "\nXtest:\n", Xtest)                     
print("\nYtrain:\n" ,Ytrain, "\nYtest:\n", Ytest)
```


## OUTPUT:
![image](https://github.com/user-attachments/assets/94e3b87a-0ebc-4c28-be53-69578d9e8143)
![image](https://github.com/user-attachments/assets/75ca120d-5c74-4bf8-af8c-444128653e77)
![image](https://github.com/user-attachments/assets/d02ab751-dbbc-462e-ae69-899aa96d51ef)
![image](https://github.com/user-attachments/assets/d2ba9ece-eebf-44fc-8c10-8c7181cd721c)
![image](https://github.com/user-attachments/assets/525a1068-a8d1-4435-93b6-50046324f45e)




## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


