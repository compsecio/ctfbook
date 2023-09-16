# SQL Injection

Many systems rely on databases as their backend. Take for instance an online store that sells items through a website. The website relies on databases to store not only pricing information, inventory status, and shipping info, but also user account information such as addresses, usernames, and passwords. The standard language used to communicate with many relational databases is known as Structured Query Language, aka SQL. 

The problem comes when the SQL query is based on elements of user input. The designers may have intended the user to provide details crucial to an inventory search, but threat actors have included portions of a SQL query.

