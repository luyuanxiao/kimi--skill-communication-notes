# 函数

## 1. 什么是函数

函数是一段**可重复使用的代码块**，用来完成特定任务。

比喻：函数就像一台榨汁机，你放入水果（参数），它输出果汁（返回值）。

## 2. 函数声明

```javascript
// 声明一个函数：计算两数之和
function add(a, b) {
  return a + b;
}

// 调用函数
let result = add(3, 5);
console.log(result);  // 8
```

- `function`：关键字
- `add`：函数名
- `a, b`：参数（形式参数）
- `return`：返回值，函数执行后交给调用者的结果

## 3. 函数表达式

把函数赋值给变量：

```javascript
const multiply = function (a, b) {
  return a * b;
};

console.log(multiply(4, 5));  // 20
```

## 4. 箭头函数（ES6 简洁写法）

```javascript
// 基本写法
const subtract = (a, b) => {
  return a - b;
};

// 如果只有一条 return 语句，可以省略大括号和 return
const square = (x) => x * x;

console.log(subtract(10, 3));  // 7
console.log(square(4));        // 16
```

## 5. 参数默认值

```javascript
function greet(name = "游客") {
  console.log("你好，" + name);
}

greet();           // "你好，游客"
greet("小明");      // "你好，小明"
```

## 6. 作用域初步

函数内部声明的变量，函数外部访问不到：

```javascript
function demo() {
  let local = "我在函数内部";
  console.log(local);
}

demo();            // 正常输出// console.log(local); // 报错！外部访问不到
```
