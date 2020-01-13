---
title: "Vue初接触"
date: 2020-01-13T15:17:00+08:00
draft: false
---

### 1.完整版和非完整版两个版本介绍

截取CDN上vue的最新版本
![完整版](/image/vue/vue.js.png)
完整版
![非完整版](/image/vue/vue.runtime.js.png)
非完整版

![区别](/image/vue/difference.png)
引用方方老师的总结，两者的区别，个人看来就是如果项目对客户体验非常看重，那么就使用非完整版，让工程师完成复杂的那部分。否则就是用完整版，简单粗暴。

### 2.template 和 render 怎么用

初学Vue这两者的区别还不是太理解，个人理解大概意思是从示例上可以看出，非完整版不能直接渲染数据，不能在template上加入html。
完整版就像官网给出的示例一样开发就可以，不需要render。
![是否需要编译器](/image/vue/vue-1.png)

template的用法我初步写了个demo，如下图
![template](/image/vue/vue-2.png)
![template效果](/image/vue/vue-3.png)

render会把template里的html编译
![render](/image/vue/vue-4.png)
![render-template](/image/vue/vue-5.png)
![render效果](/image/vue/vue-6.png)


### 3.教读者如何用 codesandbox.io 写 Vue 代码

[codesandbox官网](https://codesandbox.io/)
![codesandbox-1](/image/vue/codesandbox-1.png)
![codesandbox-2](/image/vue/codesandbox-2.png)
![codesandbox-3](/image/vue/codesandbox-3.png)
这里就可以正常使用了，网速慢可能不会第一时间展示出来，写好的代码可以在左上角的File菜单中Export to Zip导出来
