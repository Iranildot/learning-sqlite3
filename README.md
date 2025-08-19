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

```python3

```
