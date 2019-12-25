---
title: "初学jQuery的一些理解"
date: 2019-12-25T17:26:17+08:00
draft: false
---

之前只是了解一点jQuery的用法，都是现用现查

---

### 1.jQuery 如何获取元素

- $('*') // 选择所有元素，除非它自己使用，否则不建议使用，速度极慢
- $('class') // 选择类名相同的元素
- $('element') // 选择所有符合的DOM节点的标签
- $('#id') // 选择第一个该id的DOM元素
- $('input[name=first]') // 选择name属性等于first的input元素

```javascript
// 还有部分jQuery特有的选择器，暂时不太了解
```

---

### 2.jQuery 的链式操作是怎样的

选中网页元素以后，可以对它进行一系列操作，并且所有操作可以连接在一起，以链条的形式写出来

```javascript
  $('div').find('#test').addClass('red');
```

分解开来，就是下面这样：

```javascript
  $('div')  //找到div元素
    .find('#test')  //选择其中id为test的元素
    .addClass('red')   //新增class为red
```

还有一个回退操作，没用过，以后再写上

```javascript
  .end()
```

---

### 3.jQuery 如何创建元素

创建新元素只要把新元素直接传入jQuery的构造函数就行了：

```javascript
  $('<p>Hello</p>');
  $('<li class="new">new list item</li>');
  $('ul').append('<li>list item</li>');
```

---

### 4.jQuery 如何移动元素

移动元素。

第一种方法是使用.insertAfter()，把div元素移动p元素后面：

```javascript
  $('div').insertAfter($('p'));
```

第二种方法是使用.after()，把p元素加到div元素前面：

```javascript
  $('p').after($('div'));
```

这两种方法的看上去差不多。实际上它们那返回的元素不一样。第一种方法返回div元素，第二种方法返回p元素。

使用这种模式的操作方法，一共有四对：

```javascript
  .insertAfter()和.after()：在现存元素的外部，从后面插入元素
    
  .insertBefore()和.before()：在现存元素的外部，从前面插入元素
    
  .appendTo()和.append()：在现存元素的内部，从后面插入元素
    
  .prependTo()和.prepend()：在现存元素的内部，从前面插入元素
```

---

以上部分参考阮一峰老师教程，博客只个人练习用
      
      
