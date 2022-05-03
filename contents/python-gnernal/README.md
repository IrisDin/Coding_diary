---
cover: >-
  https://images.squarespace-cdn.com/content/v1/5daddb33ee92bf44231c2fef/1593634997762-75P05A5AKO859N5G9OMU/medical-algorithms.gif
coverY: 0
---

# 🐍 Python General

## Python运算符

### 算术运算符

假设变量 a=10，b=21：

| 运算符  | 描述                        | 实例                                         |
| ---- | ------------------------- | ------------------------------------------ |
| +    | 加 - 两个对象相加                | a + b 输出结果 31                              |
| -    | 减 - 得到负数或是一个数减去另一个数       | a - b 输出结果 -11                             |
| \*   | 乘 - 两个数相乘或是返回一个被重复若干次的字符串 | a \* b 输出结果 210                            |
| /    | 除 - x 除以 y                | b / a 输出结果 2.1                             |
| %    | 取模 - 返回除法的余数              | b % a 输出结果 1                               |
| \*\* | 幂 - 返回x的y次幂               | a\*\*b 为10的21次方                            |
| //   | 取整除 - 向下取接近商的整数           | <pre><code>>>> 9//2 # ans = 4</code></pre> |

### 比较运算符 <a href="#ysf2" id="ysf2"></a>

以下假设变量a为10，变量b为20：

| 运算符 | 描述                                                                    | 实例                 |
| --- | --------------------------------------------------------------------- | ------------------ |
| ==  | 等于 - 比较对象是否相等                                                         | (a == b) 返回 False。 |
| !=  | 不等于 - 比较两个对象是否不相等                                                     | (a != b) 返回 True。  |
| >   | 大于 - 返回x是否大于y                                                         | (a > b) 返回 False。  |
| <   | 小于 - 返回x是否小于y。所有比较运算符返回1表示真，返回0表示假。这分别与特殊的变量True和False等价。注意，这些变量名的大写。 | (a < b) 返回 True。   |
| >=  | 大于等于 - 返回x是否大于等于y。                                                    | (a >= b) 返回 False。 |
| <=  | 小于等于 - 返回x是否小于等于y。                                                    | (a <= b) 返回 True。  |

### 赋值运算符

以下假设变量a为10，变量b为20：

| 运算符   | 描述       | 实例                           |
| ----- | -------- | ---------------------------- |
| =     | 简单的赋值运算符 | c = a + b 将 a + b 的运算结果赋值为 c |
| +=    | 加法赋值运算符  | c += a 等效于 c = c + a         |
| -=    | 减法赋值运算符  | c -= a 等效于 c = c - a         |
| \*=   | 乘法赋值运算符  | c \*= a 等效于 c = c \* a       |
| /=    | 除法赋值运算符  | c /= a 等效于 c = c / a         |
| %=    | 取模赋值运算符  | c %= a 等效于 c = c % a         |
| \*\*= | 幂赋值运算符   | c \*\*= a 等效于 c = c \*\* a   |
| //=   | 取整除赋值运算符 | c //= a 等效于 c = c // a       |

### 逻辑运算符 <a href="#ysf4" id="ysf4"></a>

变量 a 为 10, b为 20:

| 运算符 | 逻辑表达式   | 描述                                                   | 实例                    |
| --- | ------- | ---------------------------------------------------- | --------------------- |
| and | x and y | 布尔"与" - 如果 x 为 False，x and y 返回 x 的值，否则返回 y 的计算值。    | (a and b) 返回 20。      |
| or  | x or y  | 布尔"或" - 如果 x 是 True，它返回 x 的值，否则它返回 y 的计算值。           | (a or b) 返回 10。       |
| not | not x   | 布尔"非" - 如果 x 为 True，返回 False 。如果 x 为 False，它返回 True。 | not(a and b) 返回 False |

### 成员运算符 <a href="#ysf6" id="ysf6"></a>

除了以上的一些运算符之外，Python还支持成员运算符，测试实例中包含了一系列的成员，包括字符串，列表或元组。

| 运算符    | 描述                                | 实例                                 |
| ------ | --------------------------------- | ---------------------------------- |
| in     | 如果在指定的序列中找到值返回 True，否则返回 False。   | x 在 y 序列中 , 如果 x 在 y 序列中返回 True。   |
| not in | 如果在指定的序列中没有找到值返回 True，否则返回 False。 | x 不在 y 序列中 , 如果 x 不在 y 序列中返回 True。 |

