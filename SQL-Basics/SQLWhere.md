# The SQL WHERE Clause

The WHERE clause is used to filter records.

The WHERE clause is used to extract only those records that fulfills a specified condition.

## WHERE Syntax

```
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

```
**Note:** The WHERE clause is not only used in SELECT statement, it is also used in UPDATE, DELETE statement, etc.!
```

## Demo Database 

| CustomerID  | CustomerName  | ContactName | Address | City | PostalCode | Country |
| ----------- | ------------- | ----------- | ------- | ---- | ---------- | ------- |
| 1 | Alfreds Futterkiste | Maria Anders | Obere Str. 57 | Berlin | 12209 | Germany |
| 2	| Ana Trujillo Emparedados y helados | Ana Trujillo | Avda. de la Constitución | 2222 | México D.F. | 05021	| Mexico |
| 3 | Antonio Moreno Taquería |	Antonio Moreno | Mataderos 2312 | México D.F.	| 05023 | Mexico |
| 4  | Around the Horn |	Thomas Hardy | 120 Hanover Sq. | London	| WA1 1DP |	UK |
| 5	| Berglunds snabbköp | Christina Berglund | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |



## WHERE Clause Example
The following SQL statement selects all the customers from the country "Mexico", in the "Customers" table:

### Example
```
SELECT * FROM Customers WHERE Country='Mexico';
```

### Sample output:

| CustomerID  | CustomerName  | ContactName | Address | City | PostalCode | Country |
| ----------- | ------------- | ----------- | ------- | ---- | ---------- | ------- |
| 2	| Ana Trujillo Emparedados y helados | Ana Trujillo | Avda. de la Constitución | 2222 | México D.F. | 05021	| Mexico |
| 3 | Antonio Moreno Taquería |	Antonio Moreno | Mataderos 2312 | México D.F.	| 05023 | Mexico |


## Text Fields vs. Numeric Fields
SQL requires single quotes around text values (most database systems will also allow double quotes).

However, numeric fields should not be enclosed in quotes.

### Example
```
SELECT * FROM Customers WHERE CustomerID=1;
```

Operators in The WHERE Clause
The following operators can be used in the WHERE clause:

| Operator |	Description	Example |
| -------- | ---------------------- |  
| =	| Equal	|
| >	| Greater than |	
| <	| Less than	|
| >= | Greater than or equal	|
| <= | Less than or equal |	
| <> | Not equal. **Note:** In some versions of SQL this operator may be written as != |	
| BETWEEN |	Between a certain range	|
| LIKE | Search for a pattern |	
| IN | To specify multiple possible values for a column |