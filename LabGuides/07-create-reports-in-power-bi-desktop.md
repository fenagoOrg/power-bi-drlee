---
lab:
    title: 'Create a Reports in Power BI Desktop'
    module: 'Module 5 - Create Reports'
---


# **Create a Report in Power BI Desktop**

**The estimated time to complete the lab is 60 minutes**

In this lab you learn how to:

- Design a Report

- Configure Visual fields. 

<h4><span style="color:red;">Important! Make sure that you are working on the previous lab file for this exercise before starting the current one as this a continuation series of labs.</span></h4>


### **Lab story**

Our PowerBI labs are segregated into 9 labs, we suggest you do them in the following order:

1. Load Data in Power BI Desktop

2. Prepare Data in Power BI Desktop

3. Model Data in Power BI Desktop, Part 1

4. Model Data in Power BI Desktop, Part 2

5. Create DAX Calculations in Power BI Desktop, Part 1

6. Create DAX Calculations in Power BI Desktop, Part 2

7. **Create Reports in Power BI Desktop**

8. Create a Power BI Dashboard

9. Perform Data Analysis


**Get Started!**

1. To open the Power BI Desktop, on the taskbar, click the Microsoft Power BI Desktop shortcut.

 	![Picture 8](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image1.png)


2. To open the previous Power BI Desktop file, click the **Open** option on the lest tab to open the backstage view.


3. In the **Recent** section choose your latest file that you have saved.
   
![11](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/open%20a%20saved%20file.jpg?raw=true "11")

> *NOTE:- As you keep creating the below reports , align them in the canvas by double tapping on each report and move them across the canvas.*

### Task 2: Create CARD visuals 

1. On the visualizations pane 

2. Click on **Card** Visual

![3](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/card.jpg?raw=true "3")

3. Drag and drop Total Sales option in the fields option.

![2](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/totalsa.jpg?raw=true "2")

**Example:  Creating card for Total Orders Total Profit and Total Sales.**

![1](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/totalordersc.jpg?raw=true "1")

![3](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/totalprofitc.jpg?raw=true "3")

![4](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/totalsalesc.jpg?raw=true "4")

### Task 2: Create Line Chart 

1. On the visualizations pane 

2. Click on **Line** Chart.

3. In X - axis - > Drag and drop **Order Date** from Orders Table

4. In Y- axis -> Drag and drop **Sales** from Orders table

5. In Secondary Y - axis -> Drag and drop **Profit** from Orders table

![5](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/line.jpg?raw=true "5")

![6](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/linec.jpg?raw=true "6")

### **Task 2: Create Pie Chart **

1. On the visualizations pane 

2. Click on **Pie** Chart.

3. In Legend - > Drag and drop **Segment** from Orders Table

4. In Values -> Drag and drop **Total Sales** from Orders table

![7](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/piedetail.jpg?raw=true "7")

![8](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/pie.jpg?raw=true "8")

### Task 2: Create Bar Chart

1. On the visualizations pane.

2. Click on **Clustered Bar** Chart.

3. In X - axis - > Drag and drop **Total Orders** from Customers Table

4. In Y- axis -> Drag and drop **State** from Orders table

![1](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/odersregion.jpg?raw=true "1")

![2](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/barchart.jpg?raw=true "2")


### Task 2: Create Multirow Card

1. On the visualizations pane.

2. Click on **Multi-row card**.

3. In X - axis - > Drag and drop **Total Orders** from Customers Table (or any table in which you have created the measure)

4. In Y- axis -> Drag and drop **State** from Orders table

![6](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/multirow.jpg?raw=true "6")

![7](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/multi.jpg?raw=true "7")

### Task 2: Create Map Visual

1. On the visualizations pane.

2. Click on **Map** visual.

3. Drag and drop **State** from Orders table.

4. Drag and drop **Profit** from Orders table.

![9](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/map.jpg?raw=true "9")


### **Task 2: Finish up**

In this task you will complete the lab.

1. To return to your workspace, in the banner across the window web page, click **My Workspace**.

	![Picture 99](Linked_image_Files/07-design-report-in-power-bi-desktop_image72.png)

2. Leave the Microsoft Edge browser window open.

	*You will learn enhancing the reports and create a Superstore dashboard in the upcoming lab.*
