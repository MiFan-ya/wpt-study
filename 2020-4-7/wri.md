一、javascript 函数可以被放置在：
1. <head><script></script></head>
2. <body><script></script></body>
3. 外部文件 name.js 文件内无<script>标签。调用：<script src="name.js"></script>

二、
1. 选择id选择器为a，写入html元素。
例：document.getElementById("a").innerHTML = 5 + 6;
2. 直接在网页上输出
例：document.write(1+2);
3. 网页显示警告框：
例：window.alert(1+5);
4. 浏览器控制台（F12）
例：console.log(1+6);

三、
1. js语句使用分号隔开，若有分号，可在同一行写多条语句。
例：a=1;aa=2;b=3;
2. debugger ：停止执行 JavaScript，并调用调试函数（如果可用）。
例：debugger； 点击F12
3. try ... catch ：对语句块实现错误处理。
例：try { 运行代码}
    catch(err){错误}  

四、
1. var a =1; var a; a值为1.
var a =1; var a =2; a值为2.
2. var b = "1"+2+3,c=1+1+"2";b值为123，c值为22.
3. === 值相同，类型相同。！==不等值 或不等型
4. constructor:
例：var a =[1,2];
document.getElementById("id").innerHTML = isArray(a);
function isArray(aa){return aa.constructor.toString().indexOF("Array") >-1;}
5. instanceof:
例：a instanceof b 可以判断a是否为字符串等类型，a是否属于b类型中，a是否属于他的父类型。
6. <<（零填充左位移） >>（有符号右位移） >>>（零填充右位移）

五、事件
1. onclick='document.getElementById("id").innerHTML=函数()'
2. onclick="this.innerHTML=函数()"
3. onclick="函数名()"
4. 有哪些事件：https://www.w3school.com.cn/jsref/dom_obj_event.asp

六、
1. indexOf() 返回字符串中指定文本，首次出现的位置。
lastIndexOf() 最后一次出现
2. search() 返回字符串中指定文本，首次出现的位置。
3. slice(1,3) 返回字符串1-3位置的文本。数字为负，从尾巴开始算。
slice（2） 从第二位输出之后所有。
4.  substrig（）和 slice相同 不接受负数。
5. substr（1，2） 第一位开始返回2个长度。有负数。
6. replace('a','b') b替换a ，（/a/i（g），'b'），i大小写不敏感。g所有匹配的都替换。
7.  toUpperCase()大写  toLowerCase()小写。
8. a = b.concat(c) b连接c
9. trim（） 删除字符串两端空白符。
10. charAt（0） 返回下标为0的字符。charCodeAt()  返回下标为0的字符的unicode 编码。
11. split（","） 以逗号分割。字符串转数组。
12. isNaN() 是否为数。
13. toFixed(2) 两位小数
14. parseInt() parseFloat() 一段字符串返回首个数字。

七、数组
1. 创建数组： var a = ['a','b','c']; or var a = new Array('a','b');
2. foreach() 遍历
3. push（"a"） 添加元素a
4. a[a.length] = "b" 在数组a中添加b
5. 


