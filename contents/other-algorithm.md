---
cover: >-
  https://images.squarespace-cdn.com/content/v1/5daddb33ee92bf44231c2fef/1593634997762-75P05A5AKO859N5G9OMU/medical-algorithms.gif
coverY: 0
---

# Other/Algorithm

### I**nverted index**反向索引

<mark style="background-color:purple;">（搜索引擎工作原理</mark>

简单来说，正向索引是通过key找value，反向索引是通过value来找key

文档是有许多的单词组成的，其中每个单词也可以在同一个文档中重复出现很多次，当然，同一个单词也可以出现在不同的文档中。

**正向索引(forward index)**：**从文档角度看其中的单词**，表示每个文档（用文档ID标识）都含有哪些单词，以及每个单词出现了多少次（词频/TF：**terms  frequency**）及其出现位置（相对于文档首部的偏移量）。

**反向索引(inverted index)**：**从单词角度看文档**，标识每个单词分别在那些文档中出现(文档ID)，以及在各自的文档中每个单词分别出现了多少次（词频/TF：terms  frequency）及其出现位置（相对于该文档首部的偏移量）

> An inverted index is just a dictionary, where the **keys** are the **words found in the corpus** and the **value** for a key is a **list of all the documents** that have that word in them.

**当我们把反向索引当成一个字典的时候，key是用户输入的单词，value是数据库中含有关键字的所有文档**

![example](https://static.us.edusercontent.com/files/2vV4eOC5105cnsjoxofM1v1j)

### TF-IDF算法

TF-IDF(term frequency–inverse document frequency)是一种用于**信息检索**与**数据挖掘**的常用加权技术，常用于**挖掘文章中的关键词**。

TF-IDF有两层意思，一层是**"词频"**（Term Frequency，缩写为TF），另一层是**"逆文档频率"**（Inverse Document Frequency，缩写为IDF）。

假设我们现在有一片长文，词频高在文章中往往是停用词，“**的**”，“**是**”，“**了**”等，这些在文档中最常见但对结果毫无帮助、需要过滤掉的词，**用TF可以统计到这些停用词并把它们过滤**。当高频词过滤后就只需考虑剩下的有实际意义的词。

但这样又会遇到了另一个问题，我们可能发现有些词的出现次数一样多。这是不是意味着，作为关键词，它们的重要性是一样的？



所以在**关键词排序**上，需要IDF给**常见的词较小的权重**，它的大小与一个词的常见程度成反比。

**一个词预测主题的能力越强，权重越大，反之，权重越小**。



**当有TF(词频)和IDF(逆文档频率)后，将这两个词相乘，就能得到一个词的TF-IDF的值。某个词在文章中的TF-IDF越大，那么一般而言这个词在这篇文章的重要性会越高，所以通过计算文章中各个词的TF-IDF，由大到小排序，排在最前面的几个词，就是该文章的关键词**

#### **TF-IDF算法步骤**

第一步，计算词频

![](https://pic2.zhimg.com/v2-393435b342546a2f1736d1d755adb1cd\_r.jpg)

第二步，计算逆文档频率：

这时，需要一个语料库（corpus），用来模拟语言的使用环境



![](https://pic2.zhimg.com/v2-1d5c436e04f497544d72fec6909a3fad\_r.jpg)

如果一个词越常见，那么分母就越大，逆文档频率就越小越接近0。分母之所以要加1，是为了避免分母为0（即所有文档都不包含该词）。log表示对得到的值取对数。

\
第三步，计算TF-IDF：

![](https://pic3.zhimg.com/80/v2-5560a4b2efa3330021b8b2ef13a471fe\_1440w.jpg)

TF-IDF与一个词在文档中的出现次数成正比，与该词在整个语言中的出现次数成反比。所以，自动提取关键词的算法就很清楚了，就是**计算出文档的每个词的TF-IDF值，然后按降序排列，取排在最前面的几个词**

****

**优缺点：**

TF-IDF的优点是简单快速，而且容易理解。缺点是有时候用**词频**来衡量文章中的一个词的重要性不够全面，有时候重要的词出现的可能不够多，而且这种计算无法体现位置信息，无法体现词在上下文的重要性。还有是没有考虑语序，武松打虎 ， 虎打武松，这种统计是一样的特征表示。

### &#x20;KNN算法（k-nearest neighbors）



\






####

****
