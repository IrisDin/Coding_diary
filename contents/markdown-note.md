---
cover: >-
  https://images.squarespace-cdn.com/content/v1/5daddb33ee92bf44231c2fef/1593634997762-75P05A5AKO859N5G9OMU/medical-algorithms.gif
coverY: 0
---

# Markdown Note

## Markdown 代码

用反引号把它包起来（\`）

```
`printf()` 函数：
```

用 \`\`\` 包裹一段代码，并指定一种语言（也可以不指定）：

````
```javascript
$(document).ready(function () {
    alert('RUNOOB');
});
```
````

## Markdown 链接

```
[链接名称](链接地址)

或者

<链接地址>
```

比如：

```
这是一个链接 [google](https://www.google.com)
直接使用链接地址：
<https://www.google.com>
```



## Markdown 图片

* 开头一个感叹号 !
* 接着一个方括号，里面放上图片的替代文字
* 接着一个普通括号，里面放上图片的网址，最后用引号包住并加上选择性的 'title' 属性的文字。

```
![alt 属性文本](图片地址)

![alt 属性文本](图片地址 "可选标题")
```

```
![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png)

![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png "RUNOOB")
```

Markdown 还没有办法指定图片的高度与宽度，如果需要，可以使用普通的 \<img> 标签。

```
<img src="http://static.runoob.com/images/runoob-logo.png" width="50%">
```



## Markdown 表格

Markdown 制作表格使用 | 来分隔不同的单元格，使用 - 来分隔表头和其他行。

语法格式如下：

```
|  表头   | 表头  |
|  ----  | ----  |
| 单元格  | 单元格 |
| 单元格  | 单元格 |
```

**对齐方式**

**我们可以设置表格的对齐方式：**

* \-: 设置内容和标题栏居右对齐。
* \:- 设置内容和标题栏居左对齐。
* \:-: 设置内容和标题栏居中对齐。

语法格式：

```
| 左对齐 | 右对齐 | 居中对齐 |
| :-----| ----: | :----: |
| 单元格 | 单元格 | 单元格 |
| 单元格 | 单元格 | 单元格 |
```

## Markdown 文本

### 文字样式

```
*斜体文本*
_斜体文本_
**粗体文本**
__粗体文本__
***粗斜体文本***
___粗斜体文本___
```

### 分隔线

可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：

```
***

* * *

*****

- - -

----------
```

### 删除线

文字两端加上波浪线

```
~~BAIDU.COM~~
```

### 下划线

下划线可以通过 HTML 的 \<u> 标签来实现：

```
<u>带下划线文本</u>
```

\


