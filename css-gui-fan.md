### 命名

* 类名使用小写字母，以中划线分隔
* id采用驼峰式命名
* scss中的变量、函数、混合、placeholder采用驼峰式命名

**例如**

`/* class */`

`.element-content {`

`...`

`}`

`  
`

`/* id */`

`#myDialog {`

`...`

`}`

`  
`

`/* 变量 */`

`$colorBlack: #000;`

`  
`

`/* 函数 */`

`@function pxToRem($px) {`

`...`

`}`

`/* 混合 */`

`@mixin centerBlock {`

`...`

`}`

`/* placeholder */`

`%myDialog {`

`...`

`}`

### 颜色

颜色16进制用小写字母；

颜色16进制尽量用简写。

**例如**

`/* not good */`

`.element {`

`color: #ABCDEF;`

`background-color: #001122;`

`}`

`  
`

`/* good */`

`.element {`

`color: #abcdef;`

`background-color: #012;`

`}`

### 属性简写

属性简写需要你非常清楚属性值的正确顺序，而且在大多数情况下并不需要设置属性简写中包含的所有值，所以建议尽量分开声明会更加清晰；

`margin`和`padding`相反，需要使用简写；

常见的属性简写包括：

* `font`
* `background`
* `transition`
* `animation`

**例如**

`/* not good */`

`.element {`

`transition: opacity 1s linear 2s;`

`}`

`  
`

`/* good */`

`.element {`

`transition-delay: 2s;`

`transition-timing-function: linear;`

`transition-duration: 1s;`

`transition-property: opacity;`

`}`

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

`/* good */`

`.element {`

`...`

`}`

`.dialog {`

`color: red;`

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

### 注释

注释统一用'/\* \*/'（scss中也不要用'//'），具体参照右边的写法；

缩进与下一行代码保持一致；

可位于一个代码行的末尾，与代码间隔一个空格。

**例如**

`/* Modal header */`

`.modal-header {`

`...`

`}`

`  
`

`/*`

`* Modal header`

`*/`

`.modal-header {`

`...`

`}`

`  
`

`.modal-header {`

`/* 50px */`

`width: 50px;`

`color: red; /* color red */`

`}`

### 媒体查询

尽量将媒体查询的规则靠近与他们相关的规则，不要将他们一起放到一个独立的样式文件中，或者丢在文档的最底部，这样做只会让大家以后更容易忘记他们。

**例如**

`.element {`

`    ...`

`}`

``

`.element-avatar{`

`    ...`

`}`

``

`@media (min-width: 480px) {`

`    .element {`

`        ...`

`    }`

``

`    .element-avatar {`

`        ...`

`    }`

`}`

### 引号

最外层统一使用双引号；

url的内容要用引号；

属性选择器中的属性值需要引号。

**例如**

`.element:after {`

`content: "";`

`background-image: url("logo.png");`

`}`

`li[data-type="single"] {`

`...`

`}`

### 属性声明顺序

相关的属性声明按右边的顺序做分组处理，组之间需要有一个空行。

**例如**

`.declaration-order {`

`display: block;`

`float: right;`

`  
`

`position: absolute;`

`top: 0;`

`right: 0;`

`bottom: 0;`

`left: 0;`

`z-index: 100;`

`  
`

`border: 1px solid #e5e5e5;`

`border-radius: 3px;`

`width: 100px;`

`height: 100px;`

`  
`

`font: normal 13px "Helvetica Neue", sans-serif;`

`line-height: 1.5;`

`text-align: center;`

`  
`

`color: #333;`

`background-color: #f5f5f5;`

`  
`

`opacity: 1;`

`}`

`// 下面是推荐的属性的顺序`

`[`

`[`

`"display",`

`"visibility",`

`"float",`

`"clear",`

`"overflow",`

`"overflow-x",`

`"overflow-y",`

`"clip",`

`"zoom"`

`],`

`[`

`"table-layout",`

`"empty-cells",`

`"caption-side",`

`"border-spacing",`

`"border-collapse",`

`"list-style",`

`"list-style-position",`

`"list-style-type",`

`"list-style-image"`

