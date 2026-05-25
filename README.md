# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Data Preparation: Load and explore customer data.
 2.Determine Optimal Clusters: Use the Elbow Method to find the best number of clusters.
3.Apply K Means Clustering: Perform clustering on customer data.
4.Visualize Segmented Customers: Plot clustered data to visualize customer segments. 

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: SATHISH S
RegisterNumber:  212225040390
import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv(r"C:\College\SEM 2\Machine Learning\Exp10\Mall_Customers.csv")

print(data.head())

print(data.info())

data.isnull().sum()

from sklearn.cluster import KMeans
wcss = []

for i in range(1,11):
    kmeans = KMeans(n_clusters = i,init = "k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss)
plt.xlabel("No of Cluster")
plt.ylabel("wcss")
plt.title("Elbow Method")
plt.figure()

km = KMeans(n_clusters = 5)
km.fit(data.iloc[:,3:])

KMeans(n_clusters=5)

y_pred = km.predict(data.iloc[:,3:])
print("Predicted values: \n",y_pred)

data["cluster"]=y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segments")
plt.show()
*/

```

## Output:
<img width="692" height="128" alt="596604329-a57b17f9-ea3d-4426-87dd-08b0bb7269b1" src="https://github.com/user-attachments/assets/c0ff4c91-138f-4cba-a57e-35b4c79a35ac" />
<img width="692" height="128" alt="596604406-bd1a5c1f-0852-4c11-9e83-9440ce8ad489" src="https://github.com/user-attachments/assets/40bec644-19bf-4d50-ada6-c5c5f0d2c7fc" />
<img width="717" height="157" alt="596604465-173524b3-5372-4bf9-b7e5-ef2eee608a01" src="https://github.com/user-attachments/assets/060920ee-b5f4-4c0c-8480-2bb585d4722b" />
ELBOW METHOD:
<img width="640" height="480" alt="596604870-aa26486b-f9fd-4af9-baec-a4e2435a12cf" src="https://github.com/user-attachments/assets/62448eb6-0d76-4a6d-ab30-ad0da54f6078" />
CLUSTER SEGMENTATION:
<img width="640" height="480" alt="596604992-0986a0cc-fe64-4521-8275-edcd2f79e92d" src="https://github.com/user-attachments/assets/0b9cee63-50ac-4c3b-9c85-5a8dab28426f" />



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
