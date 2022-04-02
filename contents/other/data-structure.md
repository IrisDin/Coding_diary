# Data Structure

## 排序二叉树（Binary Tree）



![binary tree](https://anran758.github.io/blog/2018/01/10/%E6%B7%B1%E5%85%A5%E5%AD%A6%E4%B9%A0%E4%B9%8B%E6%8E%92%E5%BA%8F%E4%BA%8C%E5%8F%89%E6%A0%91/banner.png)

二叉树的定义

树(Tree), 是(n>=0)个节点的有限集. 其中 n=0 时, 我们称之为空树. 在一棵非空树中, 只有一个根节点. 在二叉树中, 每个节点最多有两个子节点. 一般称为左节点和右节点(左、右子树).



排序二叉树

二叉排序树(Binary Sort Tree)又称二叉查找树，它是一种特殊的二叉树，它或为空树，或具有以下性质的二叉树:

1. 它的右子树非空，则右子树上所有节点的值都大于根节点的值。
2. 它的左子树非空，则左子树上所有节点的值都小于根节点的值。
3. 左右子树各是一颗二叉排序树。

```
// 伪代码
There are lot of T-shirt that displayed in store that well-arranged by size
Input: List of shirts sorted by size and a target value to find

### binary search
while there are more than 1 shirt remaining:
    mid = the shirt size of the shirt in the middle
    if target == mid:
        buy the shirt!
    else if target > mid:
        throw out all the shirts of size < mid
    else: # target < mid
        throw out all the shirts of size > mid

If we made it outside this loop and still haven't found the shirt,
  we can report that the shirt size is not in the list of shirts
```

![From CSE163 class example](https://static.us.edusercontent.com/files/L1acPpljKePoYxYCo2PGaIHB)

## KD-Tree

![](https://static.us.edusercontent.com/files/L4ukDreKA09zhDjayA9dFHyL)

{% embed url="https://youtu.be/9SDC8yip2kQ" %}

