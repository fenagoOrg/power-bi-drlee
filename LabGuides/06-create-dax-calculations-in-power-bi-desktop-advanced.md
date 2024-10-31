---
lab:
    title: 'Create DAX Calculations in Power BI Desktop, Part 2'
    module: 'Module 5 - Create Model Calculations using DAX in Power BI'
---


# **Create DAX Calculations in Power BI Desktop, Part 2**

**The estimated time to complete the lab is 60 minutes**



In this lab you learn how to:

- Create Measures

- Use Time Intelligence functions (Quick Measure)


<h4><span style="color:red;">Important! Make sure that you are working on the previous lab file for this exercise before starting the current one.</span></h4>


### **Lab story**

This lab is one of many in a series of labs that was designed as a complete story from data preparation to publication as reports and dashboards. You can complete the labs in any order. However, if you intend to work through multiple labs, for the first 10 labs, we suggest you do them in the following order:

1. Prepare Data in Power BI Desktop

2. Load Data in Power BI Desktop

3. Model Data in Power BI Desktop, Part 1

4. Model Data in Power BI Desktop, Part 2

5. Create DAX Calculations in Power BI Desktop, Part 1

6. **Create DAX Calculations in Power BI Desktop, Part 2**

7. Design a Report in Power BI Desktop, Part 1

8. Design a Report in Power BI Desktop, Part 2

9. Create a Power BI Dashboard


### **Task 1: Get started**

1. To open the Power BI Desktop, on the taskbar, click the Microsoft Power BI Desktop shortcut.

    ![Picture 12](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image1.png)

### **Task 2: Creating measures in PowerBI**

In this task you will create measures for the model.

**Creating Total Sales Measure:**

1. Navigate to Report View -> Select any table from the data pane -> Click on **New Measure**.

2. Enter the below formula 
`Total Sales = SUM(Orders[Sales])
`

![1](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/totalsaless.jpg?raw=true "1")

**Creating Total Profit Measure:**

1. In report view -> Select any table from the data pane -> click on N**ew Measure**

2. Enter the below formula
`Total Profit = SUM(Orders[Profit])`

![2](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/total%20profit.jpg?raw=true "2")

**Creating Total Orders Measure:**

1. In report view -> Select any table from the data pane -> click on **New Measure**

2. Enter the below formula
`Total Orders = COUNTROWS(Orders)`

![3](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/totaloders.jpg?raw=true "3")

**Creating TotalReturns Measure:**

1. In report view -> Select any table from the data pane -> click on **New Measure**

2. Enter the below formula
`Total Returns = COUNTROWS(FILTER(Returns, Returns[Returned] = "Yes"))`

![6](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/totalreturns.jpg?raw=true "6")

**Creating AverageSales Measure:**

1. In report view -> Select any table from the data pane -> click on New Measure

2. Enter the below formula
`Average Sales = AVERAGE(Orders[Sales])`

![5](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/avg%20sales.jpg?raw=true "5")

### **Task 3: Use Time Intelligence Functions **

**Calculating YTD(Year-to-Date) using Quick Measure:**

**TotalYTD:-** Helps assess overall annual performance and trends. It allows businesses to evaluate how they are doing relative to annual goals or budgets.

1. In report view -> Select any table from the data pane -> click on **Quick Measure**

![3](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/newmeasure.jpg?raw=true "3")

2. Click on the drop-dowm of calculation .

3. Scroll down to **Time Intelligence functions**

4. Select **Year-To-Date** option

![5](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/yeartodate.jpg?raw=true "5")

5. Drag and drop s**ales column** in base value and **Order Date** in date column( from Orders table)

![6](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/valuesytd.jpg?raw=true "6")

6. Click on **Add** option

**Calculating QTD(Quarter-to-Date) using Quick Measure:**

**TotalQTD:**- Helps assess progress toward quarterly goals and provides insights into performance trends within the quarter. It can be crucial for quarterly reporting and analysis.

Similarly , by following the above steps

1. Select **Quarter-To-Date** option

2. Drag and drop **Sales** column in base value and **Order Date** in date column( from Orders table)

3. Click on **Add **option

![2](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/qtd.jpg?raw=true "2")

**Calculating MTD(Month-to-Date) using Quick Measure:**

**TotalMTD:-** Useful for evaluating monthly performance and identifying trends or issues early in the month. It helps in short-term planning and adjustments.

Similarly , by following the above steps

1. Select** Month-to-date** option

2. Drag and drop **sales column** in base value and **Order date ** in date column( from Orders Table)

3. Click on **Add** option

![1](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/mtd.jpg?raw=true "1")


> In the upcoming labs , we will see how can we use these values to help us build meaningful reports. Save the progress, keep PowerBI open to countinue with next lab.
