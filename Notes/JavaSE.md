JavaSE

#  基础语法

##  Java的编译运行过程

Java语言跨平台原理

跨平台原理

在需要运行Java应用程序的操作系统上，安装一个与操作系统对应的Java虚拟机（JVM Java Virtual Machine）。

JRE和JDK

JRE(Java Runtime Environment)

是Java程序的运行时环境，包含JVM和运行时所需要的核心类库。

JDK（Java Development Kit）

是Java程序开发工具包，包含JRE和开发人员使用的工具，其中的开发工具，编译工具（javac.exe）和运行工具（java.exe）。

JDK、JRE和JVM的关系

![image-20201228182344339](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20201228182344339.png)

JDK的下载和安装

JDK的下载

www.oracle.com

###  编译过程

在使用我们IDEA进行开发时，当保存时IDEA会自动调用Jdk目录下的/bin/javac.exe，会生成对应的.class文件

Out目录下存放的时我们编译后的.class字节码文件，（为何放在out目录下，规定）

​                               ![image-20210102221557670](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102221557670.png)

###  执行过程

l 先启动JAVA的虚拟机(JVM)

l JVM加载编译后的.class字节码文件

l 进行这个类的main()方法执行(入口函数，唯一的)

  、![image-20210102221605420](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102221605420.png)

## Junit

### 导入Junit支持

 ![image-20210102221614033](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102221614033.png)

### 运行单元测试

 ![image-20210102221623745](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102221623745.png)

### 单元测试的特点

l 单元测试类独立，只用于测试阶段

l @Test注解修饰的方法可以独立执行，双击方法 右键执行

l Junit包IDEA,Eclipse都支持，无需准备，直接导入

### 单元测试和main方法有什么区别

Main方法时程序的唯一入口，一个类只能由一个main函数，如果由多个独立方法需要执行，Main就显得无能为力

Junit可以支持运行多个方法

## 基础概念

### 关键字

```java
public class HelloWorld {
    //idea里  main方法的快捷键   psvm
    /*
    这是main方法
    main方法是程序的入口方法，代码的执行是main方法开始的
    */
    public static void main(String[] args) {
        //输出语句快捷键   sout 
        System.out.println("我不能呼吸");
    }
}

```

Java程序中最基本的组成单位是类。

上面变色的字，java中我们称为关键字

在java语言中已经被赋予特定意义的一些单词，关键字不能被用作标识符。

- 关键字的字母全部小写
- 常用的代码编辑器，针对关键字都有特殊的颜色 ，非常直观。

Java中的关键字由很多，对于初学者怎么记？不用去记，熟能生巧

 ![image-20210102221713508](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102221713508.png)

 

特殊的关键字：

-  别忘了java虽然没有强调是关键字，但也不能使用
- Test.java不能使用，否则无法使用Junit的Test
- strictfp 精确浮点
-  volatile 多线程并发

### 标识符号

关键字是Java定好的名字，这些名字我们不能使用，很多时候我们要自己起名字，那这个名字java把他们成为标识符

给类，方法，变量等起名字的符号
 包名，类名，方法名，属性，变量

标识符定义规则

- 标识符可以由字母，数字，下划线(_)，$组成

- 不能以数字开头

- 严格区分大小写

- 做到见名知意

- 不能是关键字

  

常见命名约定：

###### 小驼峰命名法： 方法 变量

标识符是一个单词的时候，首字母小写

标识符由多个单词组成的时候，第一个单词首字母小写，其他单词首字母大写

###### 大驼峰命名法：类

标识符是一个单词的时候，首字母大写

标识符有多个单词组成的时候，每个单词的首字母大写

### 注释

Jaba代码的解释说明，不影响程序的运行，用于辅助读程序

  // 单行注释

  /* 多行注释 */

  /** 文档注释，参数提示，作者信息等 */

### 变量

在JAVA中，由的数据值是不固定的，总在变，我们还需要记录这些值，我们可以把这些值理解为变量

格式： 变量的类型  变量名  = 变量值；

```java
String name = **"tony"**;
 **int** count;  *//**声明**Int**类型的变量，**int**默认值为**0
\* count =19;  *//**再次设置**count**的值*
```

注意：

- l 变量名必须是一个有效的标识符
- l 变量名不可以使用Java关键字
- l 变量名不能重复

>  基本数据类型：

byte，short，int ， long， float，double，char，boolean

> 变量使用的注意事项：
>
> - 名字不能重复
> - 变量未赋值，不能使用
> - long 类型的变量定义的时候，为了防止整数过大，后面要加L
> - float类型的变量定义的时候，为了防止类型不兼容，后面要加F



### 常量

常量可以理解为一种特殊的变量，

值被设定后，在程序的运行过程中不允许被改变

 ![image-20210102232757461](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102232757461.png)



格式： final 变量类型  变量名(大写) = 值；

```java
final double PI = 3.14;//定义圆周率统一使用
final String SYSTEM_NAME = "京东";
```



### 驼峰命名法

命名规则，变量首字母小这些，多个单词第二个之后首字母大写，java中成为驼峰规则

```java
String fileName = "tony.mp4";
 String toUpperCase = "HELLO";
```

 

切记：见名知意，作为一个合格的程序员java中各种起名，所有的命名都要尽量见名知与，不然会被同行耻笑

## 基本类型

### 概念

JAVA语言是一种强类型语言，第一，所以有的变量必须先声明，才能使用，第二，指定类型的变量只能接受和声明的类型匹配的值。强类型语言的好处就是在编译阶段就可以发现源代码的错误，从而保证程序更加健壮。但是也有缺点，有时程运行中难以确定其类型值，面对这种业务产经Java的强类型就有些死板，为了弥补后期会学习泛型

 ![image-20210102221936065](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102221936065.png)

### 八大基本数据类型

|            | **类型名称** | **字节空间** | **默认值** | **取值范围**                             |
| :--------- | ------------ | ------------ | ---------- | ---------------------------------------- |
| **整数型** | byte         | 1            | 0          | -27到27-1  或者  -128到127               |
|            | short        | 2            | 0          | -2^15到2^15-1                            |
|            | **int**      | **4**        | **0**      | **-2^31**到2^31-1 +-21亿多****           |
|            | **long**     | **8**        | **0L**     | **-2^63****到2^63-1**                    |
| **浮点型** | float        | 4            | 0.0f       | 单精度，对小数部分的精度要求不高         |
|            | **double**   | **8**        | **0.0d**   | **双精度，精确的小数部分并操作值很大时** |
| **字符型** | char         | 2            | 空格       | 0到65535                                 |
| **布尔型** | boolean      | 1            | false      | 真true 假false                           |

![image-20210102234900282](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102234900282.png)

注意：声明变量类型时，会给变量分配内存，按类型的所占空间数分配内存，那这里就应该讲究讲究，例如：年龄应该使用什么类型呢，最佳byte。性别？只有男女两个值，boolean

False代表女 true代表男

### 交换值

```java
int a=10;
int b=20;
// a=20  b=10
int t = a; //中间临时变量
a=b;
b=t;
System.out.println(a);
System.out.println(b);

```



## 类型转换

###   基本类型转换

 ![image-20210102222201230](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102222201230.png)

自动类型转换， 把一个表示数据范围小的数值或者变量赋值给另一个表示数据范围大的变量。

![image-20210103093737154](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103093737154.png)

boolean是非数值型的数值类型

强制类型转换，把一个表示数据范围大的数值或者变量赋值给另一个表示数据范围小的变量。  （与上面相反）(一般不建议使用 导致精度损失)

**格式**：目标数据类型 变量名 = （目标数据类型）值或变量

**范例**：int k = (int)88.88;



### 小到大(隐士转换)

```java
//隐士转换也就是自动转换
byte a = 120;
short b = 120;
int c = a; //直接转自动
```



### 大到小(显示转换)

```java
int c = 120;
//byte d = c; 报错 在编译时发现c的类型大于d的类型
byte d = (byte) c;
```

## 运算符

运算符：对常量或者变量进行操作的符号

表达式:用运算符把常量或者变量连接起来符合java语法的句子就可以成为表达式

​			不同运算符连接的表达式体现的是不同类型的表达式

### 常见的运算符

| **算术运算符** | + - * /        | 基本运算                                                     |
| -------------- | -------------- | ------------------------------------------------------------ |
|                | %              | 取余数，求模，算整除                                         |
|                | ++   --        | 自增  自减                                                   |
| **比较运算符** | ==             | 相等比较                                                     |
|                | ！=            | 不等比较                                                     |
| **连接运算符** | +              | 字符串连接 “abc”+”xyz”=”abcxyz”                              |
| **逻辑运算符** | &&    &        | 逻辑与(短路与)，两边同为真结果才为真                         |
|                | \|\|    \|     | 逻辑或(短路或)，两边只要有一个真结果就是真                   |
|                | ！             | 非，非真是假，非假是真                                       |
| **三元运算符** | c ? x : y      | 三项运算   c?x:y  c是真取返回x，是假返回y                    |
| **赋值运算符** | =              | 赋值运算                                                     |
|                | +=、-=、*=、/= | 复合的赋值运算  a+=2; 等价于 a=a+2 写法简洁                  |
| **优先执行**   | ( )小括号      | 小括号中的先执行  x+y+z = 按顺序相加x+y+z  x+(y+z)= 优先括号内的先执行y+z+x |



![image-20210103143302273](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103143302273.png)

字符串的“ + ” 操作： 拼接 字符串  注意优先级 从左到右结合

![image-20210103143838001](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103143838001.png)

![image-20210103144341086](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103144341086.png)



### ++ -- 运算

![image-20210103144814493](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103144814493.png)

```java
int i = 5;
//  i     6           7      6    6      5
// ()     6       6       6       6
int j = (++i) + (i++) + (--i) + (i--);
System.out.println(j); //24
System.out.println(i); //5
```

 

### 取余

取余操作很多地方都会使用，特别是在redis分布式缓存中，就是使用Hash一致性算法，而其核心算法就是取余

```java
int num = 10;
//任何一个数取余2 结果只有  0 和  1
if ( 10%2==0 ){
    //做一些操作
}else{
    //做一些操作
}
```

### 逻辑运算符

> // & 和的意思 全真为真 有假则假
> // | 或者的意思 全假为假 有真则真
>
> ![image-20210103145611047](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103145611047.png)
>
>    && || 具有**短路**的功能
>
> ![image-20210103150053190](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103150053190.png)

###  三元运算符(三目)

![image-20210103150225161](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103150225161.png)



```java
//两个数找最大值
int a =100;
int b = 20;
int max = a>b?a:b;

//三个数找最大值
a =100;
b =50;
int c =200;
// max ?
max = a>b?(a>c?a:c):(b>c?b:c);
System.out.println(max);
```

##### Scanner

Scanner使用的基本步骤

导包   import java.util.Scanner;(导包的动作必须出现在类定义的上边)

创建对象  Scanner sc = new Scanner(System.in);

​				上面这个格式里面， 只有sc 是变量名，可以变， 其他的都不允许变

接收数据

int i = sc.nextInt();

​	上面的这个格式里面， 只有i 是变量名， 可以变， 其他的都不允许变。

## 方法

### 通用方法

将加法变成方法，下次直接调用即可，比较方便，改变算法也容易的多

例如：改成乘法

   

方法的作用：封装一段特定的业务逻辑，复用性

```java
public static void main(String[] args) {
    int a = 77;
    int b = 88;
    int sum = sum(a,b);
    System.out.println(sum);
    sum1(a,b);
}
//方法与方法之间是并列的关系
//方法的定义：  修饰符  返回值类型 方法名(参数){}
public static int sum(int a,int b){
    //返回值类型不为空 必须有return
    return a+b; //return的作用就是结束方法，将值返回
}
// void 返回值类型为空
public static void sum1(int c,int d){
    System.out.println(c+d);
}

```

 

### 形参实参

 ![image-20210102222526845](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102222526845.png)

### 可变参数

上面是2个数字求和，3个怎么办，4个怎么办，n个怎么办

Jdk1.5之后开始支持可变参数，智能的解决这个问题

可变参数方式非常好，让程序更加灵活

参数个数不固定 可以连续三个点表示

```java
// ...表示个数不定灵活改变
public static  void sum2(int... values){
    //这个值是一个集合/数组
    int sum =0;
    for (int x : values){
        sum+=x;
    }
    System.out.println(sum);
}

```

 

## 良好的开发习惯

### 好的变成缩进风格

### 写注释

### 熟练使用快捷键

### 要怎么写代码

注意代码不是一句一句写出来的，而是先分析需求，分析完写开发步骤，把一个复杂的问题，差你分成很多小步骤，每个小步骤去解决一个问题吗，把每个小问题解决了，整个问题也就解决了

###   养成debug习惯

Debug快捷键：

F5 – 进入方法

F6 – 单步跳过，执行下一行

F7 – 返回方法，跳出当前方法

F8 – 跳到下一个断点

# 基础语法：异常/流程控制/分支/循环



## 流程控制

### 流程控制的三种基本结构

流程控制语句分类：

- l 顺序结构：代码一次从上往下执行

  程序中最简单最基本的流程控制， 没有特定的语法结构， 按照代码的先后顺序，依次执行。

  执行流程图![image-20210103153928946](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103153928946.png)

  

- l 分支结构：根据判断，有些代码执行，有些代码不执行（if， switch）

- l 循环结构：反复执行的一段代码、（for , while , do .. while）


## 分支结构

**if 语句**：格式1：

![image-20210103154031304](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103154031304.png)![image-20210103154236312](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103154236312.png)



格式2：

![image-20210103154337902](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103154337902.png)

格式3：

![image-20210103154542952](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103154542952.png)

![image-20210103154613912](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103154613912.png)

###  单分支

```java
//自定义异常
String   password  = "123123";
if (password.equals("123456")){
    System.out.println("登录成功");
}else {

    throw new PasswordError("密码错误");
}

```



### 多分支

```java
private static void degree(int score) {
    if (score>=90){
        System.out.println("优秀");
    }else if(score >=80){ //else if可以写多个
        System.out.println("良好");
    }else if(score >=70){
        System.out.println("中等");
    }else if(score >=60){
        System.out.println("差");
    }else if(score >=0){
        System.out.println("不及格");
    }else { //上述都没有满足 则走else
        System.out.println("非法数据");
    }
}

```



## 分支结构- switch

switch(expr1) expr1是一个整数表达式，整数表达式可以是Int基本类型或者是Integer包装类型，由于我们byte,short,char都可以隐士的转型为int，所以也支持，实际开发中常用String类型在jdk1.7以后也开始支持,还支持枚举类型

switch了解即可，基本可以通过if-else来替代

 ![image-20210103161048958](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103161048958.png)

![image-20210103161325656](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103161325656.png)



案例： 

```java
public static void main(String[] args) {
    //输入当前日期    求今年已经过了多少天 2月需要判断平润年  利用switch
    int year = 2020;
    int month = 6;
    int day = 17;
    int sum = 0;
    switch (month-1){
        case 12 : sum+=31;
        case 11 : sum+=30;
        case 10 : sum+=31;
        case 9  : sum+=30;
        case 8  : sum+=31;
        case 7  : sum+=31;
        case 6  : sum+=30;
        case 5  : sum+=31;
        case 4  : sum+=30;
        case 3  : sum+=31;
        case 2  :
            if (year%4==0&&year%100!=0 || year%400==0){
                sum+=29;
            }else {
                sum+=28;
            }
        case 1 : sum+=31;
    }
    System.out.println("今年过了"+(sum+day)+"天");
}

```

