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

##### **例如**

`<!DOCTYPE html>`

`<html>`

`...`

`</html>`

### lang属性

根据HTML5规范：

> 应在html标签上加上lang属性。这会给语音工具和翻译工具帮助，告诉它们应当怎么去发音和翻译。

更多关于`lang`属性的说明[在这里](http://www.w3.org/html/wg/drafts/html/master/semantics.html#the-html-element)；在sitepoint上可以查到[语言列表](http://reference.sitepoint.com/html/lang-codes)；

但sitepoint只是给出了语言的大类，例如中文只给出了zh，但是没有区分香港，台湾，大陆。而微软给出了一份更加 [详细的语言列表](http://msdn.microsoft.com/en-us/library/ms533052%28v=vs.85%29.aspx)，其中细分了zh-cn, zh-hk, zh-tw。

##### **例如**

`<!DOCTYPE html>`

`<html lang="en-us">`

`...`

`</html>`

### 字符编码

通过声明一个明确的字符编码，让浏览器轻松、快速的确定适合网页内容的渲染方式，通常指定为'UTF-8'。

##### **例如**

`<!DOCTYPE html>`

`<html>`

`<head>`

`<meta charset="UTF-8">`

`</head>`

`...`

`</html>`



### IE兼容模式

用`<meta>`标签可以指定页面应该用什么版本的IE来渲染；

如果你想要了解更多，请点击[这里](http://stackoverflow.com/questions/6771258/whats-the-difference-if-meta-http-equiv-x-ua-compatible-content-ie-edge-e)；

不同doctype在不同浏览器下会触发不同的渲染模式（[这篇文章](https://hsivonen.fi/doctype/)总结的很到位）。

##### **例如**

`<!DOCTYPE html>`

`<html>`

`    <head>`

`        <meta http-equiv="X-UA-Compatible" content="IE=Edge">`

`    </head>`

`    ...`

`</html>`

