# bamazon

Overview
A Node.js & MySQL digital storefront. This is a command line Node app that mimics a beloved online retailer.

Node.js
Three JavaScript files replicate the basics of a simple ecommerce engine:

BamazonCustomer.js (See example here)

Receives orders from customers via the command line and interfaces with mySQL to deplete stock from the store's inventory.
BamazonManager.js (See example here)

Mimics the basics of a warehouse management system, providing managers with a list of options to view stock and adjust inventory.
A sample of the menu is below:
View Products for Sale
View Low Inventory
Add to Inventory
Add New Product
BamazonExecutive.js (See example here)

Simulates very basic profit and sales insights for upper management.
A sample of the menu is below:
View Product Sales by Department
Create New Department
MySQL
The JavaScript files mentioned above query a MySQL database called Bamazon which is locally hosted on my laptop.

Please refer to the schema.sql file to see how the database was created using raw SQL queries.

If you wish to run this app on your own machine, then please note the following commands:

If you are new to MySQL, please set up MySQL and MySQL Workbench on your laptop and then open up to your localhost connection.
Run CREATE DATABASE Bamazon; in mySQL Workbench.
Be sure to select the correct database by running the USE Bamazon;
Refer to the raw SQL commands under the === First Table === comment to set up the Products table.
Refer to the raw SQL commands under the === Second Table === comment to set up the Departments table.
Node Package Manager (npm)
If you clone this repo down to your machine, note that it has two npm dependencies! Before running the JavaScript files mentioned above, please run npm install in your terminal to download the prompt and mysql node packages.

Screenshots
Below are some screenshots that show the functionality of the app.


Below is a demo of the BamazonCustomer.js file...
Running node BamazonCustomer.js will use MySQL to pull up all the products for sale.
The customer can then choose a product using its ID and then enter a quantity to buy. Customer Order
If the inventory has enough items, the order will be processed. Order Valid
If the inventory is lacking, the order will not be processed. Order Invalid

Below is a demo of the BamazonManager.js file...
Running node BamazonManager.js will display a menu and perform the specific requests. Manager Menu
The manager can choose option 1 to view the current inventory. Manager 1
The manager can choose option 2 to see low items in inventory (less than 5 in stock). Manager 2
The manager can choose option 3 to re-stock existing items. Manager 3
The manager can choose option 4 to add new items for sale. Manager 4a
Notice how the inventory was adjusted from steps 3 and 4. Manager 4b

Below is a demo of the BamazonExecutive.js file...
Running node BamazonExecutive.js will display a menu and perform the specific requests. Executive Menu
The executive can choose option 1 to view the sales by department. Executive 1
The executive can choose option 2 to add a new department. Executive 2a
Notice how the department list was adjusted from step 2. Executive 2a
Also note that the manager can add a new item to the department and if a customer buys said item, it will cause total sales and profit to increase in that department.