![image-20210103161932562](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103161932562.png)



## 循环结构 ：for

### 

重复做某件事情，具有明确的开始和停止标志

循环结构的组成：

- 初始化语句：用于表示循环开启时的起始状态，简单说就是循环开始的时候什么样
- 条件判断语句：用于表示循环反复执行的条件，简单说就是判断循环是否能一直执行下去
- 循环体语句：用于表示循环反复执行的内容，简单的就是循环反复执行的事情
- 条件控制语句：用于表示循环执行中每次变化的内容，简单说就是控制循环是否能执行下去

循环结构对应的语法：

- 初始化语句：这里可以是一条或者多条语句， 这些语句可以完成一些初始化操作

- 条件判断语句：这里使用一个结果值为boolean类型的表达式，这个表达式能决定是否执行循环体， 例如： a<3

- 循环体语句： 这里可以是 任意语句，这些语句将反复执行

- 条件控制语句：这里通常是使用一条语句来改变变量的值，从而达到控制循环是否继续向下执行的结果， 常见 i++， i-- 这样的操作

  ![image-20210103163735962](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103163735962.png)![image-20210103163927781](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103163927781.png)

  

循环结构是实际开发非常常见的用法，他是指在程序中反复执行某个弄能而设置的一种程序结构，它由循环体中的条件，判断继续执行某个功能还是退出循环、注意条件不能少写，否则会造成死循环

```java

//   循环的初始值
//   循环结束的条件
//   循环的变量
for(int i=0;i<10;i++){
    System.out.println("打印第"+i+"张");
}
 
```

![image-20210102223139229](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102223139229.png)

案例： 求和1-5  

​			求1-100偶数和 （循环体语句中if 判断）

​			水仙花数

​			统计水仙花数个数

​			循环嵌套 打印一个矩形 高5宽10 (*)

```java
for(int i=0;i<5;i++){//外层循环控制高度
  	 for (int j=0;j<10;j++){//内层循环控制宽度
     	 System.out.print("*");
   	 }
   	 System.out.println();
}

循环嵌套的过程中，习惯变量声明为： i j k m n
```

​				打印99乘法表

```java
//外层循环控制 高度  i=0 i<=9 i++
//内层循环
for(int i=1;i<=9;i++){
    for (int j=1;j<=i;j++){
        System.out.print(j+"*"+i+"="+(j*i)+"\t");
    }
    System.out.println();
}

```

## While循环

![image-20210103165056521](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103165056521.png)



```java
int i =0;// 初始化语句
while (i<10){ 
    System.out.println("打印第"+i+"张"); // 循环体语句
    i++;    // 条件控制语句
}

```

案例：

珠穆朗玛峰

```
int count = 0;
double  paper = 0.1;
int zf = 884430;
while(paper<=zf){
paper *=2;
count++;
}
System.out.println("需要折叠："+count+"次");
```

## do-while循环

![image-20210103170138566](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103170138566.png)![image-20210103170446765](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210103170446765.png)

```java
int i=0;   // 初始化语句
 do{
     System.out.println("打印第"+i+"张"); // 循环体语句
     i++;              // 条件控制语句
}while (i<10);   // 条件判断语句

```

###  for 循环while循环和do-while区别

- for循环和while 循环先判断条件是否成立，然后决定是否执行循环体（先判断后执行）

- do...while循环先执行一次循环体， 然后判断条件是否成立，是否继续执行循环体（先执行 后判断）

  for和while的区别：

  条件控制语句所控制的自增变量，因为归属for 循环的语法结构中， 在for循环结束后，就不能再次被访问到了

  条件控制语句所控制的自增变量，对于while循环来说不归属其语法结构中， 在while循环结束后， 该变量还可以继续使用

  for循环常用于固定次数的循环    while常用于制造死循环

  while有可能一次也不执行(先判断再执行)   do-while至少会执行一次(先执行再判断)

  

### 死循环

while 的死循环格式是最常用的  命令提示符窗口中Ctrl +C 可以结束死循环

``` java
for(;;){
System.out.println("zz");
}

while(true){
    System.out.println("zz");
}

do{
    System.out.println("zz");
}while(true)
```



##  阻断循环的几种方式

###  break

在循环中，基于条件控制， 种植循环体内容的执行， 也就是说结束当前的整个循环 

利用break语句退出循环

```java
int i=0;
while (true){
    i++;
    if(i==10){
        System.out.println("人数已满，结束");
        break;
    }
    System.out.println("抢座啦");
}

```



###  continue

在循环中， 基于条件控制， 跳过某次循环体内容的执行， 继续下一次的执行

```java
// 0 1  2 4 5 6 7 8 9
for (int i=0;i<10;i++){
     if(i==3) {
         continue;// 跳过本次循环执行下次循环
     }
    System.out.println(i);
}
```

### return

结束方法

```java
for (int i=0;i<10;i++){
     if(i==3) {
         return;
     }
    System.out.println(i);
}

 System.out.println("hahahh"); //这句话不会执行

```

## 循环嵌套

循环嵌套概述

- 顺序语句 以分号结尾，表示一句话的结束

- 分支语句 一对大括号表示if 的整体结构， 整体描述一个完整的if语句

  ​				一对大括号表示switch的整体结构， 整体描述一个完整的switch语句

- 循环语句 一对大括号表示for的整体结构，整体描述一个完整的for语句

  ​				一对大括号表示while的整体结构， 整体描述一个完整的while语句

  ​				do...while 以分号结尾，整体描述一个完整的do...while语句

1. 任何语句对外都可以看成是一句话，一句代码
2. 分支语句中包含分支语句称为分支嵌套
3. 循环语句中包含循环语句称为循环嵌套

```
for(int hour=0;hour<24;hour++){   // 外循环控制小时的范围， 
	for(int minute=0;minute<60;minute++){ // 内循环控制分钟的范围
	System.out.println(hour+"时"+"分");
	}
	System.out.println("-----")
}
```

##    Random

Random 的作用和使用步骤

作用： 用于产生一个随机数

使用步骤：

- 导包   import java.util.Random
- 创建对象   Random r = new Random();
- 获取随机数  int number = r.nextInt(10)// 获取数据的范围（0，10）包括0不包括10

案例：![image-20210104083257822](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210104083257822.png)

### 附 idea

- idea概述和安装

- idea中HelloWorld

  ![image-20210104084539873](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210104084539873.png)

- idea中项目结构

- idea中内容辅助键和快捷键

- idea中模块的操作

   多模块并存。
   
   

## **方法概述**

方法时将具有独立功能的代码块组织成为一个整体， 使其具有特殊功能的代码集

注意

- 方法必须先创建才可以使用， 该过程称为方法定义
- 方法创建后并不是直接运行的， 需要手动使用后才执行，该过程称为方法调用

### **方法定义**

```java
public static void 方法名(){
   // 方法体
}
```

### **方法调用过程**

**方法练习**：打印俩个数中的较大数 

![image-20210104115644156](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210104115644156.png)

注意：

- 方法定义时，参数中的数据类型与变量名都不能缺少， 缺少任意一个程序将报错
- 方法定义时，多个参数之间使用逗号分隔

![image-20210104115840750](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210104115840750.png)

注意：

- 方法调用时， 参数的数量与类型必须与方法定义中的设置相匹配， 否则程序将报错。



**形参**： **方法 定义** 中的参数， 等同于变量定义格式，

**实参**： **方法 调用 **中的参数， 等同于使用变量或常量。

实参传递可以是常量也可以是变量名

实参要匹配形参

> 带参数方法练习

需求： 设计一个方法用于打印俩个数中的较大数，数据来自于方法参数

**带返回值方法的定义和调用**

```java
public static datatype 方法名(parameter){
    return  data
}

case1:
public static boolean isEvenNumber(int number){
    return true;
}
case2:
 public static int getMax(int a, int b){
     return 100;
 }

```

注意：

方法定义时return 后面的返回值与方法定义上的数据类型要匹配， 否则程序将报错。

```java
方法名(参数);
isEvenNumber(5);

数据类型 变量名 = 方法名（参数）
boolean flag = isEvenNumber(5);
// 创建一个boolean 类型 变量falg接收 调用方法后的返回值
// 然后输出boolean 类型的变量flag 
```

注意：

- 方法的返回值通常会使用变量接受， 否则该返回值将无意义。

![image-20210107093830438](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107093830438.png)

**带返回值方法练习** 

需求：设计一个方法可以获取俩个数的较大值， 数据来自于参数。



方法的注意事项

- 方法不能嵌套定义

  ![image-20210107094946236](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107094946236.png)

- void 表示 无返回值可以省略return，也可以单独的书写return，后面不加数据。 会报错 无法到达的代码片段

![image-20210107095109059](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107095109059.png)

方法的通用格式

格式：

> ```java
> public static 返回值类型 方法名(参数){
>         方法体;
>         return 数据;
> }
> // public static  修饰符， 
> 返回值类型 方法操作完毕之后返回的数据的数据类型
>     		如果方法操作完毕， 没有数据返回， 这里写void， 而且方法体中一般不写return。
> 
> 方法名  调用方法时使用的标识。
> 参数  有数据类型和变量组成， 多个参数之间用逗号隔开。
> 方法体  完成功能的代码块
> return 如果方法操作完毕， 有数据返回， 用于把数据返回给调用者。
>     
> 定义方法时， 要做到 俩个明确，
>     明确返回值类型，  主要是明确方法操作完毕之后是否有数据返回， 如果没有， 写void ，如果有 写对应的数据类型 明确参数，  主要是明确参数的类型和数量。
>     
> 调用方法时
>      void 类型的方法， 直接调用即可
>      非void 类型的方法， 推荐用变量接收调用
>     
> ```

## 方法重载

### **方法重载概述**

指同一个类中定义的多个方法之间的关系， 满足下列条件的多个方法相互构成重载， 

- 多个方法在同一个类中， 
- 多个方法具有**相同的方法名**
- 多个方法的**参数不相同**， **类型不同** 或者**数量不同**

### **方法重载特点** 

- 重载仅对应方法的定义， 与方法的调用无关， 调用方式参照标准格式
- 重载仅针对同一个类中方法的名称与参数进行识别， 与返回值无关， 换句话 说不能通过返回值来判定俩个方法是否相互构成重载。

![image-20210107100933397](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107100933397.png)

方法重载练习

需求： 使用方法重载的思想， 设计比较俩个整数是否相同的方法， 兼容全整数类型（byte,short,int , long）

## 方法的参数传递

### 方法参数传递（基本类型）

![image-20210107102103079](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107102103079.png)

### 方法参数传递（引用类型）

![image-20210107102341308](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107102341308.png)

### 案例

需求 设计一个方法用于数组变量， 要求遍历的结果是在一行上的。

​	例如 [11，22，33，44，55]

![image-20210107102619936](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107102619936.png)

数组最大值

需求 设计一个方法用于获取数组中元素的最大值， 调用方法并输出结果

## Debug

程序调试工具， 它可以用于查看程序的执行流程， 也可以用于追踪程序执行过程来调试程序。

Debug 调试 又被称为 断点调试， 断点其实是一个标记 ， 告诉我们从哪里开始 查看。

- 加断点    左键
- 运行加断点程序   debug运行
- 看哪里    console
- 点哪里    f7
-  如何删除断点

Debug 使用

查看循环求偶数和的执行流程

查看方法调用的执行流程

### 案例

#### 减肥计划

![image-20210107104148737](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107104148737.png)

- if 语句实现
- switch语句实现

####   逢七过

![image-20210107104923400](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107104923400.png)

#### 不死神兔

![image-20210107105044378](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107105044378.png)

![image-20210107105214367](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107105214367.png)

![image-20210107105608980](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107105608980.png)

#### 百钱百鸡

![image-20210107105811782](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107105811782.png)

![image-20210107110113868](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107110113868.png)

#### 数组元素求和

![image-20210107110151977](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107110151977.png)

#### 数组内容相同

![image-20210107110405862](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107110405862.png)

#### 查找

![image-20210107110636304](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107110636304.png)

![image-20210107110749898](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107110749898.png)

![image-20210107110905104](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107110905104.png)

#### 反转

![image-20210107110920604](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107110920604.png)

![image-20210107111354836](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107111354836.png)

#### 评委打分

![image-20210107111420816](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107111420816.png)



#  面向对象

所谓的面向对象(OOP)，是一种编程思想，通过这种思想可以把生活中复杂的事情简单化，从原来的执行者变成了指挥者，面向对象是基于面向过程发展而来



## 面向过程和面向对象的区别

举例：把大象装冰箱

面向过程：打开冰箱->存储大象->关闭冰箱

面向对象：首先得有一个冰箱:供电，有门，冷冻，存储

​     还得有一个大象：大大的耳朵，短腿，长鼻子，会跑会叫

 

面向过程(opp)：强调的是过程(动作)主要关注“怎么做”。C语言

面向对象(oop)：强调的是对象(实体)主要关注“谁来做”。java语言

 

可见不同的编程思想，思考问题的角度不同。

 

举例：到超市购物，超市有500种商品，买了5样

面向过程思考:到超市购物，买了5样商品，回家放冰箱

面向对象思考:到超市购物，超市所有500种商品都要创建实体，买了5样，回家放冰箱

需求变更：再买点猪肉

面向过程：又要卖猪肉，修改代码，才能放冰箱

面向对象：猪肉实体已经有了，无需修改代码，直接把猪肉放冰箱即可

##  定义类

###  类

类是对象的统称，一类东西。

Java不仅提供了基本类型变量，数组，还提供了类，他可有实现自定义复杂结构，使我们的程序表现力更强，生活种的事物基本都可以用类来表达

类是引用类型，类的对象放在堆中

 ![image-20210107112926547](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107112926547.png)



一个类主要有三个部分组成：

l 构造方法：用来创建对象的   冰箱

l 成员变量：也就是我们的属性  用来表示对象的状态  冰箱开着还是管着，大象鼻子长不长

l 方法： 对象的行为 打开冰箱



类的重要性， 是java程序的基本组成单位。

类是对象是生活中一类具有共同属性和行为的事物的抽象，确定对象将会拥有的属性和行为。

类的组成 ：属性和行为

- 属性 在类中通过成员变量来体现（类中方法外的变量）
- 行为 在类中通过成员方法来体现（和前面的方法相比去掉static关键字即可）

类的特点：

- 类是对象的数据类型

- 类是具有相同属性和行为的一组对象的集合。

  类的定义：

![image-20210107113336626](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107113336626.png)

![image-20210107113344005](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107113344005.png)



对象的属性

**属性** 对象具有的各种特征， 每个对象的每个**属性**都拥有特定的**值**。

对象的行为

行为： 对象能够执行的操作。

### 对象的使用

![image-20210107113701387](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107113701387.png)



###  一文多类

Java支持一个java源文件种定义多个类，但是有点小要求

l 一个Java文件可以定义多个类，但是最多只能有一个类被public修饰

