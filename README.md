# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import required libraries (pandas, chardet, sklearn, etc.).
2. Detect the encoding of the CSV file using chardet.
3. Read the CSV file with the correct encoding.
4. Check the data for structure and missing values.
5. Split the data into input (x = messages) and output (y = labels).\
6. Divide the data into training and testing sets.
7. Convert text data into numbers using CountVectorizer.
8. Train an SVM model, make predictions, and calculate accuracy.

Program:

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: ANTONY ABISHEK K
RegisterNumber:  212223240009
*/
```
```
/*

import chardet
file='spam.csv'
with open(file,'rb')as rawdata:
    result=chardet.detect(rawdata.read(100000))
result

import pandas as pd
data=pd.read_csv("spam.csv",encoding='windows-1252')
data.head()

data.info()

data.isnull().sum()

x=data["v2"].values
y=data["v1"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy 
*/
```
## Output:
### Result output
<img width="1243" height="38" alt="image" src="https://github.com/user-attachments/assets/e075e245-3a7e-45cc-907e-7b3d0cb26893" />
### data.head()
<img width="1243" height="227" alt="image" src="https://github.com/user-attachments/assets/9332b302-3217-43d1-902b-59aca2288fbc" />
### data.info()
<img width="1231" height="257" alt="image" src="https://github.com/user-attachments/assets/5aa2950a-c3f5-459e-bc34-c03e6c6d549b" />
### data.isnull().sum()
<img width="1243" height="37" alt="image" src="https://github.com/user-attachments/assets/86e95e18-79ce-448d-b711-d130d86b58e8" />
### y_pred
<img width="1231" height="130" alt="image" src="https://github.com/user-attachments/assets/2c2cc4ac-bda8-4d67-92bb-05c81159a3ba" />
### accuracy()
<img width="1243" height="38" alt="image" src="https://github.com/user-attachments/assets/bfd1c408-9afd-4a22-812f-a89e611d43ed" />

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
