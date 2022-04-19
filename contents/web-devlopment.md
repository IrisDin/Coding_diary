# 🕸 Web devlopment

crete a new branch

git checkout gh-pages

git merge main

git checkout main



\<em>emphasis\<em>

em{

font-style: normal;

text-decoration: underline;

}

```
// html style quick reference

    <!DOCTYPE html>
    <html lang="en">
       
       <head>
           <!-- metadata that gives the info about the author -->
           <meta charset="UTF-8">
           <meta name="author" content="Iris Ding">
           <title>Sherlock Holmes</title>
            <!-- link the css style -->
            <link rel="stylesheet" href="css/style.css">
       </head>
       
       <body>
           <!-- creating top-level heading -->
           <h1>Sherlock Holmes</h1>
            <!-- insert image -->
           <img src="img/sherlock.jpg" alt="the picture of detective sherlock Holmes"/>
           <p>
               Description of the character :
           </p>
               <p>
               <!-- insert hyperlink -->
               <!-- insert short paragraph with description -->
               <a href="https://www.britannica.com/topic/Sherlock-Holmes">Sherlock Holmes</a>
               is a character from the British author Sir Arthur Conan Doyl.
               Sherlock was ...
               </p>
           <p>The reason why I admire Sherlock Holmes:</p>
           <p>
           I am especially admired with his following characteristics:
           </p>
           <!-- create unordered list -->
           <ul>
               <li class="sherlock_personality">
                   Observant
               </li>
               <li>Intelligent</li>
               <li>Strong mind</li>
               <li>Loyal</li>
           </ul>
       </body>
    </html>
```

```
// css quick reference

body{
    font-size: 16px;
    font-family: 'Helvetica Neue',Helvetica, Arial,sans-serif;
}

/* change the style of paragraph */
p{
    line-height: 1.5;
}
/* change the style of the image */
img{
    max-height: 400px;
    border-radius: 10px;
}

/* use the class selector to change the specific style of a class */
.sherlock_personality {
    color:rgb(47, 92, 255);
}
```

**CSS Selector**

```
# group selctor
h2, .alert, # navbar{} 
# combined selector
p.alert{}
.alert.success
# descendant selector
h1(there is a space) .alert{find the alert but only the alert inside
the h1 class}
```

****

![](<../.gitbook/assets/截屏2022-04-07 上午8.27.12.png>)

标签🏷️



*   `<a>`标签—>他有一个必不可少的属性 href

    * `target`属性：
    * `_self`(在原来页面打开)
    * `_blank`（新窗口打开）
    * `_top`（打开时忽略所有的框架）
    * `_parent`（在父窗口中打开）



    *   `<input>`标签的掌握

        * 常用`type`类型：
          * `<input type="" name="" value="" />`
          * `type="text"` 单行文本输入框
          * `type="password"` 密码（`maxlength=""`）
          * `type="radio"` 单项选择（`checked="checked"`）
          * `type="checkbox"` 多项选择
          * `type="button"` 按钮
          * `type="submit"` 提交 `type="image"`图片提交
          * `type="file"` 上传文件
          * `type="reset"`重置
          * `type="hidden"` 隐藏



        `<label>`标签的使用

        * `<label></label>`
          * `label` 元素不会向用户呈现任何特殊效果。
          * 不过，它为鼠标用户改进了可用性。
          * 如果您在 `label` 元素内点击文本，就会触发此控件。
          * 就是说，当用户选择该标签时，浏览器就会自动将焦点转到和标签相关的表单控件上。
        * `<label>` 标签的`for` 属性应当与相关元素的 `id`属性相同。



**Font**

![](<../.gitbook/assets/截屏2022-04-10 下午9.40.59.png>)

