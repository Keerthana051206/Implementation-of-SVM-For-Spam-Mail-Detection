# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the packages.

2.Analyse the data.

3.Use modelselection and Countvectorizer to preditct the values.

4.Find the accuracy and display the result. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: KEERTHANA C
RegisterNumber: 212224220047 
*/
```
```
import pandas as pd
data=pd.read_csv("spam.csv", encoding='Windows-1252')
data

data.shape

x=data['v2'].values
y=data['v1'].values
x.shape

y.shape

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2, random_state=0)
x_train

x_train.shape
```
```
from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn.metrics import accuracy_score,confusion_matrix,classification_report
acc=accuracy_score(y_test,y_pred)
acc

con=confusion_matrix(y_test,y_pred)
print(con)

cl=classification_report(y_test,y_pred)
print(cl)
```

## Output:
DATA


<img width="917" height="502" alt="image" src="https://github.com/user-attachments/assets/3d3bd5be-35d8-4422-8fc7-ca08d74938d6" />

DATA.SHAPE()


<img width="112" height="38" alt="image" src="https://github.com/user-attachments/assets/49cab307-abcd-4e72-9985-3d85087c5c99" />

X.SHAPE()


<img width="90" height="32" alt="image" src="https://github.com/user-attachments/assets/e796509a-38da-4b9e-a4a3-05b6d4d0024d" />

Y.SHAPE()


<img width="117" height="35" alt="image" src="https://github.com/user-attachments/assets/cbc717b5-ee31-4423-9b2d-decb25dd1499" />

X_TRAIN


<img width="1373" height="220" alt="image" src="https://github.com/user-attachments/assets/6eb53f09-ae6d-46cb-8858-548d79f87253" />

X_TRAIN.SHAPE()


<img width="117" height="32" alt="image" src="https://github.com/user-attachments/assets/4b24cfa1-76a1-4c57-9c82-4a29b4f4d418" />

Y_PRED


<img width="681" height="42" alt="image" src="https://github.com/user-attachments/assets/5654999d-05d9-4ea5-8dad-15a8627bec67" />

ACC(ACCURACY)


<img width="237" height="38" alt="image" src="https://github.com/user-attachments/assets/d2a8faa1-2803-4e32-a696-42953c9efb5f" />

CON (CONFUSION MATRIX)


<img width="125" height="48" alt="image" src="https://github.com/user-attachments/assets/b0919d79-8c4f-48ea-a515-3e66ffd3c0da" />

CL (CLASSIFICATION REPORT)


<img width="532" height="175" alt="image" src="https://github.com/user-attachments/assets/fe11bf7b-c9b0-4faf-bf82-a1e4b48a983e" />

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
