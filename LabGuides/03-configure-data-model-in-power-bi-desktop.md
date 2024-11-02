---
lab:
    title: 'Model Data in Power BI Desktop, Part 1'
    module: 'Module 3 - Design a Data Model in Power BI'
---


# **Model Data in Power BI Desktop, Part 1**

**The estimated time to complete the lab is 1 hour**


In this lab you learn how to:

- Implement more data manipulation techniques.

- Deal with Cardinality error

- Create model relationships.

- Build star schema


<h4><span style="color:red;">Important! Make sure that you have downloaded the datasets before starting the lab.</span></h4>


### **Lab story**

Our PowerBI labs are segregated into 9 labs, we suggest you do them in the following order:

1. Load Data in Power BI Desktop

2. Prepare Data in Power BI Desktop

3. **Model Data in Power BI Desktop, Part 1**

4. Model Data in Power BI Desktop, Part 2

5. Create DAX Calculations in Power BI Desktop, Part 1

6. Create DAX Calculations in Power BI Desktop, Part 2

7. Design Reports in Power BI Desktop

8. Create a Power BI Dashboard

9. Perform Data Analysis in Power BI Desktop


In this exercise you will explore more options through data manipulation in power query editor.

**Get Started!**

1. To open the Power BI Desktop, on the taskbar, click the Microsoft Power BI Desktop shortcut.

 	![Picture 8](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image1.png)


2. To open the previous Power BI Desktop file, click the **Open** option on the lest tab to open the backstage view.


3. In the **Recent** section choose your latest file that you have saved.
   
![11](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/open%20a%20saved%20file.jpg?raw=true "11")
    ![Picture 12](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image1.png)


**Import Sample-Superstore dataset in PowerBI**

1. Click on **Get Data -> Excel Workbook**

2. Choose tables `Customers, Orders, Returns, Products and Region`
![1](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/loadtablesSS.jpg?raw=true "1")

3. Click on **Transform Data**

> This might take few minutes to load depending upon the operating system and its version.

### **Task 1: Manipulate the data in power query**

In this task you will do some data corrections to model the data correctly. 

1. In the power query editor you will find all the tables imported sucessfully.

2. In Products table, You observe the first row is having column names, we should move them to headers.

3. Click on the option - `Use first row as headers`
   
![2](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/observerowheaders.jpg?raw=true "2")

4. This will configure the headers for all the columns.

> Similarly, configure the headers for the Returns Table

5. In Products table there are lots of empty columns. Remove them by holding `ctrl` button and right click on the null columns -> remove columns

![4](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/removecolumn.jpg?raw=true "4")

> Similarlly, remove the null columns in Region table

6. Choose Close&Apply option.
   
7. Navigate to Model view tab

![5](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/modelview.jpg?raw=true "5")

	*In Model view, it’s possible to view each table and relationships (connectors between tables).In most cases it will autodetect relations, however if there are inconsistencies in the data it will not create any of them.

8. You can click on **Manage Relationships -> Autodetect**

9. You can also drag and drop columns between tables.
    
**Example:- CustomerId in Orders table WITH CustomerID to Customer table**

**We get a cardinality error in our case. As there is still some incomplete data cleaning steps.To Avoid this error , you need to remove duplicates from our Dimentional tables as we are trying to build a star schema model for our project.**

> **Cardinality:-**
Cardinality in Power BI is a mathematical term that describes the relationship between two tables in a data model. It defines how many unique values from one table are related to unique values in another table.

> **Star Schema:**
Star schema is a mature modeling approach widely adopted by relational data warehouses. It requires modelers to classify their model tables as either dimension or fact.

> Dimension tables describe business entities—the things you model. Entities can include products, people, places, and concepts including time itself.A dimension table contains a key column (or columns) that acts as a unique identifier, and descriptive columns.

> Fact tables store observations or events, and can be sales orders, stock balances, exchange rates, temperatures, etc. A fact table contains dimension key columns that relate to dimension tables, and numeric measure columns.

The fact and dim tables in our data model can be classified as:
- Orders(Fact Table)
- Products(Dim Table)
- Customers(Dim Table)
- Region(Dim Table)
- Returns(Dim table)

**> We should make sure that there are no duplicates in all the dimentional tables to avoid cardinality error**.

The relationship we are looking for the tables is  **one-to-many** 
 A one-to-many relationship means that a single record in one table (the "one" side) can relate to multiple records in another table (the "many" side). For example, one customer can have multiple orders.


### **Task 2: Manipulate the data in power query (Remove Duplicates for Cardinality error)**

1. Go to Transform data -> Select Customers table -> Right click on the CustomerID column -> Remove Duplicates.

![7](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/removeduplicates.jpg?raw=true "7")

> Similarly remove duplicates from  other dimentional tables.
Once all the duplicates are removed from each of the dimentional tables. Do not forget to Close&Apply.


2. Navigate back to Model View.

Check if any changes has been applied to the tables. If you still cannot find any relationship between the tables, you can drag and drop the Respective keys to create a relation.

![8](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/cid.jpg?raw=true "8")

Likewise, Drag and drop the Key Id's from dimentional table to factorial table.
- OrderID in Orders table with OrderID in Returns table
- Region key in Region table with Regionkey in Orders table

![9](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/oid.jpg?raw=true "9")

![11](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/region.jpg?raw=true "11")


This figure is called as "Star Schema".Where the fact table is our Orders in the table surrounded by dimentional tables making a proper data model figure.

**Star Schema**

![10](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/starss.jpg?raw=true "10")


### Finish up

In this task you will complete the lab.

1. Save the Power BI Desktop file.

2. If you intend to start the next lab, leave Power BI Desktop open.

We will look into creating manual relationships between the tables( Product and Orders), creating hirarchies and data categories in the upcoming lab.