l 并且这个类名与文件名必须相同

l 若这个文件种没有public类，则文件名随便是其中一个类名即可

一个文件一个类和一个文件多个类，本质没有什么区别，唯一的区别就是管理不方便，每一个文件一个类是很好的开发习惯

##  类和对象

  案例 学生

![image-20210107114105552](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107114105552.png)



```java
class Person {
    private Integer id;
    private String name;


    public static void main(String[] args) {
        Person p1 = new Person();
    }

}

```

## 内存管理

栈：局部变量

堆：new出来的对象，成员变量

方法区：字节码文件，字符串常量池 静态常量池

-  单个对象

- 多个对象

- 多个对象指向相同    堆内存 内容相同。 即输出相同。

  

  ![image-20210102223655219](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102223655219.png)

   

###  成员变量和局部变量区别

成员变量 ：类中方法外的变量 （类的属性）

局部变量    方法体内部声明的变量

 ![image-20210107121332203](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107121332203.png)![image-20210107121112040](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107121112040.png)





## 构造方法

 构造方法是一种特殊的方法

作用：创建对象

格式：

```java
public class 类名{
		修饰符 类名(参数){
     }
}
```

功能： 主要是完成对象数据的初始化

![image-20210107163303207](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107163303207.png)

**构造方法的注意事项**

-  构造方法的创建

  如果没有定义构造方法系统将给出一个默认的无参数构造方法

  如果定义了构造方法，系统将不再提供默认的构造方法。

- 构造方法的重载

  如果定了带参构造方法， 还要是用无参数构造方法， 就必须再写一个无参数构造方法。 

 推荐的使用方式：无论是否使用， 都手工书写无参数构造方法。

​								

###  无参构造方法

//如果你不写构造方法，系统会默认提供一个无参的构造方法
 //修饰符 与类同名的方法名(){}

```java
 public Person(){

}
```

###   有参构造方法

```java
class Person {
    private Integer id;
    private String name;
    public Person(){

    }
    //有参构造，常用了初始化对象时，给属性赋值
    public Person(Integer id,String name){
        this.id=id;
        this.name=name;
    }

    public Person(Integer id) {
        this.id = id;
    }

    public Person(String usernmae) {
        name = usernmae;
    }

    public static void main(String[] args) {
        Person p1 = new Person("马化腾");
        System.out.println(p1.name);
    }

}

```

### 标准类的制作

- 成员变量 使用private修饰

- 构造方法  1.提供一个无参构造方法

  ​				  2.提供一个带多个参数的构造方法

- 成员方法  1.提供每一个成员变更量的对应的setXxx()/getXxx()

  ​                  2.提供一个显示对象信息的show()

- **创建对象并为其成员变量赋值的俩种方式**

    1.无参构造方法创建对象后使用setXxx()赋值

​		 2.使用带参构造方法直接创建带有属性值的对象		

![image-20210107210858164](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107210858164.png)



### 访问修饰符权限

![image-20210108172005169](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108172005169.png)

### 状态修饰符

#### final(最终态)

> final关键字是最终的意思， 可以修饰成员方法 变量 ，类。

**final 修饰的特点：**

- 修饰方法： 表明该方法时最终方法， 不能被重写
- 修饰变量： 表明该变量时常量， 不能再次被赋值
- 修饰类：表明该类时最终类， 不能被继承

**final 修饰局部变量**

-  变量是基本类型， final 修饰指的是基本类型的**数据值**不能发生改变
- 变量是引用类型， final 修饰指的是引用类型的**地址值**不能发生改变， 但是地址里面的内容是可以发生改变的。

#### static(静态)

> static 关键字是静态的意思， 可以修饰成员方法，成员变量

![image-20210108173251623](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108173251623.png)

![image-20210108173258789](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108173258789.png)

**static 修饰的特点** 

-  被类的所有对象共享  这也是我们判断是否使用静态关键字的条件
- 可以通过类名调用 当然也可以通过对象名调用

​      推荐使用类名调用

**static 访问特点**

非静态的成员方法

- 能访问静态的成员变量
-  能访问非静态的成员变量
- 能访问静态的成员方法
- 能访问非静态的成员方法

静态的成员方法

- 能访问静态的成员变量
- 能访问静态的成员方法

>  静态成员方法只能访问静态成员

**静态成员**

被static 关键字修饰的成员成为静态成员，又被成为类成员

被static修饰的成员不再属于对象成员，而提成为类成员，可以直接通过类名调用，有且只有一份，无需创建对象，类加载到内存时静态成员随之加载

 静态成员被所有对象共享

**静态方法只能调用静态成员变量**

因为静态方法加载(加载到方法区)时对象还没有创建，非静态成员属于对象，对象此时不存在则无法调用

 

###  初始化代码块

在Java类中除了成员属性和成员方法外，还可以直接在类中构建代码块

l 构造代码块

--- { }

--- 每次实例化对象都会执行

l 静态代码块

--- static{ }

--- 类加载到内存是执行一次

 

```java
{
    System.out.println("这是构造代码块");

}

static {
    System.out.println("这是静态代码块");

```



### 重写 @Override

![image-20210108164314000](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108164314000.png)

![image-20210108164757480](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108164757480.png)

**方法重写注意事项：**

![image-20210108165054732](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108165054732.png)

> 重写发生在父子类
>
> 重写父类里的方法
>
> 修饰符  返回值类型  方法名 参数都相同  方法体不同



###   重载

重载发生在同一个类

修饰符 方法名 都相同 参数列表 方法体不同 重载和返回值类型无关

 





## 面向对象的三大特征

面向对象编程有三大概念，封装，继承，多态

###   封装

#### **封装描述**

- 封装是对面向对象方法的重要原则，就是把对象的属性和操作结合成为一个独立的整理，并且尽可能隐藏对象的内部实现细节

- 是面向对象编程语言对客观世界的模拟， 客观世界里成员变量都是隐藏在对象内部的，外界是无法直接操作的。

#### **封装原则**

- 将类的某些信息隐藏在类内部， 不允许外部程序直接访问，二十通过该类提供的方法来实现对隐藏信息的操作和访问成员变量 private，提供对应的getXxxx()/setXxxx方法
- //封装是把过程和数据包围起来(数据私有化)，对数据的访问只能通过已定义的接口(行为公开化)。

#### **封装好处**

- 通过方法来控制成员变量的操作，提高了代码的安全性，

- 把代码用方法进行封装， 提高了代码的复用性。

- 特点

  l 减少代码的耦合

  l 对外隐藏细节，安全性好

  l 规定统一的入口，控制数据访问

```java
public class User {

    private Integer id;
    private String name;
    private Integer age;

    public Integer getId() {
        return id;
    }

    public void setId(Integer id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public Integer getAge() {
        return age;
    }

    public void setAge(Integer age) {
        this.age = age;
    }
}
 
```

#### private 关键字

-  是一个权限修饰符
-  可以修饰成员 成员变量和成员方法
-  作用是保护成员不被别的类使用， 被**private**修饰的成员只在本类中才能访问

针对 private修饰的成员变量，如果需要被其他类使用， 提供相应的操作 

- 提供 get变量名 方法 ， 用于获取成员变更量的值， 方法用public 修饰
- 提供set 变量名（参数）方法， 用于设置成员变量的值， 方法用public 修饰

private关键字的使用

 一个标准类的编写:

- 把成员变量用private修饰
- 提供对应的getXxx()/setXxxx()方法

####  this 关键字

this调用本类中的属性，也就是**本类中的成员变量**

 this可以调用其他方法![image-20210107144718179](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107144718179.png)

**this修饰的变量用于指代成员变量**

1. 方法的形参如果与成员变量同名， 不带this修饰的变量指的是形参， 而不是成员变量。

2. 方法的形参没有与成员变量同名， 不带this 修饰的变量指的是成员变量，

   ![image-20210107144928789](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107144928789.png)

```
this可以调用本类种的其他构造方法，调用时要放在构造方法的首行 this() 
```

  **什么时候使用this  解决局部变量隐藏成员变量**

**this 代表所在类的对象引用**

方法被那个对象 调用， this 就代表哪个对象 

> this 内存原理
>
> 



###   继承

继承是面向对象三大特征之一， 可以使得子类具有父类的属性和方法，还可以在子类中重新定义，追加属性和方法。

#### Object 顶级的父类

他是所有类的父类

它里面有常用的一些方法

toString()

equals()

hashCode()

 

#### **继承的格式:**

​	格式： public class 子类名 extends 父类名{}

  范例 ： public class Zi extends Fu{}

父类 也被称为基类、超类。

子类 也被称为派生类。

#### **继承中子类的特点：**

- 子类可以有父类的内容

- 子类还可以有自己特有的内容





继承使用extends关键字，声明一个父类，把子类共有的属性和方法提取到父类，可以提高代码的复用性





#### **继承的好处和弊端**

- 继承的好处

>  提高了代码的复用性 多个类相同的成员可以放到同一个类中
>
> 提高了代码的维护性（如果方法的代码需要修改， 修改一处即可）

- 继承的弊端

>  继承让类与类之间产生了关系， 类的耦合性增强了， 当父类发生变化时，子类实现也不得不跟着变化， 削弱了子类的独立性。

![image-20210108161227771](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108161227771.png)

#### **继承中变量的访问特点**

在子类方法中访问一个变量：

- 子类局部范围找

- 子类成员范围找
- 父类成员范围找
- 如果都没有就报错（不考虑父亲的父亲）

#### super关键字

super 关键字的用法和this关键字的用法相似

**this**： 代表本类对象的引用 this 关键字 指向调用该方法的对象， 一般我们实在当前类中使用this 关键字 所以我们常说this代表本类对象的引用

**super**： 代表父类存储空间的标识（可以理解为父类对象引用）

![image-20210108162426679](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108162426679.png)



```java
public Dog(){
    super();//super必须放在子类构造方法的第一行 作用用来调用父类的方法
    System.out.println("狗创建成功");
}

```

#### super内存图



####  继承中构造方法的访问特点

**子类中所有的构造方法默认都会访问父类中无参的构造方法。**

- 因为子类会继承父类中的数据， 可能还会使用父类的数据， 所以，子类初始化之前， 一定要先完成父类数据的初始化。
- 每一个子类构造方法的第一条语句默认都是：super()



如果父类中没有无参构造方法， 只有带参构造方法， 该怎么办？

- 通过super 关键字去显示的调用父类的带参构造方法
- 在父类中自己提供一个无参构造方法

> **推荐 自己给出无参构造方法**



#### 继承中成员方法的访问特点

![image-20210108163811534](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108163811534.png)



#### java中继承的注意事项

- 一个类只能继承一个父类,单继承  不支持多继承
- 继承具有传递性 支持多层继承

#### 案例

##### 老师和学生

![image-20210108170227991](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108170227991.png)

##### 猫和狗

![image-20210108170811015](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108170811015.png)

![image-20210108170843894](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108170843894.png)

###### 包

> 附 包
>
> ![image-20210108171504801](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108171504801.png)
>
> 导包的概述
>
> ![image-20210108171656645](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108171656645.png)

### 多态

#### 多态概述

同一个对象， 在不同时刻表现出来的不同形态

父类的引用指向子类的对象-向上转型

![image-20210108173944072](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108173944072.png)

> 举例：
>
> 一家饭店应该是  所有人都能进去吃不管他是美国人还是中国人还是其他人都可以，我们关注的是他只要是个人就可以，不关注这个人具体的类型
>
> 工地上我们拉土，我们关注的是拉土需要车就可以，不关注他具体是什么牌子，什么颜色的车
>
> Animal animal = **new** Dog();
>

 ![image-20210108174009181](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108174009181.png)

能出什么，看左边

如果子类重写了父类里面的方法，一定会走子类重写了的

####  多态中成员访问特点

![image-20210108174640108](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108174640108.png)

#### 多态的好处和弊端

![image-20210108175724721](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108175724721.png)

#### 多态中的转型

![image-20210108175803996](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108175803996.png)

![image-20210108180010893](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108180010893.png)

#### 多态转型的内存图

 ![image-20210108193028357](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108193028357.png)

![image-20210108193131852](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108193131852.png)

#### 案例 

##### 猫和狗

![image-20210108193308506](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108193308506.png)

![image-20210108193521453](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108193521453.png)



## 抽象类

#### 抽象类概述

> 在Java中， 一个没有方法提的方法应该定义为抽象方法，二类中如果有抽象方法， 该类必须定义为抽象类，

#### 抽象类的特点

![image-20210108195226890](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108195226890.png)好处：可以灵活的规定子类必须实现的行为，可以选择性实现的行为

```java
public abstract class Person {
    
    public abstract void eat();

    public void run(){

    }
}
```

#### 抽象类的成员特点

![image-20210108195830267](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108195830267.png)

![image-20210108195649817](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108195649817.png)

#### 案例

##### 猫和狗

![image-20210108200043948](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108200043948.png)



 



 

## 接口

#### 接口概述

接口就是一种公共的规范标准，只要符合规范标准， 大家都可以通用。

Java中的接口更多的体现在对行为的抽象

#### 接口的特点

 ![image-20210108202832700](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108202832700.png)

#### 接口的成员特点

![image-20210108203722902](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108203722902.png)

#### 案例

##### 猫和狗

![image-20210108203941999](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108203941999.png) 

![image-20210108204510915](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108204510915.png)



实现接口用implements，一个类可以实现多个接口，用逗号隔开

```java
public class SuperCar implements Car,fuel{

    @Override
    public void run() {
        System.out.println("时速180");
    }

    @Override
    public void fuelgd() {
        System.out.println("国Ⅵ");
    }
}

```

####  类与接口的关系

![image-20210108204718676](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108204718676.png)

#### 抽象类和接口的区别

![image-20210108205057771](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108205057771.png)

![image-20210108205111803](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108205111803.png)

![image-20210108205233595](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108205233595.png)

![image-20210108205307217](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108205307217.png)

#### 案例

##### 运动员和教练

![image-20210108205726059](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108205726059.png)

![image-20210108205836351](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108205836351.png)



##  面向对象总结，面试题

>  类和对象的区别
>

>  成员变量和局部变量
>
> 封装
>
>  this和super
>
>  static和final
>
> 静态变量和成员变量
>
>  重写和重载区别
>
>  抽象类和接口的区别

### 形参和返回值

#### 类名作为形参和返回值

![image-20210108211713657](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108211713657.png)

#### 抽象类名作为形参和返回值

![image-20210108212113947](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108212113947.png)

#### 接口名作为形参和返回值

![image-20210108212513337](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108212513337.png)



### 内部类

#### 内部类概述

内部类:就是在一个类中定义一个类 举例 ， 在一个类A的内部定义一个类B， 类B就被称为内部类。

![image-20210108212806753](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108212806753.png)

![image-20210108212945766](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108212945766.png)

#### 成员内部类

![image-20210108213227408](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108213227408.png)

![image-20210108213349182](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108213349182.png)

![image-20210108213420855](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108213420855.png)

#### 局部内部类

局部内部类是在方法中定义的类，所以外界是无法直接使用，需要在方法内部创建对象并使用 

该类可以直接访问外部类的成员，也可以访问方法内的局部变量

