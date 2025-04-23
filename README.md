# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY
```
    Name:Sanjay S
    Reg No:212224110047
```
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
    import pandas as pd
    import numpy as np
    x = [1, 2, 3, 4, 5]
    y = [3, 6, 2, 7, 1]
    sns.lineplot(x=x,y=y)
![image](https://github.com/user-attachments/assets/5d163741-1af3-41c8-805e-66cf300f2979)

    df=sns.load_dataset("tips")
    df
![image](https://github.com/user-attachments/assets/b2b993e1-a525-4049-a652-5e6a067dc35b)

    sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle="solid",legend="auto",palette="Set1")
![image](https://github.com/user-attachments/assets/1f0b51f9-b580-4457-9988-392dcb4d2e2e)

    x=[1, 2, 3, 4, 5]
    y1=[3, 5, 2, 6, 1]
    y2=[1, 6, 4, 3, 8]
    y3=[5, 2, 7, 1, 4]
    sns.lineplot(x=x, y=y1)
    sns.lineplot(x=x, y=y2)
    sns.lineplot(x=x, y=y3)
    plt.title("Multi-Line Plot")
    plt.xlabel('X Label')
    plt.ylabel("Y Label")
![image](https://github.com/user-attachments/assets/28981188-66fb-41a8-8c4a-5cea5324ef20)

    tips = sns.load_dataset("tips")
    avg_total_bill = tips.groupby("day")["total_bill"].mean()
    avg_tip=tips.groupby("day")["tip"].mean()
    plt.figure(figsize=(8,6))
    p1=plt.bar(avg_total_bill.index,avg_total_bill,label="Total Bill")
    p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label="Tip")
    plt.xlabel("Day of the week")
    plt.ylabel("Amount")
    plt.title("Average Total Bill and Tip by Day")
    plt.legend()
    plt.show()
![image](https://github.com/user-attachments/assets/dabe07ce-a7ce-44be-b70e-f2d65e6d3b20)

    avg_total_bill=tips.groupby('time')['total_bill'].mean()
    avg_tip=tips.groupby('time')['tip'].mean()
    p1=plt.bar(avg_total_bill.index,avg_total_bill,label="Total Bill",width=0.4)
    p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label="Tip",width=0.4)
    plt.xlabel("Time of the day")
    plt.ylabel("Amount")
    plt.title("Average Total Bill and Tip by Time of the Day")
    plt.legend()
![image](https://github.com/user-attachments/assets/937862d2-2c6f-4f44-998e-8341c16bc423)

    import seaborn as sns
    df=sns.load_dataset("tips")
    sns.barplot(x="day",y="total_bill",hue="sex",data=df,palette='Set3')
    plt.xlabel("Day of the week")
    plt.ylabel("Total Bill")
    plt.title("Total Bill by Day and Gender")
![image](https://github.com/user-attachments/assets/41ef572b-e21b-4a86-9c54-d6ae30bf00e3)

    import seaborn as sns
    df=sns.load_dataset("tips")
    sns.scatterplot(x="total_bill",y="tip",hue="sex",data=df,palette="Set1")
    plt.xlabel("Totsl Bill")
    plt.ylabel("Tip")
    plt.title("Scatter Plot of Total Bill vs Tip Amount")
![image](https://github.com/user-attachments/assets/fec05807-635f-4ff4-ba9f-8a9a6e1e37a6)

    sns.histplot(data=df,x="total_bill",hue="smoker",kde=True,palette="Set1")
    plt.xlabel("Total Bill")
    plt.ylabel("Frequency")
    plt.title("Distribution of Total Bill by Gender")
![image](https://github.com/user-attachments/assets/dd69a24f-3fde-4aae-8492-4d6a54584cef)

    import seaborn as sns
    import pandas as pd
    df=sns.load_dataset('tips')
    sns.boxplot(x='day',y='total_bill',hue='sex',data=df,palette='Set2')
![image](https://github.com/user-attachments/assets/af7f9ef8-4d52-4bfe-8227-ce9b71f713fe)

    sns.boxplot(x="day",y="total_bill",hue="smoker",data=df,linewidth=2,width=0.6,fliersize=7,flierprops={"marker":"o","markerfacecolor":"grey"},boxprops={"facecolor":"red","edgecolor":"black"},whiskerprops={"color":"darkblue","linestyle":"--","linewidth":"-","linewidth":2},palette='Set1')
![image](https://github.com/user-attachments/assets/03743b0e-9308-4e1e-8e83-f222bba7cc5d)

    sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,palette='Set1',inner="quartile")
    plt.xlabel("Day of the week")
    plt.ylabel("Total Bill")
    plt.title("Violin Plot of Total Bill by Day and Smoker Status")
![image](https://github.com/user-attachments/assets/5d2e580d-deaa-434a-9b72-6b99d1efc412)

    import seaborn as sns
    sns.set(style="whitegrid")
    tip = sns.load_dataset('tips')
    sns.violinplot(x='day',y='tip',data=tip,palette="Set2")
![image](https://github.com/user-attachments/assets/25193d3a-8ad0-4cf0-8bc2-97d986cf077e)

    import seaborn as sns
    sns.set(style='whitegrid')
    tip = sns.load_dataset('tips')
    sns.violinplot(x=tip["total_bill"],palette="Set1")
![image](https://github.com/user-attachments/assets/8b3c6fa6-4457-4940-b9b6-d2e8ef3fc96b)

    import seaborn as sns
    sns.set(style="whitegrid")
    tips = sns.load_dataset("tips")
    sns.violinplot(x="tip",y="day",data=tip,palette="rainbow")
![image](https://github.com/user-attachments/assets/09a04d3a-5da6-45a4-bb54-a3556bb22a37)

    sns.kdeplot(data=tips,x='total_bill',hue='time',multiple="layer",linewidth=3,palette='Set2',alpha=0.8)
![image](https://github.com/user-attachments/assets/5d5bd079-1db1-4a67-a518-e4a5e837b52e)

    sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set3',alpha=0.8)
![image](https://github.com/user-attachments/assets/aa0b1cfd-227f-4218-9afb-6b78f14054f4)

    sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set1',alpha=0.8)
![image](https://github.com/user-attachments/assets/095fbcb5-34aa-4d05-9dff-5dd187e59c63)

    import seaborn as sns
    tip = sns.load_dataset('tips')
    num=tips.select_dtypes(include=['float64','int64']).columns
    corr = tips[num].corr()
    sns.heatmap(corr,annot=True,cmap="YlGnBu")
![image](https://github.com/user-attachments/assets/d1780750-3675-4996-aaf5-77ff83585cd5)

    sns.heatmap(corr,cmap="YlGnBu")
![image](https://github.com/user-attachments/assets/10b56108-8d01-4ce8-a432-925224a847dd)

# Result:
Thus, all the data visualization techniques using the Seaborn library have been successfully implemented. The results provided clear and insightful representations of the given data.
