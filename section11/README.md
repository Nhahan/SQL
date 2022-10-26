- FOREIGN KEY

```
CREATE TABLE customers(
    id INT AUTO_INCREMENT PRIMARY KEY,
    first_name VARCHAR(100),
    last_name VARCHAR(100),
    email VARCHAR(100)
);
```

```
CREATE TABLE orders(
    id INT AUTO_INCREMENT PRIMARY KEY,
    order_date DATE,
    amount DECIMAL(8,2),
    customer_id INT,
    FOREIGN KEY(customer_id) REFERENCES customers(id)
);
```

- IMPLICIT INNER JOIN

```
SELECT * FROM customers, orders 
WHERE customers.id = orders.customer_id;
```
 
- EXPLICIT INNER JOINS

```
SELECT * FROM customers
JOIN orders
    ON customers.id = orders.customer_id;
```