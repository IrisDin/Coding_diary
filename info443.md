# info443

Abstraction：

Abstraction is the process of generalization. It lets us work with higher-level representations rather than low-level details.



&#x20;We can evaluate "separation" in terms of cohesion and coupling.

cohesion：

"The degree to which parts of an element are related and belong together."



coupling：

"The degree to which software elements are inter-connected (and inter-dependent)." a.k.a., the degree to which software elements are not self-contained.



Orthogonality：

If two things are orthogonal, a change to one won't change the other Orthogonality 26We want software elements to be orthogonal!



Encapsulation

Encapsulation is the process of compartmentalizing the elements of an abstraction. It hides the details in the abstraction.





## Key Design Concepts

\
**Minimal complexity**. The primary goal of design should be to minimize complexity for all the reasons just described. Avoid making "clever" designs. Clever designs are usually hard to understand. Instead make "simple" and "easy-to-understand" designs. If your design doesn't let you safely ignore most other parts of the program when you're immersed in one specific part, the design isn't doing its job.

**Ease of maintenance**. Ease of maintenance means designing for the maintenance programmer. Continually imagine the questions a maintenance programmer would ask about the code you're writing. Think of the maintenance programmer as your audience, and then design the system to be self-explanatory.

**Loose coupling**. Loose coupling means designing so that you hold connections among different parts of a program to a minimum. Use the principles of good abstractions in class interfaces, encapsulation, and information hiding to design classes with as few interconnections as possible. Minimal connectedness minimizes work during integration, testing, and maintenance.

**Extensibility**. Extensibility means that you can enhance a system without causing violence to the underlying structure. You can change a piece of a system without affecting other pieces. The most likely changes cause the system the least trauma.

**Reusability**. Reusability means designing the system so that you can reuse pieces of it in other systems.

**High fan-in**. High fan-in refers to having a high number of classes that use a given class. High fan-in implies that a system has been designed to make good use of utility classes at the lower levels in the system.

**Low-to-medium fan-out**. Low-to-medium fan-out means having a given class use a low-to-medium number of other classes. High fan-out (more than about seven) indicates that a class uses a large number of other classes and may therefore be overly complex. Researchers have found that the principle of low fan-out is beneficial whether you're considering the number of routines called from within a routine or the number of classes used within a class (Card and Glass 1990; Basili, Briand, and Melo 1996).

**Portability**. Portability means designing the system so that you can easily move it to another environment.

**Leanness**. Leanness means designing the system so that it has no extra parts (Wirth 1995, McConnell 1997). Voltaire said that a book is finished not when nothing more can be added but when nothing more can be taken away. In software, this is especially true because extra code has to be developed, reviewed, tested, and considered when the other code is modified. Future versions of the software must remain backward-compatible with the extra code. The fatal question is "It's easy, so what will we hurt by putting it in?"

**Stratification**. Stratification means trying to keep the levels of decomposition stratified so that you can view the system at any single level and get a consistent view. Design the system so that you can view it at one level without dipping into other levels.



## MVC 模式

MVC 模式代表 Model-View-Controller（模型-视图-控制器） 模式。这种模式用于应用程序的分层开发。

* Model（模型） - 模型代表一个存取数据的对象或 JAVA POJO。它也可以带有逻辑，在数据变化时更新控制器。
* View（视图） - 视图代表模型包含的数据的可视化。
* Controller（控制器） - 控制器作用于模型和视图上。它控制数据流向模型对象，并在数据变化时更新视图。它使视图与模型分离开。

我们将创建一个作为模型的 _Student_ 对象。_StudentView_ 是一个把学生详细信息输出到控制台的视图类，_StudentController_ 是负责存储数据到 _Student_ 对象中的控制器类，并相应地更新视图 _StudentView_。



![](<.gitbook/assets/截屏2023-05-05 下午4.38.42.png>)

### 步骤 1:创建模型。

```
// student.java
public class Student {
   private String rollNo;
   private String name;
   public String getRollNo() {
      return rollNo;
   }
   public void setRollNo(String rollNo) {
      this.rollNo = rollNo;
   }
   public String getName() {
      return name;
   }
   public void setName(String name) {
      this.name = name;
   }
}
```

```
// StudentView.java

public class StudentView {
   public void printStudentDetails(String studentName, String studentRollNo){
      System.out.println("Student: ");
      System.out.println("Name: " + studentName);
      System.out.println("Roll No: " + studentRollNo);
   }
}
```

```
// StudentController.java
public class StudentController {
   private Student model;
   private StudentView view;
 
   public StudentController(Student model, StudentView view){
      this.model = model;
      this.view = view;
   }
 
   public void setStudentName(String name){
      model.setName(name);    
   }
 
   public String getStudentName(){
      return model.getName();    
   }
 
   public void setStudentRollNo(String rollNo){
      model.setRollNo(rollNo);      
   }
 
   public String getStudentRollNo(){
      return model.getRollNo();     
   }
 
   public void updateView(){           
      view.printStudentDetails(model.getName(), model.getRollNo());
   }  
}
```

