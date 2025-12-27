# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
<img width="1249" height="571" alt="image" src="https://github.com/user-attachments/assets/c05ce556-94af-47db-9a16-0561790c9ea9" />

df=sns.load_dataset("tips")
df
<img width="1256" height="460" alt="image" src="https://github.com/user-attachments/assets/23a38c75-1c8f-475d-ae7b-8c96358a5e42" />

sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
<img width="1252" height="597" alt="image" src="https://github.com/user-attachments/assets/6f04813e-f5aa-42f0-8e3f-50ffd7b0eaad" />

s=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title("Multi-Line plot")
plt.xlabel('x Label')
plt.ylabel('Y Label')
<img width="1253" height="629" alt="image" src="https://github.com/user-attachments/assets/a22bcda3-0c2f-490c-b53d-492d7857f0aa" />

import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill and tip by day')
<img width="1250" height="742" alt="image" src="https://github.com/user-attachments/assets/1131ac71-974f-4fc8-8439-67498d87bf86" />

avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)
plt.xlabel('Time of day')
plt.ylabel('Amount')
plt.title('Average Total Bill and tip by time of day')
plt.legend()
<img width="1247" height="620" alt="image" src="https://github.com/user-attachments/assets/da80945a-66a7-41b1-abb7-a04f4b006f8e" />

years=range(2000,2012)
apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]
oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896,]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
<img width="1246" height="575" alt="image" src="https://github.com/user-attachments/assets/e65437da-9b69-41f0-9098-1d2c270fbd03" />

import seaborn as sns
dt=sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='cool')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by day and gender')
<img width="1249" height="624" alt="image" src="https://github.com/user-attachments/assets/a3aaca9e-c70a-40b3-8a38-dffef76623f5" />

import pandas as pd
tit=pd.read_csv("Titanic_dataset.csv")
tit
<img width="1244" height="456" alt="image" src="https://github.com/user-attachments/assets/30c9d87f-6269-4a80-b49c-21e2824525e4" />

plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow')
plt.title('Fare of Passenger by Embarked Town')
<img width="1249" height="647" alt="image" src="https://github.com/user-attachments/assets/54d9c881-4b2a-48f3-b239-bd6dcdd784db" />

plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow',hue='Pclass')
plt.title("Fare of Passenger by Embarked Town,Divided By class")
<img width="1245" height="638" alt="image" src="https://github.com/user-attachments/assets/7582562b-b35b-4874-b0fd-27804ed42b1e" />

import seaborn as sns
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatterplot of the total Bill vs. Tip Amount')
<img width="1252" height="614" alt="image" src="https://github.com/user-attachments/assets/e1f4696b-df27-4ba5-992a-ddadee664af2" />

import seaborn as sns
import pandas as pd
import numpy as np
np.random.seed(1)
num_var=np.random.randn(1000)
num_var=pd.Series(num_var,name="Numerical Variable")
num_var
<img width="1260" height="280" alt="image" src="https://github.com/user-attachments/assets/cf7196b7-7ece-45be-acb0-6029ac800eb9" />

sns.histplot(data=num_var,kde=True)
<img width="1247" height="603" alt="image" src="https://github.com/user-attachments/assets/bd8639fc-4df8-4223-a786-04029521e6a1" />

df=pd.read_csv("titanic_dataset.csv")
df
<img width="1251" height="460" alt="image" src="https://github.com/user-attachments/assets/823f16fd-843e-4c1f-83e9-245be905eedc" />

sns.histplot(data=df,x='Pclass',hue='Survived',kde=True)
<img width="1253" height="597" alt="image" src="https://github.com/user-attachments/assets/b0609781-ea6b-4a0b-bb63-6f63570a1fc2" />

import seaborn as sns
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
np.random.seed(0)
marks=np.random.normal(loc=70,scale=10,size=100)
marks
<img width="1248" height="449" alt="image" src="https://github.com/user-attachments/assets/af9129ac-3f80-4d40-8a16-ee2815a4ba26" />

sns.histplot(data=marks,bins=10,kde=True,stat='count',cumulative=False,multiple='stack',element='bars',palette='Set1',shrink=0.7)
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histogram of students marks')
<img width="1246" height="621" alt="image" src="https://github.com/user-attachments/assets/2d3f1d51-8817-42f2-85ac-ae7532b95edb" />

import seaborn as sns
import pandas as pd
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])
<img width="1249" height="592" alt="image" src="https://github.com/user-attachments/assets/38dba47e-a2e3-4fd7-9b48-1ed96e0a5c65" />

