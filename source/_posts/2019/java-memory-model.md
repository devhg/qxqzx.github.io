---
title: Java中的堆区、栈区、方法区
permalink: java-memory-model
date: 2019-09-15 20:33:09
toc: true
tags:
 - Java
categories:
 - Java基础
---

JAVA的JVM的内存可分为3个区：堆(heap)、栈(stack)和方法区(method)

<br>

### 栈区: 

1. **每个线程包含一个栈区**，栈中只保存方法中（不包括对象的成员变量）的**基础数据类型和自定义对象的引用(不是对象)**，对象都存放在堆区中
2. 每个栈中的数据(原始类型和对象引用)都是私有的，其他栈不能访问。
3. 栈分为3个部分：基本类型变量区、执行环境上下文、操作指令区(存放操作指令)



<br><br>

### 堆区: 

1. 存储的全部是对象实例，每个对象都包含一个与之对应的class的信息(class信息存放在方法区)。
2. **jvm只有一个堆区(heap)被所有线程共享**，堆中不存放基本类型和对象引用，只存放对象本身，几乎所有的**对象实例和数组**都在堆中分配。

<br><br>

### 方法区: 

1. 又叫静态区，跟堆一样，被所有的线程共享。它用于存储已经被虚拟机加载的类信息、常量、静态变量、即时编译器编译后的代码等数据。