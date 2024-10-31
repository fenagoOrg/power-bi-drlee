---
lab:
    title: 'Prepare Data in Power BI Desktop'
    module: 'Module 2 - Clean And Transform The Data Using Power Query Editor In Power BI'
---

# **Prepare Data in Power BI Desktop**

**The estimated time to complete the lab is 35 minutes**


In this lab you learn how to:

- Open Power BI Desktop

- Connect to source data

- Use data preview techniques to better understand the data by data profiling tools

- Use data cleaning and transforming tools to prepare the data in Power Query Editor

<h4><span style="color:red;">Important! Make sure that you have downloaded the dataset(SalesvSalesPerson) before starting the lab.</span></h4>


### **Lab story**

Our PowerBI labs are segregated into 9 labs, we suggest you do them in the following order:

1. Load Data in Power BI Desktop

2. **Prepare Data in Power BI Desktop**

3. Model Data in Power BI Desktop, Part 1

4. Model Data in Power BI Desktop, Part 2

5. Create DAX Calculations in Power BI Desktop, Part 1

6. Create DAX Calculations in Power BI Desktop, Part 2

7. Design a Reports in Power BI Desktop

8. Create a Power BI Dashboard
    
9. Perform Data Analysis in Power BI Desktop



> As we have loaded files from our previous lab(Lab 1), we can start with data preparation in the current lab.

## **Exercise 1: Prepare Data**

In this exercise you will explore power query editor that helps us clean and transform the data using specialised tools.

### **Task 1: Transform Data**

In this task you will explore power query editor by clicking on transform data option


1. Click on **Transform Data** option on the taskbar.

 ![1](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/transformontaskbar.jpg?raw=true "1")

You will see a new window that is indeed our power query editor. All the data cleaning steps will be done in that window.

### **Task 2: Power Query Editor**

Once you are landed on Power Query Editor. You will find the table you have imported earlier, below the table you shall find the overall contents of the table(i.e count of rows and columns)

![9](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/contentsinthetable.jpg?raw=true "9")

Lets explore more intresting data manipulation tools.!

#### **1. Column Distribution, Column Profiling and Column Quality**

- **Column Distribution:-**
This feature provides a set of visuals underneath the names of the columns that showcase the frequency and distribution of the values in each of the columns. The data in these visualizations is sorted in descending order from the value with the highest frequency.

1. To view this feature in Power Query, follow the below steps.

2. In the taskbar -> View -> check the **Column Distribution** option

![2](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/columndist.jpg?raw=true "2")

![3](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/understandcolumndist.jpg?raw=true "3")

- **Column Profiling:-**
This feature provides a more in-depth look at the data in a column. Apart from the column distribution chart, it contains a column statistics chart. 

1. To view this feature in Power Query, follow the below steps.

2. In the taskbar -> View -> check the **Column Profiling** option

![4](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/columnprofile.jpg?raw=true "4")

![5](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/undestandprofiling.jpg?raw=true "5")

- **Column Quality:-**
The column quality feature labels values in rows in five categories:

1. **Valid**, shown in green.

2. **Error**, shown in red.

3. **Empty**, shown in dark grey.

4. **Unknown**, shown in dashed green. Indicates when there are errors in a column, the quality of the remaining data is unknown.

5. **Unexpected error**, shown in dashed red.

These indicators are displayed directly underneath the name of the column as part of a small bar chart.

1. To view this feature in Power Query, follow the below steps.

2. In the taskbar -> View -> check the **Column Quality** option

![6](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/columnquality.jpg?raw=true "6")

![7](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/uderstandquality.jpg?raw=true "7")



#### 2. Manipulating The Data(Removing Columns, Adjusting Datatypes, Replacing values)

**Checking Datatypes:-**
Its always important to check datatypes when the data is loaded. Unusual datatypes will result in abnormal readings in visualization.
So it's important and useful to use the correct data types for columns.

To check , you can click on the **datatype symbol** beside the column name and adjust it if needed as per the data. Else, we have nothing to worry about!

![8](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/datatypes.jpg?raw=true "8")


**Removing Columns:-**
If your query has columns you don't need, you can remove them. You can select one or more columns, and then either remove the selected ones, or remove the unselected ones, that is the other columns.

The easiest way is to just **right click** on the column and choose **Remove**. Lets remove the column `Title` as it has incomplete rows and is not bringing any insights to the table,

![9](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/removecolumn.jpg?raw=true "9")

Similarly, by looking at the perticular table we have certain columns that are unnecessary and has blank rows in the columns. We can remove them as well.

Remove the columns`(Middlename, Suffix, Addressline2)`

**Replace Values:-**
In Power Query, you can replace one value with another value in a selected column. You can replace specific values or the whole value in a cell. Replacing values in a query does not edit the external data source in any way.  

1. To do this, right click on the column name that you wish to replace values.

2. In our case, lets replace null values with 0 in the column(`SalesQuota`)

![9](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/replacevalues.jpg?raw=true "9")

Type **null** and **0** in the respective fields. 

![10](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/replacenullwith0.jpg?raw=true "10")

------------


As you keep doing these operations, you will see the changes refelecting under **Applied Steps**.

> Tip:- You can undo steps by clicking on the cross mark beside the steps

![11](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/appliedsteps.jpg?raw=true "11")

Do not forget to click on **Close&Apply** option once the changes are done.

This will navigate you back to report view.

![12](https://github.com/Neha-Chiluka/power-bi-next-level/blob/master/Images/closeandaplly.jpg?raw=true "12")


> We are using different dataset from next labs. Kindly, save and close this current lab. 
