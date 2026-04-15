# DOM 操作简介

## 1. 什么是 DOM

DOM（Document Object Model，文档对象模型）是把 HTML 页面映射成一棵"树"，JavaScript 可以通过 DOM 来**读取和修改**网页内容。

比喻：HTML 是一颗圣诞树，DOM 就是树上的每个装饰品。JS 可以帮你找到某个装饰品，然后换掉它或者给它加闪烁灯。

## 2. 获取元素

```javascript
// 通过 id 获取（唯一）
let box = document.getElementById("box");

// 通过类名获取（返回集合）
let items = document.getElementsByClassName("item");

// 通过标签名获取
let divs = document.getElementsByTagName("div");

// 更现代的方式：CSS 选择器
let btn = document.querySelector("#submit");        // 第一个匹配的
let links = document.querySelectorAll("a");          // 所有匹配的
```

## 3. 修改内容和样式

```javascript
let title = document.getElementById("title");

// 修改文字内容
title.textContent = "新标题";

// 修改 HTML 内容
title.innerHTML = "<span style='color:red'>新标题</span>";

// 修改样式
title.style.color = "blue";
title.style.fontSize = "24px";
```

## 4. 事件监听

响应用户操作（点击、输入等）：

```javascript
let btn = document.getElementById("myBtn");

btn.addEventListener("click", function () {
  alert("按钮被点击了！");
});
```

## 5. 完整小例子

```html
<p id="msg">你好</p>
<button id="btn">点我</button>

<script>
  document.getElementById("btn").addEventListener("click", () => {
    document.getElementById("msg").textContent = "欢迎学习 JavaScript！";
  });
</script>
```
