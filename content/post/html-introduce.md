---
title: "HTML入门笔记"
date: 2019-10-22T18:32:05+08:00
draft: false
---

1. HTML 是？

   - 上个世纪 90 年代由欧洲核子研究中心的物理学家蒂姆·伯纳斯-李（Tim Berners-Lee）发明，叫李爵士就行。

2. HTML 起手？

   - ! + tab 或 回车
     ![看图](/image/html/html-start.png)

3. 常用的表章节的标签?

   - article : 表示独立结构，可独立分配或复用
   - section : 新的章节
   - header : 头部
   - footer : 脚部
   - main : 主要内容
   - aside : 旁支内容

4. 全局属性有哪些?

   - class

     - 类名

   - contenteditable

     - 可编辑内容；
     - head 标签的内容不可见，但 style 标签可以放在 body 内，加上这个属性就可以编辑样式

   - hidden

     - 隐藏标签内容

   - id

     - id 如果重复出现，不会报错，尽量不用；
     - #xxx [ id=xxx ] ；
     - id 可以在 JS 里直接使用，xxx.style.border = '1px solid red' ；
     - id 不能和关键字（window.xxx）相同，否则无效

   - style

     - 行内样式，参考优先级：

   - tabindex

     - 控制键盘 tab 操作的顺序，响应键盘事件
     - 0 是最后顺序，-1 是跳过、不访问

   - title
     - 鼠标放在内容上的提示

1) 常用的内容标签有哪些？

   - ol+li

     - ordered list 有序列表
     - ol 里只能有 li

   - ul+li

     - unordered list 无序列表

   - dl+dt+dd

     - dl:description list
     - dt:term：一个概念，被描述的词
     - dd:描述的东西

   - pre

     - html 默认为多个空格、回车会被缩为 1 个空格
     - pre 标签会保留多个空格、回车，一般< code >会用

   - hr

     - 分割线

   - br

     - 换行

   - a

     - target 属性，默认为当前页面
     - "\_self" ：当前页面
     - "\_blank"：新窗口
     - "\_parent"：当前框架里打开，如果没有，同\_self
     - "\_top"：加载的响应成完整的，原来的窗口，取消所有其它 frame。

   - em

     - 语气强调重要性

   - strong
     - 本身很重要
