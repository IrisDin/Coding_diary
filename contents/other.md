---
cover: >-
  https://images.squarespace-cdn.com/content/v1/5daddb33ee92bf44231c2fef/1593634997762-75P05A5AKO859N5G9OMU/medical-algorithms.gif
coverY: 0
---

# Other

### I**nverted index**反向索引

<mark style="background-color:purple;">（搜索引擎工作原理</mark>

简单来说，正向索引是通过key找value，反向索引是通过value来找key

文档是有许多的单词组成的，其中每个单词也可以在同一个文档中重复出现很多次，当然，同一个单词也可以出现在不同的文档中。

**正向索引(forward index)**：**从文档角度看其中的单词**，表示每个文档（用文档ID标识）都含有哪些单词，以及每个单词出现了多少次（词频/TF：**terms  frequency**）及其出现位置（相对于文档首部的偏移量）。

**反向索引(inverted index)**：**从单词角度看文档**，标识每个单词分别在那些文档中出现(文档ID)，以及在各自的文档中每个单词分别出现了多少次（词频/TF：terms  frequency）及其出现位置（相对于该文档首部的偏移量）

> An inverted index is just a dictionary, where the **keys** are the **words found in the corpus** and the **value** for a key is a **list of all the documents** that have that word in them.

**当我们把反向索引当成一个字典的时候，key是用户输入的单词，value是数据库中含有关键字的所有文档**

![example](https://static.us.edusercontent.com/files/2vV4eOC5105cnsjoxofM1v1j)

****
