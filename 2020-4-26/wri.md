1. 如何居中div
①水平居中：给div设置宽度，然后添加 margin：0 auto；
②文字水平居中，text-align:center 
③绝对定位的div居中：margin：auto；上下左右为0.
④div垂直居中
position: absolute; /*相对定位或绝对定位均可*/
top: 50%;
left: 50%;
transform: translate(-50%, -50%);
or
position: absolute;
top: 50%;
left: 50%;
margin-top,margin-left,设置为高，宽的一半。
⑤内容垂直居中
display: flex;
align-items: center; /*垂直居中*/
justify-content: center; /*水平居中*/
2. position的值relative和absolute 定位原点
absolute：找到绝对定位元素的一个position的值不为static的祖先元素，然后相对于这个祖先元素的paddingbox来定位，也就是说在计算定位距离的时候，padding的值也要算进去。
relative：相对于元素本身的正常位置进行定位。
fixed：相对浏览器窗口进行定位。
inherit：从父元素继承position的值。
3. CSS3 新特性
新增各种CSS选择器	（:not(.input)：所有class不是“input”的节点）
圆角		（border-radius:8px）
多列布局	（multi-columnlayout）
阴影和反射	（Shadow\Reflect）
