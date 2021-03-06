---
cover: >-
  https://images.squarespace-cdn.com/content/v1/5daddb33ee92bf44231c2fef/1593634997762-75P05A5AKO859N5G9OMU/medical-algorithms.gif
coverY: 0
---

# ð R

{% embed url="https://www.rstudio.com/resources/cheatsheets" %}

å¿«æ·é®command+shift+ m = %>%

å¿«æ·é® âoptionâ + â-â = < -

command shift c ä¸é®æ³¨éä»£ç 

**åä»£ç æ§è¡ãCtrl+Enterã**æèå¨é¨ä»£ç æ§è¡**ãCtrl+Shift+Enterã**

## DPLYR PACKAGE

**dplyr** æ¿æäº tidyverse ä¸­æåºæ¬ä¹æéè¦çæ°æ®å¤çãè½¬æ¢ãåæåè½ã

ä¸»è¦éè¿ %>% ç®¡éç¬¦å·æ¥è¿æ¥ä¸åçåé

{% embed url="https://dplyr.tidyverse.org/reference/index.html" %}
Dplyr offcial API Document
{% endembed %}

äºä¸ª `dplyr` æ ¸å¿å½æ°ï¼

* ä½¿ç¨ `filter()` ç­éè¡\

* ä½¿ç¨ `arrange()` æåè¡\

* ä½¿ç¨ `select` éåå\

* ç¨ç°æçåéåå»ºæ°åé `mutate()`\

* èåå¹¶è®¡ç®æè¦ç»è®¡é `summarize()`

ä¸é¢çææå½æ°é½å¯ä»¥å `group_by()` å½æ°èåèµ·æ¥ä½¿ç¨ï¼`group_by()` å½æ°å¯ä»¥æ¹åä»¥ä¸æ¯ä¸ªå½æ°çä½ç¨èå´ï¼è®©å¶ä»å¨æ´ä¸ªæ°æ®éä¸æä½åä¸ºå¨æ¯ä¸ªåéçæ°´å¹³ä¸åå«æä½ã



**è¿äºå½æ°æå®å¨ç¸åçåæ°ç»æåå·¥ä½æ¹å¼ï¼**

* ç¬¬ä¸ä¸ªåæ°æ¯æ°æ®éï¼è¡¨ææä»¬æ³å¯¹ä»ä¹æ°æ®è¿è¡å¤ç\

* éåçåæ°æ¯åéåç§°ï¼ä¸å¸¦å¼å·ï¼æè¿°äºå¨æ°æ®ä¸è¿è¡ä»ä¹å¤çï¼ä¸åçåéä¹é´ç¨éå·åé\

* å®ä»¬ä¸ä¼æ¹ååæ°æ®ï¼èæ¯çæä¸ä¸ªæ°çæ°æ®æ¡**(dataframe)**



### **select()**

* select column

variable\_name < - select(dataframe, column)

selectå¯ä»¥éè¿åçéæ©è¿è¡åå¹¶å¹¶çæä¸ä¸ªæç¨çå­é

```
#ä¸¾ä¾ï¼åªéæ©caseï¼death, country è¿è¡åæ
covid_datset %>% select(case, death, country)
```

### **filter()**

* select rows

filter(dataframe, row\_name == value)

`filter()` å¯ä»¥åºäºè§æµå¼ç­éè¡ï¼ç¬¦åæ¡ä»¶çè¡çä¸ï¼ä¸ç¬¦åæ¡ä»¶çè¢«åé¤ï¼æç»å¾å°ä¸ä¸ªè§æµå­éãç¬¬ä¸ä¸ªåæ°æ¯æ°æ®éçåç§°ï¼ç¬¬äºä¸ªåæ°ä»¥åéåçåæ°æ¯ç¨æ¥ç­éè¡çæ¡ä»¶

```
# æ¯å¦ç¨æ¥éä¸­2æ13å·çæææ°å çä¾
covid_case_day %>% filter(month ==2, day == 13)
```

### **mutate()**

* create a new column

mutate(dataframe, column\_name = operation)

