---
title: "Html入门笔记"
date: 2019-10-22T18:32:05+08:00
draft: false
---

# Html入门笔记1

1. HTML是？
   * 上个世纪90年代由欧洲核子研究中心的物理学家蒂姆·伯纳斯-李（Tim Berners-Lee）发明，叫李爵士就行。

2. HTML 起手？
   * ! + tab 或 回车
  ![看图](/image/html/html-start.png)

3. 常用的表章节的标签?
   * article : 表示独立结构，可独立分配或复用
   * section : 新的章节
   * header  : 头部
   * footer  : 脚部
   * main    : 主要内容
   * aside   : 旁支内容
  
4. 全局属性有哪些?
   * 我使用的chrome大概有这些，后面有常见的再补充
   ``` css
    display: block;
    font-size: 2em;
    margin-block-start: 0.67em;
    margin-block-end: 0.67em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    font-weight: bold;
  ```

5. 常用的内容标签有哪些？
   * ol+li 
      - ordered list 有序列表
      - ol里只能有li

   * ul+li  
      - unordered list 无序列表

   * dl+dt+dd  
      - dl:description list 
      - dt:term：一个概念，被描述的词
      - dd:描述的东西

   * pre
      - html默认为多个空格、回车会被缩为1个空格
      - pre标签会保留多个空格、回车，一般< code >会用

   * hr
      - 分割线

   * br
      - 换行

   * a
      - target属性，默认为当前页面
      - "_self" ：当前页面
      - "_blank"：新窗口
      - "_parent"：当前框架里打开，如果没有，同_self
      - "_top"：加载的响应成完整的，原来的窗口，取消所有其它frame。

   * em
      - 语气强调重要性

   * strong
      - 本身很重要

