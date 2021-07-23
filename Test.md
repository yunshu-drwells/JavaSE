<font size = 4 face = "黑体">

### 选择题

##### 以下（   C ）不是Java的特点。（选择一项）  

A.平台无关性

B.高可靠性和安全性

C.指针运算

D.分布式应用和多线程


**java为了安全,中并没有引入C语言的指针概念.**




</br></br></br></br></br></br>


##### 	以下选项中关于Java跨平台原理的说法正确的是（  AC  ）。（选择二项）

A	Java源程序要先编译成与平台无关的字节码文件(.class)，然后字节码文件再被解释成机器码运行

B.	Java语言只需要编译，不需要进行解释

C.	Java虚拟机是运行Java字节码文件的虚拟计算机。不同平台的虚拟机是不同的

D.	Java语言具有一次编译，到处运行的特点，可以在所有的平台上运行

**B:Java先通过javac编译,再通过java解释器进行解释运行.**






</br></br></br></br></br></br>

##### 以下选项中是对一个Java源文件进行正确编译的语句是（  D  ）（选择一项）

A.	java Test 

B.	java Test.class 

C.	javac Test

D.	javac Test.java




编译命令是javac.且编译需要加.java文件后缀,解释时才不需要,且解释时不能加目录运行





</br></br></br></br></br></br>

##### 在Java中，源文件Test.java中包含如下代码，则程序编译运行的结果是（  B  ）。（选择一项）

public class Test {
    public static void main(String[ ] args) {
        system.out.println("Hello!");
    }
}
A	输出：Hello！

B.	编译出错，提示“无法解析system”

C.	运行正常，但没有输出任何内容

D.	运行时出现异常

**解析:java是区分大小写的,System和system是不同的,输出命令是System.out.println();**



</br></br></br></br></br></br>

##### 有一段Java 程序，其中public类名是A1，那么保存它的源文件名可以是（  A   ）。（选择一项）

A	A1.java

B.	A1.class

C.	A1

D.	都不对

**保存时必须有后缀.java,若有public类只能与public类的类名相同..class后缀是编译后的字节码的.**






</br></br></br></br></br></br>

##### 以下Java运算符中优先级别最低的两个选项是（  AB  ）。（选择二项）


A赋值运算符=

B.条件运算符 ?=

C.逻辑运算符|

D.算术运算符+
![java运算符的优先级](https://img-blog.csdnimg.cn/20200117142704590.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQzODA4NzAw,size_16,color_FFFFFF,t_70)

> = 必然是最低的,所有运算结束才赋值
> ?= 就是 += -= *= /= %= 这些,如上图


</br></br></br></br></br></br>

##### 下面（  AB  ）语句能正确通过编译

```java
A.System.out.println(1+1);

B.char i =2+'2';

System.out.println(i);

//C.String s="on"+'one';  //error

//D.int b=255.0;  //error
```


</br></br></br></br></br></br>

##### 以下语句中关于Java构造方法的说法错误的是(  D )。(选择一项)

　　A.构造方法的作用是为创建对象进行初始化工作，比如给成员变量赋值

　　B.一个Java类可以没有构造方法，也可以提供1个或多个构造方法

　　C.构造方法与类同名，不能书写返回值类型

　　D.构造方法的第一条语句如果是super()，则可以省略，该语句作用是调用父类无参数的构造方法
　　
> super()能调动所有构造方法包括有参的
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200120170103597.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQzODA4NzAw,size_16,color_FFFFFF,t_70)


</br></br></br></br></br></br>

##### 在Java中，以下程序编译运行后的输出结果为(  D )。(选择一项)

```java
public class Test {
    int x, y;
    Test(int x, int y) {
        this.x = x;
        this.y = y;
    }
    public static void main(String[] args) {
        Test pt1, pt2;
        pt1 = new Test(3, 3);
        pt2 = new Test(4, 4);
        System.out.print(pt1.x + pt2.x);
    }
}
```

　　A.6

　　B.34

　　C.8