### 步骤 5

执行程序，输出结果：

```
Student: 
Name: Robert
Roll No: 10
Student: 
Name: John
Roll No: 10
```

Python 方式：

```
from abc import abstractmethod,ABCMeta
# 创建Student类，一个Model类
class Student():
    _rollNo = ""
    _name = ""
    def getRollNo(self):
        return self._rollNo
    def setRollNo(self,inRollNo):
        self._rollNo = inRollNo
    def getName(self):
        return self._name    
    def setName(self,inName):        
        self._name = inName
# 创建视图StudentView
class StudentView():
    def printStudentDetails(self,inStudentName,inStudentRollNo):
        print("Student :")        
        print("Name : {0}".format(inStudentName))        
        print("Roll No : {0}".format(inStudentRollNo))
# 创建控制器
class StudentController():    
    def __init__(self,inModel,inView):        
        self._model = inModel        
        self._view = inView    
    def setStudentName(self,inName):        
        self._model.setName(inName)    
    def setStudentRollNo(self,inRollNo):        
        self._model.setRollNo(inRollNo)    
    def getStudentRollNo(self):        
        return model.getRollNo()    
    def updateView(self):        
        self._view.printStudentDetails(self._model.getName(),self._model.getRollNo())
# 调用输出
if __name__ == '__main__':
    def retrieveStudentFromDatabase():
        student = Student()        
        student.setName("Robert")        
        student.setRollNo("10")        
        return student
    model = retrieveStudentFromDatabase()
    view = StudentView()    
    controller = StudentController(model,view)    
    controller.updateView()    
    # 更新模型数据    
    controller.setStudentName("John")    
    controller.updateView()
```



## Flux 架构 <a href="#page-title" id="page-title"></a>

首先，Flux将一个应用分成四个部分。

* **View**： 视图层
* **Action**（动作）：视图层发出的消息（比如mouseClick）
* **Dispatcher**（派发器）：用来接收Actions、执行回调函数
* **Store**（数据层）：用来存放应用的状态，一旦发生变动，就提醒Views要更新页面

![](<.gitbook/assets/截屏2023-05-05 下午4.18.45.png>)

**Flux 的最大特点，就是数据的"单向流动"**

1. 用户访问 View
2. View 发出用户的 Action
3. Dispatcher 收到 Action，要求 Store 进行相应的更新
4. Store 更新后，发出一个"change"事件
5. View 收到"change"事件后，更新页面

上面过程中，数据总是"单向流动"，任何相邻的部分都不会发生数据的"双向流动"。这保证了流程的清晰。



```javascript

// index.jsx
var React = require('react');
var ReactDOM = require('react-dom');
var MyButtonController = require('./components/MyButtonController');

ReactDOM.render(
  <MyButtonController/>,
  document.querySelector('#example')
);
```

采用的是 React 的 [controller view](http://blog.andrewray.me/the-reactjs-controller-view-pattern/) 模式。"controller view"组件只用来保存状态，然后将其转发给子组件

```javascript
// components/MyButtonController.jsx
var React = require('react');
var ButtonActions = require('../actions/ButtonActions');
var MyButton = require('./MyButton');

var MyButtonController = React.createClass({
  createNewItem: function (event) {
    ButtonActions.addNewItem('new item');
  },

  render: function() {
    return <MyButton
      onClick={this.createNewItem}
    />;
  }
});

module.exports = MyButtonController;
```

上面代码中，`MyButtonController`将参数传给子组件`MyButton`

```javascript
// components/MyButton.jsx
var React = require('react');

var MyButton = function(props) {
  return <div>
    <button onClick={props.onClick}>New Item</button>
  </div>;
};

module.exports = MyButton;
```

[`MyButton`](https://github.com/ruanyf/extremely-simple-flux-demo/blob/master/components/MyButton.jsx)是一个纯组件（即不含有任何状态），从而方便了测试和复用。这就是"controll view"模式的最大优点。

`MyButton`只有一个逻辑，就是一旦用户点击，就调用[`this.createNewItem`](https://github.com/ruanyf/extremely-simple-flux-demo/blob/master/components/MyButtonController.jsx#L27) 方法，向Dispatcher发出一个Action。

> ```javascript
>
> // components/MyButtonController.jsx
>
>   // ...
>   createNewItem: function (event) {
>     ButtonActions.addNewItem('new item');
>   }
> ```

上面代码中，调用`createNewItem`方法，会触发名为`addNewItem`的Action。





