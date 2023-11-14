#   Implementation-of-SVM-For-Spam-Mail-Detection
## AIM:
To write a program to implement the SVM For Spam Mail Detection.
## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1. Import the necessary packages.
2. Read the given csv file and display the few contents of the data.
3. Assign the features for x and y respectively.
4. Split the x and y sets into train and test sets.
5. Convert the Alphabetical data to numeric using CountVectorizer.
6. Predict the number of spam in the data using SVC (C-Support Vector Classification) method of SVM (Support vector machine) in sklearn library.
7. Find the accuracy of the model.


## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: S Ashwinkumar
RegisterNumber:  212222040020

import chardet
file='/content/spam (1).csv'
with open(file, 'rb') as rawdata:
     print('Result output')
    result = chardet.detect(rawdata.read(10000))
result
import pandas as pd
data=pd.read_csv("/content/spam (1).csv",encoding="windows-1252")
print("Data Head ")
data.head()
print("data info")
data.info()
print("data.isnull()")
data.isnull().sum()
x=data["v1"].values
y=data["v2"].values
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
print("y_pred")
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
print("accuracy")
accuracy
*/
```

## Output:

1. data.head():
![Screenshot 2023-10-31 154459](https://github.com/arun1111j/Implementation-of-SVM-For-Spam-Mail-Detection/assets/128461833/968d89bc-0906-4928-a115-637da7c115d1)

2. data.info():
![Screenshot 2023-10-31 154610](https://github.com/arun1111j/Implementation-of-SVM-For-Spam-Mail-Detection/assets/128461833/3838a508-d25a-408f-ae70-5ce4155403ee)


3.data.isnull().sum():
![Screenshot 2023-10-31 154627](https://github.com/arun1111j/Implementation-of-SVM-For-Spam-Mail-Detection/assets/128461833/726443d4-9135-4aeb-b3c6-6d988525e73f)


4. Y_prediction Value:
![image](https://github.com/arun1111j/Implementation-of-SVM-For-Spam-Mail-Detection/assets/128461833/8b76ea17-c8b5-45f2-a312-15744521b4f7)


5. Accuracy Value:
![image](https://github.com/arun1111j/Implementation-of-SVM-For-Spam-Mail-Detection/assets/128461833/9c10b30f-cc21-4146-8134-a19b63ed41f0)




## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
