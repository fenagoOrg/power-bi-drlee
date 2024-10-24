---
lab:
    title: 'Model Data in Power BI Desktop, Part 2'
    module: 'Module 3.2 - Design a Data Model in Power BI'
---


# **Model Data in Power BI Desktop, Part 2**

**The estimated time to complete the lab is 40 minutes**

#### In this lab you learn how to:

- Build relationships between the tables manually( Manage Relationships).
- Configure cross filters between the tables.
- Create hirarchies
- Understand table properties.

<h4><span style="color:red;">Important! Make sure that you are working on the previous lab(3.1) open before starting the lab.</span></h4>

### **Lab story**

This lab is one of many in a series of labs that was designed as a complete story from data preparation to publication as reports and dashboards. You can complete the labs in any order. However, if you intend to work through multiple labs, for the first 10 labs, we suggest you do them in the following order:

1. Load Data in Power BI Desktop

2. Prepare Data in Power BI Desktop

3. Model Data in Power BI Desktop, Part 1

4. **Model Data in Power BI Desktop, Part 2**

5. Create DAX Calculations in Power BI Desktop, Part 1

6. Create DAX Calculations in Power BI Desktop, Part 2

7. Design a Report in Power BI Desktop, Part 1

8. Design a Report in Power BI Desktop, Part 2

9. Create a Power BI Dashboard

10. Create a Power BI Paginated Report

11. Perform Data Analysis in Power BI Desktop


## **Exercise 1: Build relationships manually between the fact and dimentional tables**



### **Task 1: Get started**

In this task you will setup the environment for the lab.

*Important: If you are continuing on from the previous lab (and you completed that lab successfully), do not complete this task; instead, continue from the next task.*

1. To open the Power BI Desktop, on the taskbar, click the Microsoft Power BI Desktop shortcut.

 	![Picture 8](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image1.png)


1. To open the previous Power BI Desktop file, click the **File** ribbon tab to open the backstage view.

WORK ON OPENING THE SAVED FILE

### ***Task 2: Create new relationship between Product table with Order Table***

1. Go to Model view
2. Click on Manage Relationships -> New Relationship.
3. Select from table -> choose product table -> slect productid
4. Click on To table ->choose orders table -> select productid
5. Check the cardinality, the default is one to many along with cross filter direction "Single"
6. Click on "Save"

After few seconds, you will observe a relation built from products table to orders table..

 
### ***Task 3: Setting data categories for Geogrpahical columns ***
1. In model view, tap on data pane -> expand orders table -> tap on Region.
2. In Properties pane, scroll down to Advanced section. When you expland it, click on the data category dropdown.
3. Choose Country/Region option
4. Notice the globe icon besdie Region column.

You can add more data categories to all the other geographical columns(Region, County,States or Cities)


### ***Task 3: Creating Hirarchy in Orders table***

1.In Model View, right click on country column -> Click on create hirarchy
2. In properties pane -> Under Hirarchy you will will country is selected and now we need to add more levels under it.
3. Click the dropdown to add level and choose state.
4. Click the dropdown to add level and choose city.
5.Click on Apply Level Changes

### **Task 4: Finish up**

In this task you will complete the lab.

1. Save the Power BI Desktop file.

2. If prompted to apply queries, click **Apply Later**.

3. If you intend to start the next lab, leave Power BI Desktop open.

	*You’ll enhance the data model with calculations using DAX in the **Create DAX Calculations in Power BI Desktop, Part 2** lab.*
