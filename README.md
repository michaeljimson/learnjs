- [learnjs](#learnjs)
- [What is the JavaScript?](#what-is-the-javascript)
- [JavaScript 语法](#javascript-语法)



# learnjs 
```
this is a JavaScript notebook
So let's get started.  
```


# What is the JavaScript?  
JavaScript是Netscape公司与Sun公司合作开发的使网页具有交互能力的程序设计语言。  
JavaScript是一种脚本语言，通常只能通过Web浏览器去完成一些操作而不能像普通意义上的程序那样独立运行。

# JavaScript 语法  
- 语句    
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

- 注释    
```
//这是一条注释
//这是另一条注释
/*  我也是个注释
    可以用我来注释
    多行  */
```

- 变量    
JavaScript允许程序员直接对变量赋值而无需事先声明，但提前声明变量是一种良好的编程习惯，如：
```
var mood;
var age;

var num1, num2;

var money = 100000;
var name = "michaeljimson";
```
在JavaScript中，变量名是区分大小写的，不允许变量名中包含空格或标点符号(`$`这个除外)，变量名允许包含字母、数字、`$` 和 `_`。
- 数据类型    
必须明确类型声明的语言成为*强类型（strongly typed）*语言，而JavaScript是一种*弱类型（weakly typed）*语言，因为它并不需要进行类型声明。JavaScript中有几种重要的数据类型，接下来让我们聊聊。 

  - 字符串     
字符串由零个或多个字符构成，字符包括（但不限于）*字母*、*数字*、*标点符号*和*空格*。字符串必须包在引号里，单引号双引号均可。

    ```
    var mood = 'happy';
    var mood = "happy";
    //这两句的含义相同

    var mood = "don't ask";
    var mood = 'don\'t ask';//这句将'进行了转义（escaping）
    ```
  - 数值   
如果想给一个变量赋一个数值，不用限定它必须是一个整数。Javascript允许使用小数点的数值，而且允许任意位小数，这样的数称之为浮点数：
    ```
    var age = 33.25;
    var temperature = -20;
    var temperature = -20.3333333333
    ```
  - 布尔值 
布尔数据只有两个可选值——**true**和**false**。  
`var sleeping = true;`     

- 数组
