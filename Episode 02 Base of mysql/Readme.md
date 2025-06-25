
## ✅ **1. Data Definition Language (DDL)**

| Command              | Description                           | Example                                            |
| -------------------- | ------------------------------------- | -------------------------------------------------- |
| `CREATE DATABASE`    | Create a new database                 | `CREATE DATABASE squid_game;`                      |
| `DROP DATABASE`      | Delete a database                     | `DROP DATABASE squid_game;`                        |
| `USE`                | Select a database                     | `USE squid_game;`                                  |
| `SHOW DATABASES`     | List all databases                    | `SHOW DATABASES;`                                  |
| `CREATE TABLE`       | Create a table                        | `CREATE TABLE players (id INT, name VARCHAR(50));` |
| `DROP TABLE`         | Delete a table                        | `DROP TABLE players;`                              |
| `ALTER TABLE`        | Modify table structure                | `ALTER TABLE players ADD age INT;`                 |
| `RENAME TABLE`       | Rename a table                        | `RENAME TABLE players TO contestants;`             |
| `DESC` or `DESCRIBE` | View structure of a table             | `DESC players;`                                    |
| `TRUNCATE TABLE`     | Remove all records but keep structure | `TRUNCATE TABLE players;`                          |

---

## ✅ **2. Data Manipulation Language (DML)**

| Command                     | Description                              | Example                                                  |
| --------------------------- | ---------------------------------------- | -------------------------------------------------------- |
| `INSERT INTO`               | Add a full row                           | `INSERT INTO players VALUES (1, 'Ali', 30);`             |
| `INSERT INTO ... (columns)` | Add a row with selected columns          | `INSERT INTO players (name, age) VALUES ('Gi-hun', 45);` |
| `INSERT INTO ... SET`       | Another way to insert                    | `INSERT INTO players SET name = 'Sae-byeok', age = 27;`  |
| `UPDATE`                    | Modify existing data                     | `UPDATE players SET age = 31 WHERE id = 1;`              |
| `DELETE`                    | Remove specific records                  | `DELETE FROM players WHERE id = 1;`                      |
| `TRUNCATE`                  | Remove all data (faster, can't rollback) | `TRUNCATE TABLE players;`                                |

---

## ✅ **3. Data Query Language (DQL)**

| Command                        | Description            | Example                                    |
| ------------------------------ | ---------------------- | ------------------------------------------ |
| `SELECT * FROM`                | Fetch all data         | `SELECT * FROM players;`                   |
| `SELECT column1, column2 FROM` | Fetch specific columns | `SELECT name, age FROM players;`           |
| `WHERE`                        | Filter results         | `SELECT * FROM players WHERE age > 25;`    |
| `LIMIT`                        | Limit number of rows   | `SELECT * FROM players LIMIT 5;`           |
| `ORDER BY`                     | Sort results           | `SELECT * FROM players ORDER BY age DESC;` |

---

## 📚 **Assignments to Practice**

### 🔹 **Assignment 1: Create & Manage a Database**

* Create a database called `game_arena`
* Create a table called `participants` with columns:

  * `id` (INT, primary key)
  * `name` (VARCHAR(50))
  * `age` (INT)
  * `game` (VARCHAR(30))
  * `score` (INT)
* Insert 5 records using all 3 insert styles.
* Add a new column `status` (VARCHAR(10)) to the table.
* Rename column `game` to `game_name`
* Change data type of `score` to FLOAT
* Change size of `name` column to 100 chars
* Delete the column `status`

---

### 🔹 **Assignment 2: Data Manipulation**

* Update the `score` of one player.
* Set one player's `game_name` to `NULL`
* Delete one player’s record.
* Use `TRUNCATE` to clear the table.
* Drop the table.

---

### 🔹 **Assignment 3: Queries**

* Recreate the `participants` table with data again.
* Fetch all players older than 25.
* Fetch players whose name starts with ‘A’.
* Display only names and scores.
* Order players by score (highest to lowest).
* Fetch top 3 players using `LIMIT`.

---