　　D.7
　　
　　
　　
　　
</br></br></br></br></br></br>

##### 在Java中关于静态方法，以下说法中正确的是( AC )。(选择二项)

　　A.静态方法中不能直接调用非静态方法

　　B.非静态方法中不能直接调用静态方法

　　C.静态方法可以用类名直接调用

　　D.静态方法里可以使用this
　　
　　
　　
　　
</br></br></br></br></br></br>

##### 下列选项中关于Java中类方法的说法错误的是( B )。(选择二项)

　　A.在类方法中可用this来调用本类的类方法

　　B.在类方法中调用本类的类方法时可直接调用

　　C.在类方法中只能调用本类中的类方法

　　D.在类方法中调用实例方法需要先创建对象
　　
> B  1.非静态方法必须采用对象.方法名来调用，不能直接调用</br>
> CD 2.java类如果存在继承，子类可以访问父类非私有方法，不仅仅是本类方法


实例（非静态）方法：
实例方法属于对象，通过 实例对象.方法名(参数)调用。
实例方法可以直接访问静态成员。
实例方法中可以使用对象专属this、super关键字指向调用对象本身、父类。
　　
　　
</br></br></br></br></br></br>

##### 分析如下Java程序的代码所示，则编译运行后的输出结果是( C )。(选择一项)

```java
public class Test {
    int count=9;
    public void count1(){
        count=10;
        System.out.print("count1="+count);
    }
    public void count2(){
        System.out.print("count2="+count);
    }
    public static void main(String[ ] args) {
        Test t=new Test();
        t.count1();
        t.count2();
    }
}
```

     A.count1=9; count2=9;

     B.count1=10;count2=9;

     C.count1=10; count2=10;

     D.count1=9; count2=10;
     
     
     
     
     
     







</br></br></br></br></br></br></br></br></br>

### 简答题

</br></br></br>
##### 1.计算机语言发展史中的主线。

第一代是机器语言，第二代是汇编语言，第三代是高级语言

机器语言由数字组成所有指令。

为了编程的方便，以及解决更加复杂的问题。程序员开始改进机器语言，使用英文缩写的助记符来表示基本的计算机操作。这些助记符构成了汇编语言的基础。

高级语言允许程序员使用接近日常英语的指令来编写程序。


</br></br></br>
##### 2.Java的跨平台的实现原理。

通过虚拟机 JVM(Java Virtual Machine)就是一个虚拟的用于执行bytecode字节码的”虚拟计算机”。来实现跨平。
不同的操作系统有不同的虚拟机。Java 虚拟机机制屏蔽了底层运行平台的差别，实现了“一次编译，随处运行”。




</br></br></br>
##### 3.JDK、JRE、JVM 的区别和联系。

JDk 是Java Development Kit的缩写,集成开发环境的意思,包含JRE

JRE 是Java Runtim-enviroment,是Java开发环境包含JVM,库函数和运行java程序所必须的文件

JVM 是Java Virtual Machine,虚拟机的意思

图示:
<img src = "https://img-blog.csdnimg.cn/20200119121838491.png" />


</br></br></br>
##### 4.Java程序的开发和执行过程。

Java首先利用文本编辑器编写 Java源程序，源文件的后缀名为.java；再利用编译器（javac）将源程序编译成字节码文件，字节码文件的后缀名为.class； 最后利用虚拟机（解释器，java）解释执行。


</br></br></br>
##### 5.环境变量Path的作用和配置。

环境变量是在操作系统中一个具有特定名字的对象，它包含了一个或者多个应用程序所将使用到的信息。

Path是一个常见的环境变量，它告诉操作系统，当要求系统运行一个程序而没有告诉它程序所在的完整路径时，系统除了在当前目录下寻找此程序外，还应到哪些目录下寻找。



