# RUN THIS QUERY TO CREATE TABLE
```sql
create table products(
product_id serial primary key,
name varchar(100) not null,
sku_code char(8) unique not null check (char_length(sku_code) = 8),
price numeric(10,2) default 0 check(price >= 0),
stock_quantity int default 0 check (stock_quantity >= 0),
is_available boolean default TRUE,
category text not null,
added_on text default current_date,
last_updated timestamp default now()
);
```

# RUN THIS QUERY TO INSERT DATA IN TABLE
```sql
INSERT INTO products (name, sku_code, price , stock_quantity, is_available, category)
VALUES
('Wireless Mouse', 'WM123456', 699.99, 50, TRUE, 'Electronics'),
('Bluetooth Speaker', 'BS234567', 1499.00, 30, TRUE, 'Electronics'),
('Laptop Stand', 'LS345678', 799.50, 20, TRUE, 'Accessories'),
('USB-C Hub', 'UC456789', 1299.99, 15, TRUE, 'Accessories'),
('Notebook', 'NB567890', 99.99, 100, TRUE, 'Stationery'),
('Pen Set', 'PS678901', 199.00, 200, TRUE, 'Stationery'),
('Coffee Mug', 'CM789012', 299.00, 75, TRUE, 'Home & Kitchen'),
('LED Desk Lamp', 'DL890123', 899.00, 40, TRUE, 'Home & Kitchen'),
('Yoga Mat', 'YM901234', 499.00, 25, TRUE, 'Fitness'),
('Water Bottle', 'WB012345', 349.00, 60, TRUE, 'Fitness');
```

# RUN THIS QUERY LINE BY LINE TO UNDERSTAND CLAUSES
```sql
select name, price from products;
select * from products where category = 'Electronics';
select category from products group by category;
select category, count(*) from products group by category having count(*) > 1;
select * from products order by price asc;
select * from products limit 3;
select name as item_name, price as item_price from products;
select distinct category from products;
```

# TEST 2 SOLUTION QUERY
```sql
select name, price from products where price = (select min(price) from products);
select round(avg(price),2) from products where category in ('Home & Kitchen', 'Fitness');
select name, stock_quantity from products where stock_quantity > 50 and is_available = true and price != 299.00;
```