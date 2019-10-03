# The SQL ORDER BY Keyword

The ORDER BY keyword is used to sort the result-set in ascending or descending order.

The ORDER BY keyword sorts the records in ascending order by default. To sort the records in descending order, use the DESC keyword.

## ORDER BY Syntax

```
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
```

## Demo Database
Below is a selection from the "Customers" table in the Northwind sample database:

| CustomerID  | CustomerName  | ContactName | Address | City | PostalCode | Country |
| ----------- | ------------- | ----------- | ------- | ---- | ---------- | ------- |
| 1 | Alfreds Futterkiste | Maria Anders | Obere Str. 57 | Berlin | 12209 | Germany |
| 2	| Ana Trujillo Emparedados y helados | Ana Trujillo | Avda. de la Constitución | 2222 | México D.F. | 05021	| Mexico |
| 3 | Antonio Moreno Taquería |	Antonio Moreno | Mataderos 2312 | México D.F.	| 05023 | Mexico |
| 4 | Around the Horn |	Thomas Hardy | 120 Hanover Sq. | London	| WA1 1DP |	UK |
| 5	| Berglunds snabbköp | Christina Berglund | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |


## ORDER BY Example
The following SQL statement selects all customers from the "Customers" table, sorted by the "Country" column:

### Example

```
SELECT * FROM Customers
ORDER BY Country;
```

### Output

| CustomerID  | CustomerName  | ContactName | Address | City | PostalCode | Country |
| ----------- | ------------- | ----------- | ------- | ---- | ---------- | ------- |
| 1 | Alfreds Futterkiste | Maria Anders | Obere Str. 57 | Berlin | 12209 | Germany |
| 2	| Ana Trujillo Emparedados y helados | Ana Trujillo | Avda. de la Constitución | 2222 | México D.F. | 05021	| Mexico |
| 3 | Antonio Moreno Taquería |	Antonio Moreno | Mataderos 2312 | México D.F.	| 05023 | Mexico |
| 5	| Berglunds snabbköp | Christina Berglund | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |
| 4 | Around the Horn |	Thomas Hardy | 120 Hanover Sq. | London	| WA1 1DP |	UK |


## ORDER BY DESC Example
The following SQL statement selects all customers from the "Customers" table, sorted DESCENDING by the "Country" column:

### Example

```
SELECT * FROM Customers
ORDER BY Country DESC;
```

### Output
| CustomerID  | CustomerName  | ContactName | Address | City | PostalCode | Country |
| ----------- | ------------- | ----------- | ------- | ---- | ---------- | ------- |
| 4 | Around the Horn |	Thomas Hardy | 120 Hanover Sq. | London	| WA1 1DP |	UK |
| 5	| Berglunds snabbköp | Christina Berglund | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |
| 2	| Ana Trujillo Emparedados y helados | Ana Trujillo | Avda. de la Constitución | 2222 | México D.F. | 05021	| Mexico |
| 3 | Antonio Moreno Taquería |	Antonio Moreno | Mataderos 2312 | México D.F.	| 05023 | Mexico |
| 1 | Alfreds Futterkiste | Maria Anders | Obere Str. 57 | Berlin | 12209 | Germany |


## ORDER BY Several Columns Example
The following SQL statement selects all customers from the "Customers" table, sorted by the "Country" and the "CustomerName" column. This means that it orders by Country, but if some rows have the same Country, it orders them by CustomerName:

### Example

```
SELECT * FROM Customers
ORDER BY Country, CustomerName;
```

## ORDER BY Several Columns Example 2
The following SQL statement selects all customers from the "Customers" table, sorted ascending by the "Country" and descending by the "CustomerName" column:

### Example

```
SELECT * FROM Customers
ORDER BY Country ASC, CustomerName DESC;
```