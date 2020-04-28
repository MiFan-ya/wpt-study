一、 解释CSS3的flexbox（弹性盒布局模型），适用场景。
1. 设置为flex布局后，子元素float、clear、vertical-align属性将失效。
vertical-align可用于设置图片与文字上对齐还是下对齐。
2. 通过将一个元素的display属性值设置为flex从而使它成为一个flex
容器，它的所有子元素都会成为它的项目。
3. 一个容器默认有两条轴，一个是水平的主轴，一个是与主轴垂直的交叉轴。我们可以使用flex-direction来指定主轴的方向。
我们可以使用justify-content来指定元素在主轴上的排列方式，使用align-items来指定元素在交叉轴上的排列方式。还
可以使用flex-wrap来规定当一行排列不下时的换行方式。
4. 对于容器中的项目，我们可以使用order属性来指定项目的排列顺序，还可以使用flex-grow来指定当排列空间有剩余的时候，
项目的放大比例。还可以使用flex-shrink来指定当排列空间不足时，项目的缩小比例。
5. 例:骰子的一面（1-9解锁）
div{<span></span>}
数字1：
div{display：flex;}/*flex布局默认首行左对齐，所以无需设置其他*/
数字2：
div{display：flex;justify-content: center;}
数字三：
div{display：flex;justify-content: flex-end;}
数字四：
div{display：flex;align-items: center;}/*垂直移动主轴*/
数字五：
div{display：flex;align-items: center;justify-content: center;}
数字八：
div{display：flex;align-items: flex-end;justify-content: center;}
数字一和三：
div{display：flex;justify-content: space-between;}
数字一和七：
div{display：flex;flex-direction: column;justify-content: space-between;}
数字二和八：
div{display：flex;flex-direction: column;justify-content: space-between;align-items: center;}
数字三和九：
div{display：flex;flex-direction: column;justify-content: space-between;align-items: flex-end;}
数字一和五：
div{display: flex;}
span:nth-child(2) {align-self: center;}
数字一和九：
div{display: flex;justify-content: space-between;}
span:nth-child(2) {align-self: flex-end;}
数字一五九：
div{display: flex;}
span:nth-child(2) {align-self: center;}
span:nth-child(3) {align-self: flex-end;}
数字一二三九：
div {display: flex;flex-wrap: wrap;justify-content: flex-end;align-content: space-between;}
数字一三七九：

