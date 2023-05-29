# Ex-04 Multivariate analysis

## AIM
  To do multivariate analysis on the given dataset
 
## ALGORITHM
 ### STEP 1
 
 Read the dataset
 
 ### STEP 2
 
 Get the data types of each column
 
 ### STEP 3
 
 Do multivariate analysis using heatmap and correlation function
 
 ### STEP 4
 
 Print the result
 
 ## CODE
 
import pandas as pd

df=pd.read_csv('/content/SuperStore.csv')

df.head()

df.dtypes

df.corr()

import seaborn as sns

sns.heatmap(df.corr(),annot=True)

import matplotlib.pyplot as plt

states=df.loc[:,["State","Postal Code"]]

states=states.groupby(by=["State"]).sum().sort_values(by="Postal Code")

plt.figure(figsize=(10,7))

sns.barplot(x=states.index,y="Postal Code",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("STATE")

plt.ylabel=("POSTAL CODE")

plt.show()

## OUTPUT

![op1](https://user-images.githubusercontent.com/112301582/231126358-ab07afe8-10fa-4618-9f84-510ce9494c41.png)

![op2](https://user-images.githubusercontent.com/112301582/231126396-72e4d98d-f8c7-4fdd-b00b-50b81d305cb4.png)

![op3](https://user-images.githubusercontent.com/112301582/231126407-fda3880b-0bff-40e0-bfe1-b7f686207176.png)

![op4](https://user-images.githubusercontent.com/112301582/231126414-e95fa628-ac7d-45d1-8cab-b50f76896e2f.png)

![op5](https://user-images.githubusercontent.com/112301582/231126420-ab066681-240f-4b65-9cc7-80c486493616.png)

## RESULT
   
   Thus the multivariate analysis on the given dataset is done successfully.


