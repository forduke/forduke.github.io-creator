---
title: "JS 对象基本用法"
date: 2019-11-26T17:47:09+08:00
draft: false
---

### 一、声明对象的两种语法

```javascript
let obj1 = {
	'name': 'zhang',
	'age': 24
}
// 或
let obj2 = new Object({
	'name': 'zhang',
	'age': 24,
  'gf': undefined
})
```
### 二、如何删除对象的key(属性),value(值)

```javascript
delete obj1.name
// 或
delete obj1['name']
```
- 即可删除obj的xxx的key
- 重复使用delete不会报错，会返回true

判断object是否包含相关key

```javascript
'name' in obj2 === true
```

object某个key的value可能为undefined，所以不能只通过判断value是否存在，来判断key是否存在

```javascript
obj1.gf === undefined
'gf' in obj1 && obj1.gf === undefined
// 对比
obj2.gf === undefined
'gf' in obj2 && obj2.gf === undefined
```
![对比图](/image/js-object/img-1.png)

### 三、如何查看对象的key(属性)

```javascript
// 查看自身所有属性
Object.keys(obj1)

// 查看自身+共有属性
console.dir(obj1)

// 判断一个属性是自身的还是共有的
obj1.hasOwnProperty('toString')
```

![查看属性](/image/js-object/img-2.png)

### 四、如何修改或增加对象的key(属性)

1. 直接赋值
   
```javascript
let obj = {
  'name': 'zhang'
}
```

2. 批量赋值
   
```javascript
Object.assign(obj, {
  'age': 24,
  gender: 'name'
})
```

![赋值](/image/js-object/img-3.png)

3. 关于公共属性的增加这里不是很熟练，先留个坑

### 五、'name' in obj和obj.hasOwnProperty('name') 的区别

![属性](/image/js-object/img-4.png)

- 'name' in obj

判断 obj 对象里是否有 name 这个属性，包括原型链中的属性

- obj.hasOwnProperty('name')

只判断 obj 自身是否有 name 这个属性，不包括原型链

![比较](/image/js-object/img-5.png)