## Python数据结构总结

### 列表(List)

Python中列表是可变的，这是它区别于字符串和元组的最重要的特点，一句话概括即：列表可以修改，而字符串和元组不能。

以下是 Python 中列表的方法：

| 方法                | 描述                                                                                                                         |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------- |
| list.append(x)    | 把一个元素添加到列表的结尾，相当于 a\[len(a):] = \[x]。                                                                                      |
| list.extend(L)    | 通过添加指定列表的所有元素来扩充列表，相当于 a\[len(a):] = L。                                                                                    |
| list.insert(i, x) | 在指定位置插入一个元素。第一个参数是准备插入到其前面的那个元素的索引，例如 a.insert(0, x) 会插入到整个列表之前，而 a.insert(len(a), x) 相当于 a.append(x) 。                    |
| list.remove(x)    | 删除列表中值为 x 的第一个元素。如果没有这样的元素，就会返回一个错误。                                                                                       |
| list.pop(\[i])    | 从列表的指定位置移除元素，并将其返回。如果没有指定索引，a.pop()返回最后一个元素。元素随即从列表中被移除。（方法中 i 两边的方括号表示这个参数是可选的，而不是要求你输入一对方括号，你会经常在 Python 库参考手册中遇到这样的标记。） |
| list.clear()      | 移除列表中的所有项，等于del a\[:]。                                                                                                     |
| list.index(x)     | 返回列表中第一个值为 x 的元素的索引。如果没有匹配的元素就会返回一个错误。                                                                                     |
| list.count(x)     | 返回 x 在列表中出现的次数。                                                                                                            |
| list.sort()       | 对列表中的元素进行排序。                                                                                                               |
| list.reverse()    | 倒排列表中的元素。                                                                                                                  |
| list.copy()       | 返回列表的浅复制，等于a\[:]。                                                                                                          |

### 元组(Tuple)

Python 的元组与列表类似，不同之处在于元组的元素不能修改。

元组使用小括号 ( )，列表使用方括号 \[ ]。

元组创建很简单，只需要在括号中添加元素，并使用逗号隔开即可。

### 集合(Set)

集合是一个无序不重复元素的集。基本功能包括关系测试和消除重复元素。

可以用大括号({})创建集合。注意：如果要创建一个空集合，你必须用 set() 而不是 {} ；后者创建一个空的字典

### 字典(Dictionary)

序列是以连续的整数为索引，与此不同的是，字典以关键字为索引，关键字可以是任意不可变类型，通常用字符串或数值。

理解字典的最佳方式是把它看做无序的键=>值对集合。在同一个字典之内，关键字必须是互不相同。

一对大括号创建一个空的字典：{}

## zip函数

zip() 函数用于将可迭代的对象作为参数，将对象中对应的元素打包成一个个元组，然后返回由这些元组组成的列表。如果各个迭代器的元素个数不一致，则返回列表长度与最短的对象相同，利用 \* 号操作符，可以将元组解压为列表

```
>>>a = [1,2,3]
>>> b = [4,5,6]
>>> c = [4,5,6,7,8]
>>> zipped = zip(a,b)     # 打包为元组的列表
[(1, 4), (2, 5), (3, 6)]
>>> zip(a,c)              # 元素个数与最短的列表一致
[(1, 4), (2, 5), (3, 6)]
>>> zip(*zipped)          # 与 zip 相反，可理解为解压，返回二维矩阵式
[(1, 2, 3), (4, 5, 6)]
```

## 排序：

排序基本函数：**sorted()**, **lambda**

```
# sorted函数可以接受三个变量，key指定排序的元素，reverse判断是否逆序
sorted(iterable[,key][,reverse])

# lambda一般结构
 lambda argument: expression
 # 实际应用中一般会把lambda和sorted（）的key参数结合
```

### list/tuple排序

以下代码展示的是list的排序方法，tuple与list排序方法差差不多

```
lis = ['a', 'b', 'c']
print(sorted(lis))
# 运行结果：['a', 'b', 'c']
print(sorted(lis, reverse=True))
# 运行结果：['c', 'b', 'a']
```

### dict key排序

