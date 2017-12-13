### 语法

* 缩进使用soft tab（4个空格）；
* 嵌套的节点应该缩进；
* 在属性上，使用双引号，不要使用单引号；
* 属性名全小写，用中划线做分隔符；
* 不要在自动闭合标签结尾处使用斜线（[HTML5 规范](http://dev.w3.org/html5/spec-author-view/syntax.html#syntax-start-tag) 指出他们是可选的）；
* 不要忽略可选的关闭标签，例：`</li>`和`</body>`。

##### **例如**

`<!DOCTYPE html>`

`<html>`

`<head>`

`<title>Page title</title>`

`</head>`

`<body>`

`<img src="images/company_logo.png" alt="Company"/>`

`<h1 class="hello-world">Hello, world!</h1>`

`</body>`

`</html>`



### HTML5 doctype

在页面开头使用这个简单地 doctype 来启用标准模式，使其在每个浏览器中尽可能一致的展现；

虽然 doctype 不区分大小写，但是按照惯例，doctype 大写 （[关于html属性，大写还是小写](http://stackoverflow.com/questions/15594877/is-there-any-benefits-to-use-uppercase-or-lowercase-letters-with-html5-tagname)）。



`<!DOCTYPE html>`

`<html>`

`	...`

`</html>`

