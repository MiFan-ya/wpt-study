一、CSS3 新特性
1. 新增各种CSS选择器	（:not(.input)：所有class不是“input”的节点）

2. 圆角		（border-radius:8px）

3. 多列布局	（multi-columnlayout）如：报纸
例：
div{
 /* div中文本被分成三列 */ 
-moz-column-count:3; 	/* Firefox */
-webkit-column-count:3; /* Safari 和 Chrome */
column-count:3；

 /* 相邻两列之间的间隔 */ 
-moz-column-gap:40px;		/* Firefox */
-webkit-column-gap:40px;	/* Safari 和 Chrome */
column-gap:40px;

/* 相邻两列之间设置分割线（px、样式、颜色） */
-moz-column-rule:3px outset red;	/* Firefox */
-webkit-column-rule:3px outset red;	/* Safari and Chrome */
column-rule:3px outset red;
}

/* h1在div中，使h1元素横跨所有列*/
h1{
-webkit-column-span:all; /* Chrome */
column-span:all;
}

4. 阴影和反射	（Shadow\Reflect）
例：
/* 文字阴影效果（水平阴影的位置、垂直阴影的位置、模糊的距离、颜色）*/
text-shadow:2px 2px 2px red;
/* 边框阴影效果*/
box-shadow:2px 2px 2px red;
反射:
none：无倒影、above：倒影在对象的上边、below：倒影在对象的下边、left：倒影在对象的左边、right：倒影在对象的右边
1px：实体和倒影间的距离
50%：倒影显示一半
.6：倒影透明度
-webkit-box-reflect:below 1px  -webkit-linear-gradient(transparent,transparent 50%,rgba(255,255,255,.6));

5. 文字渲染：
text-decoration: overline（横线文字在上方）、line-through（中间）、underline（下方）、none、blink（闪烁的文本）；

6. 线性渐变：
从上至下：
background-image: linear-gradient(color1,color2,...);
从左至右：
background-image: linear-gradient(to right,color1,color2,...);
从右至左：to left
从下至上：to top
对角：
background-image: linear-gradient(to bottom right,color1,color2,...);
也可以使用角度：
background-image: linear-gradient(90deg,color1,color2,...);
使用透明度：
background-image: linear-gradient(to right, rgba(255,0,0,0), rgba(255,0,0,1));
重复的线性渐变：红黄绿红黄绿重复
background-image: repeating-linear-gradient(red , yellow 10%, green 20%);
径向渐变：椭圆 均匀分布
background-image: radial-gradient(red, yellow, green);
径向渐变：椭圆 不均匀分布
background-image: radial-gradient(red 5%, yellow 15%, green 60%);
设置形状：circle：圆形；默认ellipse椭圆形
background-image: radial-gradient(circle, red, yellow, green);
重复的径向渐变：
background-image: repeating-radial-gradient(red, yellow 10%, green 15%);

7. 旋转：
方形从左上角向右转
div{
transform:rotate(7deg);
-ms-transform:rotate(7deg); 	/* IE 9 */
-moz-transform:rotate(7deg); 	/* Firefox */
-webkit-transform:rotate(7deg); /* Safari 和 Chrome */
-o-transform:rotate(7deg); 	/* Opera */}

二、解释CSS3的flexbox（弹性盒布局模型），适用场景。



