##    DDL-COMMANDS ASSIGNMENT  

**Create a database called “Sales” and create a new table named “Orders” in the Sales database with columns: (Order_Id, Customer_name, Product_Category, Ordered_item, Contact_No). Use constraints: Primary Key Unique Not Null**.

•	1. Add a new column named “order_quantity” to the orders table

•	2. Rename the orders table to the sales_orders table. 

•	3. Insert 10 rows into the sales_orders table

•	4. Retrieve customer_name and Ordered_Item from the sales_orders table

•	5. Use the update command to change the name of the product for any row

•	6. Delete the sales_orders table from the database

### **SQL COMMANDS** 
##### **CREATE DATABASE**
CREATE DATABASE SALES;


#####  **SPECIFY WHICH DATABASE TO BE USED FOR THE SUBSEQUENT ACTIVITY**

USE SALES;

#####  **CREATE TABLE WITH CONSTRAINTS**

CREATE TABLE ORDERS (
    C_ORDER_ID INT auto_increment,
    C_SALES_ID INT unique ,
    C_CUSTOMER_NAME VARCHAR(50) NOT NULL ,
    C_PRODUCT_CATEGORY VARCHAR(50) NOT NULL,
    C_ORDER_ITEM VARCHAR(100) ,
    C_CONCAT_NO VARCHAR(10) NOT NULL,
    primary key (C_ORDER_ID)	
  );

#####  **ADD A NEW COLUMN TO THE TABLE**
ALTER TABLE ORDERS ADD ORDER_QUANTITY INT NOT NULL; 


#####  **VIEW THE DETAILS OF THE TABLE**
SELECT * FROM ORDERS;

#####  **CHANGE THE TABLE NEME**

ALTER TABLE ORDERS RENAME TO SALES_ORDER;

#####  **VERIFY THE TABLE NEAME HAS CHANGED**

  SELECT * FROM SALES_ORDER;

#####  **TO ENSURE THAT THE C_ORDER_ID AUTO INCREMENT NUMBER SHOULD INCREMENT FROM THIS NUMBER**
 ALTER TABLE SALES_ORDER AUTO_INCREMENT=10000;

#####  **INSERT DATA INTO THE TABLE**

  INSERT INTO SALES_ORDER	(C_SALES_ID,C_CUSTOMER_NAME,
C_PRODUCT_CATEGORY,C_ORDER_ITEM,                  C_CONCAT_NO,  ORDER_QUANTITY )
       					VALUES
        ('123465','Raju','Ornaments','bangles','8856451237',15);


#####  **RETRIEVE CUSTOMER NAME AND ORDER ITEM FROM THE TABLE**

SELECT C_CUSTOMER_NAME,C_ORDER_ITEM FROM SALES_ORDER;


#####  **CHANGE THE NAME OF  ANY PRODUCT**

UPDATE SALES_ORDER
        SET
C_ORDER_ITEM ='BOTTLE'
    WHERE
C_ORDER_ID=10008;


#####  **DELETE THE SALES_ORDER TABLE FROM THE DATABASE**

DROP TABLE SALES_ORDER;



