Write the SELECT queries to do the following:-
Note : To solve below queries use “sales” database
1. Write a query that produces all rows from the Customers
table for which the salesperson’s number is 1001.

sol . select * from customers where snum=1001;


2. Write a select command that produces the rating followed
by the name of each customer in San Jose.

Sol. select rating , cname from customers WHERE city='San Jose';

3. Write a query that will produce the snum values of all
salespeople from the Orders table (with the duplicate values
suppressed).

Sol. SELECT DISTINCT snum FROM orders;

4. Write a query that will display all the orders for amount
more than Rs. 1,000.

Sol.SELECT * FROM orders WHERE amt>1000;

5. Write a query that will give you the names and cities of
all salespeople in London with a commission above 0.10.

sol. SELECT sname, city FROM salespeople where city='London' AND comm>0.10;

6. Write an SQL query that returns all customers who have a rating greater than 100, along with the customers located in Rome regardless of their rating.

sol. SELECT * FROM customers WHERE rating > 100 OR city='Rome';

7. What will be the output from the following query?
Select * from Orders where (amt < 1000 OR NOT (odate = ‘1990-10-03’ AND cnum > 2003));

sol. Qry1 . SELECT * FROM orders WHERE amt<1000;
        --it will return all orders of amount less then 1000.
    
    Qry2 . SELECT * FROM orders WHERE odate='1990-10-03' AND cnum>2003;
        --it will return all orders whose date is '1990-10-03' and cnum is greater than 2003.
    
    Qry3 . SELECT * FROM orders WHERE NOT(odate='1990-10-03' AND cnum>2003);
        --it will return orders whose odate and cnum is not '1990-10-03' and greater than 2003 respectively at same time.

    Qry4 . SELECT * FROM orders WHERE (amt < 1000 OR NOT (odate ='1990-10-03' AND cnum > 2003));
        --it will return all orders whose odate and cnum is not '1990-10-03' and greater than 2003 at same time or where amt is less than 1000.  

8. What will be the output of the following query?
Select * from Orders where NOT (odate = ‘1990-10-03’ OR snum>1006) AND amt >= 1500;

sol. it is very similar to last question with very little difference .
     it will return orders odate is not '1990-10-03' and snum is not greater than 1006 and amt is greater than 1500.

9. What is a simpler way to write this query?
Select snum, sname, city, comm 
from Salespeople
Where (comm >= .12 AND comm <= .14);

sol. select * 
     FROM salespeople
     WHERE comm BETWEEN .12 AND .14;

10. Write a query that selects all orders except those
with amount less than 100.

sol. SELECT *
     FROM orders
     WHERE NOT(amt<100);