[1Java简介](#Java简介)

- [1.1Java发展史](#Java发展史)
- [1.2 Java语言特点](#Java语言特点)
- [1.3 Java三个版本](#1.3 Java三个版本)
- [1.4 Java程序运行机制](#1.4 Java程序运行机制)
- [1.5 Java 常见各名词解释](#1.5 Java 常见各名词解释)
- [1.6 JDK安装后个路径解释](#1.6 JDK安装后个路径解释)
- [1.6 JDK安装后个路径解释](#1.6 JDK安装后个路径解释)
- [1.7  第一个Java程序](#1.7  第一个Java程序)
- [小结](#小结)

## 1.Java简介

### 1.1  Java 发展史

Java最早是由SUN公司（已被Oracle收购）的[詹姆斯·高斯林](https://en.wikipedia.org/wiki/James_Gosling)（高司令，人称Java之父）开发的一种编程语言，最初被命名为Oak，目标是针对小型家电设备的嵌入式应用。互联网和浏览器的出现不仅给广大互联网用户带来了福音，也给Oak语言带来了新的生机，于是[詹姆斯·高斯林](https://en.wikipedia.org/wiki/James_Gosling)对Oak进行了小规模改造，在1995年以Java的名称正式发布，原因是Oak已经被人注册了，因此SUN注册了Java这个商标。随着互联网的高速发展，Java逐渐成为最重要的网络编程语言。

### 1.2 Java语言特点

1. 简单易学；
2. 面向对象（封装，继承，多态）；
3. 跨平台（一次编写，到处运行）；
4. 可靠性；
5. 安全性；
6. 支持多线程（ C++ 语言没有内置的多线程机制，因此必须调用操作系统的多线程功能来进行多线程程序设计，而 Java 语言却提供了多线程支持）；
7. 支持网络编程并且很方便（ Java 语言诞生本身就是为简化网络编程设计的，因此 Java 语言不仅支持网络编程而且很方便）；
8. 编译与解释并存；

### 1.3 Java三个版本

随着Java的发展，Sun将java分成三个不同的版本

- Java SE：整个Java技术的核心和基础，是J2ME和J2EE编程的基础
- Java EE：Java技术中应用最广泛的版本，提供企业应用开发解决方案
- Java ME：主要用于控制移动设备

### 1.4 Java程序运行机制

​    ![image-20201109224651668](https://gitee.com/xiezhr/image-learn-bed/raw/master/image/image-20201109224651668.png)

Java 语音既是编译型语言又是解释型语言。Java程序的执行过程必须经过先编译，后解释两个步骤。在编译步骤并不会生成特定的机器码，而是生成一种与平台无关的字节码（*.class文件），这种字节码不是可执行的，必须使用Java解释器来解释执行。负责解释执行字节码的是Java虚拟机（JVM）。

当使用Java编译器编译Java程序时，生成的是与平台无关的字节码，这些字节码不面向任何具体平台，只面向JVM。不同平台上的JVM都是不同的，但他们都提供了相同的接口。JVM是Java程序跨平台的关键部分，只要为不同平台实现了相应的虚拟机，编译后的Java字节码就可以在该平台上运行。字节码需要在不同平台上运行，JVM充当了转换器的作用。

### 1.5 Java 常见各名词解释

大家经常会听到jdk，jre这些名词，它们到底是什么？

- JDK （Java Development Kit） Java标准开发包，提供了编译、运行程序所需的各种工具和资源。包括Java编译器、Java运行时环境、Java类库等。

- JRE （Java Runtime Environment）  Java运行环境 。

- JVM  运行Java程序的虚拟机

  JRE 包含JVM，JVM是运行java程序核心虚拟机，而运行Java程序不仅需要核心虚拟机，还需要其他的类加载器、字节码校验器以及大量的基础类库。JRE除了包含JVM外，还包含运行Java程序的其他支持。

### 1.6 JDK安装后个路径解释

- bin：该路径下存放了JDK的各种工具命令，常用的javac、java等命令就存放在该路径下。
- db：该路径是安装Java DB 的路径
- jre：该路径下安装的就是运行Java程序所必须的jre环境
- lib：该路径下存放的是JDK工具命令的实际执行程序
- src.zip：该压缩文件里存放的就是Java所有核心类库的源代码
- README和LICENSE 说明性文档

### 1.7  第一个Java程序

我们来编写我们的第一个Java程序，输出 hello world !

打开文本编辑器输入如下代码

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}
```

在上述代码中

```java
public class Hello {
    ...
}
```

定义了一个类，这里的类名是Hello,大小写敏感。按照习惯，首字母`H`要大写。而花括号`{}`中间则是类的定义。

```java
public static void main(String[] args) {
        ...
    }
```

定义了一个main方法，()里的为参数，参数类型为String[] 参数名是args .`public`、`static`用来修饰方法，这里表示它是一个公开的静态方法，`void`是方法的返回类型，而花括号`{}`中间的就是方法的代码。

```java
System.out.println("Hello, world!");
```

具体的代码，代码的每一行用;结束

Java规定，某个类定义的`public static void main(String[] args)`是Java程序的固定入口方法，因此，Java程序总是从`main`方法开始执行。

最后，当我们把代码保存为文件时，文件名必须是`Hello.java`，而且文件名也要注意大小写，因为要和我们定义的类名`Hello`完全保持一致。

**小结：**

一个Java源码只能定义一个`public`类型的class，并且class名称和文件名要完全一致；

使用`javac`可以将`.java`源码编译成`.class`字节码；

使用`java`可以运行一个已编译的Java程序，参数是类名。