![image-20210108225839774](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108225839774.png)

![image-20210108225852156](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108225852156.png)

##### 匿名内部类

前提： 存在一个类或者接口 ， 这里的类可以是具体类也可以是抽象类。

![image-20210108230232907](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108230232907.png)

![image-20210108230448069](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108230448069.png)

![image-20210108230348904](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108230348904.png)

![image-20210108230746705](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108230746705.png)

![image-20210108230806719](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108230806719.png)

##### 匿名内部类在开发中的使用

![image-20210108230941398](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108230941398.png)

![image-20210108231321684](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108231321684.png)



#  数组

数组（array） 是一种用于存储多个相同类型数据的存储模型。

数组是同一种类型数据的集合，是一个数据容器，数组是引用类型的变量

数组可以自动为其中的元素从0开始编号，方便操作这些元素

***格式***：

- 数据类型[ ] 变量名 例： int[] arr  定义了一个int 类型的数组， 数组名是arr
- 数据类型 变量名[] 例 ： int arr [] 定义了一个int类型的变量， 变量名是arr数组

### 数组初始化之动态初始化

java中的数组必须先初始化， 然后才能使用

所谓初始化： 就是为数组中的数组元素分配内存空间，并未每个数组元素赋值。

数组初始化方式：

**动态初始化**： 初始化时只指定数组长度，由系统为数组分配初始值

格式 数据类型[] 变量名= new 数据类型[**数组长度**]   

范例

```java
 int[] arr = new int[3]     //arr 此时为内存空间地址值
 左边：int 说明数组中的元素类型是int类型
 [] :说明这是一个数组  
 arr 数组名称
 右边：new 为数组申请内存空间
 int 说明数组中的元素类型是int 类型
 [] 说明这是个一个数组
 3 数组长度 ， 其实就是数组中的元素个数
```

###  数组初始化之静态初始化

静态初始化：初始化时指定每个数组元素的初始值，由系统决定数组长度

格式：数据类型[] 变量名 = new 数据类型[ ] {数据1，数据2， 数据3，......};

范例

```java
int[] arr =new int[]{1,2,3};
// 简化格式:数据类型[] 变量名 = {数据1,数据2,数据3,....};
// 范例: 
int[] arr = {1,2,3};
```

**数组操作的俩个常见小问题：**

- 索引越界： 访问了数组中不存在的索引对应的元素，造成索引越界问题                                  ArrayIndexOutOfBoundsException

-  空指针异常：访问的数组已经不再指向堆内存的数据， 造成空指针异常                                    Null Pointer Exception

- null空值，引用数据类型的默认值，表示不指向任何有效对象。

  ![image-20210104100847204](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210104100847204.png)



### **数组元素访问**

数组变量访问方式  格式：数组名

数组内部保存的数据的访问方式  格式：数组名[索引]

**索引**是数组中数据的编号方式

作用：索引用于访问数组中的数据使用，数组名[索引] 等同于变量名，是一种特殊的变量名

特征 索引是从0开始的 是连续的 ，逐一增加， 每次加1

### **Java中内存分配**

java 程序在运行是， 需要在内存中分配空间， 为了提高运算效率，就对空间进行了不同区域的划分，因为每一片区域都有特定的处理数据方式和内存管理方式。

![image-20210104093519625](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210104093519625.png)

通过数组的地址逐步寻找

![image-20210104093620622](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210104093620622.png)

多个数组指向相同 任何一个数组修改堆内存数据 另一个所读也会改变 



### 遍历数组

![image-20210104101503337](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210104101503337.png)

**arr.length** **获取数组元素数量**

```java
int [] arr = {......};
for(int i=0;i<arr.length;i++){
    System.out.println(arr[i]);
}

```

### 求数组中的最大值/最小值

```java
//求出数组中的最大值
int max =0;  // 定义一个变量， 用  于保存最大值/最小值
for(int i=0;i<arr2.length;i++){ 
    // 与数组中数据逐个比对， 每次比对将最大值保存到变量中 
    if(max<arr2[i]){
        max=arr2[i];
    }
}
System.out.println("最大值为:"+max);

```



### 求数组中的平均值

```java
for (int i=0;i<arr2.length;i++){
    sum+=arr2[i];
}
double avg = sum/arr2.length;
System.out.println("平均数为："+avg
);

```

 

### 数组排序

```java
//数组排序 利用Arrays里提供的工具类
Arrays.sort(arr2);
System.out.println("排序后的数组："+Arrays.toString(arr2));
```



### 冒泡排序

```java
//冒泡排序
for(int i=0;i<arr2.length-1;i++){ //外轮循环控制 比较的轮数
    for(int j=0;j<arr2.length-1-i;j++){ //每轮比较的次数
        if(arr2[j]>arr2[j+1]){
            int t = arr2[j];
            arr2[j] = arr2[j+1];
            arr2[j+1] = t;
        }
    }
}
System.out.println("冒泡排序后的顺序：" +Arrays.toString(arr2));


```

![image-20210102224120155](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102224120155.png)

## 多维数组

在java中很容易的可以实现多维数组

一维数组中的元素都为普通元素(相同数据类型)

二维数组中的元素为一维数组

三维数组中的元素为二维数组

```java
int [][] arr = new int [3][5];      
int [][][] arr1 = new int [2][2][3];

```

多维数组遍历

```java
int [][] arr = {{1,3,5},{2,4,6}};
for(int i=0;i<arr.length;i++){
    for(int j=0;j<arr[i].length;j++){
        System.out.println(arr[i][j]);
    }
}

```

# API

API(Appliation Programming Interface): 应用程序编程接口

Java API ：指的就是JDK中提供的各种功能的Java类

​	这些类将底层的实现封装了起来， 我们不需要关心这些类是如何实现的，只需要学习这些类如何使用即可， 我们可以通过帮助文档来学习这些API如何使用

> 帮助文档				



API 使用练习

需求： 按照帮助文档的使用步骤学习Scanner类的使用， 并实现键盘录入一个字符串，最后输出在控制台。

> ### JDK

 ![image-20210102224218007](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102224218007.png)



## 常用API

### Math(java.lang)

![image-20210108231955362](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108231955362.png)

### System(java.lang)

System 包含几个有用的类字段和方法， 它不能被实例化

![image-20210108232630369](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108232630369.png)

![image-20210108233034313](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108233034313.png)





### Object (java.lang)

#### Object类概述

类Object是类层次结构的根，每个类都有Object作为超类， 所有类都直接或者间接的继承自该类 

构造方法 ： public Object()

回想面向对象中， 为什么说子类的构造方法 默认访问的是父类的无参构造方法

因为它们的顶级父类只有无参构造方法

所有对象包括数组都实现了这个类的方法



![image-20210108233720255](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108233720255.png)

#### Object类的常用方法

![image-20210108234842615](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108234842615.png)

##### toString

```java
public class Person {
    public static void main(String[] args) {
        Person person = new Person();
        System.out.println(person);
        System.out.println(person.toString());
    }
}
//输出结果：为对象的内存地址

//day04.Person@6d6f6e28
//day04.Person@6d6f6e28
```

```java
//源码
public String toString() {
    return getClass().getName() + "@" + Integer.toHexString(hashCode());
}

```

```java
//重写toString方法
@Override
public String toString() {
    return "Person{ 重写父类的toString方法 }";
}
```

```java
//hashCode
//如果两个对象相同，equals方法返回一定为true,并且这两个对象的hashCode值也一定相同
String s ="abc";
System.out.println(s.hashCode()); //1
String y = "abc";
System.out.println(y.hashCode()); //1
String h = "a"+"bc";
System.out.println(h.hashCode()); //1
String k = "ab";
String l = k+"c";
System.out.println(k.hashCode()); //2

```

#####  equals

![image-20210108234703673](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108234703673.png)

### String (java.lang)

> String 类代表字符串， Java程序中的所有字符串文字 都被时限为此类的实例。也就是说，Java程序中所有的双引号字符串， 都是String类的对象。
>
> String 类在Java.lang包下， 所以使用的时候不需要导包

![image-20210107213153407](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107213153407.png)

- 存储在字符串常量池中，相同的字符有且只有一份
- 在字面量直接比较时地址为同一份

- 在字面量直接拼接时地址为同一份

- 在有变量参与拼接时就会重新开辟一块内存地址


```java
String s = "abc";
System.out.println(s.hashCode());  //34567
String y = "abc";
System.out.println("s==y"+(s==y)); // true
System.out.println(y.hashCode()); // 34567
String h = "a"+"bc";
System.out.println(h.hashCode()); //34567
System.out.println("y==h:"+(y==h)); //true
String k = "ab";
String l = k+"c";
System.out.println(l.hashCode());  // 34567
System.out.println("l==y:"+(l==y));  //false

```

#### 通过帮助文档查看String 方法

![image-20210107222212504](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107222212504.png)

######  trim

截取字符串两边的空格

```java
String str = "   不用多久，我就会升职加薪，当上总经理，出任 CEO，迎娶白富美，醒醒  ";
System.out.println(str);
System.out.println(str.trim());
```



###### subString

截取 （0，3） 根据下标截取 下标从0开始 遵循含前不含后的原则

```java
String phone = "13345679876";  // 133-4567-9876
//              012345678910
String p1 = phone.substring(0,3); // 133
String p2 = phone.substring(3,7); // 4567
String p3 = phone.substring(7,11);// 9876
phone = p1+"-"+p2+"-"+p3;
System.out.println(phone);
```

######  转换大小写

```java
String str = "HelloWorld";
System.out.println("全大写"+str.toUpperCase());
System.out.println("全小写"+str.toLowerCase());
```

######  indexOf

查询字符串所在位置，返回下标

```java
String mail = "5742373426@163.com";
int index = mail.indexOf("@");
System.out.println(index);
//获取用户的QQ号
System.out.println("用户的账号为："+mail.substring(0,index));
//获取邮箱服务器域名
System.out.println("域名为:"+mail.substring(index+1));

```

 

###### lastIndexOf

获取字符串最后出现的位置，倒数位置

```java
String str = "HelloWorld";
System.out.println(str.lastIndexOf("o"));
//获取文件后缀
String file = "a.s.da.mp4";
System.out.println(file.substring(file.lastIndexOf(".")+1));

```



######  判断以什么开始，什么结束

startWith() 以什么开头

endWith() 以什么结尾

```java
String fileName = "HelloWorld.class";
if(fileName.endsWith(".java")){
    System.out.println("源文件");
}else if(fileName.endsWith(".class")){
    System.out.println("字节码文件");
}

```

######   replace

替换

```java
String str ="去你大爷的";
System.out.println(str.replace("爷","*"));

```

######  split

字符串拆分，返回值是一个数组类型

```java
String str ="java.day04.HelloWorld";

String [] arr = str.split("\\.");

for(String s : arr){
    System.out.println(s);
}
```

### 

#### String构造方法

![image-20210107213317743](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107213317743.png)

![image-20210107213613648](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107213613648.png)

> 推荐使用直接赋值的方式得到字符串对象

![image-20210107214251723](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107214251723.png)



#### String对象的特点

![image-20210107213732677](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107213732677.png)

![image-20210107213831807](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107213831807.png)



####  案例

##### 用户登录

![image-20210107214846036](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107214846036.png)

![image-20210107215318052](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107215318052.png)

##### 字符串的比较

###### 使用== 作比较

- 基本类型： 比较的是数据值是否相同

- 引用类型： 比较的是地址值是否相同

######  equals

![image-20210107214519480](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107214519480.png)

![image-20210107214745294](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107214745294.png)

String重写了equals方法：在String里 比较内容是否相等

```java
String str1 ="abc";
String str2 ="abc";
System.out.println(str1.equals(str2));

```

### 

##### 遍历字符串

![image-20210107215630863](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107215630863.png)



![image-20210107220111305](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107220111305.png)

###### Length

```java
String name = "Memory";
int len = name.length();
System.out.println(len);

int [] arr = new int[5];
System.out.println(arr.length);

//String 和  数组   求长度都是用.length() 对吗
//不对  String 方法  数组 属性

```

######   charAt

获取指定位置的字符

```java
String str = "山西太原";
System.out.println(str.charAt(1));// 山

```

#####  统计字符次数

![image-20210107220226806](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107220226806.png)

##### 拼接字符串

![image-20210107221237444](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107221237444.png)

![image-20210107221458401](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107221458401.png)

##### 字符串反转

![image-20210107221558113](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107221558113.png)

![image-20210107221951705](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107221951705.png)

### Arrays

#### 冒泡排序

![image-20210108235326116](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108235326116.png)

![image-20210108235403320](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108235403320.png)

![image-20210108235811196](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108235811196.png)

![image-20210108235737357](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108235737357.png)

![image-20210108235754866](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108235754866.png)

#### Arrays类的概述和常用方法

![image-20210108235923618](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108235923618.png)![image-20210109000015147](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109000015147.png)

工具类的设计思想：

- 构造方法用private修饰
- 成员用public static修饰



### 基本类型包装类

#### 基本类型包装类概述

- 将基本数据类型封装成对象的好处在于可以在对象中定义更多的功能方法操作该数据

- 常用的操作之一： 用于基本数据类型与字符串之间的转换。

  

  ```java
  // 包装类常用操作
  //1.帮助我们做类型转换
  String str ="188";
  //int price = str;
  int price = Integer.parseInt(str);
  //2.本身定义了一些常用的操作
  System.out.println(Integer.MAX_VALUE);
  System.out.println(Byte.MAX_VALUE);
  System.out.println(Short.MIN_VALUE);
  
  ```

  ####  

![image-20210109114526959](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109114526959.png)

**包装类**

Wrapper Class包装类：

| **类型名称** | **基本类型** | **包装类型** | **父类** |
| ------------ | ------------ | ------------ | -------- |
| 字节型       | byte         | Byte         | Number   |
| 短整型       | short        | Short        |          |
| 整型         | int          | Integer      |          |
| 长整型       | long         | Long         |          |
| 单精度浮点型 | float        | Float        |          |
| 双精度浮点型 | double       | Double       |          |
| 字符型       | char         | Character    | Object   |
| 布尔型       | boolean      | Boolean      |          |

 

> 基本类型时沿用面向过程开发的特性，java中的基本数据类型int,double…等不是对象，无法使用Object提供的方法，而String就可以，因为String是一个对象而不是一个类型，基本数据类型由于这样的特性，导致无法参与转换，泛型，反射等过程
>
> 为了弥补这个缺陷，java提供了包装类



#### Interger 类的概述和使用

Integer： 包装一个对象中的原始类型int 的值

**构造方法**

![image-20210109114740115](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109114740115.png)

 ![image-20210109115035451](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109115035451.png)

#### int 和String 的相互转换

基本类型包装类的最常见操作就是： 用于基本类型和字符串之间的相互转换

**int   -> String**

> public static String valueOf(int): 返回 int 参数的字符串表示形式， 该方法是String类中的方法

![image-20210109115744853](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109115744853.png)

**String  ->  int**

> public static int parseInt(String s): 将字符串解析为int 类型， 该方法时Integer类中的方法

![image-20210109120143355](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109120143355.png)

#### 案例

##### 字符串中数据排序

![image-20210109121033273](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109121033273.png)

![image-20210109121621884](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109121621884.png)

