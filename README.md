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
df=pd.read_csv("/content/Churn_Modelling (1).csv",index_col="RowNumber")        
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
![Screenshot 2025-03-07 113629](https://github.com/user-attachments/assets/e79fb6c7-9d38-4a15-b839-8fdbf5e85360)
![Screenshot 2025-03-07 113732](https://github.com/user-attachments/assets/36f71788-5206-4fc9-b0b4-01053f93a510)
![Screenshot 2025-03-07 113811](https://github.com/user-attachments/assets/0d24aa4f-4ed8-48c1-9440-d7f9f0e51aa1)
![Screenshot 2025-03-07 113858](https://github.com/user-attachments/assets/92696038-bc73-4b7e-89a7-e713356e6fff)
![Screenshot 2025-03-07 113939](https://github.com/user-attachments/assets/29545581-80de-44da-8649-5dcc86084dad)



## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


