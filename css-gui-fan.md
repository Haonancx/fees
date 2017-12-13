### 缩进

使用soft tab（4个空格）。

**例如**

`.element {`

`position: absolute;`

`top: 10px;`

`left: 10px;`

`border-radius: 10px;`

`width: 50px;`

`height: 50px;`

`}`



### 分号

每个属性声明末尾都要加分号。

**例如**

`.element {`

`    width: 20px;`

`    height: 20px;`

`    background-color: red;`

`}`



### 空格

以下几种情况不需要空格：

* 属性名后
* 多个规则的分隔符','前
* `!important`'!'后
* 属性值中'\('后和'\)'前
* 行末不要有多余的空格

以下几种情况需要空格：

* 属性值前
* 选择器 '&gt;', '+', '~'前后
* '{'前
* `!important`'!'前
* `@else`前后
* 属性值中的','后
* 注释'/\*'后和'\*/'前

**例如**



`/* not good */`

`.element {`

`    color :red! important;`

`    background-color: rgba(0,0,0,.5);`

`}`

``

`/* good */`

`.element {`

`    color: red !important;`

`    background-color: rgba(0, 0, 0, .5);`

`}`

``

`/* not good */`

`.element ,`

`.dialog{`

`    ...`

`}`

``

`/* good */`

`.element,`

`.dialog {`

``

`}`

``

`/* not good */`

`.element>.dialog{`

`    ...`

`}`

``

`/* good */`

`.element > .dialog{`

`    ...`

`}`

``

`/* not good */`

`.element{`

`    ...`

`}`

``

`/* good */`

`.element {`

`    ...`

`}`

``

`/* not good */`

`@if{`

`    ...`

`}@else{`

`    ...`

`}`

``

`/* good */`

`@if {`

`    ...`

`} @else {`

`    ...`

`}`