![image-20210109121647532](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109121647532.png)

####  自动装箱和拆箱

装箱：将基本数据类型转变为包装类对象

自动装箱：

![image-20210109122027834](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109122027834.png)

拆箱：将包装类对象，转变为基本数据类型

自动拆箱：

![image-20210109122308849](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109122308849.png)



![image-20210109122342147](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109122342147.png)



![image-20210109122509056](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109122509056.png)





### 日期类 Date

#### Date类概述和构造方法

Date代表了一个特定的时间，精确到毫秒

![image-20210109122912109](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109122912109.png)

![image-20210109123608058](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109123608058.png)



#### Date类的常用方法：

![image-20210109123652051](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109123652051.png)

![image-20210109124122551](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109124122551.png)

####  SimpleDateFormat

SimpDateFormat是一个具体的类，用于以区域设置敏感的方法格式化和解析日期，我们重点学习日期格式化和解析

![image-20210109152100261](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109152100261.png)

![image-20210109124436192](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109124436192.png)

##### SimpleDateFormat的构造方法

![image-20210109152139003](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109152139003.png)

##### Simple DateFormat格式化和解析日期

![image-20210109152234797](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109152234797.png)

可以自定义格式来解析日期

![image-20210109152647385](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109152647385.png)



#### 案例

##### 日期工具类

![image-20210109152807811](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109152807811.png)

![image-20210109153025243](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109153025243.png)

![image-20210109153227665](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109153227665.png)

#### Calendar 类概述

> Calendar 为谋一时刻和一组日历字段之间的转换提供了一些方法， 并为操作日历字段提供了一些方法

```java
//Calenda提供了一个类方法 getInstance用于获取Calendar对象， 其日历字段已使用当前日期和时间初始化
Calendar rightNow = Calendar.getInstance();

```

![image-20210109154156111](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109154156111.png)

##### Calendar 的常用方法

![image-20210109154222082](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109154222082.png)

![image-20210109154444260](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109154444260.png)

##### 案例

###### 二月天

![image-20210109154546471](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109154546471.png)

![image-20210109154703190](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109154703190.png)





### StringBuilder (java.lang)

#### **StringBuilder概述**

![image-20210107223030565](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107223030565.png)



区别：

- **StringBuilder 是一个可变的字符串类，** 我们可以把它看成是一个容器，这里的的可变子的是StringBuilder对象中的内容是可变的。

- String的值是**不可变**的，**每次对String操作都会生成新的String对象，效率低**

> 当我们对字符串进行频繁的修改时，需要使用StringBuffer和StringBuilder
>
> 
>
> StringBuilder线程不安全的，速度快
>
> StringBuffer 是线程安全的，速度慢

#### StringBuilder 构造方法

 ![image-20210107223826900](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107223826900.png)

![image-20210107224730386](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107224730386.png)

#### StringBuilder的添加和反转方法

![image-20210107224805455](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107224805455.png)

![image-20210107225226091](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107225226091.png)



#### StringBuilder和String 相互转换

1.StringBuilder 转换为String

public String **toString()**: 通过toString()就可以实现把StringBuilder转换为String

2.String 转换为StringBuilder

public **StringBuilder(String s)**: 通过构造方法就可以把String转换为StringBuilder

 ![image-20210107225811656](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107225811656.png)

#### 案例

##### 拼接字符串 升级版

![image-20210107225945072](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107225945072.png)

![image-20210107230147629](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107230147629.png)

![image-20210107230123921](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107230123921.png)

##### 字符串反转 升级版 

![image-20210107230255373](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107230255373.png)

![image-20210107230518943](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107230518943.png)

#### 通过帮助文档查看StringBuilder中的方法

![image-20210107230603932](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107230603932.png)

##  面试题

l 举5个String常用的api

l 数组的长度和字符串的长度

l 笔试题中  == 判断

l String&StringBuilder&StringBuffer区别



# 异常

### 异常概述

异常就是程序在运行的过程中可能会出现的错误

![image-20210109155219502](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109155219502.png)



### JVM的默认处理方案

如果程序出现了问题， 我们没有做任何处理，最终JVM会做默认的处理

- 把异常的名称，异常原因及异常出现的位置等信息输出在了控制台
- 程序停止运行



```java
int i = 3/0;
System.out.println(i);
```

报错：不能除以0

![image-20210102222728793](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102222728793.png)



### 异常处理

#### try-catch 

自己处理异常 程序还可以往下继续执行

![image-20210109155912702](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109155912702.png)

**处理异常**

```java
try {  //try里面写的是可能会出现异常的代码
    int i = a/b;
    System.out.println(i);
} catch (ArithmeticException e){
    System.out.println("恭喜你出错了不能除以0");
} catch (Exception e){ //catch捕获异常信息，catch可以写多个
    System.out.println("恭喜你出错了不能除以0"+e.getMessage());
}

```



#### throws

延时处理 仅仅只是抛出去了  真正处理还是需要try catch处理

![image-20210109161228705](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109161228705.png)

![image-20210109161611312](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109161611312.png)



**抛出异常**

谁调用抛给谁

分两步：

（1）  抛异常

（2）  接异常

```java
//throws写在方法上  声明该方法接收的异常,多个异常逗号隔开
public static void division(int a,int b) throws Exception,RuntimeException {
    
    try {
        int i = a/b;
        System.out.println(i);
    }catch (RuntimeException e){
        throw new RuntimeException();
    }catch (Exception e){
        //主动抛出异常
        throw new Exception("除数不能为0"); //throw 抛出指定异常
    }
}

```



### Throwable的成员方法

![image-20210109160204727](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109160204727.png)

![image-20210109160514039](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109160514039.png)

![image-20210109160646950](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109160646950.png)



### 编译时异常和运行时异常的区别

![image-20210109160755058](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109160755058.png)

![image-20210109161144974](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109161144974.png)









###   Finally 一定会执行

```java
//throws写在方法上  声明该方法接收的异常,多个异常逗号隔开
public static void division(int a,int b) throws Exception,RuntimeException {
    try {
        int i = a/b;
        System.out.println("愿世界和平");
        System.out.println(i);
    }catch (RuntimeException e){
        throw new RuntimeException();
    }catch (Exception e){
        //主动抛出异常
        throw new Exception("除数不能为0"); //throw 抛出指定异常
    }finally { //一定会执行的代码  常用的操作关闭流释放资源等
        System.out.println("我来处理后事");
    }
}

```

### 自定义异常

![image-20210109162155375](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109162155375.png)

 ![image-20210109162601037](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109162601037.png)![image-20210109162608501](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109162608501.png)

![image-20210109162628618](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109162628618.png)



```java
/**
 * 自定义异常步骤
 * 1.继承Exception 或者 RuntimeException
 * 2.定义构造方法
 */
public class PasswordError extends RuntimeException{

    public PasswordError(){

    }
    public PasswordError(String message){
        super(message);
    }

}

```

```java
//自定义异常
String   password  = "123123";
if (password.equals("123456")){
    System.out.println("登录成功");
}else {

    throw new PasswordError("密码错误");
}

```

### throw 和 throws区别

![image-20210109162723482](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109162723482.png)





###  常见面试题

throw 和 throws区别

final 和 finally区别

# 集合 



## 集合类体系结构



集合类型主要分为三种：

- Set 
- List  
- Map

![image-20210109163317351](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109163317351.png)



单列集合

 ![image-20210102224858973](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102224858973.png)

双列集合![image-20210102224905423](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102224905423.png)

##  集合特点

集合类的特点： 提供一种存储空间可变的存储模型，存储的数据容量可以发生改变

集合类对象存放的都是对象的引用，而非对象本身

集合就是一个存放数据的容器，可以存放不同数据类型的数据

Lis接口 存储一组不唯一，有序的对象

--ArrayList 底层是可变长度的数组 查询快  增删慢



 ![image-20210102224915042](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102224915042.png)

--LinkedList 底层是双向链表方式 查询慢 增删快

 ![image-20210102224922033](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102224922033.png)

Set接口 存储一组唯一，无序的对象

Map 接口 存储一组键值对象  Key value

## Collection

### Collection集合概述

- 是单例集合的顶层接口，它表示一组对象，这些对象也称为Collection的元素

- JDK不提供此接口的任何直接实现， 它提供更具体的子接口(如

  Set和List)实现

创建Collection集合的对象

- 多态的方式
- 具体的实现类ArrayList

**基本使用**

![image-20210109165001502](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109165001502.png)

### Collection集合常用方法

![image-20210109165033572](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109165033572.png)

### Collection集合的遍历

Iterator：迭代器，集合的专用遍历方式

- Iterator<E> iterator():返回刺激和中元素的的迭代器，通过集合的iterator()方法得到
- 迭代器是通过集合的iterator()得到的，所以我们说它是依赖于集合而存在的

**Iterator中的常用方法**

- E next(): 返回迭代中的下一个元素
- boolean hasNext(): 如果迭代具有更多元素， 则返回true

### 集合的使用步骤

![image-20210109173213591](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109173213591.png)

### 案例

#### Collection集合存储学生对象并遍历

![image-20210109173349457](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109173349457.png)

![image-20210109173609255](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109173609255.png)













### List

#### list集合概述和特点

**list集合概述**

- 有序集合也称为序列， 用户可以精确控制列表中每个元素的插入位置，用户可以通过整数索引访问元素， 并搜索列表中的元素。
- 与set集合不同，列表通常允许重复的元素

**list集合特点**

- 有序：存储和取出的元素顺序一致
- 可重复：存储的元素可以重复

![image-20210109174640653](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109174640653.png)



#### list集合常用的方法

 ![image-20210109174733930](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109174733930.png)

![image-20210102224937692](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102224937692.png)

![image-20210109175444265](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109175444265.png)

#### 案例

##### List集合存储学生对象并遍历

![image-20210109175628234](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109175628234.png)

 ![image-20210109175829893](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109175829893.png)

#### 并发修改异常

 并发修改异常

- ConcurrentModificationException

产生原因(观察源码 )

- 迭代器便利过程中， 通过集合对象修改了集合中元素的长度， 造成了迭代器获取元素中判断预期修改值和实际修改值不一致。

解决方案

- 用for 循环遍历， 然后用集合对象做对应的操作即可

#### ListIterator

ListIterator：列表迭代器

- 通过List集合 的listIterator()方法得到，所以说它是list集合特有的迭代器  
- 用于允许程序员沿任一方向遍历列表的列表迭代器，在迭代期间修改列表，并获取列表中迭代器的当前位置

ListIterator中的常用方法

- E next(): 返回迭代中的下一个元素
- boolean hasNext()：如果迭代具有更多元素， 则返回true
- E previous(): 返回列表中的上一个元素
- boolean hasPrevious(): 如果此列表迭代器在相反方向遍历列表时具有更多元素， 则返回true
- void add(E e): 将指定的元素插入列表

![image-20210109192825998](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109192825998.png)

![image-20210109193030728](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109193030728.png)

#### 增强for循环

增强for：简化数组和Collection集合的遍历

- 实现Iterable接口的类允许其对象称为增强型for语句的目标
- 它是JDK5之后出现的， 其内部原理是一个**Iterator迭代器**

增强for的格式

格式   for(元素数据类型变量名：**数组或者Collection集合**){

​				//在此处使用变量即可，该变量就是元素

​			}

范例：

```java
int[] arr = {1,2,3,4,5};

for(int i :arr){

System.out.println(i)

}
```

 ![image-20210109194347844](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109194347844.png)

![image-20210109194506867](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109194506867.png)

会抛出并发修改异常



#### 案例

##### List集合存储学生对象用三种方式遍历

![image-20210109194620155](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109194620155.png)

![image-20210109194751679](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109194751679.png)

![image-20210109194811064](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109194811064.png)

#### 数据结构

数据结构时计算机存储、组织数据的方式，是指相互之间存在一种或多种特定关系的数据元素的集合

##### **常见数据结构之栈**

##### **常见数据结构之队列**

##### **常见数据结构之数组**

- 查询数据通过索引定位，查询任意数据耗时相同， **查询速度快**

- 删除数据时，要将原始数据删除， 同时后面每个数据前移，删除效率低
- 添加数据时， 添加位置后的每个数据后移，再添加元素，添加效率极低

数组是一种查询快，增删满的模型

##### **常见数据结构之链表**

![image-20210109195531612](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109195531612.png)

![image-20210109195617837](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109195617837.png)



![image-20210109195657786](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109195657786.png)

 ![image-20210109195738372](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109195738372.png)

![image-20210109195812414](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109195812414.png)

#### List集合子类特点

**list集合常用子类**: ArrayList , LinkedList

- ArrayList: 底层数据结构是数组， 查询快， 增删慢
- LinkedList：底层数据结构是链表，查询慢， 增删快

> 练习： 分别使用ArrayList和LinkedList完成存储字符串并遍历

![image-20210109200652118](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109200652118.png)





#### Arraylist<E>

- 可调整大小的数组实现

- <E>:是一种特殊的数据类型， 泛型。

![image-20210107231658765](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107231658765.png)

##### ArrayList构造方法和添加方法

![image-20210107231748177](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107231748177.png)

![image-20210107232349692](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107232349692.png)





##### ArrayList集合常用方法

![image-20210107233700022](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107233700022.png)

![image-20210107233928015](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107233928015.png)

![image-20210107234107349](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107234107349.png)

```java
ArrayList list = new ArrayList();
//添加元素，向末尾添加
list.add("张三");
list.add(18);
list.add(new Person());
System.out.println(list.toString());
System.out.println(list.size());
list.add(1,'男');
System.out.println(list.toString());
System.out.println(list.get(1));
//判断是否包含
boolean b = list.contains("李四");
System.out.println(b);
list.add("张三");

list.remove(4);
list.remove("张三");
list.clear();

```

#####  案例

##### 存储字符串并遍历

![image-20210107234249264](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107234249264.png)

##### 存储学生对象并遍历

![image-20210107234430198](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107234430198.png)

![image-20210107234521776](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107234521776.png)

![image-20210109200902688](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109200902688.png)



##### 存储学生对象并遍历修改

![image-20210107234609610](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107234609610.png)

![image-20210107234752101](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107234752101.png)

![image-20210107234738823](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107234738823.png)

#### 学生管理系统 

##### 项目演示

![image-20210107234912472](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210107234912472.png)

##### 学生管理系统的实现思路

![image-20210108105037580](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108105037580.png)

**定义学生类**

![image-20210108105111667](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108105111667.png)

![image-20210108105255415](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108105255415.png)

**主界面的代码编写**

![image-20210108105359646](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108105359646.png)

 ![image-20210108105916685](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108105916685.png)

**添加学生的代码编写**

![image-20210108110055754](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108110055754.png)

![image-20210108110431000](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108110431000.png)

**查看学生的代码编写**

![image-20210108110537995](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108110537995.png)

![image-20210108110918304](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108110918304.png)

**查看学生的代码编写升级版**

![image-20210108111123380](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108111123380.png)

![image-20210108111337538](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108111337538.png)

**删除学生的代码编写**

![image-20210108111449411](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108111449411.png)

![image-20210108111611628](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108111611628.png)

**修改学生的代码编写**

![image-20210108111720376](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108111720376.png)