sns.boxplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,boxprops={"facecolor": "lightblue","edgecolor":"darkblue"},
           whiskerprops={"color":"black","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})
<img width="1256" height="579" alt="image" src="https://github.com/user-attachments/assets/256925ca-5ef4-4d3d-8a6a-f2dfbb79ad6b" />

sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age by Passenger class,Titanic")
<img width="1244" height="625" alt="image" src="https://github.com/user-attachments/assets/b69b004f-dc86-47e8-8bef-5ee21ce69c26" />

sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6)
plt.xlabel("Day of the week")
plt.ylabel("Total bill")
plt.title("Violin plot of the total bill by day and smoker status")
<img width="1254" height="620" alt="image" src="https://github.com/user-attachments/assets/bbb3992e-4690-49a2-817c-fb8f1b71b80a" />

import seaborn as sns
sns.set(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x='day',y='tip',data=tip)
<img width="1254" height="600" alt="image" src="https://github.com/user-attachments/assets/248444f1-42d3-481f-bea9-52c71c524ffd" />

import seaborn as sns
sns.set(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
<img width="1256" height="597" alt="image" src="https://github.com/user-attachments/assets/ac71e4ee-1dea-4ee2-a0a2-70712976eb5f" />

import seaborn as sns
sns.set(style='whitegrid')
tips=sns.load_dataset("tips")
sns.violinplot(x='tip',y='day',data=tip)
<img width="1253" height="596" alt="image" src="https://github.com/user-attachments/assets/28fee9c3-a104-4aac-a5fe-812e7c6971c7" />

sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
<img width="1254" height="599" alt="image" src="https://github.com/user-attachments/assets/e23b495b-590d-4074-a1e4-5360a2aec87a" />

sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='layer',linewidth=3,palette='Set2',alpha=0.8)
<img width="1253" height="604" alt="image" src="https://github.com/user-attachments/assets/6763bdbb-4433-4c31-8737-b281df87209b" />

sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set2',alpha=0.8)
<img width="1248" height="596" alt="image" src="https://github.com/user-attachments/assets/16eae437-4aa7-468c-bda6-82e8d74fd4a5" />

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
mart=pd.read_csv("supermarket.csv")
mart
<img width="1251" height="650" alt="image" src="https://github.com/user-attachments/assets/0ebd3a52-cc1b-441a-8172-621025544225" />

mart=mart[['Gender','Payment','Unit price','Quantity','Total','gross income']]
mart.head(10)

<img width="1243" height="380" alt="image" src="https://github.com/user-attachments/assets/ba689c69-8679-4ea5-b9bf-c3dc9c46913e" />

sns.kdeplot(data=mart,x='Total')
<img width="1252" height="590" alt="image" src="https://github.com/user-attachments/assets/b6c1dfdf-f5db-46d6-907b-11dcb425eb09" />

sns.kdeplot(data=mart,x='Unit price')
<img width="1256" height="609" alt="image" src="https://github.com/user-attachments/assets/1f6b5808-752d-456d-957a-733e2575193b" />

sns.kdeplot(data=mart)
<img width="1255" height="566" alt="image" src="https://github.com/user-attachments/assets/176f180b-8d27-4283-886c-d8d81670de38" />

sns.kdeplot(data=mart,x='Total',hue='Payment',multiple='stack')
<img width="1245" height="597" alt="image" src="https://github.com/user-attachments/assets/b6c818ea-e2be-454e-9d1d-29cda5fa4ac7" />

sns.kdeplot(data=mart,x='Unit price',y='gross income')
<img width="1251" height="596" alt="image" src="https://github.com/user-attachments/assets/01e23e82-d795-4eba-9e15-60fd00f38946" />

data=np.random.randint(low=1,high=100,size=(10,10))
print("The data to be plotted:\n")
print(data)
<img width="1248" height="275" alt="image" src="https://github.com/user-attachments/assets/143254cd-e9d9-48b6-8552-cffecf0aa4ee" />

hm=sns.heatmap(data=data)
<img width="1253" height="534" alt="image" src="https://github.com/user-attachments/assets/4c11e07b-1d3e-499a-be70-33c7af29103d" />

hm=sns.heatmap(data=data,annot=True)
<img width="1249" height="544" alt="image" src="https://github.com/user-attachments/assets/2a8205bc-d89e-43c0-9ae3-66ac0e3f65a7" />

import seaborn as sns
import numpy as np
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
numeric_cols=tips.select_dtypes(include=np.number).columns
corr=tips[numeric_cols].corr()
sns.heatmap(corr,annot=True,cmap='plasma',linewidth=0.5)
<img width="1249" height="578" alt="image" src="https://github.com/user-attachments/assets/5e0012f5-abf7-48a7-bf11-01f8c72b8dbd" />



# Result:
 Thus, the Data visualization using seaborn is executed successfully and the output is verified.
