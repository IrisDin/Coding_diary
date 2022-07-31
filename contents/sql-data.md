# 1 SQL/DATA

### SQL 查询

Select 查询某些属性列（specific columns）的语法

`SELECT column（列名）, another_column, … FROM mytable（表名）;`

Select 查询所有列`SELECT * FROM mytable（表名）;`

``

### 条件查询 (constraints)

![](<../.gitbook/assets/截屏2022-07-30 下午8.41.55.png>)

![](<../.gitbook/assets/截屏2022-07-30 下午8.42.23.png>)

虽然之前我们的SQL 关键之如 `SELECT`, `WHERE`, `AND,OR` 都是大写的，但SQL其实是兼容写成 select,where小写的. 大写这些关键字有助于我们把 关键字 和 你的表名，列名区分开，让 SQL更容易理解。

\
我们已经学会了`WHERE` 语句来筛选数字类型的属性，如果属性是字符串, 我们会用到字符串相关的一些操作符号，其中 LIKE（模糊查询） 和 %（通配符） 是新增的两个

![](<../.gitbook/assets/截屏2022-07-30 下午8.58.49.png>)



### SQL Filtering过滤 和 sorting排序

选取出唯一的结果的语法`SELECT`` `**`DISTINCT`**` ``column, another_column, … FROM mytable WHERE`` `_`condition(s)`_`;`

``

结果排序（ordered results）`SELECT column, another_column, … FROM mytable WHERE`` `_`condition(s)`_` ```` `**`ORDER BY column ASC/DESC`**`;`

``

limited查询`SELECT column, another_column, … FROM mytable WHERE`` `_`condition(s)`_` ``ORDER BY column ASC/DESC`` `**`LIMIT num_limit OFFSET num_offset`**`;`

``

``
