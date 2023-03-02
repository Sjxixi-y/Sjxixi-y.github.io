# **Java基本知识**

## 三大平台

- ### JavaSE
    标准平台。JavaEE、JavaME基础。

- ### JavaEE
    企业平台。在SE的基础上封装了很多便于开发的包。

- ### JavaME
    微型平台。主要时开发移动端、嵌入式等。

## JDK、JRE、JVM

- ### JDK
    Java开发环境。内部集成了很多开发环境，比如Javac等。
    也包括JRE。

- ### JRE
    Java运行平台。主要有JVM和一些基础包，主要时负责运行。
    程序。

- ### JVM
    Java虚拟机。用于运行被编译完成的.class文件。

## 虚拟机
    模拟计算机的一种应用程序，与外界环境隔离。比如在
    Windows操作系统中装了Linux虚拟机，就可以使用Linux系
    统进行一些测试。

## Java程序运行过程
    .java(源码)文件在javac.exe工具编译后变成.class(字节码),
    再交给JVM运行，将结果呈现给用户。

## Java跨平台原理
    源文件被编译为中立的字节码文件，再交给JVM运行。