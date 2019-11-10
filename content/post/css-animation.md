---
title: "浏览器渲染 和 css animation"
date: 2019-11-04T17:16:49+08:00
draft: false
---

### 一、浏览器渲染原理个人理解

CSSOM 树和 DOM 树合并成渲染树，然后用于计算每个可见元素的布局，并输出给绘制流程，将像素渲染到屏幕上。

- DOM 树与 CSSOM 树合并后形成渲染树。
- 渲染树只包含渲染网页所需的节点。
- 布局计算每个对象的精确位置和大小。
- 最后一步是绘制，使用最终渲染树将像素渲染到屏幕上。

  第一步是让浏览器将 DOM 和 CSSOM 合并成一个“渲染树”，网罗网页上所有可见的 DOM 内容，以及每个节点的所有 CSSOM 样式信息。

![树图](/image/animation/animation-1.png)

为构建渲染树，浏览器大体上完成了下列工作：

- 从 DOM 树的根节点开始遍历每个可见节点。
- 某些节点不可见（例如脚本标记、元标记等），因为它们不会体现在渲染输出中，所以会被忽略。
  某些节点通过 CSS 隐藏，因此在渲染树中也会被忽略，例如，上例中的 span 节点---不会出现在渲染树中，---因为有一个显式规则在该节点上设置了“display: none”属性。
  对于每个可见节点，为其找到适配的 CSSOM 规则并应用它们。
- 发射可见节点，连同其内容和计算的样式。

简要概述浏览器完成的步骤：

1. 处理 HTML 标记并构建 DOM 树。
2. 处理 CSS 标记并构建 CSSOM 树。
3. 将 DOM 与 CSSOM 合并成一个渲染树。
4. 根据渲染树来布局，以计算每个节点的几何信息。
5. 将各个节点绘制到屏幕上。

---

### css transition 过渡

**作用**

补充中间帧

**语法**

- transition: 属性名 时长 过渡方式 延迟
- transition: left 200ms linear
- 可以用逗号分隔两个不同属性
- transition: left 200ms, top 400ms
- 可以用 all 代表所有属性
- transition: all 200ms
- 过渡方式有: linear | ease | ease-in | ease-out | ease-in-out | cubic-bezier 等

**注意：不是所有属性都能过渡**

- display:none=>block 不能过渡
- 一般改成 visibility:hidden=>visible
- 过渡必须有起始

---

### css animation

**语法**

**animation**: 时长|过渡方式|延迟|次数|方向|填充模式|是否暂停|动画名

- 时长: 1S 或 1000ms
- 过渡方式: 跟 transition 取值一样，如 linear
- 次数: 3 或 2.4 或 infinite
- 方向: normal | reverse | alternate | alternate-reverse
- 填充模式: none | forwards | backwards | both
- 是否暂停: running | paused

**注意：不是所有属性都能过渡**

- display:none=>block 不能过渡
- 一般改成 visibility:hidden=>visible
- 过渡必须有起始
