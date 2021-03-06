---
title: "浅谈MVC"
date: 2020-01-10T09:43:50+08:00
draft: false
---

### 1.MVC 的三个对象。

MVC是一种架构设计模式，没有严格的定义

    M: Model(数据模型)负责操作所有数据
     V: View(试图)负责所有UI界面
     C: Controller(控制器)负责其他
    
![mvc](/image/mvc/mvc.jpg)

个人理解就是：

(V)点击事件 → (C)控制器做出相应操作 → (M)更新数据

(V)输入数据 → (M)更新数据，通知(C) → (C)控制器相应操作 → (M)更新数据

### 2.EventBus 的部分 API 和作用
根据方方老师的讲解和谷歌了下，没找到详解，大概理解event bus 是一个概念词：事件总栈的意思。把所有的API都聚合在一起调用。
打印了$(window)，解释了部分这几天用上的API

    children 获得匹配元素集合中每个元素的子元素，选择器选择性筛选。
     siblings 获得匹配元素集合中每个元素的兄弟元素,可以提供一个可选的选择器。
     appendTo 将匹配的元素插入到目标元素的最后面
     on 监听事件
     trigger 触发事件

![mvc](/image/mvc/eventBus.png)

### 3.表驱动编程？

简单讲是指用查表的方法获取值。

数值不多的时候我们可以用逻辑语句(if 或case)的方法来获取值,但随着数值的增多逻辑语句就会越来越长,此时表驱动法的优势就显现出来。

例如:根据月份获取天数
```javascript
let mouth;
if (mouth === 1) {
    return 31;
} else if (mouth === 2) {
    return 28;
}else if (mouth === 3) {
    return 31;
}
// ...
else if (mouth === 12) {
    return 31;
} else {
    return 0;
}

// 改良后

let array = [31,28,31,30,31,30,31,31,30,31,30,31];
let days = array[month - 1];
```

优点：

    更加易读和直白；
     用数据代替逻辑，容易维护；
     可以把表中的数据存放在文件中，运行时读取，减少代码体量。数据变更时只需要修改文件；
     降低复杂度。

### 4.我是如何理解模块化的？

对模块理解的并不是很多，之前没有用到过，联想到之前开发小程序时候，一个JS里写了N个函数，还有很多相同的代码，想想就头大

模块大概意思是：

  - 将一个复杂的程序依据一定的规则(规范)封装成几个块(文件), 并进行组合在一起
  - 块的内部数据与实现是私有的, 只是向外部暴露一些接口(方法)与外部其它模块通信

优点：

  - 避免命名冲突(减少命名空间污染)
  - 更好的分离, 按需加载
  - 更高复用性
  - 高可维护性
