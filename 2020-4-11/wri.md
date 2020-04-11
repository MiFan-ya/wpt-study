十二、表单
1. <input required> 必须填写
2. <input value="a"> 该输入框显示初始值为a。
3. <input readonly> 该input输入字段为只读，不能修改。
4. <input disabled> 该input 不可用不可点击不被提交。输入字段为禁用。
5. <input size="1"> input 长度为1
6. <input maxlength="5"> input 内只能输入5个字段
7. <input autocomplete="on/off"> on：重新加载页面后 可选择刚刚input输入的值，不用再手动输入。 off：需要手动输入。
8. <form novalidate> 属于form属性。表单在提交时不进行验证。也就是input的type属性为Emil时，不符合规范也可以提交。
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

13. 