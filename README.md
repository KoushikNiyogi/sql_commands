# sql_commands
**Problem 1:**

- **Prerequisite**: Understand creating tables in SQL / collections in MongoDB
- **Problem**: Create a **`Customers`** table / collection with the following fields: **`id`** (unique identifier), **`name`**, **`email`**, **`address`**, and **`phone_number`**.
   ANS -> CREATE TABLE CUSTOMERS(NAME TEXT,ID TEXT,EMAIL TEXT,PHONE_NUMBER TEXT,PASSWORD TEXT);
      

**Problem 2:**

- **Prerequisite**: Understand inserting data into SQL tables / MongoDB collections
- **Problem**: Insert five rows / documents into the **`Customers`** table / collection with data of your choice.

   ->  INSERT INTO CUSTOMERS(NAME, ID, EMAIL,PHONE_NUMBER,PASSWORD) VALUES("Koushik","1","koushi@gmail.com","1234567890","1234");

**Problem 3:**

- **Prerequisite**: Understand basic data fetching in SQL / MongoDB
- **Problem**: Write a query to fetch all data from the **`Customers`** table / collection.

  -> SELECT * FROM CUSTOMERS

**Problem 4:**

- **Prerequisite**: Understand how to select specific fields in SQL / MongoDB
- **Problem**: Write a query to select only the **`name`** and **`email`** fields for all customers.

->SELECT NAME,EMAIL FROM CUSTOMERS;

**Problem 5:**

- **Prerequisite**: Understand basic WHERE clause in SQL / MongoDB's find method
- **Problem**: Write a query to fetch the customer with the **`id`** of 3.
-> SELECT * FROM CUSTOMERS WHERE ID = 3;

**Problem 6:**

- **Prerequisite**: Understand using string patterns in SQL (LIKE clause) / using regex in MongoDB
- **Problem**: Write a query to fetch all customers whose **`name`** starts with 'A'.
 -> SELECT * FROM CUSTOMERS WHERE NAME LIKE "K%";


**Problem 7:**

- **Prerequisite**: Understand how to order data in SQL / MongoDB
- **Problem**: Write a query to fetch all customers, ordered by **`name`** in descending order.

-> SELECT * FROM CUSTOMERS ORDER BY NAME DESC;

**Problem 8:**

- **Prerequisite**: Understand data updating in SQL / MongoDB
- **Problem**: Write a query to update the **`address`** of the customer with **`id`** 4.

->  UPDATE CUSTOMERS SET EMAIL = "RAJESHBIT@GMAIL.COM" WHERE ID = 3;

**Problem 9:**

- **Prerequisite**: Understand how to limit results in SQL / MongoDB
- **Problem**: Write a query to fetch the top 3 customers when ordered by **`id`** in ascending order.
 ->  SELECT * FROM CUSTOMERS ORDER BY ID ASC LIMIT 3;

**Problem 10:**

- **Prerequisite**: Understand data deletion in SQL / MongoDB
- **Problem**: Write a query to delete the customer with **`id`** 2.

->DELETE FROM CUSTOMERS WHERE ID=2;


**Problem 11:**

- **Prerequisite**: Understand how to count rows / documents in SQL / MongoDB
- **Problem**: Write a query to count the number of customers.
->SELECT COUNT(*) FROM customers;


**Problem 12:**

- **Prerequisite**: Understand how to skip rows / documents in SQL / MongoDB
- **Problem**: Write a query to fetch all customers except the first two when ordered by **`id`** in ascending order.
-> SELECT * FROM customers LIMIT 18446744073709551615 OFFSET 2;

**Problem 13:**

- **Prerequisite**: Understand filtering with multiple conditions in SQL / MongoDB
- **Problem**: Write a query to fetch all customers whose **`id`** is greater than 2 and **`name`** starts with 'B'.
->  SELECT * FROM CUSTOMERS WHERE ID < 3 AND NAME LIKE "K%";

**Problem 14:**

- **Prerequisite**: Understand how to use OR conditions in SQL / MongoDB
- **Problem**: Write a query to fetch all customers whose **`id`** is less than 3 or **`name`** ends with 's'.
-> SELECT * FROM CUSTOMERS WHERE ID < 3 AND NAME LIKE "%k";

**Problem 15:**

- **Prerequisite**: Understand how to use NULL checks in SQL / MongoDB
- **Problem**: Write a query to fetch all customers where the **`phone_number`** field is not set or is null.
 ->SELECT * FROM employees WHERE phone_number IS NULL;