```
dic = {'c': 1, 'b': 2, 'a': 3}
print(sorted(dic))
# 运行结果：['a', 'b', 'c']
# 运行结果按照字母表顺序
print(sorted(dic, reverse=True))
# 运行结果：['c', 'b', 'a']
```

### dict value排序

**dict的排序只会取其`key`，所以需要`lambda`首先将其转换为`value`才能操作`value`排序**

```
dic = {'c': 1, 'b': 2, 'a': 3}
print(sorted(dic, key=lambda k: dic[k]))
# 运行结果：['c', 'b', 'a']
# 按照值排序
print(sorted(dic, key=lambda k: dic[k], reverse=True))
# 运行结果：['a', 'b', 'c']
```

### list嵌套排序

```
lis = [[4, 2, 9], [1, 5, 6], [7, 8, 3]]
# 按照list当中的第一个值作为key进行排序（默认从小到大
print(sorted(lis, key=lambda k: k[0]))
# 运行结果：[[1, 5, 6], [4, 2, 9], [7, 8, 3]]

# 按照list当中的第二个值作为key进行排序（默认从小到大
print(sorted(lis, key=lambda k: k[1]))
# 运行结果：[[4, 2, 9], [1, 5, 6], [7, 8, 3]]

# 按照list当中的第三个值作为key进行排序（默认从小到大
print(sorted(lis, key=lambda k: k[2]))
# 运行结果[[7, 8, 3], [1, 5, 6], [4, 2, 9]]

# 按照list当中的第一个值作为key进行排序（reverse = TRUE为反向排序（从大到小）
print(sorted(lis, key=lambda k: k[0], reverse=True))
# [[7, 8, 3], [4, 2, 9], [1, 5, 6]]
```

### dict嵌套排序

```
dic = {
    'a': {'x': 3, 'y': 2, 'z': 1},
    'b': {'x': 2, 'y': 1, 'z': 3},
    'c': {'x': 1, 'y': 3, 'z': 2},
}

# 按照dict value中的 x 的大小排序（从小到大）
print(sorted(dic, key=lambda k: dic[k]['x']))
# 运行结果['c', 'b', 'a']

# 按照dict value中的 y 的大小排序（从小到大）
print(sorted(dic, key=lambda k: dic[k]['y']))
# 运行结果['b', 'a', 'c']

# 按照dict value中的 x 的大小反向排序（从大到小）
print(sorted(dic, key=lambda k: dic[k]['x'], reverse=True))
# 运行结果['a', 'b', 'c']
```

### list嵌套dict排序

```
lis = [
    {'x': 3, 'y': 2, 'z': 1},
    {'x': 2, 'y': 1, 'z': 3},
    {'x': 1, 'y': 3, 'z': 2},
]

# 按照list当中的x的值进行排序（从小到大
print(sorted(lis, key=lambda k: k['x']))
# [{'z': 2, 'x': 1, 'y': 3}, {'z': 3, 'x': 2, 'y': 1},
  {'z': 1, 'x': 3, 'y': 2}]

# 按照list当中的y的值进行排序（从小到大
print(sorted(lis, key=lambda k: k['y']))
# [{'z': 3, 'x': 2, 'y': 1}, {'z': 1, 'x': 3, 'y': 2},
  {'z': 2, 'x': 1, 'y': 3}]

# 按照list当中的x的值进行反向排序（从大到小
print(sorted(lis, key=lambda k: k['x'], reverse=True))
# [{'z': 1, 'x': 3, 'y': 2}, {'z': 3, 'x': 2, 'y': 1},
  {'z': 2, 'x': 1, 'y': 3}]
```

### dict嵌套list排序

```
dic = {
    'a': [1, 2, 3],
    'b': [2, 1, 3],
    'c': [3, 1, 2],
}
# 按照dic value的第一个值从小到大排序，（value是一个list）
print(sorted(dic, key=lambda k: dic[k][0]))
# 运行结果['a', 'b', 'c']

# 按照dic value的第二个值从小到大排序，（value是一个list）
print(sorted(dic, key=lambda k: dic[k][1]))
# 运行结果['b', 'c', 'a']

# 按照dic value的第一个值从大到小反向排序，（value是一个list）
print(sorted(dic, key=lambda k: dic[k][0], reverse=True))
# 运行结果['c', 'b', 'a']
```

