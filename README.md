# learnjs 
```
this is a JavaScript notebook
So let's get started.  
```


- [learnjs](#learnjs)
- [What is the JavaScript?](#what-is-the-javascript)
- [JavaScript 语法](#javascript-语法)
  - [语句](#语句)
  - [注释](#注释)
  - [变量](#变量)
  - [数据类型](#数据类型)
    - [字符串](#字符串)
    - [数值](#数值)
    - [布尔值](#布尔值)
  - [数组](#数组)
    - [关联数组](#关联数组)
  - [对象](#对象)
  - [操作](#操作)
    - [算术操作符](#算术操作符)
  - [条件语句](#条件语句)
    - [比较操作符](#比较操作符)
    - [逻辑操作符](#逻辑操作符)
  - [循环语句](#循环语句)
    - [while循环](#while循环)
    - [for循环](#for循环)
  - [函数](#函数)
  - [再探对象](#再探对象)
    - [内建对象](#内建对象)
    - [宿主对象](#宿主对象)
- [DOM](#dom)
  - [节点](#节点)
    - [元素节点](#元素节点)
    - [文本节点](#文本节点)
    - [属性节点](#属性节点)
    - [获取元素](#获取元素)
    - [获取和设置属性](#获取和设置属性)
 







# What is the JavaScript?  
JavaScript是Netscape公司与Sun公司合作开发的使网页具有交互能力的程序设计语言。  
JavaScript是一种脚本语言，通常只能通过Web浏览器去完成一些操作而不能像普通意义上的程序那样独立运行。
_______________________________________________
# JavaScript 语法  
## 语句    
JavaSrcipt语句只需要把不同的语句放在不同行上就可以分隔他们，例如:
  ```
  first statement
  second statement
  ```
如果想把多条语句放在同一行上，那么就要用`;`分隔他们。  
  ```
  first statement; second statement;
  ``` 
建议将每条语句的末尾都加上一个分号。
  ```
  first statement;
  second statement;
  ```

## 注释    
  ```
  //这是一条注释
  //这是另一条注释
  /*  我也是个注释
      可以用我来注释
      多行  */
  ```

## 变量    
JavaScript允许程序员直接对变量赋值而无需事先声明，但提前声明变量是一种良好的编程习惯，如：
  ```
  var mood;
  var age;

  var num1, num2;

  var money = 100000;
  var name = "michaeljimson";
  ```
在JavaScript中，变量名是区分大小写的，不允许变量名中包含空格或标点符号(`$`这个除外)，变量名允许包含字母、数字、`$` 和 `_`。
## 数据类型    
必须明确类型声明的语言成为*强类型*（strongly typed）语言，而JavaScript是一种 *弱类型*（weakly typed）语言，因为它并不需要进行类型声明。JavaScript中有几种重要的数据类型，接下来让我们聊聊。 

### 字符串     
字符串由零个或多个字符构成，字符包括（但不限于）*字母*、*数字*、*标点符号*和*空格*。字符串必须包在引号里，单引号双引号均可。

  ```
  var mood = 'happy';
  var mood = "happy";
  //这两句的含义相同

  var mood = "don't ask";
  var mood = 'don\'t ask';//这句将'进行了转义（escaping）
  ```
### 数值   
如果想给一个变量赋一个数值，不用限定它必须是一个整数。Javascript允许使用小数点的数值，而且允许任意位小数，这样的数称之为浮点数：
  ```
    var age = 33.25;
    var temperature = -20;
    var temperature = -20.3333333333
  ```
### 布尔值 
布尔数据只有两个可选值——**true**和**false**。  
`var sleeping = true;`     

## 数组     
数组是指用一个变量表示一个值的集合，集合中的每个值都是这个数组的元素。在JavaScript中，我们用`Array`关键字声明数组，如：     
  ```
  var beatles = Array(4);

  //可以不指定元素个数
  var beatles = Array();

  //填充元素 array[index] = element;
  beatles[0] = "John";
  beatles[1] = "Paul";
  beatles[2] = "George";
  beatles[3] = "Ringo";

  //或者以这种形式
  var beatles = Array("John", "Paul", "George", "Ringo");
  //再或者这样
  var beatles = ["John", "Paul", "George", "Ringo"];
  ```   
  数组的元素不必非得是一种数据结构，可以混搭，如：    
  ```
  var jimson = [ "michael", "24", "185"];
  ```    
  也可以将数组元素换成其他的数组，如：     
  ```
  var lennon = [ "John", 1940, false];
  var beatles = [];
  beatles[0] = lennon;
  ```    
### 关联数组   
  ```
  var lennon = Array();
  lennon["name"] = "John";
  lennon["year"] = 1940;
  lennon["living"] = false;
  ```  


## 对象     
与数组类似， 对象也是使用一个名字表示一组值。对象的每个值都是对象的一个属性，创建对象可以使用Object关键字，如：
  ```
  var lennon = Object();
  lennon.name = "John";
  lennon.year = 1940;
  lennon.living = false;
  ```
也可以用花括号语法：
  ```
  { propertyName:value, propertyName:value }

  var lennon = {name:"John", year:1940, living:false };

  var beatles = {};
  beatles.vocalist = lennon;
  //beatles.vocalist.name的值是"John"，beatles.vocalist.year的值是1940，beatles.vocalist.living的值是false。
  ```

## 操作   
### 算术操作符  
    
赋值操作符`=`，加法操作符`+`，减法操作符`-`， 乘法操作符`*`，除法操作符`/` 。   

  ```
  1 + 4
  1 + 4 * 5
  1 + (4 * 5)
  (1 + 4) * 5
  var total = (1 + 4) * 5;

  var temp_fahrenheit = 95;
  var celsius = (temp_fahrenheit - 32) / 1.8;

  year = year + 1;
  year++;
    
  //加法操作符不仅适用于数值，而且还适用于字符串拼接
  var message = "I am feeling " + "good"; 
    
  var mood = "古德古德";
  var message = "I am feeling " + mood;

  var year = 2021;
  var message = "The year is " + year;
  ```
## 条件语句    
  ```
  if (condition) {
      statement;
  }

  if (1 > 2) {
      alert("The world has gone mad!");
  } else {
      alert("All is well with the world");
  }
  ```
### 比较操作符
JavaScript提供了`>`，`<`，`>=`，`<=`，`==`，`!=`，`===`，`!==`等比较操作符。     
### 逻辑操作符  
JavaScript提供了逻辑与操作符`&&`，逻辑或操作符`||`，逻辑非操作符`!`。   
## 循环语句  
### while循环
while语句的结构为，
```
while (condition) {
  statements;
}


do {
  statements;
} while (condition);
//do while循环会提前执行一次statements
```
### for循环
for语句的结构为，
```
for(initial condition; test condition; alter condition) {
  statements;
}
```

## 函数
如果需要多次使用同一代码，可以把他们封装成一个函数。*函数*(function)就是一组允许在你的代码中随时调用的语句。每个函数实际上是一个短小的脚本。函数由下述结构定义：
```
function name(arguments) {
  statements;
}
```
如果在某个函数中使用了var，那个变量就将被视为一个局部变量，它只存在于这个函数的上下文中；繁殖，如果没使用var，那个变量就将被视为一个全局变量，如果脚本里已经存在一个与之同名的全局变量，这个函数就会改变那个全局变量的值。

## 再探对象  
对象是自包含的数据集合，包含在对象里的数据可以通过两种形式访问——*属性*（property）和*方法*（method）:    
- 属性是隶属于某个特定对象的变量；
- 方法是只有某个特定对象才能调用的函数。   
JavaScript中，属性和方法都是用“点”语法来访问：  
`Object.property`      
`Object.method()`   
实例是对象的具体个体，为给定对象创建一个新实例需要使用`new`关键字，如下所示：  
```
var jeremy = new Person;
```
### 内建对象  
数组就是一种内建对象，当我们使用new关键字去初始化一个数组的时候，实际上就是再创建一个Array对象的新实例:  
```
var beatles = new Array();
beatles.length;
```
### 宿主对象  
由浏览器提供的预定义对象被称为*宿主对象*(host object), 宿主对象包括From，Image和Element等。
   

__________________________________

# DOM
DOM的含义为面向文档模型，其中的D为document，O为object，M为model。   

## 节点   
DOM中有许多不同类型的节点，其中有三种基本的节点，分别为元素节点(element node)、文本节点(text node)和属性节点(attribute node)。

### 元素节点    
DOM的原子是元素节点，元素可以包含其他的元素，没有被包含在其他元素里的唯一元素是<html>元素，他是我们的节点树的根节点。    
### 文本节点   
在XHTML文档中，文本节点总是被包含在元素节点的内部，例如:
```
<p title="a gentle reminder">Don't forget to buy this stuff.</p>
```
但并非所有元素节点都包含有文本节点。
### 属性节点   
属性节点用来对元素做出更具体的描述，如：
```
<p title="a gentle reminder">Don't forget to buy this stuff.</p>
```   
在DOM中，`title="a gentle reminder"`是一个属性节点，属性节点总是被包含在元素节点中。并非所有的元素都包含着属性，但所有的属性都被元素包含。    

### 获取元素  
有三种DOM方法可以获取元素节点，分别是通过元素ID，通过标签名字和通过类名字来获取。    

- getElementById   
  DOM提供了一个名为getElementById的方法，这个方法将返回一个与那个有着给定id属性值的元素节点对应的对象。它是document对象特有的函数，在脚本代码中，函数名的后面必须跟有一对圆括号，这对圆括号包含着函数的参数。getElementById方法只有一个参数：你想获得的那个元素的id属性的值，这个id值必须放在单引号或双引号里。
  ```
  document.getElementById(id)

  document.getElementById("purchases")
  ```
- getElementsByTagName   
  getElementsByTagName方法返回一个对象数组，每个对象分别对应着文档里有着给定标签的一个元素，类似于getElementById，这个方法也是只有一个参数的函数，它的参数是标签的名字：   
  ```
  element.getElementsByTagName(tag)

  element.getElementsByTagName("li")

  alert(document.getElementsByTagName("li").length);
  
  var items = document.getElementsByTagName("li");
  for(var i=0;i < items.length; i++) {
    alert(typeof items[i]);
  }
  ```
- getElementsByClassName    
  getElementsByClassName可以让我们能够通过class属性中的类名来访问元素。
  ```
  getElementsByClassName(class)

  document.getElementsByClassName("sale")

  alert(document.getElementsByClassName("important sale").length);

  //适用于新老浏览器的搜索类名函数
  function getElementsByClassName(node, classname) {
    if (node.getElementsByClassName){
      //使用现有方法
      return node.getElementsByClassName(classname);
    } else {
      var results = new Array();
      var elems = node.getElementsByTagName("*");
      for(var i=0; i<elems.length; i++) {
        if (elems[i].className.indexOf(classname) != -1) {
          results[results.length] = elems[i];
        }
      }
      return results;
    }
  }
  ```
  
### 获取和设置属性
- getAttribute  
  getAttribute是一个函数，他只有一个参数——你打算查询的属性的名字：   
  ``object.getAttribute(attribute)``  
- setAttribute  
  setAttribute允许我们对属性节点的值作出修改。与getAttribute一样，setAttribute也只能用于元素节点：  
  ``object.setAttribute(attribute, value)``  
  


