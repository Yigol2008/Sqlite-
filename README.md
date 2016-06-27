

##创建数据库
```sql
CREATE DATABASE database_name
```

##创建一个新表
```sql
CREATE TABLE database_name.table_name(
   column1 datatype  PRIMARY KEY(one or more columns),
   column2 datatype,
   column3 datatype,
   .....
   columnN datatype,
);
```

##INSERT INTO语句
####有两个基本的语法INSERT INTO语句如下：
```sql
INSERT INTO TABLE_NAME (column1, column2, column3,...columnN)]  
VALUES (value1, value2, value3,...valueN);
```

####在这里， column1, column2,...columnN 是要插入数据表中的列的名称。也可能不需要指定列名在SQLite查询，如果要添加表中的所有列的值。但要确保的是在相同的顺序表中的列值的顺序。 SQLite 的 INSERT INTO语法如下：
```sql
INSERT INTO TABLE_NAME VALUES (value1,value2,value3,...valueN);
```



##SELECT语句：

####SQLite 的 SELECT语句的基本语法如下：
```sql
SELECT column1, column2, columnN FROM table_name;
```
####在这里， column1, column2...是一个表，要将其值取的字段。如果想获取在该字段的所有可用的字段，那么可以使用下面的语法：
```sql
SELECT * FROM table_name;
```
####列出了所有在数据库中创建表: 
```sql
SELECT tbl_name FROM sqlite_master WHERE type = 'table';
```

<!--####表达式SELECT语句的基本语法：
```sql
SELECT column1, column2, columnN 
FROM table_name 
WHERE [CONTION | EXPRESSION];
```-->

##WHERE子句：
####SELECT语句的基本语法与WHERE子句如下：
```sql
SELECT column1, column2, columnN 
FROM table_name
WHERE [condition]
```

##AND/OR操作符
```sql
SELECT column1, column2, columnN 
FROM table_name
WHERE [condition1] AND [condition2]...AND [conditionN];

SELECT column1, column2, columnN 
FROM table_name
WHERE [condition1] OR [condition2]...OR [conditionN]
```


##UPDATE 查询
####SQLite 的UPDATE查询用于修改现有的表中的记录。可以使用UPDATE查询的WHERE子句更新选定行，否则所有的行会被更新。
```sql
UPDATE table_name
SET column1 = value1, column2 = value2...., columnN = valueN
WHERE [condition];
```

```sql
```

##AND和OR运算符:
```sql
SELECT column1, column2, columnN 
FROM table_name
WHERE [condition1] AND [condition2]...AND [conditionN];
```

##UPDATE查询用于修改现有的表中的记录:
```sql
UPDATE table_name
SET column1 = value1, column2 = value2...., columnN = valueN
WHERE [condition];
```

####LIMIT 子句用于限制由 SELECT 语句返回的数据量:
```sql
 SELECT column1, column2, columnN 
FROM table_name
LIMIT [no of rows]

SELECT column1, column2, columnN 
FROM table_name
LIMIT [no of rows] OFFSET [row num]
```

##ORDER BY 子句
####ORDER BY是用来递增或递减的顺序，根据一个或多个列中的数据进行排序,ORDER BY子句的基本语法如下：
```sql
SELECT column-list 
FROM table_name 
[WHERE condition] 
[ORDER BY column1, column2, .. columnN] [ASC | DESC];
```
##LIKE 子句
####LIKE操作符是用来反对使用通配符的模式匹配的文本值。如果搜索表达式可以匹配的图案表达，LIKE运算将返回true，也就是1。有两个通配符与LIKE运算符一起使用：
####百分号 (%)
####下划线 (_)
####百分号表示零个，一个或多个数字或字符。下划线代表一个单一的数字或字符。这些符号可以被组合使用。
####％和_的基本语法如下：
```sql
SELECT FROM table_name
WHERE column LIKE 'XXXX%'
```

####or 
```sql
SELECT FROM table_name
WHERE column LIKE '%XXXX%'
```

####or
```sql
SELECT FROM table_name
WHERE column LIKE 'XXXX_'
```

####or
```sql
SELECT FROM table_name
WHERE column LIKE '_XXXX'
```

####or
```sql
SELECT FROM table_name
WHERE column LIKE '_XXXX_'
```



##LIMIT 子句
####LIMIT子句的SELECT语句的基本语法如下：
```sql
SELECT column1, column2, columnN 
FROM table_name
LIMIT [no of rows]
```
####以下是LIMIT子句时一起使用OFFSET子句的语法：
```sql
SELECT column1, column2, columnN 
FROM table_name
LIMIT [no of rows] OFFSET [row num]
```

##GROUP BY
####SQLite 的 GROUP BY子句用于协作 SELECT语句相同的数据成组以便安排。GROUP BY 子句如下SELECT语句中的WHERE子句之前的ORDER BY子句。
```sql
SELECT column-list
FROM table_name
WHERE [ conditions ]
GROUP BY column1, column2....columnN
ORDER BY column1, column2....columnN
```

##HAVING 子句
####以下是HAVING子句的SELECT查询中的位置：
```sql
SELECT
FROM
WHERE
GROUP BY
HAVING
ORDER BY
```
####HAVING子句必须遵循在GROUP BY子句中的查询，也必须先如果使用ORDER BY子句。以下是SELECT语句的语法，包括HAVING子句：
```sql
SELECT column1, column2
FROM table1, table2
WHERE [ conditions ]
GROUP BY column1, column2
HAVING [ conditions ]
ORDER BY column1, column2
```
##DISTINCT 关键字
####DISTINCT关键字消除重复记录的基本语法如下：
```sql
SELECT DISTINCT column1, column2,.....columnN 
FROM table_name
WHERE [condition]
```

##JOINS连接
####INNER JOIN
```sql
SELECT column_name(s)
FROM table_name1
INNER JOIN table_name2 
ON table_name1.column_name=table_name2.column_name
```
####LEFT JOIN
```sql
SELECT column_name(s)
FROM table_name1
LEFT JOIN table_name2 
ON table_name1.column_name=table_name2.column_name
```
####RIGHT JOIN
```sql
SELECT column_name(s)
FROM table_name1
RIGHT JOIN table_name2 
ON table_name1.column_name=table_name2.column_name
```


##SQL MAX() 函数

####SQL MAX() 语法，MAX 函数返回一列中的最大值。NULL 值不包括在计算中。
```sql
SELECT MAX(column_name) FROM table_name
```
