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

