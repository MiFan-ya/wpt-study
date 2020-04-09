七、数组
1. 创建数组： var a = ['a','b','c']; or var a = new Array('a','b');
2. a.foreach() 遍历
3. a.push（"b"） 数组a中添加元素b。var x = a.push("b") x的值为新数组的长度
4. a[a.length] = "b" 在数组a中添加b
5. a.join("*") 将数组a中元素输出 1*2*3*4 可规定分隔符
6. a.pop() 删除数组最后一个元素 。var x =a.pop() x的值为数组a中的最后一个元素
7. a.shift() 删除数组a中的第一个元素。var x =a.shift() x的值为数组a中的第一个元素
8. a.unshift() a数组开头添加元素。var x = a.unshift("b") x的值为新数组的长度
9. delete a[0] 删除数组中第一个元素 但是首个元素被改为undefind
10. a.splice(添加元素的位置（添加元素的下标），从添加的元素后面要删除的元素数量，"添加的元素"，"")  a.splice（0，1） 删除数组中第一个元素
11. concat ：合并 
例：1.var a =b.concat(c) 2.var a =b.concat(c,d) 3.var a =b.concat(["","",""])
12. var a =b.slice(1) 从下标为1的元素（包括）切出成为新的数组。
var a =b.slice(1，3) 生成新数组前包后不包，即b[1]和b[2]。
13. a.reverse() 倒序排序（字母）
14. 对数组数值进行排序（比值函数），x.sort(function(a, b){return b - a}); 倒序：a-b；
15. 随机顺序排序数组：x.sort(function(a, b){return 0.5 - Math.random()}); 
16. var a =b.map(函数) 成为新的数组a，数组b不发生改变
17. var a =b.filter(函数) 成为新的数组a，分离出符合的函数。
18. reduce（）每个数组元素上运行函数，从左往右 
例：算总和
var a = [1, 2, 3, 4, 5];
var sum = a.reduce(b);
function b(x, y) {
  return x + y;}
  可以接受初始值reduce（b,2）
19. var a =b.every(函数) 数组b是否满足函数中的条件。a值true or false
20. some同上
21. a.indexOf（"b"）搜索b返回下标（从0开始）
22. a.lastIndexOf("c") 从结尾开始搜索（-1~+∞开始）
23. a.find(函数) 满足函数的第一个元素
24. a.findIndex(函数) 满足函数的第一个元素的下标

八、日期
1. var a=new Date() 括号内可指定 1月份为0
2. getFullYear() 返回年份；getMonth() 返回月份（0-11）；getDate() 返回日（1-31）；
getHours() 返回小时（0-23）；getMinutes() 返回分钟（0-59）；getSeconds() 返回秒（0-59）；getDay() 返回星期（1-7）；
将get改为set 变为修改

九、数学
1. Math.round（数字） ：四舍五入 。ceil 6.4返回7 上舍入。floor 2.7返回2 下舍入。
2. Math.random 0-1之间的随机数
3. Math.floor(Math.random() * (max - min + 1) ) + min; 包含

十、