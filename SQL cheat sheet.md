# SQL cheat sheet

## Querying data from a table
Query data in columns c1, c2 from a table:
> SELECT c1, c2 FROM t;

Query all rows and columns from a table SELECT c1, c2 FROM t:
> SELECT * FROM t;

Query data and filter rows with a condition:
> SELECT c1, c2 FROM t WHERE condition;

Query distinct rows from a table:
> SELECT DISTINCT c1 FROM t WHERE condition;

Sort the result set in ascending or descending
order:
> SELECT c1, 62 FROM t ORDER BY c1 ASC [DESC];

Skip offset of rows and return the next n rows:
> SELECT c1, 62 FROM t ORDER BY c1 LIMIT n OFFSET offset;

Group rows using an aggregate function:
> SELECT c1, aggregate(c2) FROM t GROUP BY cl;

Filter groups using HAVING clause:
> SELECT c1, aggregate(c2) FROM t GROUP BY cl HAVING condition;

## Querying data from multiple tables
Inner join t1 and t2:
> SELECT c1, c2 FROM t1 INNER JOIN t2 ON condition;

Left join t1 and t2:
> SELECT c1, c2 FROM t1 LEFT JOIN t2 ON condition;

Right join t1 and t2:
> SELECT c1, c2 FROM t1 RIGHT JOIN t2 ON condition;

Perform full outer join:
> SELECT c1, c2 FROM t1 FULL OUTER JOIN t2 ON condition;

Produce a Cartesian product of rows in tables:
> SELECT c1, c2 FROM t1 CROSS JOIN t2;

Another way to perform cross join:
> SELECT c1, c2 FROM t1, t2;

Join t1 to itself using INNER JOIN clause:
> SELECT c1, c2 FROM t1 A INNER JOIN t2 B ON condition;

## Using SQL operators
Combine rows from two queries:
> SELECT c1, c2 FROM t1 UNION [ALL] SELECT c1, C2 FROM 12;

Return the intersection of two queries:
> SELECT c1, 62 FROM t1 INTERSECT SELECT c1, 62 FROM 12;

Subtract a result set from another result set:
> SELECT c1, c2 FROM t1 MINUS SELECT c1, c2 FROM 12;

Query rows using pattern matching %, _:
> SELECT c1, 62 FROM t1 WHERE c1 [NOT] LIKE pattern;

Query rows in a list:
> SELECT c1, C2 FROM t WHERE c1 [NOT] IN value list;

Query rows between two values SELECT c1, c2 FROM t:
> SELECT c1, c2 FROM t WHERE c1 BETWEEN low AND high;

Check if values in a table is NULL or not:
> WHERE c1 IS [NOT] NULL;
