# SQL cheat sheet

## Querying data from a table
Query data in columns c1, c2 from a table:
> SELECT c1, c2 FROM t;

Query all rows and columns from a table SELECT c1, c2 FROM t:
> SELECT * FROM t;

Query data and filter rows with a condition
> WHERE condition;

SELECT DISTINCT c1 FROM t
WHERE condition;
Query distinct rows from a table
SELECT c1, 62 FROM t
ORDER BY c1 ASC [DESC]; Sort the result set in ascending or descending
order
SELECT c1, 62 FROM t
ORDER BY c1
LIMIT n OFFSET offset;
Skip offset of rows and return the next n rows
SELECT c1, aggregate(c2)
FROM t
GROUP BY cl;
Group rows using an aggregate function
SELECT c1, aggregate(c2)
FROM t
GROUP BY cl
HAVING condition;
Filter groups using HAVING clause
