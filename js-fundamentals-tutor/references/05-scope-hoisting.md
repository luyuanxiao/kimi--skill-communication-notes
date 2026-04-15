# 作用域与变量提升

## 1. 作用域（Scope）

作用域就是变量能生效的范围。

比喻：作用域就像房间。你在自己房间里（函数内）写的便签，客厅（函数外）的人是看不到的。

### 全局作用域

在函数外部声明的变量，整个程序都能访问：

```javascript
let globalVar = "我是全局变量";

function test() {
  console.log(globalVar);  // 可以访问
}
```

### 局部作用域（函数作用域）

在函数内部声明的变量，只能在函数内访问：

```javascript
function test() {
  let localVar = "我是局部变量";
  console.log(localVar);
}

// console.log(localVar);  // 报错！
```

### 块级作用域

用 `let` 和 `const` 在 `{}` 内声明的变量，只在 `{}` 内有效：

```javascript
if (true) {
  let blockVar = "只在 if 里有效";
  console.log(blockVar);
}

// console.log(blockVar);  // 报错！
```

## 2. 变量提升（Hoisting）

JS 的一个特殊行为：用 `var` 声明的变量，声明会被"提升"到作用域顶部。

```javascript
console.log(a);  // undefined（不会报错，但值为 undefined）
var a = 10;
```

实际上等价于：

```javascript
var a;
console.log(a);  // undefined
a = 10;
```

### 为什么推荐用 let/const？

```javascript
console.log(b);  // 报错！Cannot access 'b' before initialization
let b = 20;
```

`let` 和 `const` 虽然也有提升，但会形成"暂时性死区"，在声明前访问会直接报错，行为更可预测。