![image-20210108111828297](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108111828297.png)

**解决删除/修改学生学号不存在问题**

![image-20210108111937996](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108111937996.png)

![image-20210108112033785](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108112033785.png)

**解决添加学生学号重复问题**

![image-20210108112136030](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108112136030.png)

![image-20210108112203929](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108112203929.png)

![image-20210108112321890](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210108112321890.png)





#### LinkedList特有方法

 ![image-20210109201004577](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109201004577.png)



### Set

#### Set 集合概述和特点

**Set集合特点**

- 不包含重复元素的集合
- 没有带索引的方法， 所以不能使用普通for循环遍历

Set集合练习

- 存储字符串并遍历
- HashSet： 对集合的迭代顺序不做保证



![image-20210109201911450](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109201911450.png)

#### 哈希值

哈希值 ，

是JDK根据对象的地址或者字符串或者数字算出来的**int类型的数值** 

Object类中有一个方法可以获取对象的哈希值

- public int hashCode(): 返回对象的哈希码值

对象的哈希值特点

- 同一个对象多次调用hashCode()方法返回的哈希值是相同的

- 默认情况下， 不同对象的哈希值是不同的，而重写hashCode()方法， 可以实现让不同对象的哈希值相同

  哈希值有范围



![image-20210109202855875](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109202855875.png)

#### HashSet集合概述和特点

![image-20210109203305676](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109203305676.png)



#### HashSet集合保证元素唯一性源码分析

   ![image-20210109222111251](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109222111251.png)



#### 常见数据结构之哈希表

哈希表

- JDK8之前， 底层采用数组+链表实现， 可以说是一个元素为链表的数组
- JDK8以后，在长度比较长的时候，底层实现了优化

![image-20210109222457304](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109222457304.png)

重复元素不存储。

#### 案例

##### HashSet集合存储学生对象并遍历

![image-20210109224813964](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109224813964.png)

#### LinkedHashSet集合概述和特点

![image-20210109225001715](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210109225001715.png)

#### TreeSet集合概述和特点

  ![image-20210111101813217](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111101813217.png)

![image-20210111102135927](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111102135927.png)

#### 自然排序Comparable的使用

元素类实现接口Comparable 然后重写方法进行比较自然排序

![image-20210111102226332](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111102226332.png)

  ![image-20210111103502777](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111103502777.png)

![image-20210111103429530](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111103429530.png)

![image-20210111103439448](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111103439448.png)

#### 比较器排序Comparator的使用

在 TreeSet构造方法中传递一个比较器接口Comparator

规则定义是一样的。

![image-20210111103642391](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111103642391.png)

![image-20210111104247465](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111104247465.png)



![image-20210111104008733](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111104008733.png)

> 匿名内部类





#### 案例

##### 成绩排序

 ![image-20210111104506990](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111104506990.png)

 ![image-20210111104915509](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111104915509.png)

![image-20210111105318350](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111105318350.png)

##### 不重复的随机数

![image-20210111105507609](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111105507609.png)

 ![image-20210111105942964](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111105942964.png)

![image-20210111110006442](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111110006442.png)

### 泛型

#### 泛型概述

![image-20210111110152295](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111110152295.png)

![image-20210111110718844](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111110718844.png)



![image-20210111110709972](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111110709972.png)

#### 泛型类

![image-20210111110943784](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111110943784.png)

![image-20210111111020046](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111111020046.png)

![image-20210111111220657](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111111220657.png)

#### 泛型方法

![image-20210111111512206](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111111512206.png)

![image-20210111111801979](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111111801979.png)



![image-20210111111606056](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111111606056.png)

![image-20210111111824435](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111111824435.png)





![image-20210111111644238](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111111644238.png)

#### 泛型接口

![image-20210111111936097](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111111936097.png)

![image-20210111112156273](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111112156273.png)

![image-20210111112201504](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111112201504.png)

![image-20210111112209462](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111112209462.png)



#### 类型通配符

![image-20210111112334963](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111112334963.png)

![image-20210111112657810](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111112657810.png)



#### 可变参数

![image-20210111113301006](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111113301006.png)



![image-20210111113247171](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111113247171.png)



#### 可变参数的使用

![image-20210111114025722](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111114025722.png)

![image-20210111114009527](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111114009527.png)



##  Map

#### Map集合概述和使用

![image-20210111114553749](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111114553749.png)

Map用于保存具有映射关系的数据（key-value）

![image-20210111115035203](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111115035203.png)



#### Map集合的基本功能

 ![image-20210111115111437](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111115111437.png)

![image-20210111115755983](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111115755983.png)



#### Map集合的获取功能

![image-20210111115820230](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111115820230.png)

![image-20210111120109514](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111120109514.png)

#### Map集合的遍历(方式1)

![image-20210111120321414](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111120321414.png)

![image-20210111120426157](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111120426157.png)

#### Map集合的遍历(方式2)

![image-20210111120646166](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111120646166.png)

![image-20210111130409590](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111130409590.png)

#### 案例

##### HashMap集合存储学生对象并遍历

![image-20210111130739266](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111130739266.png)

![image-20210111131059429](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111131059429.png)

![image-20210111131107088](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111131107088.png)



##### HashMap集合存储学生对象并遍历(键是Student，值是String)

![image-20210111131458297](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111131458297.png)

![image-20210111131841740](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111131841740.png)



##### ArrayList集合存储HashMap元素并遍历

![image-20210111132016636](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111132016636.png)

![image-20210111132859825](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210111132859825.png)

##### HashMap集合存储ArrayList元素并遍历

![image-20210112155024557](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112155024557.png)

![image-20210112155938315](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112155938315.png)

![image-20210112155945426](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112155945426.png)

#####  统计字符串中每个字符出现的次数

![image-20210112160616329](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112160616329.png)

![image-20210112170202071](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112170202071.png)

![image-20210112170507106](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112170507106.png)

> 改进：  
>
> TreeMap  可以使其key 按照无参构造方法自然顺序排序
>
> 类似于TreeSet





#### HashMap存储过程

HashMap是由数组+链表+红黑二叉树组成

equals相同的key hashcode值一定相等 确保了key不重复

hashcode值相等的key equals不一定相同  这个时候就会产生链表

 ![image-20210102225055830](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102225055830.png)

##  Collections

### Collections 概述和使用

![image-20210112171510857](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112171510857.png)

![image-20210112171845417](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112171845417.png)

### 案例

#### ArrayList 存储学生对象 并排序

![image-20210112172025145](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112172025145.png)

![image-20210112172256529](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112172256529.png)

![image-20210112172314380](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112172314380.png)



#### 模拟斗地主

  ![image-20210112181024374](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112181024374.png)

![image-20210112182046148](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112182046148.png)

![image-20210112182057544](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112182057544.png)

![image-20210112182846862](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112182846862.png)



####  模拟斗地主升级版

![image-20210112183453442](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112183453442.png)



![image-20210112183603871](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112183603871.png)

![image-20210112184608871](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112184608871.png)



![image-20210112184917870](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112184917870.png)

![image-20210112185140696](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112185140696.png)





## 集合面试题

- List 和 Set区别

- ArrayList 和 LinkedList区别

- HashMap底层存储原理

- Map属于collection

- 各个集合之间的关系







# IO流

## File

### File类概述和构造方法

![image-20210112190504535](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112190504535.png)



![image-20210112190839310](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112190839310.png)

### File类创建功能

![image-20210112190945511](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112190945511.png)

 ![image-20210112191725309](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112191725309.png)



![image-20210112191620338](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112191620338.png)

### File类判断和获取功能

![image-20210112191910463](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112191910463.png)

![image-20210112192843922](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112192843922.png)

![image-20210112192812863](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112192812863.png)

### File类删除功能

![image-20210112200314647](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112200314647.png)

![image-20210112200301229](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112200301229.png)

### 递归

![image-20210112201214755](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112201214755.png)



![image-20210112201115401](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112201115401.png)

#### 案例  

##### 递归求阶乘

![image-20210112201326412](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112201326412.png)

![image-20210112201343682](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112201343682.png)

![image-20210112201452393](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112201452393.png)

##### 遍历目录

![image-20210112202145454](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112202145454.png)

![image-20210112202517679](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112202517679.png)





## 字节流

### IO流概述和分类

![image-20210112203021171](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112203021171.png)

> 我们编写的程序除了自身定义一些数据信息以外，经常还会引用外界的数据，或者是将自身的数据发送到外界
>
> 什么是输入，什么是输出
>
> -输入时一个从外界进到程序的方向，通常我们需要读取外界数据时，使用输入(IS)
>
> -输出时从一个程序发送到外界的方向,通常我们需要写出数据时，使用输出(OS)

![image-20210112203058457](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112203058457.png)

![image-20210112203215422](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112203215422.png)

### ---------------------

### 字节流写数据

![image-20210112204517386](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112204517386.png)

![image-20210112210105913](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112210105913.png)



![image-20210112205959766](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112205959766.png)

### 字节流写数据的3种方式

![image-20210112210133276](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112210133276.png)

![image-20210112211831077](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112211831077.png)

![image-20210112212836465](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112212836465.png)

![image-20210112212909488](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112212909488.png)

![image-20210112213052580](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112213052580.png)

### 字节流写数据的俩个小问题

![image-20210112213929391](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112213929391.png)

![image-20210112213749762](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112213749762.png)

![image-20210112213800210](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112213800210.png)

### 字节流写数据加异常处理

![image-20210112214346007](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112214346007.png)

![image-20210112215039509](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112215039509.png)

### ------------------

### 字节流读数据(一次读一个字节数据)

![image-20210112220020533](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112220020533.png)

![image-20210112222030343](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112222030343.png)

![image-20210112223102277](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112223102277.png)



### 案例 复制文本文件

![image-20210112223829642](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112223829642.png)

![image-20210112224103064](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112224103064.png)

![image-20210112224401697](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112224401697.png)

### 字节流读数据(一次读一个字节数组数据)

![image-20210112224809367](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112224809367.png)

![image-20210112230845240](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112230845240.png)

![image-20210112230752075](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112230752075.png)

![image-20210112231236620](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112231236620.png)

> new String（byte[], offset,len）
>
> 字符串 读取

### 案例 复制图片

![image-20210112231519836](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112231519836.png)

![image-20210112231750249](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112231750249.png)

### ----------------

### 字节缓冲流

![image-20210112232532023](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112232532023.png)

![image-20210112233330852](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112233330852.png)

### 案例 复制视频

![image-20210112233941781](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112233941781.png)



  ![image-20210112234909871](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112234909871.png)![image-20210112234852410](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112234852410.png)![image-20210112234824582](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112234824582.png)

![image-20210112234759575](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112234759575.png)![image-20210112234438630](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210112234438630.png)







### 附

#### 文件流

**FileOutPutStream是文件字节输出流，我们使用该流可以以字节为单位将数据写入文件**

**重写模式**：若指定文件已经包含内容，使用FOS对其写入数据时会将该文件中原有数据全部删除

New FileOutPutStream(String filename)

追加模式：在文件末尾追加

New FileOutPutStream(String filename,true)

 

```java
OutputStream os = new FileOutputStream("a.txt",true);
String str = "Hello Word";
for (int i=0;i<str.length();i++){
   int b = (int)str.charAt(i);
   os.write(b);
}
String str2 = "Memory";
byte[] bytes = str2.getBytes();
os.write(bytes);
System.out.println("输出成功");

```



**FileInputStream是文件字节输入流，我们使用该流可以以字节为单位从文件中读取数据**

**FileInputStream(File file)**

FileInputStream(String fileName)

 

```java
FileInputStream fis = new FileInputStream("data.txt");
char c = (char) fis.read();
System.out.println(c);

byte[] bytes = new byte[5];
int length = fis.read(bytes);
System.out.println(length);
```



#### 缓冲字节流

在向硬件设备中读写操作时，增大写出次数无疑会降低写出效率，为此我们可以使用缓冲输出流来一次性批量的写出若干数据减少写出次数来提高效率

 

#####   BufferedOutPutStream缓冲字节输出流

BufferedOutPutStream缓冲输出流，内部维护着一个缓冲区，每当我们向该流写数据时，都会先将数据存如缓存区，当缓存区已满时，缓冲流会将数据一次性写出

```java
FileOutputStream fos = new FileOutputStream("data.txt",true);
BufferedOutputStream bos = new BufferedOutputStream(fos);
bos.write("day day up".getBytes());
bos.flush();//如果缓存没满，强制输出
bos.close();//关闭流时，系统会自动调用flush方法
System.out.println("输出成功");
```

 

 

#####  BufferedInputStream缓冲字节输入流

BufferedInputStream是缓冲字节输入流，其内部维护着一个缓冲区(字节数组)，使得用户在读取一个字节时，会尽可能的一次性读取若干个存入缓存区

```java
public class BIS {
    public static void main(String[] args) throws Exception {
        FileInputStream fis = new FileInputStream("data.txt");
        BufferedInputStream bis = new BufferedInputStream(fis);
        int d = -1;
        while ((d=bis.read())!=-1){
            char c = (char)d;
            System.out.print(c);
        }
        bis.close();
    }
}

```

 



###  对象流

对象是存储在内存中，有时候我们需要将对象保存到硬盘上，有时我们需要将对象传输到另一台计算机上等等这一系列操作，这时我们需要将对象转换为一个字节序列，而这个过程就称为对象的序列化，相反，我们由这样一个字节序列需要将其转换为对象时，这个过程就称之为对象的反序列化

 

对象在进行序列化时有一个要求，就是必须实现Serializable接口

实现该接口不需要重写任何方法，只是作为可序列化的一个标志

通常实现该接口需要提供一个常量serialVersionUID

表名该类的版本，若不声明，在对象序列化时也会根据当前类的各个方面计算该类的默认序列化版本ID

 

#### ObjectOutPutStream实现对象的序列化

\-  Void writeObject(Object o);

 

```java
FileOutputStream fos = new FileOutputStream("person.obj");
ObjectOutputStream oos = new ObjectOutputStream(fos);
Person person = new Person(18,"张三");
oos.writeObject(person);
System.out.println("序列化完毕");
oos.close();
```



####   ObjectInputStream实习对象的反序列化

\-  Object readObject() 

\-  

```java
FileInputStream fis = new FileInputStream("person.obj");
ObjectInputStream ois = new ObjectInputStream(fis);

Person person = (Person) ois.readObject();
System.out.println(person);

```

 

####  一定要从上述例子中体会多态的好处

 

### 节点流与处理流

按照流是否直接与特定的地方(磁盘，内存等)相连，分为节点流和处理流两类

--节点流:可以从或向一个特定的地方读写数据，我们成为低级流

--处理流:是一个已存在的流的连接和封装，通过所封装的流的功能调用实现数据读写，我们称之为高级流、

 

 

 

##  字符流 

> Reader是字符输入流的父类
>
> Writer是字符输出流的父类
>
> 字符流是以字符(char)为单位读写数据，一次处理一个unicode编码
>
> 字符流的底层仍是基本的字节流
>

###  为什么会出现字符流

![image-20210113095430521](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113095430521.png)

![image-20210113095513877](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113095513877.png)

### **编码表**

![image-20210113095803841](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113095803841.png)

