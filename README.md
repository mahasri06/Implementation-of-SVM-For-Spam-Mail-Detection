# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: 
RegisterNumber:  
*/
```
```
import chardet
file='C:/Users/admin/Downloads/printed pdfs/spam.csv'
with open(file, 'rb') as rawdata:
    result = chardet.detect(rawdata.read(100000))
result

import pandas as pd
data=pd.read_csv('C:/Users/admin/Downloads/printed pdfs/spam.csv',encoding="Windows-1252")

data.head()

data.info()

data.isnull().sum()

x=data["v1"].values

y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()

x_train = cv.fit_transform(x_train)
x_test = cv.transform(x_test)

from sklearn.svm import SVC
svc = SVC()
svc.fit(x_train, y_train)
y_pred = svc.predict(x_test)
y_pred
```

## Output:
### head():
![image](https://github.com/Sajetha13/Implementation-of-SVM-For-Spam-Mail-Detection/assets/138849316/46045a38-22c7-4957-b31b-caa5a67c0077)
### info():
![image](https://github.com/Sajetha13/Implementation-of-SVM-For-Spam-Mail-Detection/assets/138849316/e0ca8e5e-04fe-4d38-823d-e5f2e29cb4cd)
### isnull().sum():
![image](https://github.com/Sajetha13/Implementation-of-SVM-For-Spam-Mail-Detection/assets/138849316/5b39b86e-f4ac-4a31-bfa7-450a013de026)

### predicated values:
![image](https://github.com/Sajetha13/Implementation-of-SVM-For-Spam-Mail-Detection/assets/138849316/c2cedf4c-ad25-4a36-894c-5aee73795752)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
