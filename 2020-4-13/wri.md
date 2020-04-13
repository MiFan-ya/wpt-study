十二、表单
1. <input required> 必须填写
2. <input value="a"> 该输入框显示初始值为a。
3. <input readonly> 该input输入字段为只读，不能修改。
4. <input disabled> 该input 不可用不可点击不被提交。输入字段为禁用。
5. <input size="1"> input 长度为1
6. <input maxlength="5"> input 内只能输入5个字段
7. <input autocomplete="on/off"> on：重新加载页面后 可选择刚刚input输入的值，不用再手动输入。 off：需要手动输入。
8. <form novalidate> 属于form属性。表单在提交时不进行验证。也就是input的type属性为Emil时，不符合规范也可以提交。
14. formnovalidate 适用于type="submit"。覆盖form中novalidate属性。
<form >
   E-mail: <input type="email">
   <input type="submit" formnovalidate value="不进行验证提交">
</form>
9. <input autofocus> 规定页面加载时，该input自动获得焦点。
10. <input form="form1的id"> 表示这个input仍属于form1.
11. formaction 适用于type 为submit 和image。
覆盖form的action 提交到 demo...
<form action="action_page.php">
<input type="submit" formaction="demo_admin.asp">

12. formenctype 提交至服务器时，如何对其编码。仅适用于method="post"。type 为submit 和image。
覆盖form 的enctype 以multi。。编码提交。 
<form action="demo_post_enctype.asp" method="post">
<input type="submit" formenctype="multipart/form-data">

13. formmethod 覆盖form的method属性。
<form  method="get">
<input type="submit" formmethod="post" formaction="demo_post.asp"

15. formtarget 提交表单后在何处显示接收到的响应。覆盖 form 的 target 属性。
与 type="submit" 和 type="image" 使用。
<form >
   <input type="submit" formtarget="_blank" value="新标签页打开">
</form> 

16. list  列表框 可选值
<input list="cars" />
<datalist id="cars">
	<option value="BMW">
	<option value="Ford">
</datalist>

17. <input pattern="正则"> 
18. <input placeholder="input框内灰色字体">
19. <input step="3">输入数字间隔为3，如：0，3，6，-3.出现input框为上下可选数字。
20.  。。innerHTML = a.validationMessage; 输出错误信息。
21. a.checkValidity()  表单验证通过返回true。
22. 表单验证： https://www.w3school.com.cn/js/js_validation_api.asp

十三、对象验证
1. var a = {
    firstName:"a",
    lastName:"b",
    age:34
};
var a = new Object();
a.firstName = "a";
a.lastName = "b";
a.age = 50;
2. 如果对象内使用函数 调用时要加括号否则返回函数内容。a.fullname().
3. var person = {
  language : "en",
  get lang() {
    return this.language;
  }
};
innerHTML = person.lang; //en
var person = {
  language : "en",
  set lang(value) {
    this.language = value;
  }
};
person.lang = "zh";
innerHTML = person.language;//zh
4. function Person(first, last, age) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
}
var myFriend = new Person("Bill", "Gates", 62);
var myBrother = new Person("Steve", "Jobs", 56);
innerHTML =myFriend.age +myBrother.age; //6256
5. 已有对象构造器（如上）不能直接添加属性。使用prototype
function Person(first, last) {
  this.firstName = first;
  this.lastName = last;
}
Person.prototype.nationality = "English";
var myFriend = new Person("Bill", "Gates");
innerHTML =myFriend.nationality; //English
or
Person.prototype.name = function() {
    return this.firstName + " " + this.lastName;
};