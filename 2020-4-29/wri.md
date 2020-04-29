一、flex布局
1. flex-direction属性决定主轴的方向（即项目的排列方向）:
取值：
row(默认值) ：主轴为水平方向，起点在左端，从左开始。
row-reverse：主轴为水平方向，起点在右端。从右开始。
column：主轴为垂直方向，起点在上。从上开始。
column-reverse：主轴为垂直方向，起点在下。从下开始。
2. flex-wrap属性决定排不下，如何换行。
取值：
nowrap（默认）：不换行。
wrap：换行，第一行在上方。
wrap-reverse：换行，第一行在下方。
3. flex-flow属性是flex-direction属性和flex-wrap属性的简写形式.
4. justify-content属性定义了项目在主轴上的对齐方式。
属性：
flex-start（默认值）：左对齐
flex-end：右对齐
center： 居中
space-between：两端对齐，项目之间的间隔都相等。
space-around：每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。
5. align-items属性定义项目在交叉轴上如何对齐。
取值：
flex-start：交叉轴的起点对齐。
flex-end：交叉轴的终点对齐。
center：交叉轴的中点对齐。
baseline: 项目的第一行文字的基线对齐。
stretch（默认值）：如果项目未设置高度或设为auto，将占满整个容器的高度。
6. align-content属性定义了多根轴线的对齐方式。如果项目只有一根轴线，该属性不起作用。
取值：
flex-start：与交叉轴的起点对齐。
flex-end：与交叉轴的终点对齐。
center：与交叉轴的中点对齐。
space-between：与交叉轴两端对齐，轴线之间的间隔平均分布。
space-around：每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。
stretch（默认值）：轴线占满整个交叉轴。
7. order属性定义项目的排列顺序。数值越小，排列越靠前，默认为0. 取值：整数。
8. flex-grow属性定义项目的放大比例，默认为0，即如果存在剩余空间，也不放大。取值：数字。
9. flex-shrink属性定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。
10. flex-basis属性定义了在分配多余空间之前，项目占据的主轴空间。浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为auto，即项目的本来大小。
可以设为跟width或height属性一样的值（比如350px），则项目将占据固定空间。
11. flex属性是flex-grow, flex-shrink 和 flex-basis的简写.
12. align-self属性允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。默认值为auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch。
取值：
比align-items多了个auto属性。
13. 例:骰子的一面（1-9解锁）
数字一三七九：
<div class="box">
  <div class="column">
    <span class="item"></span>
    <span class="item"></span>
  </div>
  <div class="column">
    <span class="item"></span>
    <span class="item"></span>
  </div>
</div>

.box {
  display: flex;
  flex-wrap: wrap;
  align-content: space-between;
}
.column {
  flex-basis: 100%;
  display: flex;
  justify-content: space-between;
}
二、用纯 CSS 创建一个三角形
1. 采用的是相邻边框连接处的均分原理。
2. 代码：
#demo {
width: 0;
height: 0;
border-left: 50px solid transparent;
border-right: 50px solid transparent;
border-bottom: 100px solid blue;
}
or
#demo {
  width: 0;
  height: 0;
  border-width: 20px;
  border-style: solid;
  border-color: transparent transparent red transparent;
}上右下左
三、满屏品字布局
1. 上面的div宽100%，
2. 下面的两个div分别宽50%，
3. 然后用float或者inline使其不换行即可
四、


