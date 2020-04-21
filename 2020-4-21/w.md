css:
1. 标准css盒子模型，低版本IE的盒子模型有什么不同？
盒子模型有两种，IE盒模型（border-box）和W3C标准盒模型（content-box）
盒模型都是由四个部分组成的，分别是margin、border、padding和content。
区别在于：
标准盒模型的width，height 只包含内容，不包含border和padding。
IE盒模型的width，height 属性包含了border、padding和content。
可以通过修改元素的box-sizing属性来改变元素的盒模型。默认w3c
2. CSS选择符有哪些
id选择器、类选择器、伪类选择器、标签选择器、兄弟选择器（li~a）、相邻兄弟选择器（li+a）、
后代选择器、相邻后代选择器（>）、伪元素选择器（::before）、通配符选择器、属性选择器
3. ::before 和:after 中双冒号和单冒号有什么区别？解释一下这 2 个伪元素的作用。
单冒号表示伪类，双冒号表示伪元素。为了兼容已有的伪元素的写法，在一些浏览器中也可以使用单冒号来表示伪元素。 伪类一般匹配的是元素的一些特殊状态，如hover、link等，而伪元素一般匹配的特殊的位置，比如after、before等。