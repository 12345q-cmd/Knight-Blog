---
title: JavaScript 核心用法
cover: https://img-baofun.zhhainiao.com/pcwallpaper_ugc/static/bd26f78c344b3ad6afef7b12b1421227.jpg?x-oss-process=image%2fresize%2cm_lfit%2cw_1920%2ch_1080
tags:
  - 教程
categories: 技术
---
以下是 JavaScript 核心用法的结构化总结：

---

### **一、基础概念**

1. **变量声明**  
   - `var`：函数作用域（存在变量提升）
   - `let/const`：块级作用域（推荐，`const`用于常量）

2. **数据类型**  
   - **原始类型**：`String`、`Number`、`Boolean`、`Null`、`Undefined`、`Symbol`、`BigInt`  
   - **引用类型**：`Object`（含 `Array`、`Function`、`Date`等）

---

### **二、核心语法**

1. **函数**  

   ```javascript
   // 函数声明
   function add(a, b) { return a + b; }

   // 箭头函数（无this绑定）
   const add = (a, b) => a + b;
   ```

2. **对象与类**  

   ```javascript
   // 对象字面量
   const obj = { key: "value", method() {} };

   // Class语法
   class Person {
     constructor(name) { this.name = name; }
     greet() { console.log(this.name); }
   }
   ```

---

### **三、异步编程**

1. **Promise**  

   ```javascript
   fetch(url)
     .then(response => response.json())
     .catch(error => console.error(error));
   ```

2. **Async/Await**  

   ```javascript
   async function fetchData() {
     const data = await fetch(url);
     console.log(data);
   }
   ```

---

### **四、常用操作**

1. **数组方法**  
   - `map()`：映射新数组  
   - `filter()`：过滤元素  
   - `reduce()`：累计计算  

2. **解构与扩展**  

   ```javascript
   const [a, b] = [1, 2];          // 数组解构
   const { x, y } = { x: 1, y: 2 }; // 对象解构
   const arr = [...oldArr, newItem]; // 扩展运算符
   ```

---

### **五、模块化**

```javascript
// 导出
export const PI = 3.14;
export default function() {};

// 导入
import { PI } from './math.js';
import myFunc from './module.js';
```

---

### **六、最佳实践**

1. 使用 `===` 严格相等比较  
2. 避免全局变量污染  
3. 错误处理（`try/catch`或`.catch()`）  
4. 使用ESLint + Prettier统一代码风格  

---

### **七、典型应用场景**

- **DOM操作**：`document.querySelector()`  
- **事件监听**：`element.addEventListener()`  
- **API请求**：`fetch()` / `axios`  
- **状态管理**：Vuex/Redux（框架相关）  

---

> JavaScript的灵活性既是优势也是挑战，建议结合TypeScript提升大型项目维护性。
