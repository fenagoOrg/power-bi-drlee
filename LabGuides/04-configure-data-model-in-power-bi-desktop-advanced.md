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

<h4><span style="color:red;">Important! Make sure that you are working on the previous lab. </span></h4>

### **Lab story**

Our PowerBI labs are segregated into 9 labs, we suggest you do them in the following order:

1. Load Data in Power BI Desktop

2. Prepare Data in Power BI Desktop

3. Model Data in Power BI Desktop, Part 1

4. **Model Data in Power BI Desktop, Part 2**

5. Create DAX Calculations in Power BI Desktop, Part 1

6. Create DAX Calculations in Power BI Desktop, Part 2

7. Design a Reports in Power BI Desktop

8. Create a Power BI Dashboard

9. Perform Data Analysis in Power BI Desktop



### **Task 1: Get started**

In this task you will setup the environment for the lab.

1. To open the Power BI Desktop, on the taskbar, click the Microsoft Power BI Desktop shortcut.

 	![Picture 8](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image1.png)

2. To open the previous Power BI Desktop file, click the **Open** option on the lest tab to open the backstage view.

![11](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/open%20a%20saved%20file.jpg?raw=true "11")

3. In the recent section choose your latest file that you have saved

## Task 2: Create new relationship between Product table with Order Table

1. Go to Model view

2. Click on Manage Relationships -> New Relationship.

3. Select from table -> choose product table -> slect productid

4. Click on To table ->choose orders table -> select productid

5. Check the cardinality, the default is one to many along with cross filter direction "Single"

6. Click on "Save"

![2](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/new%20relationship.jpg?raw=true "2")

![3](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/relationprod-order.jpg?raw=true "3")

After few seconds, you will observe a relation built from products table to orders table..

**STAR SCHEMA**
![8](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/starschema.jpg?raw=true "8")

 
### Task 3: Setting data categories for Geogrpahical columns

1. In model view, tap on data pane -> expand orders table -> tap on **Country**.

2. In Properties pane, scroll down to Advanced section. When you expand it, click on the **Data Category** dropdown.

![4](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/datacategory1.jpg?raw=true "4")

3. Choose **Country/Region** option

![5](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/datacategory2.jpg?raw=true "5")

4. Notice the **globe icon** beside **Country** column.

> You can add more data categories to all the other geographical columns(Region, County,States or Cities)

![6](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/globe.jpg?raw=true "6")


### ***Task 4: Creating Hirarchy in Orders table***

1.In Model View, right click on country column -> Click on create hirarchy
![9](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/created%20hirarcy.jpg?raw=true "9")

2. In properties pane -> Under Hirarchy you will see country is selected and now we need to add more levels under it.

3. Click the dropdown to add level and choose state.

4. Click the dropdown to add level and choose city.

5.Click on Apply Level Changes

![10](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/applylevelchanges.jpg?raw=true "10")

> You will find the complete hirarchy under "**Country Hirarchy**"

![11](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/countryhirarchu.jpg?raw=true "11")

### **Task 5: Finish up**

In this task you will complete the lab.

1. Save the Power BI Desktop file.

2. If prompted to apply queries, click **Apply Later**.

3. If you intend to start the next lab, leave Power BI Desktop open.

	*You’ll enhance the data model with calculations using DAX in the **Create DAX Calculations in Power BI Desktop, Part 1** lab.*