## 循环：

### While条件控制循环

![](https://pic1.zhimg.com/80/v2-c77b71617c152203dd267269943f488c\_1440w.jpg)

> 注意：while循环条件表达式总是为True，就会无限循环下去，变成死循环，所以要特别留意 while 循环的退出条件。

```
# 问：求 1-100的和
# 初始化i 和 sum的值
sum = i = 0  
while i <= 100:  # 循环控制条件
    sum = sum + i
    i + = 1   # 等同于i=i+1
print(sum) # 输出结果5050
```

### **break和continue语句**

* **break的功能是中断整个循环。**

```
# 使用for..in..循环遍历列表s1，当遍历的结果等于4的时候会执行break语句。
# 该语句的功能是中断了整个循环。所以4之后的所有数字都不会被打印出来。
s1 = [1, 2, 3, 4, 5, 6, 7, 8, 9]
for i in s1:
    if i == 4:
        break
    print(i)

# 运行结果应该为 1,2,3
```

```
# break嵌套循环
for i in range(3):    # i=0,1,2
    for j in range(4):   # j=0,1,2,3
        if j > i:
            break
    print((i,j))  # 和第二个for对齐
    
# 运行结果
(0, 1)
(1, 2)
(2, 3)
```

* **continue的功能是跳出某一次循环并继续执行下一次。**

```
# 使用for..in..循环遍历列表s1，当遍历的结果等于4的时候会执行continue语句。
# 该语句的功能是跳出当前循环，继续执行下一次循环。所以除了数字4其他的数字都可以被打印出来。
s1 = [1, 2, 3, 4, 5]
for i in s1:
    if i == 4:
        continue
    print(i)
# 运行结果应该为 1,2,3,5
```

```
# continue嵌套循环
for i in range(3):
    for j in range(4):
        if j > i:
            continue
    print((i,j))
    
# 运行结果
(0, 3)
(1, 3)
(2, 3)
```

## 数据结构复杂度

### Big-O 表示法：

Big-O 表示法是一种测量操作时间复杂度的方法。

在一个算法中会执行许多操作。这些操作包括迭代集合，复制元素或整个集合，将元素附加到集合，在集合的开头或结尾插入元素，删除元素或更新集合中的元素。

**Big-O** 用来衡量操作的时间复杂度。它测量算法运行需要花费的时间

假设程序输入的大小为 n ,以下的是常见的Big-O符号。

* <mark style="background-color:yellow;">O(1)</mark>: 无论输入的 n 有多大，执行操作所需的**时间恒定**。这是常数复杂度，最快的算法。例如，检查集合中是否存在元素，时间复杂度是 O(1)。不论算法代码有多少行，只要其中没有**循环、递归，**按前文所介绍计算方法，其时间复杂度都是Ο(1)。\


```
# example of O(1) from CSE163
# 尽管函数中有循环，但是与输入值n无关，所以时间复杂度为O(1)
def method(n):
    t = 0
    for i in range(3):
        for j in range(14):
            t += n
        
        for j in range(200):
            t += j
    return j
```

* <mark style="background-color:yellow;">O(log n):</mark> 随着输入的增加，执行操作所需的时间呈**对数增加**。这是对数时间复杂度。一般优化后搜索算法是O(log n)，比如二分查找。\

* <mark style="background-color:yellow;">O(n)</mark>: 随着输入的增加，执行操作所需的时间呈**线性增加**。这是线性时间复杂度。就性能而言，属于中等。 例如，如果想对一个集合中的所有元素求和，那么必须遍历该集合中的全部元素。 因此时间复杂度是O(n)。

```
# example of O(n) from course CSE163
def method1(n):
    value = 0
    for i in range(n):
        for j in range(9):
            value += 7 * i + j
    return value ** 2 
```

* <mark style="background-color:yellow;">O(nlog n)</mark>: 快速排序算法的时间复杂度通常为O(nlog n)。\

* <mark style="background-color:yellow;">O(n^2)</mark>: 平方时间度复杂度，如两层嵌套的循环

```
# example of O(n^2) from course CSE163
# 有两层嵌套的循环（nested for loop),所以时间复杂度为n^2
def method(nums):
    max_diff = None
    for n1 in nums:
        for n2 in nums:
            diff = n1 - n2
            if max_diff is None or diff > max_diff:
                diff = max_diff
    return max_diff
```

```
# example of O(n^2) from course CSE163
# for this code, "n" is the length of the given list of numbers nums
def method(nums):
    x = len(nums)
    t = 0
    for i in range(x * x / 2):
        t += i
    return t
```

* <mark style="background-color:yellow;">O(n!):</mark> 阶乘时间复杂度，它非常缓慢。

![comparison between different models](https://d33wubrfki0l68.cloudfront.net/1010f5d18ec531e5f14ab93361391e2d51e7bc82/51941/images/big-o/big-o-graph.svg)

![](https://pic4.zhimg.com/80/v2-51a7065f3b3ea8c68a42c03832fb5853\_1440w.jpg)

**\*简单的例子比较函数的复杂度**

```
def sum1(n):                 # Total: n + 3 steps
    total = 0                # 1 step
    for i in range(n + 1):   # Runs n + 1 times, for a total of n + 1
        total += i           #   1 step
    return total             # 1 step


def sum2(n):                 # Total: 1 step
    return n * (n + 1) // 2  # 1 step
```

Sum1 (n)运行**（n+3）**步，而sum2(n)总是运行**1**步

如图所示，所以sum1（n）会随着输入值n的增加而呈线性增加，而sum2（n）是恒定的

![](https://static.us.edusercontent.com/files/UEmjcGL60KC1zovZQd88i3Q4)

## Python 类（Class)

### 类定义

语法格式如下：

```
class ClassName（object）:
    <statement-1>
    .
    <statement-N>
```

```
 class MyClass:
    """一个简单的类实例"""
    i = 12345
    def f(self):
        return 'hello world'
 
# 实例化类
x = MyClass()
 
# 访问类的属性和方法
print("MyClass 类的属性 i 为：", x.i)
print("MyClass 类的方法 f 输出为：", x.f())
```

以上创建了一个新的类实例并将该对象赋给局部变量 x，x 为空的对象。

执行以上程序输出结果为：

```
MyClass 类的属性 i 为： 12345
MyClass 类的方法 f 输出为： hello world
```

类有一个名为 \_\_init\_\_() 的特殊方法（**构造方法**）

**init**() 方法可以有参数，参数通过 **init**() 传递到类的实例化操作上。例如:

```
class Complex:
    def __init__(self, realpart, imagpart):
        self.r = realpart
        self.i = imagpart
x = Complex(3.0, -4.5)
print(x.r, x.i)   # 输出结果：3.0 -4.5
```

#### self代表类的实例，而非类

类的方法与普通的函数只有一个特别的区别——它们必须有一个额外的**第一个参数名称**, 按照惯例它的名称是 **self**

### 类的方法

在类的内部，使用 def 关键字来定义一个方法，与一般函数定义不同，类方法必须包含参数 self, 且为第一个参数，self 代表的是类的实例。

```
#类定义
class people:
    #定义基本属性
    name = ''
    age = 0
    #定义私有属性,私有属性在类外部无法直接进行访问(private filed)
    __weight = 0
    #定义构造方法
    def __init__(self,n,a,w):
        self.name = n
        self.age = a
        self.__weight = w
    def speak(self):
        print("%s 说: 我 %d 岁。" %(self.name,self.age))
 
# 实例化类
p = people('runoob',10,30)
p.speak()
```

执行以上程序输出结果为：

```
runoob 说: 我 10 岁。
```

**\_\_private\_attrs**：两个下划线开头，声明该属性为私有，不能在类的外部被使用或直接访问

### 类的专有方法：

* **\_\_init\_\_ :** 构造函数，在生成对象时调用
* **\_\_del\_\_ :** 析构函数，释放对象时使用
* **\_\_repr\_\_ :** 打印，转换
* **\_\_setitem\_\_ :** 按照索引赋值
* **\_\_getitem\_\_:** 按照索引获取值
* **\_\_len\_\_:** 获得长度
* **\_\_cmp\_\_:** 比较运算
* **\_\_call\_\_:** 函数调用
* **\_\_add\_\_:** 加运算
* **\_\_sub\_\_:** 减运算
* **\_\_mul\_\_:** 乘运算
* **\_\_truediv\_\_:** 除运算
* **\_\_mod\_\_:** 求余运算
* **\_\_pow\_\_:** 乘方
