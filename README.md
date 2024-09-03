[合集 \- Python(11\)](https://github.com)[1\.1 安装Python08\-28](https://github.com/GilbertDu/p/18384986)[2\.2 Python开发工具：PyCharm08\-28](https://github.com/GilbertDu/p/18384992)[3\.3 Python开发工具：VSCode\+插件08\-28](https://github.com/GilbertDu/p/18385035)[4\.4 Python虚拟环境介绍08\-28](https://github.com/GilbertDu/p/18385047)[5\.5 Python变量08\-28](https://github.com/GilbertDu/p/18385062)[6\.6 Python运算符和表达式08\-28](https://github.com/GilbertDu/p/18385065)[7\.7 Python流程控制08\-28](https://github.com/GilbertDu/p/18385075):[MeoMiao 萌喵加速](https://biqumo.org)[8\.8 Python基本数据结构08\-28](https://github.com/GilbertDu/p/18385079)[9\.9 Python函数08\-28](https://github.com/GilbertDu/p/18385082)10\.10 Python面向对象编程：类和对象以及和Java的对比09\-03[11\.11 Python面向对象编程：三大特性，封装、继承、多态09\-03](https://github.com/GilbertDu/p/18394032)收起

> 本篇是 Python 系列教程第 10 篇，更多内容敬请访问我的 Python 合集



> 这里只介绍类和对象，self、属性、方法、访问控制、类继承、方法重写在后面的文章里介绍


在Python中，类和对象是面向对象编程的基础。


## 1 类的概念


类是一种创建对象的蓝图或模板。它定义了一组属性（变量）和方法（函数），这些属性和方法描述了该类的对象应该具有哪些特征和行为。


## 2 定义一个类


在Python中，你可以使用`class`关键字来定义一个类。例如，定义一个名为`Person`的简单类：



```
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def display(self):
        print(f"Name: {self.name}, Age: {self.age}")

```

* `__init__`方法是一个特殊的方法，称为构造器，用于初始化类的新实例。
* `self`参数代表类的实例本身，并且是类任何方法的第一个参数。
* 类方法需要通过`self`来访问类属性。


## 3 创建对象


创建一个类的实例（即对象）非常简单。只需调用类名后跟一对括号即可：



```
person1 = Person("Alice", 25)
person2 = Person("Bob", 30)

```

## 4 访问属性和方法


可以通过点符号访问对象的属性和方法：



```
person1.display()  
# 输出: Name: Alice, Age: 25
print(f"Name: {person2.name}, Age: {person2.age}")  
# 输出: Name: Bob, Age: 30

```

Python 还有一个很牛逼的操作就是可以直接给对象赋值类里不存在的属性，比如我给 person2 的一个不存在的属性 gender 赋值：



```
person2.gender = "男"
print(getattr(person2,"gender"))
# 输出：男

```

## 5 和Java类的对比


### 5\.1 类和文件


在 Python 中，一个文件可以包含多个类。我们新建一个 example.py 文件，里面创建两个类，并在 main.py 文件中使用它们。


**example.py**



```
class MyClass1:
    def __init__(self, value):
        self.value = value
        
    def display(self):
        print("MyClass1 Value is:", self.value)

class MyClass2:
    def __init__(self, value):
        self.value = value
        
    def display(self):
        print("MyClass2 Value is:", self.value)

```

你可以在另一个文件中导入并使用这些类：


**main.py**



```
from example import MyClass1, MyClass2

# 创建MyClass1的实例
instance1 = MyClass1("AAA")
instance1.display()
# 输出：MyClass1 Value is: AAA

# 创建MyClass2的实例
instance2 = MyClass2("BBB")
instance2.display()
# 输出：MyClass2 Value is: BBB

```

Java 一个文件也可以有多个类，但只能有一个 public 的类，并且 public 的类名必须与文件名相一致。这是编译器的基本要求。虽然可以有非 public 的类，但是在外部无法使用，只能在本文件的类里使用。


### 5\.2 构造函数


Python 构造函数第一个参数是 self 代表类的实例本身，并且 self 是类任何方法的第一个参数。构造函数里用 self.xx \= xx 赋值过的参数就是类的属性，不用像 Java 一样先声明属性。


 \_\_EOF\_\_

   ![](https://github.com/GilbertDu)救苦救难韩天尊  - **本文链接：** [https://github.com/GilbertDu/p/18394028](https://github.com)
 - **关于博主：** 评论和私信会在第一时间回复。或者[直接私信](https://github.com)我。
 - **版权声明：** 本博客所有文章除特别声明外，均采用 [BY\-NC\-SA](https://github.com "BY-NC-SA") 许可协议。转载请注明出处！
 - **声援博主：** 如果您觉得文章对您有帮助，可以点击文章右下角**【[推荐](javascript:void(0);)】**一下。
     
