```
缩进
```

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

`.element {`

`width: 20px;`

`height: 20px;`

`background-color: red;`

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

`/* not good */`

`.element {`

`color :red! important;`

`background-color: rgba(0,0,0,.5);`

`}`

`  
`

`/* good */`

`.element {`

`color: red !important;`

`background-color: rgba(0, 0, 0, .5);`

`}`

`  
`

`/* not good */`

`.element ,`

`.dialog{`

`...`

`}`



`/* good */`

`.element,`

`.dialog {`

`}`



`/* not good */`

`.element>.dialog{`

`...`

`}`



`/* good */`

`.element > .dialog{`

`...`

`}`



`/* not good */`

`.element{`

`...`

`}`



`/* good */`

`.element {`

`...`

`}`



`/* not good */`

`@if{`

`...`

`}@else{`

`...`

`}`



`/* good */`

`@if {`

`...`

`} @else {`

`...`

`}`

### 空行

以下几种情况需要空行：

* 文件最后保留一个空行
* '}'后最好跟一个空行，包括scss中嵌套的规则
* 属性之间需要适当的空行，具体见
  [属性声明顺序](http://alloyteam.github.io/CodeGuide/#css-declaration-order)

**例如**

`/* not good */`

`.element {`

`...`

`}`

`.dialog {`

`color: red;`

`&:after {`

`...`

`}`

`}`

`  
`

`/* good */`

`.element {`

`...`

`}`

`  
`

`.dialog {`

`color: red;`

`  
`

`&:after {`

`...`

`}`

`}`

### 换行

以下几种情况不需要换行：

* '{'前

以下几种情况需要换行：

* '{'后和'}'前
* 每个属性独占一行
* 多个规则的分隔符','后

**例如**

`/* not good */`

`.element`

`{color: red; background-color: black;}`

`/* good */`

`.element {`

```
color: red;

background-color: black;
```

`}`

`/* not good */`

`.element, .dialog {`

```
...
```

`}`

`/* good */`

`.element,`

`.dialog {`

```
...
```

`}`

