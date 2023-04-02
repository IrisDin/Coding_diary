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

![](<../.gitbook/assets/截屏2022-08-01 下午7.52.24.png>)

### 用JOINs进行多表联合查询

用INNER JOIN 连接表的语法

`SELECT column, another_table_column, … FROM mytable （主表）`&#x20;

**`INNER JOIN another_table （要连接的表） ON mytable.id = another_table.id (想象一下刚才讲的主键连接，两个相同的连成1条)`**

&#x20;`WHERE`` `_`condition(s)`_` ``ORDER BY column, … ASC/DESC`&#x20;

`LIMIT num_limit OFFSET num_offset;`

![](<../.gitbook/assets/截屏2022-08-01 下午8.13.06.png>)

* `INNER JOIN` 只会保留两个表都存在的数据

用LEFT/RIGHT/FULL JOINs 做多表查询

`SELECT column, another_column, … FROM mytable`&#x20;

**`INNER/LEFT/RIGHT/FULL JOIN another_table`**

&#x20;**`ON mytable.id = another_table.matching_id`**` ```&#x20;

`WHERE`` `_`condition(s)`_` ```&#x20;

`ORDER BY column, … ASC/DESC`&#x20;

`LIMIT num_limit OFFSET num_offset;`

![](<../.gitbook/assets/截屏2022-08-01 下午8.38.11.png>)



### NULL



