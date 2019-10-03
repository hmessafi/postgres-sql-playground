# SQL NULL Values

## What is a NULL Value?
A field with a NULL value is a field with no value.

If a field in a table is optional, it is possible to insert a new record or update a record without adding a value to this field. Then, the field will be saved with a NULL value.

```
**Note**: A NULL value is different from a zero value or a field that contains spaces. A field with a NULL value is one that has been left blank during record creation!
```

## How to Test for NULL Values?
It is not possible to test for NULL values with comparison operators, such as =, <, or <>.

We will have to use the IS NULL and IS NOT NULL operators instead.

## IS NULL Syntax

```
SELECT column_names
FROM table_name
WHERE column_name IS NULL;
```

## IS NOT NULL Syntax

```
SELECT column_names
FROM table_name
WHERE column_name IS NOT NULL;
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


## The IS NULL Operator
The IS NULL operator is used to test for empty values (NULL values).

The following SQL lists all customers with a NULL value in the "Address" field:

### Example

```
SELECT CustomerName, ContactName, Address
FROM Customers
WHERE Address IS NULL;
```

```
**Tip**: Always use IS NULL to look for NULL values.
```

## The IS NOT NULL Operator
The IS NOT NULL operator is used to test for non-empty values (NOT NULL values).

The following SQL lists all customers with a value in the "Address" field:

### Example

```
SELECT CustomerName, ContactName, Address
FROM Customers
WHERE Address IS NOT NULL;
```



