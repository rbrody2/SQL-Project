# SQL-Project
The first thing that I wanted to do was to create a customer table. In this table I included the ID of the customer, their first name and last name, their age, and the city they live in. As you can see I made the CustomerID column in a way that it would increment by 1 with each new customer. 

![customer table](https://user-images.githubusercontent.com/74119720/102001205-4d66cb80-3cbd-11eb-9a7e-658c2d169a7d.png) 

The second thing that I wanted to do was make a product table with the ID of the product, the product name, and the price of the product. 

![product](https://user-images.githubusercontent.com/74119720/102001209-56579d00-3cbd-11eb-90cb-227cd19367f1.png)

The next task I had to do was create an orders table with the ID of the customer, and the order date. I added the CustomerID column from the customer table as a foreign key to the orders table. I then joined these two tables together through the CustomerID column of the customer table and the Customer_ID column of the orders table as shown below: 

![order](https://user-images.githubusercontent.com/74119720/102001211-5c4d7e00-3cbd-11eb-9fd4-88cf85c3c607.png)

My next task was to create an ER diagram in order to understand how to relate my tables. As you can see I have the products table with its three attributes and the ProductID as the primary key. You can also see that products and orders have a many to many relationship. In the customer table we can see its five attributes the CustomerID as the primary key. The customer table has a one to many relationship with the orders table so we can use a foreign key from the customer table to relate to the orders table. We next look at the orders table with its three attributes and OrderID as the primary key. The Customer_ID attribute will actually be used to join the customer and orders table later on. The last table we will look at is the purchases table which related all the other tables together. It has purchase_id as its primary key and its three other attributes being used to join the other three tables together into one table. 
![ER](https://user-images.githubusercontent.com/74119720/102001223-70917b00-3cbd-11eb-9e44-85aa58e7a7b8.png)
I then created a relational scheme to relate all of my tables. As you can see I took the CustomerID from the customer table and used it as a foreign key in the orders table. In order to relate all of my tables together, I then took the ProductID, OrderID, and CustomerID and used them on foreign keys on my purchases table.  
![relational](https://user-images.githubusercontent.com/74119720/102001217-64a5b900-3cbd-11eb-9b13-6967ddd9ce98.png)
By creating the ER diagram and relational schema, I was able to create my purchases table which relates all of my tables together. As you can see I have the purchase_id as the primary key and this table also include the order_id, the product_id and the customer_id. I joined the customer table with this table through the CustomerID column of the customer table and the customer_id column of the purchases table. I also joined the orders table with this table through the OrderID column of the orders table and the order_id column of the purchases tables. Lastly, I joined the product table with this table through the ProductID column of the products table and the product_id column of the purchases table. As you can see, there are 4 orders and order 1 has two products purchases by Ron Brody where he bought two baseballs.  
![purchases](https://user-images.githubusercontent.com/74119720/102001221-6c655d80-3cbd-11eb-8c8d-ac44599358d2.png)

My last task was to find which customer spent the most money. I grouped the customers by LastName and found that Brody spent the most money with 13.5 dollars. 

![total last name](https://user-images.githubusercontent.com/74119720/102001212-62435f00-3cbd-11eb-9b0b-c79e25051749.png)
