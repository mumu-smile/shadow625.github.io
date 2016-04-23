---
layout:     post
title:      min stack-java
date:       2016-04-19 12:32:18
summary:    leetcode 155
categories: django
thumbnail: jekyll
author: "shadow"
tags:
 - leetcode
 - shadow grand
---

### 0X00:问题描述  
Design a stack that supports push, pop, top, and retrieving the minimum element in constant time.
it's an algorithm problem from the leetcode 155.  
### 0X01:minstack <br>
可以为每一个元素设置一个额外属性 min
每当进行一次压栈操作时，将压入的元素值与当前栈顶元素的min属性比较，求取最小的座位当前元素的min属性值
这样可以保证每次需要知道当前栈内最小元素的时候只需一次就可以求解得到，实现难度也较低<br>

### 0X02:具体结构分析 
首先在栈对象初始化时 创建一个entry对象 head 作为栈的第一个元素 也是栈的结束标志当entry的next为空时说明栈已到底<br>		
**1.push：**
输入一个元素x 使用entry（int x，entry next）构造一个entry对象 将x输入为她的num  next输入为她的next
剩下一个min 最小值的比较与存储 由于我们的数据结构 所以只需要比较栈顶第二个元素的min和当前元素（即栈顶元素）的num 取较小的即可 但是会存在一些特殊情况 当栈为空时 加入一个新元素  <br><br>
**2.pop ：**
希望弹出一个元素，则可以直接将当前的head变成head.next 当栈为空时则弹出0<br><br>
**3.getmin ：**
到了这个问题的核心了，这也是这个数据结构设计的原因所在，得到当前的最小值，即直接输出head.min。  

### 0x03:代码实现
哇咔咔 这里贴上我的JAVA代码实现，不知道为什么，速度要比C/C++ 快很多，大神知道的留个言，多谢指导。
