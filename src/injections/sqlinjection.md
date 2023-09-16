# SQL Injection

Many systems rely on databases as their backend. Take for instance an online store that sells items through a website. The website relies on databases to store not only pricing information, inventory status, and shipping info, but also user account information such as addresses, usernames, and passwords. The standard language used to communicate with many relational databases is known as Structured Query Language, aka SQL. 

The problem comes when the SQL query is based on elements of user input. The designers may have intended the user to provide details crucial to an inventory search, but threat actors have included portions of a SQL query itself to steer execution in their desired direction.

The classic example is evaluating username and password by simply pulling them from a database. A query might look like 

```SQL
SELECT * FROM users WHERE userid = 
```

A developer could build this query in a naive way by reading in a string from the user and storing it in a variable, say ```userid_input```.

Then 
```
sql_string = "SELECT * FROM users WHERE userid = " + userid_input;
```

The string above would allow malicious users to inject SQL commands of their own. For example, if the user entered ```something OR 1 = 1```, the query would then be:
```
sql_string = "SELECT * FROM users WHERE userid = something OR 1 = 1";
```

where the OR statement is paired with something that is always true.

---

Most CTF players will develop cheat sheets on common SQL injections, especially since there can be subtle differences in how different database vendors handle queries. 

[Example SQL Injection cheat sheet.](https://exploit-notes.hdks.org/exploit/web/security-risk/sql-injection-cheat-sheet/)

