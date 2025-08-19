# LEARNING SQLITE3

## Connecting to a Database

```python3
connection = sqlite3.connect("database.db")
```

## Creating a Cursor

```python3
cursor = connection.cursor()
```

## Creating Table

```python3
cursor.execute("""
CREATE TABLE customers (
  first_name DATATYPE,
  last_name DATATYPE,
  age DATATYPE,
  email DATATYPE
)
""")
```

### Type of Data

| Type | How to Declare |
|------|----------------|
| Text | TEXT |
| Numeric | NUM |
| Integer | INT |
| Real | REAL |
| Blob | (empty string) |

```python3
cursor.execute("""
CREATE TABLE customers (
  first_name TEXT,
  last_name TEXT,
  age INT,
  email TEXT
)
""")
```

## Commiting and Closing

```python3
connection.commit()
connection.close()
```

## Insering Data into Database

```python3
connection.execute("INSERT INTO customers VALUES ('Jotta', 'Vanish', 30, 'jottavanish@email.com')")
```
## Inserting More Than One Data at a Time

```python3
customers = [
  ('Mary', 'Kuewa', 69, mary@email.com),
  ('Steeve', 'Pas', 47, steeve@email.com),
  ('Dan', 'Brown', 50, dan@email.com),
]

connection.executemany("INSERT INTO customers VALUES (?,?,?)", customers)
```

## Seeing What's Inside the Database

```python3
connection.execute("SELECT * FROM customers")
# print(connection.fetchone())
# print(connection.fetchmany(2))
print(connection.fetchall())
```

```python3

```
