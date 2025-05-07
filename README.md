# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas and matplotlib.pyplot
2. Read the dataset and transform it
3. Import KMeans and fit the data in the model
4. Plot the Cluster graph
## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Hanshika Varthini R
RegisterNumber: 212223240046

import pandas as pd
 import matplotlib.pyplot as plt
 data = pd.read_csv("Mall_Customers.csv")
 data.head()
 data.info()
 data.isnull().sum()


 from sklearn.cluster import KMeans
 wcss = []
 for i in range(1,11):
     kmeans = KMeans(n_clusters = i,init = "k-means++")
     kmeans.fit(data.iloc[:,3:])
     wcss.append(kmeans.inertia_)


 plt.plot(range(1,11),wcss)
 plt.xlabel("No. of Clusters")
 plt.ylabel("wcss")
 plt.title("Elbow Method")


 km = KMeans(n_clusters = 5)
 km.fit(data.iloc[:,3:])
 KMeans(n_clusters=5)
 y_pred = km.predict(data.iloc[:,3:])
 y_pred


 data["cluster"] = y_pred
 df0 = data[data["cluster"]==0]
 df1 = data[data["cluster"]==1]
 df2 = data[data["cluster"]==2]
 df3 = data[data["cluster"]==3]
 df4 = data[data["cluster"]==4]
 plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster")
 plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster")
 plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster")
 plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster")
 plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster")
 plt.legend()
 plt.title("Customer Segments")
*/
```

## Output:
![Screenshot 2025-05-07 091743](https://github.com/user-attachments/assets/cbbea73b-5525-4f98-bd6b-a5655d4227ff)
![Screenshot 2025-05-07 091817](https://github.com/user-attachments/assets/7d670c3a-f91f-49fd-9896-171f08ceb476)
![399780135-f2f12774-3974-4d6e-81bd-77f734dc5f3f](https://github.com/user-attachments/assets/cd4aa26a-f227-40d7-81fc-986a4efb53ae)
![Screenshot 2025-05-07 091855](https://github.com/user-attachments/assets/06bdfaf1-fa07-4200-ba18-728854fec7e0)


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