![image-20210113095832136](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113095832136.png)

![image-20210113095917571](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113095917571.png)

![image-20210113100234801](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113100234801.png)

![image-20210113100424086](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113100424086.png)



### 字符串中的编码解码问题

![image-20210113100551865](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113100551865.png)

 ![image-20210113101009069](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113101009069.png)



### 字符流中的编码解码问题

![image-20210113101951919](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113101951919.png)

![image-20210113101928908](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113101928908.png)



![image-20210113101910043](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113101910043.png)

### 字符流写数据的5种方式

![image-20210113102059883](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113102059883.png)

 ![image-20210113102559682](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113102559682.png)

![image-20210113102808936](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113102808936.png)

![image-20210113102819493](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113102819493.png)



### 字符流读数据的2种方式

![image-20210113102904403](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113102904403.png)

 ![image-20210113103353337](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113103353337.png)

### 案例

#### 复制java文件

![image-20210113103907536](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113103907536.png)

![image-20210113103855871](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113103855871.png)

#### 复制Java文件(改进版)

![image-20210113104255752](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113104255752.png)

![image-20210113104354494](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113104354494.png)

![image-20210113104649536](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113104649536.png)

### 字符缓冲流![image-20210113105127240](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113105127240.png)

![image-20210113105141762](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113105141762.png)

  

![image-20210113105843019](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113105843019.png)

### --------------------

### 案例:复制Java文件(字符缓冲流改进版)



![image-20210113105946020](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113105946020.png)

![image-20210113110137135](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113110137135.png)



### 字符缓冲流特有功能

![image-20210113110227210](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113110227210.png)

![image-20210113110649217](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113110649217.png)

![image-20210113110853267](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113110853267.png)

### 案例： 复制Java文件(字符缓冲流特有功能改进版)

![image-20210113111027205](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113111027205.png)

![image-20210113111324986](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113111324986.png)

### -----------------

### IO流小结

![image-20210113111729733](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113111729733.png)

![image-20210113111747964](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113111747964.png)



![image-20210113111818694](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113111818694.png)

![image-20210113112003620](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113112003620.png)

### -------------------

### 案例 ： 集合到文件

![image-20210113112208370](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113112208370.png)

![image-20210113112529197](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113112529197.png)

### 案例：   集合到文件(改进版)

![image-20210113113931090](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113113931090.png)

![image-20210113114300114](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113114300114.png)

### 案例： 集合到文件(数据排序改进版)

![image-20210113161931105](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113161931105.png)

![image-20210113162448215](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113162448215.png)

![image-20210113162524186](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113162524186.png)

![image-20210113162614932](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113162614932.png)

![image-20210113162805806](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113162805806.png)

















### 案例：  文件到集合

![image-20210113112729802](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113112729802.png)

![image-20210113112907741](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113112907741.png)

### 案例：   文件到集合(改进版)

![image-20210113114557725](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113114557725.png)

![image-20210113114944867](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113114944867.png)

![image-20210113115027632](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113115027632.png)







### 案例： 点名器

![image-20210113113214119](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113113214119.png)

![image-20210113113651377](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113113651377.png)

![image-20210113113718709](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113113718709.png)



### 案例： 复制单级文件夹

![image-20210113163237035](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113163237035.png)

 

![image-20210113170555474](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113170555474.png)

![image-20210113170608774](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113170608774.png)

### 案例：复制多级文件夹

![image-20210113170914938](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113170914938.png)

![image-20210113171423782](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113171423782.png)

![image-20210113171523021](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113171523021.png)

### ------------------

### 复制文件的异常处理

![image-20210113172429581](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113172429581.png)

![image-20210113172500239](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113172500239.png)

![image-20210113172512042](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113172512042.png)

try... catch ...finally

![image-20210113172240984](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113172240984.png)

![image-20210113172525894](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113172525894.png)



## 特殊操作流

### 标准输入输出流

![image-20210113173724659](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113173724659.png)

![image-20210113173510818](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113173510818.png)

![image-20210113173619562](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113173619562.png)

![image-20210113173653817](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113173653817.png)

![image-20210113174206724](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113174206724.png)



![image-20210113174140067](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113174140067.png)



### 打印流

![image-20210113174814814](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113174814814.png)

#### 字节打印流

![image-20210113174835561](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113174835561.png)

#### 字符打印流

![image-20210113175130291](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113175130291.png)

![image-20210113175424484](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113175424484.png)

![image-20210113175604848](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113175604848.png)

#### 案例： 复制Java文件(打印流改进版)

![image-20210113175730832](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113175730832.png)

![image-20210113175858883](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113175858883.png)

![image-20210113180022526](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113180022526.png)



### 对象序列化流

![image-20210113180237168](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113180237168.png)



**对象序列化流**

![image-20210113180926964](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113180926964.png)

![image-20210113180948926](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113180948926.png)

**对象反序列化流**

![image-20210113181217417](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113181217417.png)

![image-20210113181405009](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113181405009.png)



![image-20210113182400759](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113182400759.png)

 ![image-20210113182511033](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113182511033.png)

![image-20210113182432878](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113182432878.png)



### Properties

![image-20210113182655096](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113182655096.png)

![image-20210113182914558](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113182914558.png)

![image-20210113183007920](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113183007920.png)

![image-20210113183700146](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113183700146.png)



![image-20210113183751161](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113183751161.png)

![image-20210113184212355](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113184212355.png)

![image-20210113184225568](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113184225568.png)



### 案例： 游戏次数

![image-20210113184526451](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113184526451.png)



![image-20210113184544331](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113184544331.png)

![image-20210113184800639](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113184800639.png)



 











##  常见面试题

l 简述节点流与处理流的区别

l 什么是序列化什么是反序列化

l 流的分类

 







#   进程与线程

## 实现多线程

###   进程

进程： 是正在运行的程序

- 是系统进行资源分配和调用的独立单位
- 每一个进程都有它自己的内存空间和系统资源



> 进程是操作系统中运行的一个任务(一个应用程序运行在一个进程中)
>
> 进程是一块包含了某些资源的内存区域，操作系统利用进程把他们的工作划分为一些功能单元
>
> 进程中包含的一个或多个执行单元称为线程，
>
> 进程还拥有一个私有的虚拟地址空间，该空间只能被他所包含的线程访问
>
> 线程只能属于一个进程并且它只能访问该进程所拥有的资源，当操作系统创建一个线程后，该进程会自动申请一个主线程
>
> 一个进程至少包含一个线程



###  线程

是进程中的单个顺序控制流， 是一条执行路径

- 单线程：一个进程如果只有一条执行路径，则称为单线程程序
- 多线程：一个进程如果有多条执行路径， 则称为多线程程序

举例:

> 记事本程序
>
> 扫雷程序

> 一个线程是进程的一个顺序执行单元
>
> 同类的多个线程共享一块内存空间和一组系统资源，线程本身有一个供程序执行时的堆栈
>
> 一个进程中可以包含多个线程

**线程的使用场合**

 线程通常用于在一个程序中需要同步完成的多个任务情况，我们可以将每个任务定义为一个线程，使得他们统一 一起工作

也可以使用单线程完成，但是多线程可以更快，比如下载文件

 

### 多线程的实现方式

#### 继承Thread类



**方式1： 继承Thread类**

- **定义一个类MyThread继承Thread类**
- **在MyThread类中重写run()方法**
- **创建MyThread类的对象**
- **启动线程**

![image-20210113201112122](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113201112122.png)

Thread是线程类，其每一个实例表示一个可以并发运行的线程，我们可以通过继承该类并重写run方法来定义一个具体的线程，其实重写run方法的目的就是定义该线程要执行的逻辑，启动线程调用start方法而非run方法，start方法会将当前线程纳入线程调度，使得当前线程可以并发运行，当线程获取时间片段后，会自动执行run方法中的逻辑

```java
public class MyThread extends Thread{
    //run方法里面写  要执行的代码
    @Override
    public void run() {
        for (int i=0;i<=100;i++){
            System.out.println(i);
        }
    }

    
    
public static void main(String[] args) {
        //创建两个线程
        Thread t1 = new MyThread();
        Thread t2 = new MyThread();
        //启动线程
        t1.start();
        t2.start();
    }
}
```

#### 实现Runnable接口



**方式2： 实现Runnable接口**

- **定义一个类MyRunnable实现Runnable接口**
- **在MyRunnable类中重写run()方法**
- **创建MyRunnable类的对象**
- **创建Thread类的对象， 把MyRunnable对象作为构造方法的参数**
- **启动线程**

![image-20210113205027975](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113205027975.png)

![image-20210113205303647](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113205303647.png)



> 相比继承Thread类，实现Runnable接口的好处
>
> - 避免了Java单继承的局限性
> - 适合多个相同程序的代码去处理同一个资源的情况，把线程和程序的代码、数据有效分离，较好的体现了面向对象的设计思想





**实现Runnable接口**

实现Runnable接口并重写run方法来定义线程，然后再创建线程的时候将Runnable的实例传入Thread并启动线程

这样做的好处在于可以将线程与线程要执行的任务分离减少耦合。同时java是单继承的，定义一个类实现Runnable接口这样的作法可以更好的区实现其他父类或接口，因为接口可以多实现

```java
public class TestRunnable implements Runnable {
    @Override
    public void run() {
        for (int i=1;i<=100;i++){
            System.out.println(i);
        }
    }

    
    
    
    public static void main(String[] args) {
        TestRunnable tr = new TestRunnable();
        Thread t1 = new Thread(tr);
        t1.start();
        Thread t2 = new Thread(tr);
        t2.start();
    }
}

```

 









### 设置和获取线程名称

####  获取线程的信息

>  **t.getName() 获取当前线程名称**

> **t.getID（）获取当前线程ID**

![image-20210113202350636](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113202350636.png)

```java
Thread t1 = new Thread();
System.out.println(t1.getName());
System.out.println(t1.getId());

Thread t2 = new Thread();
System.out.println(t2.getName());
System.out.println(t2.getId());

Thread t3 = new Thread("我是查水表的");
System.out.println(t3.getName());
System.out.println(t3.getId());

```

> **Thread.currentThread() – 获取当前线程**

```java
public static void main(String[] args) {
    System.out.println("运行Main方法的线程："+Thread.currentThread());
    testCurrent();
    Thread t1 = new Thread(){
        @Override
        public void run() {
            System.out.println("运行t1的线程是："+Thread.currentThread());
            testCurrent();
        }
    };
    t1.start();
}
public static void testCurrent(){
    System.out.println("运行testCurrent方法的线程是："+Thread.currentThread());
}

```

### 线程调度

![image-20210113203123645](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113203123645.png)

![image-20210113202643886](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113202643886.png)

![image-20210113203101915](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113203101915.png)

**线程的优先级**

线程的切换是由线程调度控制的，我们无法通过代码来干涉，但是我们可以通过提高优先级来最大程度的改善线程获得时间片的机率

线程的优先级划分为10个等级 1-10 其中1最低 10最高

Int getPriority() -返回线程的优先级

Void stt Priority() -设置线程优先级

```java
//创建两个线程
Thread t1 = new MyThread();
Thread t2 = new MyThread();
System.out.println("t1的优先级"+t1.getPriority());
System.out.println("t2的优先级"+t2.getPriority());
t1.setPriority(10);
t2.setPriority(1);
//启动线程
t1.start();
t2.start();
```

### 线程控制

![image-20210113203324621](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113203324621.png)





####  Sleep 

Thread的静态方法sleep用于使当前线程进入阻塞状态

-Thread.sleep(long ms);

该方法会使得当先线程进入阻塞状态指定毫秒值，当阻塞指定毫秒后，当前线程会重新进入Runnable状态，等待分配之间片





​     ![image-20210102225804943](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102225804943.png)

 

```java
Thread t1 = new Thread(){
    @Override
    public void run() {
        for (int i=0;i<10;i++){
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
            System.out.println("你好在吗");
        }
    }
};
t1.start();

```





####   Join

> **Void join（）该方法用于等待当前线程结束**



```java
public static void main(String[] args) {
    //一个线程下载图片   另一个线程显示图片
    Thread t1 = new Thread(){
        @Override
        public void run() {
            for (int i=0;i<=10;i++){
                System.out.println("t1正在下载图片："+i*10+"%");
                try {
                    Thread.sleep(1000);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }

        }
    };
    t1.start();
    Thread t2 = new Thread(){
        @Override
        public void run() {
            System.out.println("t2等待t1图片下载完毕");
            try {
                t1.join();//等待t1线程全部执行完毕
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
            System.out.println("显示图片");
        }
    };
    t2.start();
}

```



####  setDaemon

守护线程与普通线程表现上没有什么区别，我们只需要通过Thread提供的方法设定即可

> **Void setDaemon(Boolean true) 当参数为true时，表示为守护线程**

**守护线程的特点**

当进程中只剩下守护线程时，所有守护线程强制终止， 但并不是立即终止

GC就是运行在一个守护线程上的

![image-20210113204246154](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113204246154.png)



####  Yield

Thread的静态方法

-static void yield()

该方法用于使当前线程主动让出此CPU的时间片，回到Runnable状态等待分配时间片

```
Thread t1 = new Thread(){
    @Override
    public void run() {
        System.out.println("t1开始跑步");
        for(int i=0;i<=400;i++){
            System.out.println("t1跑了"+i+"米");
            if (i==200){
                Thread.yield();
            }
        }
        System.out.println("t1跑完了");
    }
};
Thread t2 = new Thread(){
    @Override
    public void run() {
        System.out.println("t2开始跑步");
        for(int i=1;i<=400;i++){
            System.out.println("t2跑了"+i+"米");
        }
        System.out.println("t2跑完了");
    }
};
t1.start();
t2.start();
```

###  线程生命周期

要想实现多线程，必须再主线程中创建新的线程对象，任何线程一般具有五种状态：

创建，就绪，运行，阻塞，终止

![image-20210113204608572](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113204608572.png)



###  (了解 匿名内部类的方式创建线程)

通常我们可以通过匿名内部类的方式创建线程，使用该方式可以简化编写代码的复杂度

当一个线程仅需要一个实例时我们可以通过这种方式来进行创建

```java
//内部类创建线程
Thread t = new Thread(){
    @Override
    public void run() {
        for(int i=0;i<1000;i++){
            System.out.println(i);
        }
    }
};
t.start();
Runnable r = new Runnable() {
    @Override
    public void run() {
        for(int i=0;i<1000;i++){
            System.out.println(i);
        }
    }
};
Thread t1 = new Thread(r);
t1.start();

```

### 并发

多个线程“同时运行”只是我们感官上的一种表现，事实上线程是并发运行的

系统将时间划分为很多时间片段(时间片)，尽可能均匀的分配给每一个线程，获取时间片的线程被CPU调用运行，其他线程全部等待，微观上走走停停，宏观上都在运行，这种现象叫并发，并发不是绝对意义上的同时运行。



## 线程同步

###  案例 卖票

 ![image-20210113210017129](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113210017129.png)

![image-20210113210350282](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113210350282.png)

![image-20210113210408205](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113210408205.png)

**卖票案例的思考**

![image-20210113211358320](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113211358320.png)

### 卖票案例数据安全问题的解决

![image-20210113211643543](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113211643543.png)



