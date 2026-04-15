# 数组与对象

## 1. 数组（Array）

数组是用来存储**一组有序数据**的容器。

```javascript
let fruits = ["苹果", "香蕉", "橙子"];

// 访问元素（索引从 0 开始）
console.log(fruits[0]);  // "苹果"
console.log(fruits[1]);  // "香蕉"

// 修改元素
fruits[1] = "葡萄";

// 数组长度
console.log(fruits.length);  // 3
```

### 常用数组方法

```javascript
let nums = [1, 2, 3];

nums.push(4);        // 末尾添加 → [1,2,3,4]
nums.pop();          // 末尾移除 → [1,2,3]
nums.unshift(0);     // 开头添加 → [0,1,2,3]
nums.shift();        // 开头移除 → [1,2,3]

// 遍历数组
for (let i = 0; i < nums.length; i++) {
  console.log(nums[i]);
}
```

## 2. 对象（Object）

对象是用来存储**一组键值对**的数据结构。

```javascript
let person = {
  name: "小明",
  age: 18,
  isStudent: true
};

// 访问属性：点语法
console.log(person.name);  // "小明"

// 访问属性： bracket 语法
console.log(person["age"]); // 18

// 修改和新增
person.age = 19;
person.city = "北京";

// 删除属性
delete person.isStudent;
```

## 3. 数组与对象的组合

实际开发中常见"数组里放对象"：

```javascript
let students = [
  { name: "小明", score: 85 },
  { name: "小红", score: 92 },
  { name: "小刚", score: 78 }
];

console.log(students[1].name);  // "小红"
```
