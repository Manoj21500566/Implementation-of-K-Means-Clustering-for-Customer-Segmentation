# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
~~~
1.Import pandas and matplot libraries.
2.import Kmeans algorithm to solve customer segmentation.
3.Using the for loop cluster the given data
4.Predict the output and plot data graphs.
5.Display the outputs
~~~
## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Manoj M
RegisterNumber:  212221240027
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("Mall_Customers.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wess=[]
for i in range(1,11):
  kmeans=KMeans(n_clusters=i,init="k-means++")
  kmeans.fit(data.iloc[:,3:])
  wess.append(kmeans.inertia_)
plt.plot(range(1,11),wess);
plt.xlabel("no of clusters")
plt.ylabel("wess")
plt.title("elbow method")
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
y_pred=km.predict(data.iloc[:,3:])
data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income"],df0["Score"],c="red",label="cluster0")
plt.scatter(df1["Annual Income"],df1["Score"],c="black",label="cluster1")
plt.scatter(df2["Annual Income"],df2["Score"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income"],df3["Score"],c="green",label="cluster3")
plt.scatter(df4["Annual Income"],df4["Score"],c="red",label="cluster4")
plt.legend()
plt.title("Customer Segments")
*/
```

## Output:
DATA.HEAD()



![1](https://user-images.githubusercontent.com/94588708/173183785-7e200c94-32d6-4a42-9c37-daf220668096.png)



DATA.INFO()




![2](https://user-images.githubusercontent.com/94588708/173183801-c8d17c9f-c9e2-480d-934e-e351b34fe9cb.png)

![3](https://user-images.githubusercontent.com/94588708/173183814-3f79336b-9c41-44b5-a962-9697a674d5c2.png)

![4](https://user-images.githubusercontent.com/94588708/173183824-419e2ae8-6013-4dc9-99fd-79d95ff1699e.png)










## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