`],`

`[`

`"-webkit-box-orient",`

`"-webkit-box-direction",`

`"-webkit-box-decoration-break",`

`"-webkit-box-pack",`

`"-webkit-box-align",`

`"-webkit-box-flex"`

`],`

`[`

`"position",`

`"top",`

`"right",`

`"bottom",`

`"left",`

`"z-index"`

`],`

`[`

`"margin",`

`"margin-top",`

`"margin-right",`

`"margin-bottom",`

`"margin-left",`

`"-webkit-box-sizing",`

`"-moz-box-sizing",`

`"box-sizing",`

`"border",`

`"border-width",`

`"border-style",`

`"border-color",`

`"border-top",`

`"border-top-width",`

`"border-top-style",`

`"border-top-color",`

`"border-right",`

`"border-right-width",`

`"border-right-style",`

`"border-right-color",`

`"border-bottom",`

`"border-bottom-width",`

`"border-bottom-style",`

`"border-bottom-color",`

`"border-left",`

`"border-left-width",`

`"border-left-style",`

`"border-left-color",`

`"-webkit-border-radius",`

`"-moz-border-radius",`

`"border-radius",`

`"-webkit-border-top-left-radius",`

`"-moz-border-radius-topleft",`

`"border-top-left-radius",`

`"-webkit-border-top-right-radius",`

`"-moz-border-radius-topright",`

`"border-top-right-radius",`

`"-webkit-border-bottom-right-radius",`

`"-moz-border-radius-bottomright",`

`"border-bottom-right-radius",`

`"-webkit-border-bottom-left-radius",`

`"-moz-border-radius-bottomleft",`

`"border-bottom-left-radius",`

`"-webkit-border-image",`

`"-moz-border-image",`

`"-o-border-image",`

`"border-image",`

`"-webkit-border-image-source",`

`"-moz-border-image-source",`

`"-o-border-image-source",`

`"border-image-source",`

`"-webkit-border-image-slice",`

`"-moz-border-image-slice",`

`"-o-border-image-slice",`

`"border-image-slice",`

`"-webkit-border-image-width",`

`"-moz-border-image-width",`

`"-o-border-image-width",`

`"border-image-width",`

`"-webkit-border-image-outset",`

`"-moz-border-image-outset",`

`"-o-border-image-outset",`

`"border-image-outset",`

`"-webkit-border-image-repeat",`

`"-moz-border-image-repeat",`

`"-o-border-image-repeat",`

`"border-image-repeat",`

`"padding",`

`"padding-top",`

`"padding-right",`

`"padding-bottom",`

`"padding-left",`

`"width",`

`"min-width",`

`"max-width",`

`"height",`

`"min-height",`

`"max-height"`

`],`

`[`

`"font",`

`"font-family",`

`"font-size",`

`"font-weight",`

`"font-style",`

`"font-variant",`

`"font-size-adjust",`

`"font-stretch",`

`"font-effect",`

`"font-emphasize",`

`"font-emphasize-position",`

`"font-emphasize-style",`

`"font-smooth",`

`"line-height",`

`"text-align",`

`"-webkit-text-align-last",`

`"-moz-text-align-last",`

`"-ms-text-align-last",`

`"text-align-last",`

`"vertical-align",`

`"white-space",`

`"text-decoration",`

`"text-emphasis",`

`"text-emphasis-color",`

`"text-emphasis-style",`

`"text-emphasis-position",`

`"text-indent",`

`"-ms-text-justify",`

`"text-justify",`

`"letter-spacing",`

`"word-spacing",`

`"-ms-writing-mode",`

`"text-outline",`

`"text-transform",`

`"text-wrap",`

`"-ms-text-overflow",`

`"text-overflow",`

`"text-overflow-ellipsis",`

`"text-overflow-mode",`

`"-ms-word-wrap",`

`"word-wrap",`

`"-ms-word-break",`

`"word-break"`

`],`

`[`

`"color",`

`"background",`

`"filter:progid:DXImageTransform.Microsoft.AlphaImageLoader",`

`"background-color",`

`"background-image",`

`"background-repeat",`

