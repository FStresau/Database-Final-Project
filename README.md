# Food Delivery System Database  

### Team Members:  
- Jack Rodriguez  
- Sebastian Stresau  
- Charles Cahill  
- Susan Nunez  

---

## Overview  
The **Food Delivery System** is a database project designed for a service similar to Uber Eats. This system facilitates food delivery by connecting customers, drivers, and restaurants through a mobile application.  

### Types of Users:  
1. **Customers**: Place orders via the app and receive food deliveries.  
2. **Drivers**: Accept and deliver orders using the app.  
3. **Restaurants**: Manage incoming orders through their app interface.  
4. **Administrators**: Oversee the database and app operations.  

---

## Business Rules  
1. Each customer can be assigned multiple drivers.  
2. Each customer can place multiple orders.  
3. Each driver can serve multiple customers.  
4. Each driver can deliver multiple orders.  
5. Each driver is associated with one vehicle.  
6. Each order is assigned to one driver.  
7. Each order is placed by one customer.  
8. Each order is fulfilled by one restaurant.  
9. Each restaurant can fulfill multiple orders.  
10. Each vehicle is registered to one driver.  
11. The app is downloaded by multiple customers.  
12. The app is downloaded by multiple drivers.  
13. The app is owned by one company.  
14. Each customer uses one app account.  
15. Each driver uses one app account.  
16. The app is managed by one company.  
17. Each company can have multiple managers.  
18. Each manager oversees multiple drivers.  
19. Each driver reports to one manager.  
20. Each company employs multiple drivers.  

---

## Entity Relationship (ER) Model  

### Entities and Attributes  
1. **Customer**  
   - Name  
   - Order History  
   - Rating  
   - Address  

2. **Driver**  
   - Name  
   - Rating  
   - Age  
   - Experience  

3. **Vehicle**  
   - Type  
   - Model Number  
   - Color  
   - Location  

4. **Order**  
   - Food  
   - Drink  
   - Special Requests  
   - Price  

5. **Restaurant**  
   - Name  
   - Address  
   - Cuisine Type  
   - Rating  

6. **App**  
   - User Count  
   - Rating  
   - Storage Size  
   - Feedback System  

7. **Company**  
   - Name  
   - Headquarters  
   - Regions  
   - Employee Count  

8. **Management**  
   - Name  
   - Location  
   - Age  
   - Salary  

---

## Relational Schema  

### Example Schema:  
```sql
CREATE TABLE Customer (
    Customer_ID INTEGER NOT NULL PRIMARY KEY,
    Customer_Name VARCHAR NOT NULL,
    Customer_Rating DOUBLE NOT NULL,
    Customer_Address VARCHAR NOT NULL
);

CREATE TABLE Driver (
    Driver_ID INTEGER NOT NULL PRIMARY KEY,
    Driver_Name VARCHAR NOT NULL,
    Driver_Rating DOUBLE NOT NULL,
    Driver_Age INTEGER NOT NULL
);

CREATE TABLE Vehicle (
    License_Plate VARCHAR NOT NULL PRIMARY KEY,
    Make VARCHAR NOT NULL,
    Model_NUM INTEGER NOT NULL,
    Color VARCHAR NOT NULL
);

CREATE TABLE FoodOrder (
    Order_ID INTEGER NOT NULL PRIMARY KEY,
    Food VARCHAR,
    Drink VARCHAR,
    Price DOUBLE NOT NULL
);


