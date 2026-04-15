# 语法基础：变量、数据类型与运算符

## 1. 变量声明

JavaScript 使用 `let`、`const` 和 `var` 声明变量。初学者现阶段只需掌握 `let` 和 `const`：

- `let`：变量值可以修改
- `const`：常量，声明后不能重新赋值

```javascript
let age = 18;        // 可以变的量
age = 19;

const PI = 3.14;     // 不变的量
// PI = 3.15;        // 报错！
```

## 2. 数据类型

JS 中常见的 6 种基础类型：

| 类型 | 说明 | 示例 |
|------|------|------|
| `number` | 数字（整数、小数） | `10`, `3.14` |
| `string` | 字符串 | `"hello"`, `'world'` |
| `boolean` | 布尔值 | `true`, `false` |
| `undefined` | 未定义 | `let a;` 此时 `a` 的值 |
| `null` | 空值 | `let b = null;` |
| `object` | 对象（含数组） | `{name: "Tom"}`, `[1,2,3]` |

用 `typeof` 检查类型：

```javascript
console.log(typeof 100);        // "number"
console.log(typeof "abc");      // "string"
console.log(typeof true);       // "boolean"
```

## 3. 运算符

### 算术运算符
```javascript
let a = 10 + 5;   // 15  加
let b = 10 - 5;   // 5   减
let c = 10 * 5;   // 50  乘
let d = 10 / 5;   // 2   除
let e = 10 % 3;   // 1   取余
```

### 比较运算符
```javascript
console.log(5 == "5");   // true  （值相等，类型不同）
console.log(5 === "5");  // false （值和类型都相等）
console.log(5 != "5");   // false
console.log(5 !== "5");  // true
console.log(3 > 2);      // true
```

> 建议始终使用 `===` 和 `!==`，避免隐式类型转换带来的意外。

### 逻辑运算符
```javascript
console.log(true && false);  // false （与：两边都为 true 才为 true）
console.log(true || false);  // true  （或：有一个为 true 就为 true）
console.log(!true);          // false （非：取反）
```

## 4. 字符串基础

```javascript
let firstName = "李";
let lastName = "明";
let fullName = firstName + lastName;
console.log(fullName);           // "李明"
console.log(fullName.length);    // 2
console.log("Hello".toUpperCase()); // "HELLO"
```