`"background-attachment",`

`"background-position",`

`"-ms-background-position-x",`

`"background-position-x",`

`"-ms-background-position-y",`

`"background-position-y",`

`"-webkit-background-clip",`

`"-moz-background-clip",`

`"background-clip",`

`"background-origin",`

`"-webkit-background-size",`

`"-moz-background-size",`

`"-o-background-size",`

`"background-size"`

`],`

`[`

`"outline",`

`"outline-width",`

`"outline-style",`

`"outline-color",`

`"outline-offset",`

`"opacity",`

`"filter:progid:DXImageTransform.Microsoft.Alpha(Opacity",`

`"-ms-filter:\\'progid:DXImageTransform.Microsoft.Alpha",`

`"-ms-interpolation-mode",`

`"-webkit-box-shadow",`

`"-moz-box-shadow",`

`"box-shadow",`

`"filter:progid:DXImageTransform.Microsoft.gradient",`

`"-ms-filter:\\'progid:DXImageTransform.Microsoft.gradient",`

`"text-shadow"`

`],`

`[`

`"-webkit-transition",`

`"-moz-transition",`

`"-ms-transition",`

`"-o-transition",`

`"transition",`

`"-webkit-transition-delay",`

`"-moz-transition-delay",`

`"-ms-transition-delay",`

`"-o-transition-delay",`

`"transition-delay",`

`"-webkit-transition-timing-function",`

`"-moz-transition-timing-function",`

`"-ms-transition-timing-function",`

`"-o-transition-timing-function",`

`"transition-timing-function",`

`"-webkit-transition-duration",`

`"-moz-transition-duration",`

`"-ms-transition-duration",`

`"-o-transition-duration",`

`"transition-duration",`

`"-webkit-transition-property",`

`"-moz-transition-property",`

`"-ms-transition-property",`

`"-o-transition-property",`

`"transition-property",`

`"-webkit-transform",`

`"-moz-transform",`

`"-ms-transform",`

`"-o-transform",`

`"transform",`

`"-webkit-transform-origin",`

`"-moz-transform-origin",`

`"-ms-transform-origin",`

`"-o-transform-origin",`

`"transform-origin",`

`"-webkit-animation",`

`"-moz-animation",`

`"-ms-animation",`

`"-o-animation",`

`"animation",`

`"-webkit-animation-name",`

`"-moz-animation-name",`

`"-ms-animation-name",`

`"-o-animation-name",`

`"animation-name",`

`"-webkit-animation-duration",`

`"-moz-animation-duration",`

`"-ms-animation-duration",`

`"-o-animation-duration",`

`"animation-duration",`

`"-webkit-animation-play-state",`

`"-moz-animation-play-state",`

`"-ms-animation-play-state",`

`"-o-animation-play-state",`

`"animation-play-state",`

`"-webkit-animation-timing-function",`

`"-moz-animation-timing-function",`

`"-ms-animation-timing-function",`

`"-o-animation-timing-function",`

`"animation-timing-function",`

`"-webkit-animation-delay",`

`"-moz-animation-delay",`

`"-ms-animation-delay",`

`"-o-animation-delay",`

`"animation-delay",`

`"-webkit-animation-iteration-count",`

`"-moz-animation-iteration-count",`

`"-ms-animation-iteration-count",`

`"-o-animation-iteration-count",`

`"animation-iteration-count",`

`"-webkit-animation-direction",`

`"-moz-animation-direction",`

`"-ms-animation-direction",`

`"-o-animation-direction",`

`"animation-direction"`

`],`

`[`

`"content",`

`"quotes",`

`"counter-reset",`

`"counter-increment",`

`"resize",`

`"cursor",`

`"-webkit-user-select",`

`"-moz-user-select",`

`"-ms-user-select",`

`"user-select",`

`"nav-index",`

`"nav-up",`

`"nav-right",`

`"nav-down",`

`"nav-left",`

`"-moz-tab-size",`

`"-o-tab-size",`

`"tab-size",`

`"-webkit-hyphens",`

`"-moz-hyphens",`

`"hyphens",`

`"pointer-events"`

`]`

`]`

