---
lab:
    title: 'Create DAX Calculations in Power BI Desktop, Part 1'
    module: 'Module 4 - Create Model Calculations using DAX in Power BI'
---


# **Create DAX Calculations in Power BI Desktop, Part 1**

**The estimated time to complete the lab is 60 minutes**

In this lab you will create calculated tables, calculated columns using Data Analysis Expressions (DAX).

In this lab you learn how to:

- Create calculated Date Table

- Create calculated columns


<h4><span style="color:red;">Important! Make sure that you are working on the previous lab file for this exercise before starting the current one.</span></h4>


### **Lab story**

Our PowerBI labs are segregated into 9 labs, we suggest you do them in the following order:

1. Prepare Data in Power BI Desktop

2. Load Data in Power BI Desktop

3. Model Data in Power BI Desktop, Part 1

4. Model Data in Power BI Desktop, Part 2

5. **Create DAX Calculations in Power BI Desktop, Part 1**

6. Create DAX Calculations in Power BI Desktop, Part 2

7. Design a Reports in Power BI Desktop

8. Create a Power BI Dashboard
   
9. Perform Data Analysis  


1. To open the Power BI Desktop, on the taskbar, click the Microsoft Power BI Desktop shortcut.

 	![Picture 8](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image1.png)


1. To open the previous Power BI Desktop file, click the **Open** option on the lest tab to open the backstage view.
   
2. In the recent section choose your latest file that you have saved
   
![11](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/open%20a%20saved%20file.jpg?raw=true "11")

![12](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/findfrom%20recent.jpg?raw=true "12")

## **Task 1: Create Calculated Table**

Lets create a DATE table.

1. Navigate to "table view"

![2](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/table%20view.jpg?raw=true "2")

2. Click on "New Table"

![1](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/new%20table.jpg?raw=true "1")

3. Enter the below formula in the formula bar, and press enter
`Dim Date = CALENDARAUTO()`

Note: Dimdate is our table name and calenderauto() is a function.

![3](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/dimdate.jpg?raw=true "3")

4. Under Column Tools -> Change the datatype to Date -> Change the format to shortdate


![5](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/datetype.jpg?raw=true "5")

![6](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/formatdate.jpg?raw=true "6")


The CALENDARAUTO() function returns a single-column table consisting of date values. The “auto” behavior scans all data model date columns to determine the earliest and latest date values stored in the data model. 


### **Task 2: Calculated Columns**

In this task you will create calculated columns use DAX formulas.

#### Creating **Profit Category** calculated column:

1. Click on **New Column** option located in the taskbar

2. Enter the below expression in the formula bar and press enter
`Profit Category = 
SWITCH(
    TRUE(),
    [Profit] > 80, "Very High Profit",
    [Profit] >50 , "High Profit",
    [Profit] <50 , "Low Profit",
    "No Profit"
)`

![8](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/profitcategory.jpg?raw=true "11")

In the above formula we have used SWITCH function to write a conditonal formula that has alloted values Low, High and Very High profits as per the values in the expression.

#### Creating **Sales After Discount** calculated column:

If you want to calculate the total sales amount after applying the discount, you can create another calculated column

1. Click on **New Column** option located in the taskbar
2. Enter the below expression in the formula bar and press enter
`Sales After Discount = Orders[Sales] * (1 - Orders[Discount])
`
![9](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/salesafterdiscount.jpg?raw=true "9")

#### Creating **Profit Margin** calculated column:

If you want to calculate the total sales amount after applying the discount, you can create another calculated column

1. Click on **New Column** option located in the taskbar

2. Enter the below expression in the formula bar and press enter
`Profit Margin = DIVIDE(Orders[Profit], Orders[Sales], 0)`

![10](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/profitmargin.jpg?raw=true "10")


### **Task 3: Finish up**

In this task you will complete the lab.

1. Save the Power BI Desktop file.

2. If you intend to start the next lab, leave Power BI Desktop open.

	*You’ll enhance the data model with more advanced calculations using DAX in the **Create DAX Calculations in Power BI Desktop, Part 2** lab.*
