# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the necessary packages (numpy, pandas, SVC, etc).
2. Load the dataset and vectorize text information using CountVectorizer()
3. Fit the data into the model.
4. Check Accuracy Score and Confusion matrix.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Gedipudi Darshani
RegisterNumber: 212223230062
*/
```
```
import pandas as pd
data=pd.read_csv("spam.csv",encoding='windows-1252')
```
### Output:

```
data.head()
```
### Output:

```
data.tail()
```
### Output:

```
data.info()
```
### Output:

```
data.isnull().sum()
```
### Output:

```
x=data['v2'].values
```
### Output:

```
y=data['v1'].values
```
### Output:

```
y.shape
```
### Output:

```
x.shape
```
### Output:

```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
```
```
x_train.shape
```
### Output:


```
y_train.shape
```
### Output:

```
from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
```
```
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
```
```
x_train.shape
```
### Output:

```
type(x_train)
```
### Output:

```
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
```
### Output:

```
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
```
### Output:


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
