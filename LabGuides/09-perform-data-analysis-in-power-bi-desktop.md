---
lab:
    title: 'Perform Data Analysis in Power BI Desktop'
    module: 'Module 7 - Perform Advanced Analytics'
---


# **Perform Data Analysis in Power BI Desktop**

**The estimated time to complete the lab is 45 minutes**

In this lab you learn how to:

- Scatter Plot 

- Build KPI

- Work with the decomposition tree visual

- Work with the key influencers visual


<h4><span style="color:red;">Important! Make sure that you have copied **DA100** folder from `Desktop/power-bi-next-level` folder into D:\ drive before starting the lab.</span></h4>


### **Lab story**

This lab is one of many in a series of labs that was designed as a complete story from data preparation to publication as reports and dashboards. You can complete the labs in any order. However, if you intend to work through multiple labs, for the first 10 labs, we suggest you do them in the following order:

1.Load Data in Power BI Desktop

2. Prepare Data in Power BI Desktop

3. Model Data in Power BI Desktop, Part 1

4. Model Data in Power BI Desktop, Part 2

5. Create DAX Calculations in Power BI Desktop, Part 1

6. Create DAX Calculations in Power BI Desktop, Part 2

7. Create Reports in Power BI

8. Create a Power BI Dashboard

9. **Perform Data Analysis in Power BI Desktop**


**Get Started!**

1. To open the Power BI Desktop, on the taskbar, click the Microsoft Power BI Desktop shortcut.

 	![Picture 8](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image1.png)


2. To open the previous Power BI Desktop file, click the **Open** option on the lest tab to open the backstage view.


3. In the **Recent** section choose your latest file that you have saved.
   
![11](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/open%20a%20saved%20file.jpg?raw=true "11")

**NOTE: Please complete the lab in a new sheet. You can do that by switching to page 2!.**

![11](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/sheet2.jpg?raw=true "11")


## Task 1: Creating Decomposition Tree

Click on the "Visualizations" pane and select the Decomposition Tree icon.

1. Analyze: Drag a measure "Total Profit" 

2. Explain by: Add dimensions you want to analyze by, such as "Category," "Sub-Category," & "Region," 

Once set up, you can click on the nodes to drill down and explore how each dimension contributes to your total profit.

![1](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/dtsettings.jpg?raw=true "1")

![2](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/dt.jpg?raw=true "2")


## Task 2: Creating ScatterPlot

Configure the Scatter Plot:

Click on the "Visualizations" pane and select the Scatter Plot icon.

1. X-Axis: Add the Quantity Column.

2. Y-Axis: Add the Total Sales column .

3. Values: Add a categorical variable, such as "Category" to differentiate the data points.

4. Size: Add the "Total Orders" column to adjust the size of the data points, giving you an idea of the volume.

5. Play Axis: Add OrderDatecolumn -> choose only "Year"

Click on the play button to see the moving animation of the components!

![3](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/scsettings.jpg?raw=true "3")

![4](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/sc.jpg?raw=true "4")

## Task 3: Creating KPI

1. Value: Choose a measure "Total Sales."

3. Target: Choose a measure "Average Sales" .

5. Trend Axis: Choose Order Date column

![5](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/kpisettiings.jpg?raw=true "5")

![6](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/kpi.jpg?raw=true "6")

## Task 4: Creating Key Influencer

1. Analyze: Drag a target measure "Profit Margin".

3. Explain by: Add potential influencing factors, such as "Sub-Category".

![7](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/ki.jpg?raw=true "7")

![8](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/kii.jpg?raw=true "8")


------------


**The final data analysis sheet looks like below!**

![9](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/DA.jpg?raw=true "9")

### Finish up


You can save the file by either .pbix extenion or publish to your PowerBI workspace by logging in your microsoft account!