### 同步代码块

![image-20210113212116169](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113212116169.png)

![image-20210113212338543](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113212338543.png)

![image-20210113211939535](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113211939535.png)



### 同步方法

![image-20210113212908633](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113212908633.png)



![image-20210113212341810](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113212341810.png)

![image-20210113212835055](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113212835055.png)

![image-20210113212936705](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113212936705.png)





### ----------------

**锁机制 synchronized**

多个线程并发读写同一个资源时，会产生线程并发安全问题

-多线程共享的实例变量

-多线程共享的静态公共变量

 

若想解决线程安全问题，需要将异步操作，改变为同步操作

-异步操作：多线程并发执行，相当于各干各的

-同步操作：有先后的执行顺序，相当于你干完我在再干



### 线程安全的类

![image-20210113213243450](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113213243450.png)

### Lock锁

![image-20210113213750790](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113213750790.png)

![image-20210113213945048](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113213945048.png)



## 生产者消费者

### 生产者消费者模式概述

![image-20210113214134110](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113214134110.png)

![image-20210113214200440](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113214200440.png)

### 生产者消费者案例

![image-20210113214343431](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113214343431.png)

![image-20210113215334050](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113215334050.png)

![image-20210113215319923](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113215319923.png)

![image-20210113214601689](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113214601689.png)

![image-20210113214641838](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113214641838.png)

![image-20210113214740651](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113214740651.png)





















## 面试题总结

l 创建线程几种方式 你更常用哪一种 为什么

l sleep()和wait()区别

l 什么是并发

l 进程跟线程的区别

l 简述锁机制

Java提供了一种内置的锁机制来支持原子性

Synchronized用法

每个java对象都可以用作一个实现同步的锁，线程进入同步代码块之前会自动获得锁，并且再退出代码块时自动释放锁







# 网络编程

## 网络编程入门

### 网络编程概述

![image-20210113220203683](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113220203683.png)

![image-20210113220237110](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113220237110.png)

### 网络编程三要素

![image-20210113220503085](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210113220503085.png)

### IP地址

![image-20210116110622247](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116110622247.png)

![image-20210116111043570](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116111043570.png)

### InetAddress的使用

![image-20210116111307651](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116111307651.png)

![image-20210116111510097](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116111510097.png)

### 端口

![image-20210116111653491](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116111653491.png)

### 协议

![image-20210116111800957](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116111800957.png)

![image-20210116111927893](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116111927893.png)



![image-20210116111919559](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116111919559.png)



## UDP通信程序

### UDP通信原理

![image-20210116112139940](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116112139940.png)

### UDP发送数据

**datagram socket(数据报套接字)**

![image-20210116112904050](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116112904050.png)

![image-20210116112748091](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116112748091.png)

![image-20210116112844717](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116112844717.png)



### UDP接收数据

![image-20210116113604490](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116113604490.png)



![image-20210116113501672](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116113501672.png)

![image-20210116113541997](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116113541997.png)



### UDP通信程序练习

![image-20210116113747972](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116113747972.png)

![image-20210116114007444](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116114007444.png)

 ![image-20210116114206777](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210116114206777.png)



## TCP通信程序

 ![image-20210117164217491](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210117164217491.png)

### TCP发送数据

![image-20210125103743018](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125103743018.png)

![image-20210125103550113](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125103550113.png)

###   **TCP接收数据**

![image-20210125105924056](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125105924056.png)



![image-20210125105838466](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125105838466.png)

 

### TCP通信程序练习

#### -------------1

![image-20210125121014008](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125121014008.png)

![image-20210125110250755](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125110250755.png)

![image-20210125110521824](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125110521824.png)

#### -------------2

![image-20210125121005722](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125121005722.png)

![image-20210125114928622](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125114928622.png)

![image-20210125120712275](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125120712275.png)



#### -------------3

![image-20210125120952590](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125120952590.png)

![image-20210125121231196](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125121231196.png)

![image-20210125121423710](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125121423710.png)



#### ------------ 4

 ![image-20210125190537027](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125190537027.png)

![image-20210125203915613](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125203915613.png)

![image-20210125203339730](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125203339730.png)

####  -------------5

 ![image-20210125212247942](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125212247942.png)



![image-20210125211225216](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125211225216.png)

// 备注  自定义结束标记

![image-20210125213028657](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125213028657.png)

![image-20210125211748074](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125211748074.png)



![image-20210125211805723](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125211805723.png)

####  -------------6 

![image-20210125213848393](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125213848393.png)

![image-20210125214727518](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125214727518.png)

![image-20210125214817747](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125214817747.png)



![image-20210125214422084](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125214422084.png)

![image-20210125214934988](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125214934988.png)

![image-20210125214632769](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125214632769.png)

![image-20210125214908107](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125214908107.png)



# Lambda表达式

## 函数式编程思想概述

![image-20210125215455817](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125215455817.png)

## 体验Lambda表达式

![image-20210125215547284](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125215547284.png)

![image-20210125220041687](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125220041687.png)



![image-20210125215644851](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125215644851.png)

![image-20210125220016464](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125220016464.png)

## Lambda表达式的标准格式



![image-20210125220526939](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125220526939.png)

![image-20210125220612087](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210125220612087.png)

## Lambda表达式的练习

### 抽象方法无参无返回值

![image-20210126100748259](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126100748259.png)

![image-20210126101200366](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126101200366.png)

![image-20210126101244074](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126101244074.png)

![image-20210126101213343](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126101213343.png)



### 抽象方法带参无返回值

![image-20210126101501249](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126101501249.png)

![image-20210126101551452](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126101551452.png)

![image-20210126101846725](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126101846725.png)



### 抽象方法带参带返回值

![image-20210126101933947](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126101933947.png)

![image-20210126102022250](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126102022250.png)

![image-20210126102253385](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126102253385.png)

## Lambda表达式的省略模式

![image-20210126102419120](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126102419120.png)

![image-20210126102423532](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126102423532.png)

![image-20210126103202004](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126103202004.png)

![image-20210126103224558](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126103224558.png)

![image-20210126103318204](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126103318204.png)

![image-20210126103234435](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126103234435.png)



![image-20210126103352063](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126103352063.png)

## Lambda表达式的注意事项

![image-20210126103719345](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126103719345.png)

![image-20210126104037088](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126104037088.png)

![image-20210126104104008](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126104104008.png)



## Lambda表达式和匿名内部类的区别

![image-20210126104212193](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126104212193.png)

![image-20210126104223866](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126104223866.png)

![image-20210126104252989](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126104252989.png)



 ![image-20210126104511710](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126104511710.png)

![image-20210126104633317](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126104633317.png)



![image-20210126104320354](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126104320354.png)

![image-20210126105020527](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126105020527.png)



# 接口组成更新

## 接口组成更新概述

![image-20210126105531325](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126105531325.png)

## 接口中默认方法

![image-20210126110438766](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126110438766.png)

![image-20210126105805260](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126105805260.png)

![image-20210126105834327](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126105834327.png)

![image-20210126110115584](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126110115584.png)

![image-20210126110459259](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126110459259.png)



## 接口中静态方法

![image-20210126110838924](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126110838924.png)



![image-20210126112002774](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126112002774.png)

![image-20210126111607525](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126111607525.png)

![image-20210126111553899](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126111553899.png)

![image-20210126111825089](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126111825089.png)



![image-20210126112019313](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126112019313.png)

## 接口中私有方法

![image-20210126113101480](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126113101480.png)



![image-20210126112409063](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126112409063.png)

![image-20210126113048516](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126113048516.png)





![image-20210126113003376](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126113003376.png)

![image-20210126112457797](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126112457797.png)

![image-20210126112528146](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126112528146.png)



# 方法引用

## 体验方法引用

![image-20210126113435617](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126113435617.png)

![image-20210126113458850](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126113458850.png)

![image-20210126114336337](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126114336337.png)

![image-20210126113528398](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126113528398.png)

## 方法引用符

![image-20210126114635451](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126114635451.png)

![image-20210126114656887](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126114656887.png)

![image-20210126114811670](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126114811670.png)



## Lambda表达式支持的方法引用

![image-20210126114942694](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126114942694.png)

### 引用类方法

![image-20210126115026660](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126115026660.png)

![image-20210126115139023](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126115139023.png)

![image-20210126115440440](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126115440440.png)



### 引用对象的实例方法

![image-20210126144430380](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126144430380.png)

![image-20210126144630297](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126144630297.png)

![image-20210126144700333](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126144700333.png)

![image-20210126145054545](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126145054545.png)



### 引用类的实例方法

![image-20210126145204017](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126145204017.png)

![image-20210126145247853](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126145247853.png)

![image-20210126145608865](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126145608865.png)



### 引用构造器

![image-20210126145648551](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126145648551.png)



![image-20210126145831449](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126145831449.png)

![image-20210126145821125](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126145821125.png)

![image-20210126150134638](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126150134638.png)

  



# 函数式接口

## 函数式接口概述

![image-20210126150734258](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126150734258.png)

![image-20210126150652326](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126150652326.png)

## 函数式接口作为方法的参数

![image-20210126151130486](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126151130486.png)

![image-20210126151110110](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126151110110.png)



## 函数式接口作为方法的返回值

![image-20210126151831212](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126151831212.png)



![image-20210126151803345](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126151803345.png)



![image-20210126151736983](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126151736983.png)



## 常用的函数式接口

![image-20210126151911182](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126151911182.png)

### Supplier接口

![image-20210126152032245](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126152032245.png)

![image-20210126152322848](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126152322848.png)



![image-20210126152349360](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126152349360.png)

![image-20210126152618418](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126152618418.png)



### Consumer接口

![image-20210126152836090](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126152836090.png)

![image-20210126153501003](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126153501003.png)



![image-20210126153547914](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126153547914.png)

![image-20210126153924113](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126153924113.png)

![image-20210126154049755](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126154049755.png)



### Predicate接口

![image-20210126154340183](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126154340183.png)

![image-20210126154826930](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126154826930.png)

![image-20210126155230078](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126155230078.png)



![image-20210126155333249](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126155333249.png)

![image-20210126155510355](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126155510355.png)



### Function接口

![image-20210126155708926](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126155708926.png)

![image-20210126160210453](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126160210453.png)

![image-20210126160201393](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126160201393.png)

![image-20210126160323829](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126160323829.png)



![image-20210126160457089](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126160457089.png)

![image-20210126160919133](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126160919133.png)



# Stream流

## 体验Stream流

![image-20210126173904006](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126173904006.png)

![image-20210126173444928](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126173444928.png)

![image-20210126173456039](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126173456039.png)

![image-20210126173820276](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126173820276.png)



## Stream流的生成方式

![image-20210126174153350](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126174153350.png)

![image-20210126174446359](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126174446359.png)



![image-20210126174520279](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126174520279.png)

![image-20210126174831753](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126174831753.png)



## Stream流的常见中间操作方法

![image-20210126180049317](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126180049317.png)

![image-20210126180035451](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126180035451.png)

![image-20210126180302741](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126180302741.png)

![image-20210126180655499](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126180655499.png)

![image-20210126180955702](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126180955702.png)

![image-20210126181203308](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126181203308.png)

![image-20210126181231484](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126181231484.png)

![image-20210126181523756](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126181523756.png)

![image-20210126181607202](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126181607202.png)

![image-20210126181936905](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126181936905.png)



## Stream流的常见终结操作方法

![image-20210126182028751](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126182028751.png)

![image-20210126182129941](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126182129941.png)



## Stream流的练习

![image-20210126182242829](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126182242829.png)



![image-20210126182621328](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126182621328.png)

![image-20210126182638317](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126182638317.png)

![image-20210126182810824](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126182810824.png)



## Stream流的收集操作

![image-20210126183138123](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126183138123.png)



![image-20210126183243821](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126183243821.png)

![image-20210126183350436](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126183350436.png)

![image-20210126183703540](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126183703540.png)











# 枚举

枚举可以实现一个或多个接口,使用enum定义的枚举类默认继承了java.lang.Enum类而不是直接继承Object，因此不能再继承别的类

```java
public class DateTest {
    private static final int hours = 24;
    private static final int days = 365;
    private static final int months = 12;
}
```

上述常量定义这种方式并没有什么错误，但是它存在许多不足，在类型安全或者方便性来讲没有很大的好处，我们更提倡使用枚举来声明

```java
public enum SeasonEnum {

    SPRING,SUMMER,FALL,WINTER

}
```

```java
switch (SeasonEnum.SPRING){
    case SPRING:
        System.out.println("春天来了");
}
```

#   反射

## 类加载器

### 类加载

![image-20210126184205633](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126184205633.png)



![image-20210126184350781](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126184350781.png)



### 类加载器

![image-20210126184832886](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126184832886.png)

![image-20210126185004039](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126185004039.png)













##  反射

### 反射的概述

![image-20210126185210291](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126185210291.png)

![image-20210126185257562](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126185257562.png)



在编译时不确定哪个类被加载，而在程序运行时才加载，探知，使用

JAVA反射机制是在运行状态中，

对于任意一个类，都能够知道这个类的所有的属性和方法；

对于任意一个对象，都能够调用它的任意一个方法和属性，这种动态获取的信息以及动态调用对象的方法和功能，我们称之为java语言的反射

 ![image-20210102230155811](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210102230155811.png)

### 获取Class类的对象

![image-20210126185455858](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126185455858.png)

![image-20210126185550580](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126185550580.png)

![image-20210126185600667](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126185600667.png)

![image-20210126185831584](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126185831584.png)



### 反射获取构造方法并使用

![image-20210126191202498](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126191202498.png)



![image-20210126191104574](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126191104574.png)



### 反射获取构造方法并使用练习

![image-20210126191602814](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126191602814.png)

![image-20210126191538483](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126191538483.png)





![image-20210126192138243](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126192138243.png)

![image-20210126192126263](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126192126263.png)



### 反射获取成员变量并使用

![image-20210126220508842](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126220508842.png)

![image-20210126220523298](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126220523298.png)

### 反射获取成员变量并使用练习



![image-20210126220942540](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126220942540.png)

![image-20210126221002191](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126221002191.png)

### 反射获取成员方法并使用

![image-20210126221433089](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126221433089.png)

![image-20210126221636312](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126221636312.png)

![image-20210126221658658](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126221658658.png)





### 反射获取成员方法并使用练习

![image-20210126221724432](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126221724432.png)

![image-20210126221828087](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126221828087.png)

![image-20210126221933417](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126221933417.png)



## 反射练习

![image-20210126223104340](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126223104340.png)

1

![image-20210126222228018](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126222228018.png)



2

![image-20210126222731781](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126222731781.png)

![image-20210126223001561](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126223001561.png)

![image-20210126223016571](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126223016571.png)





# 模块化

## 模块化概述

![image-20210126223430618](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126223430618.png)

![image-20210126223529131](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126223529131.png)



## 模块的基本使用

![image-20210126224239356](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126224239356.png)



## 模块服务的使用

![image-20210126224345933](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126224345933.png)

![image-20210126224652297](C:\Users\Hanpengr\AppData\Roaming\Typora\typora-user-images\image-20210126224652297.png)



> 例子 机制：https://www.bilibili.com/video/BV18J411W7cE?p=410



















































