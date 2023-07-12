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

**Problem 16:**

- **Prerequisite**: Understand creating tables in SQL / collections in MongoDB
- **Problem**: Create a **`Restaurants`** table / collection with the fields defined above.
- >CREATE TABLE Restaurants (
    ->     id INT AUTO_INCREMENT PRIMARY KEY,
    ->     name VARCHAR(100),
    ->     cuisine_type VARCHAR(100),
    ->     location VARCHAR(255),
    ->     average_rating DECIMAL(3,2),
    ->     delivery_available BOOLEAN
    -> );

**Problem 17:**

- **Prerequisite**: Understand inserting data into SQL tables / MongoDB collections
- **Problem**: Insert five rows / documents into the **`Restaurants`** table / collection with data of your choice.
- > INSERT INTO Restaurants (name, cuisine_type, location, average_rating, delivery_available)
    -> VALUES ('Empire', 'North Indian', 'Rajajinagar', 3.5, TRUE);

**Problem 18:**

- **Prerequisite**: Understand how to order data in SQL / MongoDB
- **Problem**: Write a query to fetch all restaurants, ordered by **`average_rating`** in descending order.
- > SELECT * FROM RESTAURANTS ORDER BY average_rating DESC;

**Problem 19:**

- **Prerequisite**: Understand filtering with multiple conditions in SQL / MongoDB
- **Problem**: Write a query to fetch all restaurants that offer **`delivery_available`** and have an **`average_rating`** of more than 4.
- 
  SELECT * FROM RESTAURANTS WHERE average_rating > 4 AND delivery_available = TRUE;

**Problem 20:**

- **Prerequisite**: Understand how to use NULL checks in SQL / MongoDB
- **Problem**: Write a query to fetch all restaurants where the **`cuisine_type`** field is not set or is null.
- SELECT * FROM RESTAURANTS WHERE cusine_type IS NULL;

**Problem 21:**

- **Prerequisite**: Understand how to count rows / documents in SQL / MongoDB
- **Problem**: Write a query to count the number of restaurants that have **`delivery_available`**.
- SELECT COUNT(*) FROM RESTAURANTS WHERE DELIVERY_AVAILABLE = TRUE;

**Problem 22:**

- **Prerequisite**: Understand using string patterns in SQL (LIKE clause) / using regex in MongoDB
- **Problem**: Write a query to fetch all restaurants whose **`location`** contains 'New York'.
-  SELECT * FROM RESTAURANTS WHERE LOCATION LIKE "bengaluru%";

**Problem 23:**

- **Prerequisite**: Understand how to use the AVG function in SQL / MongoDB's aggregate functions
- **Problem**: Write a query to calculate the average **`average_rating`** of all restaurants.
- SELECT AVG(average_rating) FROM RESTAURANTS;

**Problem 24:**

- **Prerequisite**: Understand how to limit results in SQL / MongoDB
- **Problem**: Write a query to fetch the top 5 restaurants when ordered by **`average_rating`** in descending order.
- SELECT * FROM RESTAURANTS ORDER BY average_rating DESC LIMIT 5;

**Problem 25:**

- **Prerequisite**: Understand data deletion in SQL / MongoDB
- **Problem**: Write a query to delete the restaurant with **`id`** 3.
- DELETE FROM RESTAURANTS WHERE ID = 3;

**Problem 26:**

- **Prerequisite**: Understand creating tables in SQL / collections in MongoDB
- **Problem**: Create a **`Rides`** table / collection with the fields defined above.
- CREATE TABLE Rides (
    id INT AUTO_INCREMENT PRIMARY KEY,
    driver_id INT,
    passenger_id INT,
    start_location VARCHAR(255),
    end_location VARCHAR(255),
    distance DECIMAL(5,2),
    ride_time DECIMAL(5,2),
    fare DECIMAL(6,2)
);

**Problem 27:**

- **Prerequisite**: Understand inserting data into SQL tables / MongoDB collections
- **Problem**: Insert five rows / documents into the **`Rides`** table / collection with data of your choice.
- INSERT INTO Rides (driver_id, passenger_id, start_location, end_location, distance, ride_time, fare)
VALUES (1, 101, 'Park Street', 'Downtown', 7.2, 30.5, 15.75);


**Problem 28:**

- **Prerequisite**: Understand how to order data in SQL / MongoDB
- **Problem**: Write a query to fetch all rides, ordered by **`fare`** in descending order.
- >SELECT * FROM RIDES ORDER BY fare DESC;

**Problem 29:**

- **Prerequisite**: Understand using math operations in SQL / MongoDB
- **Problem**: Write a query to calculate the total **`distance`** and total **`fare`** for all rides.
- >SELECT SUM(distance) AS total_distance, SUM(fare) AS total_fare FROM RIDES;

**Problem 30:**

- **Prerequisite**: Understand how to use the AVG function in SQL / MongoDB's aggregate functions
- **Problem**: Write a query to calculate the average **`ride_time`** of all rides.
- > SELECT AVG(ride_time) FROM RIDES;

**Problem 31:**

- **Prerequisite**: Understand using string patterns in SQL (LIKE clause) / using regex in MongoDB
- **Problem**: Write a query to fetch all rides whose **`start_location`** or **`end_location`** contains 'Downtown'.
- >SELECT * FROM RIDES WHERE start_location LIKE "Park%" OR end_location LIKE "Downtown%";

**Problem 32:**

- **Prerequisite**: Understand how to use the COUNT function in SQL / MongoDB's aggregate functions
- **Problem**: Write a query to count the number of rides for a given **`driver_id`**.
- >SELECT SUM(driver_id) FROM RIDES WHERE driver_id = 1;

**Problem 33:**

- **Prerequisite**: Understand data updating in SQL / MongoDB
- **Problem**: Write a query to update the **`fare`** of the ride with **`id`** 4.
- >UPDATE RIDES SET fare = 30.00 WHERE ID =6;

**Problem 34:**

- **Prerequisite**: Understand using GROUP BY in SQL / MongoDB's aggregate functions
- **Problem**: Write a query to calculate the total **`fare`** for each **`driver_id`**.
- ->SELECT DRIVER_ID, SUM(FARE) FROM RIDES GROUP BY DRIVER_ID;

**Problem 35:**

- **Prerequisite**: Understand data deletion in SQL / MongoDB
- **Problem**: Write a query to delete the ride with **`id`** 2.
- ->DELETE * FROM RIDES WHERE ID =3;