çæä¸ä¸ªæ°çå

### **arrange()**

* change the order of rows

arrange(dataframe, column\_to\_arrrange\_by)

`arrange()`ä¸ `filter()` ç¸ä¼¼ï¼ä½å®ä¸æ¯ç­éè¡ï¼èæ¯æ¹åè¡çé¡ºåºã

å®æ¥åä¸ä¸ªæ°æ®éåä¸ç»ä½ä¸ºæåºä¾æ®çååï¼æèæ´å¤æçè¡¨è¾¾å¼ï¼

ä½ä¸ºåæ°ï¼å¦æååä¸æ­¢ä¸ä¸ªï¼é£ä¹å°±æ¯ç¨åé¢çåå¨åé¢æåºçåºç¡ä¸ç»§ç»­æåº

```
# ä¾æ¬¡æç§ year -> month -> day ä¸ä¸ªåéæååºæåº
cases %>% arrange(year, month, day)
```

å¦ææ³è¦ææåéåºæåè¡ï¼å¯ä»¥å¯¹è¯¥ååä½¿ç¨å½æ°`desc()`ï¼

```
# æç§caseçæ°éä»å¤§å°å°æåº
cases %>% arrange(desc(case))
```

### **summarize()**

* consolidate data in rows

summarize(dataframe, column\_name = function(column))

ç¨æ¥è®¡ç®æè¦ç»è®¡éï¼å¯ä»¥å°æ°æ®æ¡(dataframe)æå æä¸è¡

```
# è®¡ç®èªç­å¹³åå»¶è¯¯æ¶é´
summarize(flights,delay = mean(dep_delay,na.rm = TRUE))
```

### **group\_by()**

* segregate groups in dataframe

group\_by(dataframe, column\_\_name)

&#x20;**E.g. np\_data %>% group\_by(Region) %>% summarize(distinct\_parks = n\_distinct(ParkName))**



æä»¬ä¸è¬å°group\_byå½æ°åsummarize ä¸èµ·ä½¿ç¨ï¼



### **nï¼ï¼è®¡æ°å½æ°**

`n()` å½æ°æ¯ä¸ä¸ªä¸æè¦å½æ° `summarize()` éåçè®¡æ°å½æ°**ã**

å®ä¸éè¦ä»»ä½åæ°ï¼åç¬ä½¿ç¨æ¶ï¼å®è®¡ç®çå°±æ¯è¡è®¡æ°ï¼nrowï¼

å `group_by()` èåä½¿ç¨æ¶ï¼å®å¯ä»¥è®¡ç®åç»åéçæ¯ä¸ªæ°´å¹³ä¸åæå¤å°ä¸ªè§æµ**ï¼observationï¼**

****

`n()`ä¼æç¼ºå¤±å¼ä¹åå«å°è®¡æ°ä¸­ï¼å¦ææ³è¦è®¡ç®åºéç¼ºå¤±å¼çæ°éï¼å¯ä»¥ä½¿ç¨`sum(is.na(x))`ãå¦ææ³è¦è®¡ç®å¯ä¸å¼çæ°éï¼å¯ä»¥ä½¿ç¨`n_distinct()`

```
## åªä¸ªç®çå°ææå¤çèªç©ºå¬å¸ï¼
flights %>% 
  group_by(dest) %>% 
  summarize(carriers = n_distinct(carrier)) %>% 
  arrange(desc(carriers))

# è¾åºç»æ
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

![](<../.gitbook/assets/æªå±2022-02-07 ä¸å9.26.41.png>)

![](<../.gitbook/assets/æªå±2022-02-07 ä¸å9.27.16.png>)

## GGPLOT PACKAGE

{% embed url="https://ggplot2.tidyverse.org/reference" %}
ggplot documentation
{% endembed %}

### ggplot Cheatsheet

![](<../.gitbook/assets/æªå±2022-02-10 ä¸å8.14.49.png>)

![](<../.gitbook/assets/æªå±2022-02-10 ä¸å8.15.06 (1).png>)
