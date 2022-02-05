---
cover: >-
  https://images.squarespace-cdn.com/content/v1/5daddb33ee92bf44231c2fef/1593634997762-75P05A5AKO859N5G9OMU/medical-algorithms.gif
coverY: 0
---

# R

快捷键command+shift+ m = %>%

## DPLYR PACKAGE

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

arrange(dataframe, column_to_arrrange\_by)



**summarize()**

* consolidate data in rows

summarize(dataframe, column\_name = function(column))



**group\_by()**

* segregate groups in dataframe

group_by(dataframe, column_\_name)

**np\_data %>% group\_by(Region) %>% summarize(distinct\_parks = n\_distinct(ParkName))**

__

_**Pull** a vector or value_

pull() can extract specific vectors and values It is similar to $ It is mostly useful because it looks a little nicer in pipes



**Lag**

cases  < - c(1, 5, 10, 17, 19, 25)&#x20;

lag(cases) NA 1 5 10 17 19

cases - lag(cases)

&#x20;NA 4 5 7 2 6



__















