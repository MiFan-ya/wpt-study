十、正则
1. （x|y）查找由|分隔的任何选项
2. \d 查找数字 。\s查找空白字符。
3. test（）
例：/e/.test("aae efsf f"); 返回true 只要有一个e，就成立。

"use strict"; 定义 JavaScript 代码应该以“严格模式”执行。

十一、let和const、JSON
1.let
 var x = 10;       var x = 10;        
// 此处 x 为 10       // 此处 x 为 10         
 { var x = 6;          {let x = 6;       
  // 此处 x 为 6 }     // 此处 x 为 6 }    
// 此处 x 为 6       // 此处 x 为 10    
-------------------------------------------
  var i = 7;                          let i=7;  
  for (var i = 0; i < 10; i++)     for (let i = 0; i < 10; i++) { 
  { // 一些语句   }                      //}                  
  // 此处，i 为 10                      //i=7
2. const
与let相似，但赋值后不能重新赋值。必须在声明时赋值。
3. JSON.parse（text） parse转换为js对象。
把 JavaScript 对象转换为 JSON 字符串，然后发送到服务器。
var myObj = { "name":"Bill Gates",  "age":62, "city":"Seattle" };
var myJSON = JSON.stringify(myObj);
window.location = "/demo/demo_json.php?x=" + myJSON; 
