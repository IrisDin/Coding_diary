---
cover: >-
  https://images.squarespace-cdn.com/content/v1/5daddb33ee92bf44231c2fef/1593634997762-75P05A5AKO859N5G9OMU/medical-algorithms.gif
coverY: 0
---

# R

{% embed url="https://www.rstudio.com/resources/cheatsheets" %}

快捷键command+shift+ m = %>%

## DPLYR PACKAGE

{% embed url="https://dplyr.tidyverse.org/reference/index.html" %}
Dplyr offcial API Document
{% endembed %}

**select()**

* select column

variable\_name < - select(dataframe, column)

**filter()**

* select rows

filter(dataframe, row\_name == value)

**mutate()**

* create a new column

mutate(dataframe, column\_name = operation)

**arrange()**

* change the order of rows

arrange(dataframe, column\_to\_arrrange\_by)

**summarize()**

* consolidate data in rows

summarize(dataframe, column\_name = function(column))

**group\_by()**

* segregate groups in dataframe

group\_by(dataframe, column\_\_name)

**np\_data %>% group\_by(Region) %>% summarize(distinct\_parks = n\_distinct(ParkName))**

\_\_

_**Pull** a vector or value_

pull() can extract specific vectors and values It is similar to $ It is mostly useful because it looks a little nicer in pipes

**Lag**

find the previous values in a vetor

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
