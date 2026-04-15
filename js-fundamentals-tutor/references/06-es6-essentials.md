# ES6 基础

ES6（2015 年发布）给 JavaScript 带来了许多现代化语法，初学者需要掌握以下核心内容。

## 1. let 与 const

比 `var` 更安全：

```javascript
let count = 0;      // 可变
count = 1;

const MAX = 100;    // 不可重新赋值
// MAX = 200;       // 报错
```

## 2. 模板字符串

用反引号 `` ` `` 包裹字符串，可以嵌入变量：

```javascript
let name = "小明";
let age = 18;

// 旧写法
let old = "我叫" + name + "，今年" + age + "岁";

// 新写法
let neu = `我叫${name}，今年${age}岁`;
console.log(neu);
```

## 3. 解构赋值

从数组或对象中快速提取值：

```javascript
// 数组解构
let [a, b] = [1, 2];
console.log(a);  // 1

// 对象解构
let person = { name: "小明", age: 18 };
let { name, age } = person;
console.log(name);  // "小明"
```

## 4. 展开运算符

三个点 `...` 可以把数组或对象"展开"：

```javascript
let arr1 = [1, 2];
let arr2 = [...arr1, 3, 4];
console.log(arr2);  // [1, 2, 3, 4]

let obj1 = { a: 1 };
let obj2 = { ...obj1, b: 2 };
console.log(obj2);  // { a: 1, b: 2 }
```

## 5. 数组常用高阶方法

```javascript
let nums = [1, 2, 3, 4];

// map：对每个元素做转换，返回新数组
let doubled = nums.map(n => n * 2);
console.log(doubled);  // [2, 4, 6, 8]

// filter：按条件筛选
let evens = nums.filter(n => n % 2 === 0);
console.log(evens);    // [2, 4]

// find：找到第一个符合条件的元素
let first = nums.find(n => n > 2);
console.log(first);    // 3
```
