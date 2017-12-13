# JavaScript 规范

### 缩进

使用 soft tab（4个空格）。

**例如**

`var x = 1,`

`y = 1;`

`if (x < y) {`

`x += 10;`

`} else {`

`x += 1;`

`}`

---

### 单行长度

不要超过80，但如果编辑器开启word wrap可以不考虑单行长度。

---

### 分号

以下几种情况后需加分号：

* 变量声明
* 表达式
* return
* throw
* break
* continue
* do-while

**例如**

`/* var declaration */`

`var x = 1;`





`/* expression statement */`

`x++;`





`/* do-while */`

`do {`

`x++;`

`} while (x < 10);`

