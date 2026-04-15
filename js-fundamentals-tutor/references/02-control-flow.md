# 控制流：条件与循环

## 1. 条件语句 if / else if / else

根据条件决定执行哪段代码：

```javascript
let score = 85;

if (score >= 90) {
  console.log("优秀");
} else if (score >= 60) {
  console.log("及格");
} else {
  console.log("不及格");
}
```

### 三元运算符（简化版 if/else）
```javascript
let result = score >= 60 ? "及格" : "不及格";
```

## 2. switch 语句

当变量有多个离散值时使用：

```javascript
let day = 1;

switch (day) {
  case 1:
    console.log("星期一");
    break;
  case 2:
    console.log("星期二");
    break;
  default:
    console.log("其他");
}
```

## 3. for 循环

重复执行一段代码指定次数：

```javascript
// 打印 0 到 4
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

执行过程：
1. `let i = 0` — 初始化
2. `i < 5` — 判断条件，为 true 则执行循环体
3. `console.log(i)` — 执行代码
4. `i++` — 更新变量，回到第 2 步

## 4. while 循环

当条件为 true 时持续执行：

```javascript
let n = 0;
while (n < 3) {
  console.log(n);
  n++;
}
```

## 5. break 与 continue

- `break`：立即跳出整个循环
- `continue`：跳过当前轮，进入下一轮

```javascript
for (let i = 0; i < 5; i++) {
  if (i === 2) {
    continue;  // 跳过 2
  }
  if (i === 4) {
    break;     // 到 4 时直接退出
  }
  console.log(i);  // 输出 0, 1, 3
}
```
