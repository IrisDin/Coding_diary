---
cover: >-
  https://images.squarespace-cdn.com/content/v1/5daddb33ee92bf44231c2fef/1593634997762-75P05A5AKO859N5G9OMU/medical-algorithms.gif
coverY: 0
---

# 🐇 R

{% embed url="https://www.rstudio.com/resources/cheatsheets" %}

快捷键command+shift+ m = %>%

快捷键 “option” + “-” = < -

command shift c 一键注释代码

**块代码执行【Ctrl+Enter】**或者全部代码执行**【Ctrl+Shift+Enter】**

## DPLYR PACKAGE

**dplyr** 承担了 tidyverse 中最基本也最重要的数据处理、转换、分析功能。

主要通过 %>% 管道符号来连接不同的变量

{% embed url="https://dplyr.tidyverse.org/reference/index.html" %}
Dplyr offcial API Document
{% endembed %}

五个 `dplyr` 核心函数：

* 使用 `filter()` 筛选行\

* 使用 `arrange()` 排列行\

* 使用 `select` 选取列\

* 用现有的变量创建新变量 `mutate()`\

* 聚合并计算摘要统计量 `summarize()`

上面的所有函数都可以和 `group_by()` 函数联合起来使用，`group_by()` 函数可以改变以上每个函数的作用范围，让其从在整个数据集上操作变为在每个变量的水平上分别操作。



**这些函数有完全相同的参数结构和工作方式：**

* 第一个参数是数据集，表明我们想对什么数据进行处理\

* 随后的参数是变量名称（不带引号）描述了在数据上进行什么处理，不同的变量之间用逗号分隔\

* 它们不会改变原数据，而是生成一个新的数据框**(dataframe)**



### **select()**

* select column

variable\_name < - select(dataframe, column)

select可以通过列的选择进行合并并生成一个有用的子集

```
#举例，只选择case，death, country 进行分析
covid_datset %>% select(case, death, country)
```

### **filter()**

* select rows

filter(dataframe, row\_name == value)

`filter()` 可以基于观测值筛选行，符合条件的行留下，不符合条件的被剔除，最终得到一个观测子集。第一个参数是数据集的名称，第二个参数以及随后的参数是用来筛选行的条件

```
# 比如用来选中2月13号的所有新冠病例
covid_case_day %>% filter(month ==2, day == 13)
```

### **mutate()**

* create a new column

mutate(dataframe, column\_name = operation)

生成一个新的列

### **arrange()**

* change the order of rows

arrange(dataframe, column\_to\_arrrange\_by)

`arrange()`与 `filter()` 相似，但它不是筛选行，而是改变行的顺序。

它接受一个数据集和一组作为排序依据的列名（或者更复杂的表达式）

作为参数，如果列名不止一个，那么就是用后面的列在前面排序的基础上继续排序

```
# 依次按照 year -> month -> day 三个变量按升序排序
cases %>% arrange(year, month, day)
```

如果想要按某列降序排列行，可以对该列名使用函数`desc()`：

```
# 按照case的数量从大到小排序
cases %>% arrange(desc(case))
```

### **summarize()**

* consolidate data in rows

summarize(dataframe, column\_name = function(column))

用来计算摘要统计量，可以将数据框(dataframe)折叠成一行

```
# 计算航班平均延误时间
summarize(flights,delay = mean(dep_delay,na.rm = TRUE))
```

### **group\_by()**

* segregate groups in dataframe

group\_by(dataframe, column\_\_name)

&#x20;**E.g. np\_data %>% group\_by(Region) %>% summarize(distinct\_parks = n\_distinct(ParkName))**



我们一般将group\_by函数和summarize 一起使用，



### **n（）计数函数**

`n()` 函数是一个与摘要函数 `summarize()` 配合的计数函数**。**

它不需要任何参数，单独使用时，它计算的就是行计数（nrow）

和 `group_by()` 联合使用时，它可以计算分组变量的每个水平上各有多少个观测**（observation）**

****

`n()`会把缺失值也包含到计数中，如果想要计算出非缺失值的数量，可以使用`sum(is.na(x))`。如果想要计算唯一值的数量，可以使用`n_distinct()`

```
## 哪个目的地有最多的航空公司？
flights %>% 
  group_by(dest) %>% 
  summarize(carriers = n_distinct(carrier)) %>% 
  arrange(desc(carriers))

# 输出结果
#> # A tibble: 105 x 2
#>   dest  carriers
#>   <chr>    <int>
#> 1 ATL          7
#> 2 BOS          7
#> 3 CLT          7
#> 4 ORD          7
#> 5 TPA          7
#> 6 AUS          6
#> # ... 
```

_**Pull** a vector or value_

pull() can extract specific vectors and values It is similar to $ It is mostly useful because it looks a little nicer in pipes



**Lag**

**find the previous values in a vetor**

useful in comparing values behind the current values

cases < - c(1, 5, 10, 17, 19, 25)

lag(cases) NA 1 5 10 17 19

cases - lag(cases)

NA 4 5 7 2 6



**Unite**

* unite mutiple dataframe into a single column
* unite(df,col='col\_name', c('col1,col2), sep="")





### DPLYR Cheatsheet

![](<../.gitbook/assets/截屏2022-02-07 下午9.26.41.png>)

![](<../.gitbook/assets/截屏2022-02-07 下午9.27.16.png>)

## GGPLOT PACKAGE

{% embed url="https://ggplot2.tidyverse.org/reference" %}
ggplot documentation
{% endembed %}

### ggplot Cheatsheet

![](<../.gitbook/assets/截屏2022-02-10 下午8.14.49.png>)

![](<../.gitbook/assets/截屏2022-02-10 下午8.15.06 (1).png>)
