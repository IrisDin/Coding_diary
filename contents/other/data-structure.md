---
cover: >-
  https://images.squarespace-cdn.com/content/v1/5daddb33ee92bf44231c2fef/1593634997762-75P05A5AKO859N5G9OMU/medical-algorithms.gif
coverY: 0
---

# ð² Data Structure

## æåºäºåæ ï¼Binary Treeï¼



![binary tree](https://anran758.github.io/blog/2018/01/10/%E6%B7%B1%E5%85%A5%E5%AD%A6%E4%B9%A0%E4%B9%8B%E6%8E%92%E5%BA%8F%E4%BA%8C%E5%8F%89%E6%A0%91/banner.png)

äºåæ çå®ä¹

æ (Tree), æ¯(n>=0)ä¸ªèç¹çæéé. å¶ä¸­ n=0 æ¶, æä»¬ç§°ä¹ä¸ºç©ºæ . å¨ä¸æ£µéç©ºæ ä¸­, åªæä¸ä¸ªæ ¹èç¹. å¨äºåæ ä¸­, æ¯ä¸ªèç¹æå¤æä¸¤ä¸ªå­èç¹. ä¸è¬ç§°ä¸ºå·¦èç¹åå³èç¹(å·¦ãå³å­æ ).



æåºäºåæ 

äºåæåºæ (Binary Sort Tree)åç§°äºåæ¥æ¾æ ï¼å®æ¯ä¸ç§ç¹æ®çäºåæ ï¼å®æä¸ºç©ºæ ï¼æå·æä»¥ä¸æ§è´¨çäºåæ :

1. å®çå³å­æ éç©ºï¼åå³å­æ ä¸ææèç¹çå¼é½å¤§äºæ ¹èç¹çå¼ã
2. å®çå·¦å­æ éç©ºï¼åå·¦å­æ ä¸ææèç¹çå¼é½å°äºæ ¹èç¹çå¼ã
3. å·¦å³å­æ åæ¯ä¸é¢äºåæåºæ ã

```
// ä¼ªä»£ç 
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