**Box Model(盒子模型）**

![](<../.gitbook/assets/截屏2022-04-10 下午9.51.23.png>)

****

> CSS盒模型可以看作是一个盒子，用来装东西的容器，封装周围的HTML元素，它包括：边距，边框，填充，和实际内容。在网页中，每个盒子都有自己的位置，大小，还影响着其它盒子的位置和大小。

\
Margin(外边距) - 清除边框外的区域，外边距是透明的。&#x20;

Border(边框) - 围绕在内边距和内容外的边框。&#x20;

Padding(内边距) - 清除内容周围的区域，内边距是透明的。&#x20;

Content(内容) - 盒子的内容，显示文本和图



CSS breakpoint



## Javascript

print function =  console.log("Hello World")

#### JAVASCRIPT VARIABLES:

```
let x = 'hello'; //value is a String

x = 42; //value is now a Number


//create a variable (not assigned)
let hoursSlept; 
console.log(hoursSlept); //=> undefined
```

```
//Numbers (no difference between int and float)
const x = 4;   //'number'
const y = 1.5; //'number'


//Strings (single or double quotes, just be consistent)
const message = "Hello world";


//Booleans
const likesCode = true;


//Arrays - like lists in Python
const letters = ['a', 'b', 'c']; //literal syntax
const things = ['raindrops', 2.5, true, [3,4,3]]; //mix types
console.log(letters[0]); //'a'
console.log(letters[4]); //undefined
letters[5] = 'f'; //assigning out of bounds grows array
console.log(letters); //['a', 'b', 'c', , , 'f']
letters.push('z'); //arrays have methods as well
```

#### Nested arrays

```
// an array of different dinners available at a fancy party
// this list has 4 elements, each of which is a list of 3 elements
// the indentation is just for human readability

const dinnerOptions = [
    ['chicken', 'mashed potatoes', 'mixed veggies'],
    ['steak', 'seasoned potatoes', 'asparagus'],
    ['fish', "rice", 'green beans'],
    ['portobello steak', 'rice', 'green beans']
];

console.log(dinnerOptions.length); //4

const fishOption = dinnerOptions[2]; // ['fish', 'rice', 'green beans']

// fishOption is an array, so can reference its elements by index
console.log(fishOption[0]); //"fish"

// Access the 2th element's 0th element
console.log(dinnerOption[2][0]); //"fish"
```



```
'40' + 2 # The answer is 402 '' represent string
'40' - 4 # The answer is 36 (miuns will turn the string into numbers

const num = 10
const str = '10'

//comparisons: these will all be booleans (true/false)
num == str  #(the answer is true)
num === str #(the answer is false/ use triple equals to make comparison)
'' == 0 //empty String compare to 0 #(the answer is true)
```

#### Object

```
const ages = {'sarah':42, 'amit':35, 'zhang':13}

//can omit quotes on keys, but they are actually strings!
const englishToSpanish = {one:'uno', two:'dos'}
const numWords = {1:'one', 2:'two', 3:'three'}
const keys = Object.keys(numWords) //[ '1', '2', '3' ]

//mixed values
const typeExamples = {'int':12, 'str':'dog', 'list':[1,2]}
const empty = {}
```

#### Accessing Properties

```
const ages = {alice:40, bob:35, charles:13};

//access ("look up") values
console.log( ages['alice'] ); //=> 40
console.log( ages['bob'] ); //=> 35
console.log( ages['charles'] ); //=> 13

//keys not in the object have undefined values
console.log( ages['fred']); //=> undefined

//assign values
ages['alice'] = 41;
console.log( ages['alice'] ); //=> 41

ages['fred'] = 19; //adds the key and assigns value


```

```
const person = {
  firstName: 'Alice',
  lastName: 'Wong',
  age: 40,
  favorites: {
    music: 'jazz',
    food: 'pizza',
    numbers: [12, 42]
  }
};

const name = person['firstName']; //get value of 'firstName' key
person['lastName'] = 'Jones'; //set value of 'lastName' key
console.log(person['firstName']+' '+person['lastName']); //"Alice Jones"


const favFood = person['favorites'][inputtedValue]; //object in the object
                //object           //value

const firstNumber = person['favorites']['numbers'][0]; //12
person['favorites']['numbers'].push(7); //push 7 onto the Array
```

#### DataTable

```
//Arbitrary list of people's names, heights, and weights
const people = [
    {name: 'Ada', height: 64, weight: 135},
    {name: 'Bob', height: 74, weight: 156},
    {name: 'Chris', height: 69, weight: 139},
    {name: 'Diya', height: 69, weight: 144},
    {name: 'Emma', height: 71, weight: 152}
]
```

#### Conditions:

```
if(outside_temperature < 60) {
  console.log("Wear a jacket");
}
else if(outside_temperature > 90) {
  console.log("Wear sunscreen");
}
else if(outside_temperature == 72) {
  console.log("Perfect weather!");
}
else {
  console.log("Wear a t-shirt");
}
```

#### For loops:

```
const myArray = [1, 2, 3, 4];
for(const theItem of myArray) { //loop array items
  console.log(theItem)
}


const myObject = {a: 1, b: 2, c: 3};
for(const theKey in myObject) { //loop object keys
  console.log(theKey, ":", myObject[theKey])
}

//explicit key looping
const keys = Object.keys(myObject);
for(const theKey of keys) { /*...* /}
```

#### Functions:

```
//Java
public static String greet(String greeting, String name){
    return greeting  + ", " + name;
}

public static void main(String[] args){
    String msg = greet("Hello", "World");
}


# Python
def greet(greeting, name):
    return greeting  + ", " + name


msg = greet("Hello", "World")



//JavaScript
function greet(greeting, name){
    return greeting + ", " + name;
}
const msg = greet("Hello", "World");
```
