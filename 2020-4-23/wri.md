CSS
1. 关于伪类 LVHA 的解释?
a标签有四种状态：链接访问前，访问后，鼠标悬浮，鼠标点击。：link ：visited ：hover：active。
当鼠标滑过a链接时，满足:link和:hover两种状态，要改变a标签的颜色，就必须将:hover伪类在:link伪类后面声明。
当鼠标点击激活a链接时，同时满足:link、:hover、:active三种状态，要显示a标签激活时的样式（:active），必须将:active声明放到:link和:hover之后。因此得出LVHA这个顺序。
2. CSS3新增伪类
（1）elem:nth-child(n)选中父元素下的第n个子元素，并且这个子元素的标签名为elem，n可以接受具体的数值，也可以接受函数。
（2）elem:nth-last-child(n)作用同上，不过是从后开始查找。
（3）elem:last-child选中最后一个子元素。
（4）elem:only-child如果elem是父元素下唯一的子元素，则选中之。
（5）elem:nth-of-type(n)选中父元素下第n个elem类型元素，n可以接受具体的数值，也可以接受函数。
（6）elem:first-of-type选中父元素下第一个elem类型元素。
（7）elem:last-of-type选中父元素下最后一个elem类型元素。
（8）elem:only-of-type如果父元素下的子元素只有一个elem类型元素，则选中该元素。
（9）elem:empty选中不包含子元素和内容的elem类型元素。
（10）elem:target选择当前活动的elem元素。
（11）:not(elem)选择非elem元素的每个元素。
（12）:enabled	控制表单控件的禁用状态。
（13）:disabled		控制表单控件的禁用状态。
 (14):checked单选框或复选框被选中。
3. display有哪些值？
block 块类型。换行显示，默认宽度为父元素宽度，可设置宽高。
none 元素不显示，并从文档流中移除。
inline 行内元素。同一行显示，默认宽度为内容宽度，不可设置宽高。
inline-block 同一行显示，默认宽度为内容宽度，可以设置宽高。
list-item 像块类型元素一样显示，并添加样式列表标记。
table 此元素会作为块级表格来显示。
inherit 规定应该从父元素继承display属性的值。