</br></br></br>
##### 1.Java是一种强类型语言，说明Java的数据类型分类。
![Java数据类型的分类](https://img-blog.csdnimg.cn/20200116141443133.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQzODA4NzAw,size_16,color_FFFFFF,t_70)


</br></br></br>
##### 2.i++ 和 ++i的异同之处
1、i++ 返回原来的值,++i 返回加1后的值。
2、i++ 不能作为左值,而++i可以。
3、i++前者是先赋值,然后再自增;++i后者是先自增,后赋值。

</br></br></br>
##### 3.运算符||和|的异同之处
|是逻辑或运算符,两个操作数有一个是true，结果就是true,如果两个操作数是数字,是两个数据按二进制展开后每位进行或运算,结果是一个数
||是短路或运算符,只要有一个为true， 则直接返回true

</br></br></br>
##### 4.Java中基本数据类型转换的规则
![Java自动类型转换](https://img-blog.csdnimg.cn/20200117145316991.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQzODA4NzAw,size_16,color_FFFFFF,t_70)

> 红色实线是没有精度损失的转换,蓝虚线是有精度损失的



</br></br></br>
##### 1. 面向过程和面向对象的区别。

面向过程适合简单任务，按照一定的步骤实现事务，而面向对象可以封装数据和功能，将大的问题分解成一个个小块，适合复杂的系统任务，但是底层还是使用的面向过程思想。



</br></br></br>
##### 2. 类和对象的关系

类是对对象的抽象，对象是类的实体。



</br></br></br>
##### 3. 构造方法的作用和特征

构造方法用于对象的初始化，也叫构造器，构造器是一个创建对象时被自动调用的特殊方法，目的是对象的初始化。

特征:
构造器的名称应与类的名称一致。
没有返回类型
不能有返回值





</br></br></br>
##### 4. this关键字的作用和用法

this是创建好的对象的地址，代表当前对象，因此在构造方法中也可以使用

this的用法如下：
1. 当程序中产生二义性的时候，使用this来指明当前对象，普通方法中，this指向调用该方法的对象，在构造函数中，this指向正要初始化的对象。
2. 在构造函数中this调用重载的构造函数，并且只能在构造函数中，并且只能在第一句。
3. this不能用于static方法中。





</br></br></br>
##### 5. 简述static关键字的作用。

　　提示：从static可以修饰变量，方法，代码块，三个方面来回答。

修饰变量：static声明的变量为静态成员变量，为类变量，生命周期和类相同。被static修饰的成员变量被类的所有对象所共享，其只有一份，省去内存空间。

修饰成员函数：叫做静态方法,从而属于类,可以使用"类名.方法名"的方式操作方法，避免了先要new出对象的繁琐和资源消耗。

修饰代码块：
静态初始化块，用于类的初始化操作!上溯到Object类，先执行Object的静态初始化块，再向下执行子类的静态初始化块，直到当前类的静态初始化块为止。













</br></br></br></br></br></br></br></br></br>

### 编码题

</br></br></br>
##### 1.输入圆形半径，求圆形的周长和圆形的面积，并将结果输出。

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200119125720930.png)


```java
import java.util.Scanner;

public class 圆周长和面积 {
	public static void main(String[] args) {
		//输入圆形半径，求圆形的周长和圆形的面积，并将结果输出
		Scanner scan = new Scanner(System.in);
		System.out.println("请输入圆的半径");
		double R = scan.nextFloat();
		System.out.printf("该圆的周长是:%.3f%n", 2*Math.PI*R);
		System.out.printf("该圆的面积是:%.3f%n", Math.PI* Math.pow(R, 2));
	}
	
}
```


</br></br></br>
##### 2.银行利率表如下表所示，请计算存款10000元，活期1年、活期2年，定期1年，定期2年后的本息合计。

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200119125731392.png)

结果如下图所示（结果四舍五入，不保留小数位。使用Math.round(double d)实现）。

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200119125738665.png)











</br></br></br>
##### 3.某个公司采用公用电话传递数据，数据是四位的整数，在传递过程中是加密的，加密规则如下：每位数字都加上5,然后用和除以10的余数代替该数字，再将第一位和第四位交换，第二位和第三位交换。结果如图所示。

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200119125743328.png)












</font>