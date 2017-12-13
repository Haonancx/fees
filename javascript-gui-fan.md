# JavaScript 规范

### 缩进

使用 soft tab（4个空格）。

**例如**

```js
var x = 1,
y = 1;
if (x < y) {
x += 10;
} else {
x += 1;
}
```

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

```js
/* var declaration */
var x = 1;
/* expression statement */
x++;
/* do-while */
do {
x++;
} while (x < 10);
```

---

### 空格

以下几种情况不需要空格：

* 对象的属性名后
* 前缀一元运算符后
* 后缀一元运算符前
* 函数调用括号前
* 无论是函数声明还是函数表达式，'\('前不要空格
* 数组的'\['后和'\]'前
* 对象的'{'后和'}'前
* 运算符'\('后和'\)'前

以下几种情况需要空格：

* 二元运算符前后
* 三元运算符'?:'前后
* 代码块'{'前
* 下列关键字前：`else`,`while`,`catch`,`finally`
* 下列关键字后：`if`,`else`,`for`,`while`,`do`,`switch`,`case`,`try`,`catch`,`finally`,`with`,`return`,`typeof`
* 单行注释'//'后（若单行注释和代码同行，则'//'前也需要），多行注释'\*'后
* 对象的属性值前
* for循环，分号后留有一个空格，前置条件如果有多个，逗号后留一个空格
* 无论是函数声明还是函数表达式，'{'前一定要有空格
* 函数的参数之间

**例如**

```js
// not good
var a = {
b :1
};
// good
var a = {
b: 1
};
// not good
++ x;
y ++;
z = x?1:2;
// good
++x;
y++;
z = x ? 1 : 2;
// not good
var a = [ 1, 2 ];
// good
var a = [1, 2];
// not good
var a = ( 1+2 )*3;
// good
var a = (1 + 2) * 3;
// no space before '(', one space before '{', one space between function parameters
var doSomething = function(a, b, c) {
// do something
};
// no space before '('
doSomething(item);
// not good
for(i=0;i<6;i++){
x++;
}
// good
for (i = 0; i < 6; i++) {
x++;
}
```

---

### 空行

以下几种情况需要空行：

* 变量声明后（当变量声明在代码块的最后一行时，则无需空行）
* 注释前（当注释在代码块的第一行时，则无需空行）
* 代码块后（在函数调用、数组、对象中则无需空行）
* 文件最后保留一个空行

**例如**

```js
// need blank line after variable declaration
var x = 1;


// not need blank line when variable declaration is last expression in the current block
if (x >= 1) {
var y = x + 1;
}


var a = 2;


// need blank line before line comment
a++;


function b() {
// not need blank line when comment is first line of block
return a;
}


// need blank line after blocks
for (var i = 0; i < 2; i++) {
if (true) {
return false;
}


continue;
}


var obj = {
foo: function() {
return 1;
},


bar: function() {
return 2;
}
};


// not need blank line when in argument list, array, object
func(
2,
function() {
a++;
},
3
);


var foo = [
2,
function() {
a++;
},
3
];


var foo = {
a: 2,
b: function() {
a++;
},
c: 3
};
```

---

### 换行

换行的地方，行末必须有','或者运算符；

以下几种情况不需要换行：

* 下列关键字后：`else`,`catch`,`finally`
* 代码块'{'前

以下几种情况需要换行：

* 代码块'{'后和'}'前
* 变量赋值后

**例如**

```js
// not good
var a = {
b: 1
, c: 2
};


x = y
? 1 : 2;


// good
var a = {
b: 1,
c: 2
};


x = y ? 1 : 2;
x = y ?
1 : 2;


// no need line break with 'else', 'catch', 'finally'
if (condition) {
...
} else {
...
}


try {
...
} catch (e) {
...
} finally {
...
}


// not good
function test()
{
...
}


// good
function test() {
...
}


// not good
var a, foo = 7, b,
c, bar = 8;


// good
var a,
foo = 7,
b, c, bar = 8;
```

---

### 单行注释

双斜线后，必须跟一个空格；

缩进与下一行代码保持一致；

可位于一个代码行的末尾，与代码间隔一个空格。

**例如**

```js
if (condition) {
    // if you made it here, then all security checks passed
    allowed();
}

var zhangsan = 'zhangsan'; // one space after code
```

---

### 多行注释

最少三行, '\*'后跟一个空格，具体参照右边的写法；

建议在以下情况下使用：

* 难于理解的代码段
* 可能存在错误的代码段
* 浏览器特殊的HACK代码
* 业务逻辑强相关的代码

```js
/*
 * one space after '*'
 */
var x = 1;
```

---

