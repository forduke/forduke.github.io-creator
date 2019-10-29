---
title: "HTML重点标签"
date: 2019-10-24T10:17:03+08:00
draft: false
---

# HTML重点标签

### 1. a 标签的用法？
   
  **href**

  * 要打开的链接，为空的话会刷新页面，"#"不刷新、但会滚动到顶部
  * 网址：
    * https://google.com
    * http://google.com
    * //google.com  (无协议网址)
  
  * 路径
    * /a/b/c  ( 绝对路径，“/”我理解是服务器开项目后的根目录)
   	* a/b/c  （相对路径，在当前目录找）
   	* index.html 以及 ./index.html （在当前目录找）
  
  * 伪协议
   	* javascript:代码; （无效的点击事件，不会刷新页面，不会滚动到顶部）
   	* #xxx  （跳转到 id=xxx 的标签）
   	* mailto:邮箱 （打开邮件）
   	* tel:手机  （）

**target**

  * 在哪个窗口打开链接，默认为当前页面
  * 属性
    * "_blank" ：空白页面打开，新窗口
  	* "_top"：顶层窗口打开
  	* "_parent"：当前链接所在的 iframe 打开（谷歌不允许在iframe打开）
  	* "_self"：当前页面
  	* 也可以作为名字，每次跳转都会在相同窗口打开，window的name，iframe的name

**download**

  * 下载网页，一般用的不多

**rel=noopener**

  * 防止BUG，不知道是啥

### 2. img 标签的用法？
**img** 

  * 永远不要让图片变形！注意宽高比例
  * 发出get请求，展示一张图片，开发者工具可以检查出来
  * 属性
    * alt: 图片加载失败时显示的文字
    * height: 不是CSS，直接写数字，不写会自适应
    * width: 不是CSS，直接写数字，不写会自适应，
    * src:  可以用JS事件控制图片加载失败时的替换图片

  * 响应式
    * 可以在全局CSS样式上加，img{max-width:100%}

### 2. table 标签的用法？
**table** 

  用的不多，暂时我这么理解
  ```html
  <table>
    <thead></thead>
    <tbody>
        <th></th>
        <tr>
            <td></td>
        </tr>
    </tbody>
    <tfoot></tfoot>
  </table> 
  ```

**相关的样式**

  * table-layout: 间距
  * border-spacing: 边框距离
  * border-collapse: collapse; 边框之间是否合并



