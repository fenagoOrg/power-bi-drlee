---
lab:
    title: 'Model Data in Power BI Desktop, Part 1'
    module: 'Module 3 - Design a Data Model in Power BI'
---


# **Model Data in Power BI Desktop, Part 1**

**The estimated time to complete the lab is 45 minutes**

In this lab you will commence developing the data model. It will involve creating relationships between tables, and then configuring table and column properties to improve the friendliness and usability of the data model. You will also create hierarchies and create quick measures.

In this lab you learn how to:

- Implement more data manipulation techniques

- Create model relationships

- Configure table and column properties

- Create hierarchies


<h4><span style="color:red;">Important! Make sure that you have downloaded the datasets before starting the lab.</span></h4>


### **Lab story**

This lab is one of many in a series of labs that was designed as a complete story from data preparation to publication as reports and dashboards. You can complete the labs in any order. However, if you intend to work through multiple labs, for the first 10 labs, we suggest you do them in the following order:

1. Load Data in Power BI Desktop

2. Prepare Data in Power BI Desktop

3. **Model Data in Power BI Desktop, Part 1**

4. Model Data in Power BI Desktop, Part 2

5. Create DAX Calculations in Power BI Desktop, Part 1

6. Create DAX Calculations in Power BI Desktop, Part 2

7. Design a Report in Power BI Desktop, Part 1

8. Design a Report in Power BI Desktop, Part 2

9. Create a Power BI Dashboard

10. Create a Power BI Paginated Report

11. Perform Data Analysis in Power BI Desktop

12. Enforce Row-Level Security

## **Exercise 1: Implement Data Manipulation Techniques**

In this exercise you will explore more options through data manipulation in power query editor.

### **Task 1: Get started**

In this task you will setup the environment for the lab.

*Important: This is a new dataset, please make sure you import "Sample - Superstore as it is used in further labs as well.*

1. To open the Power BI Desktop, on the taskbar, click the Microsoft Power BI Desktop shortcut.

    ![Picture 12](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image1.png)

2. Import Sample-Superstore dataset in PowerBI

**Get Data -> Excel Workbook**

3. Choose tables `Customers, Orders, Returns,Products and Region`
![1](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/loadtablesSS.jpg?raw=true "1")
4. Click on **Transform Data**

> This might take few minutes to load depending upon the operating system and its version.

### **Task 2: Manipulate the data in power query**

In this task you will do some data corrections to model the data correctly. 

1. In the power query editor you will find all the tables imported sucessfully.
2. In Products table, You observe the first row is having column names, we should move them to headers.
3. Click on the option - `Use first row as headers`
![2](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/observerowheaders.jpg?raw=true "2")

4. This will configure the headers for all the columns.

> Similarlly, configure the headers for the Returns Table

5. In Products table there are lots of empty columns. Remove them by holding `ctrl` button and right click on the null columns -> remove columns

![4](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/removecolumn.jpg?raw=true "4")

> Similarlly, remove the null columns in Region table

6. Choose Close&Apply option.
7. Navigate to Model view tab

![5](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/modelview.jpg?raw=true "5")

	*In Model view, it’s possible to view each table and relationships (connectors between tables).In most cases it will autodetect relations, however if there are inconsistencies in the data it will not create any of them.

9. You can click on **Manage Relationships -> Autodetect**

10. You can also drag and drop columns between tables.
Example:- CustomerId in Orders table WITH CustomerID to Customer table

**We get a cardinality error in our case. As there is still some incomplete data cleaning steps.**

> Cardinality:- Cardinality in Power BI is a mathematical term that describes the relationship between two tables in a data model. It defines how many unique values from one table are related to unique values in another table.

To Avoid this error , you need to remove duplicates from our Dimentional tables as we are trying to build a star schema model for our project.

> Star Schema:
Star schema is a mature modeling approach widely adopted by relational data warehouses. It requires modelers to classify their model tables as either dimension or fact.

> Dimension tables describe business entities—the things you model. Entities can include products, people, places, and concepts including time itself.A dimension table contains a key column (or columns) that acts as a unique identifier, and descriptive columns.

> Fact tables store observations or events, and can be sales orders, stock balances, exchange rates, temperatures, etc. A fact table contains dimension key columns that relate to dimension tables, and numeric measure columns.


The fact and dim tables in our data model can be classified as:
- Orders(Fact Table)
- Products(Dim Table)
- Customers(Dim Table)
- Region(Dim Table)
- Returns(Dim table)

> We should make sure that there are no duplicates in all the dimentional tables to avoid cardinality error.

The relationship we are looking for the tables is  **one-to-many** 
The relationships, the cross filter direction is always from the "one" side, and optionally from the "many" side (bi-directional).


### **Task 3: Manipulate the data in power query (Remove Duplicates for Cardinality error)**

1. Go to Transform data -> Select Customers table -> Right click on the CustomerID column -> Remove Duplicates.
![7](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/removeduplicates.jpg?raw=true "7")

**> Similarlly remove duplicates from  other dimentional tables.
Once all the duplicates are removed from each of the dimentional tables. Do not forget to Close&Apply.**


2. Navigate back to Model View.
Check if any changes has been applied to the tables. If you still cannot find any relationship between the tables, you can drag and drop the Respective keys to create a relation.
![8](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/cid.jpg?raw=true "8")

Likewise, Drag and drop the Key Id's from dimentional table to factorial table.
- OrderID in Orders table with OrderID in Returns table
- ProductID in Products table with ProductID in Orders table
- Region key in Region table with Regionkey in Orders table

![9](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/oid.jpg?raw=true "9")
![10](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/pid.jpg?raw=true "10")
![11](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/region.jpg?raw=true "11")


This figure is called as "Star Schema". Where the fact table is our Orders in the table surrounded by dimentional tables making a proper data model figure.

**Star Schema**
![12](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/starschema.jpg?raw=true "12")

We will look into creating manual relationships between the tables, creating hirarchies and look at table properties in the upcoming lab(3.2)

