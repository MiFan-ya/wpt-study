一、 CSS多列等高如何实现？
1. 使用负margin-bottom和正padding-bottom。
float: left;
margin-bottom: -9999px;
padding-bottom: 9999px;
2. 模仿table布局：table元素中的table-cell元素默认就是等高的
总div{ display: table;table-layout: fixed;}
分div{display: table-cell;}
3. 利用flex布局：
总div{ display: flex;}
分div{ flex: 1;}

二、经常遇到的浏览器的兼容性有哪些？原因，解决方法是什么，常用 hack 的技巧
1. png24位的图片在iE6浏览器上出现背景解决方案：做成PNG8，也可以引用一段脚本处理。
2. 浏览器默认的margin和padding不同解决方案：加一个全局的*{margin:0;padding:0;}来统一。
3. IE6双边距bug：在IE6下，如果对元素设置了浮动，同时又设置了margin-left或margin-right，margin值会加倍。
解决：在float的标签样式控制中加入_display:inline;将其转化为行内属性。(_这个符号只有ie6会识别)
4. 渐进识别的方式，从总体中逐渐排除局部。
首先，巧妙的使用"\9"这一标记，将IE游览器从所有情况中分离出来。
接着，再次使用"+"将IE8和IE7、IE6分离开来，这样IE8已经独立识别。
.bb{
background-color:#f1ee18;/*所有识别*/
.background-color:#00deff\9;/*IE6、7、8识别*/
+background-color:#a200ff;/*IE6、7识别*/
_background-color:#1e0bd1;/*IE6识别*/
}
5. 超链接访问过后hover样式就不出现了，被点击访问过的超链接样式不再具有hover和active了解决方法：改变CSS属性的排列顺序L-V-H-A 。
