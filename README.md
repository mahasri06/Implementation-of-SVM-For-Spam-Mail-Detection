# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Data Preparation: Load and handle the dataset, separating features and target variables.
2. Data Splitting: Split the dataset into training and testing sets.
3. Feature Engineering: Transform text data into numerical feature vectors.
4. Model Building and Evaluation: Initialize SVM classifier, train the model, and predict target labels for evaluation.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: S.Sajetha
RegisterNumber: 212223100049 
*/
```
```
import pandas as pd
data=pd.read_csv('C:/Users/admin/Downloads/printed pdfs/spam.csv',encoding="Windows-1252")
from sklearn.model_selection import train_test_split

data

data.shape

x=data['v2'].values

y=data['v1'].values

x.shape

y.shape

x_train, x_test, y_train, y_test = train_test_split(x,y,test_size=0.35, random_state=0)

x_train

x_train.shape

from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()

x_train = cv.fit_transform(x_train)
x_test = cv.transform(x_test)

from sklearn.svm import SVC

svc=SVC()

svc.fit(x_train, y_train)

y_pred=svc.predict(x_test)

y_pred

from sklearn.metrics import accuracy_score, confusion_matrix, classification_report

acc=accuracy_score(y_test, y_pred)
acc

con=confusion_matrix(y_test,y_pred)
print(con)

cl=classification_report(y_test,y_pred)
print(cl)
```

## Output:
### data:
![image](https://github.com/Sajetha13/Implementation-of-SVM-For-Spam-Mail-Detection/assets/138849316/0a86ceb6-1c87-4108-a09b-7172f60caed3)

### data.shape:
![image](https://github.com/Sajetha13/Implementation-of-SVM-For-Spam-Mail-Detection/assets/138849316/b94e824f-74ab-48e3-8ac7-2aead572c4b4)
### x_shape:
![image](https://github.com/Sajetha13/Implementation-of-SVM-For-Spam-Mail-Detection/assets/138849316/63dd570e-9992-472b-a2de-c66c7a86c836)

### y_shape:
![image](https://github.com/Sajetha13/Implementation-of-SVM-For-Spam-Mail-Detection/assets/138849316/85f0aa79-3cbc-4f2a-b84b-16d3f5956b89)

### x_train:
![image](https://github.com/Sajetha13/Implementation-of-SVM-For-Spam-Mail-Detection/assets/138849316/9cce3e36-5496-4282-9255-882010f62405)

### x_train.shape:
![image](https://github.com/Sajetha13/Implementation-of-SVM-For-Spam-Mail-Detection/assets/138849316/f586b0ec-d30b-4fa5-9c0c-94b3daf8c19a)

### y_pred:
![image](https://github.com/Sajetha13/Implementation-of-SVM-For-Spam-Mail-Detection/assets/138849316/000a6f61-9369-4c80-8755-fb9c2cf83459)

### accuracy:
![image](https://github.com/Sajetha13/Implementation-of-SVM-For-Spam-Mail-Detection/assets/138849316/923d92dd-5af8-4c68-b2bb-f3c1a3d41b9b)

### confusion matrix:
![image](https://github.com/Sajetha13/Implementation-of-SVM-For-Spam-Mail-Detection/assets/138849316/265e3ddd-3790-425e-972b-b52059b10e99)

### classification report:
![image](https://github.com/Sajetha13/Implementation-of-SVM-For-Spam-Mail-Detection/assets/138849316/5d5e0cfb-97be-4ad3-9eb9-13c756f82ea7)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
