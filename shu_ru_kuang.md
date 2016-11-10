# 输入框

**基本说明:**所有包裹在`.mui-input-row` 类中的 input、textarea等元素都将被默认设置宽度属性为`width: 100%;` 。 将 label 元素和上述控件控件包裹在`.mui-input-group`中可以获得最好的排列。

```js
<form class="mui-input-group">
    <div class="mui-input-row">
        <label>用户名</label>
    <input type="text" class="mui-input-clear" placeholder="请输入用户名">
    </div>
    <div class="mui-input-row">
        <label>密码</label>
        <input type="password" class="mui-input-password" placeholder="请输入密码">
    </div>
    <div class="mui-button-row">
        <button type="button" class="mui-btn mui-btn-primary" >确认</button>
        <button type="button" class="mui-btn mui-btn-danger" >取消</button>
    </div>
</form>
```

**输入增强:**mui目前提供的输入增强包括：**快速删除**、**语音输入\*5+ only**和**密码框显示隐藏密码。**

* 快速删除：只需要在input控件上添加`.mui-input-clear`类，当input 控件中有内容时，右侧会有一个删除图标，点击会清空当前input的内容；
  ```js
  <form class="mui-input-group">
      <div class="mui-input-row">
          <label>快速删除</label>
          <input type="text" class="mui-input-clear" placeholder="请输入内容">
      </div>
  </form>
  ```


 搜索框：在`.mui-input-row`同级添加`.mui-input-search` 类，就可以使用search控件 

```js
<div class="mui-input-row mui-search">
    <input type="search" class="mui-input-clear" placeholder="">
</div>
```

* 语音输入**\*5+ only**：为了方便快速输入，mui集成了 HTML5+的语音输入，只需要在对应input控件上添加`.mui-input-speech` 类，就可以在5+环境下使用语音输入



* 密码框：给input元素添加`.mui-input-password`类即可使用
  ```js
  <form class="mui-input-group">
      <div class="mui-input-row">
          <label>密码框</label>
          <input type="password" class="mui-input-password" placeholder="请输入密码">
      </div>
  </form>
  ```


**初始化：**mui在mui.init\(\)中会自动初始化基本控件,但是 **动态添加的元素需要重新进行初始化** 

打开chrome控制台运行下面这段代码,赋予☝️此密码框生命力😀

```js
mui('.mui-input-row input').input(); 
```

#### 示例:

验证表单是否为空

```js
<div class="mui-input-group">
    <div class="mui-input-row">
        <label>用户名：</label>
        <input type="text" class="mui-input-clear" placeholder="请输入用户名">
    </div>
    <div class="mui-input-row">
        <label>密码：</label>
        <input type="password" class="mui-input-clear mui-input-password" placeholder="请输入密码">
    </div>
</div>
```

提交时校验三个字段均不能为空，若为空则提醒并终止业务逻辑运行，使用`each()`方法循环校验，如下： 

```js
mui("#input_example input").each(function() {
//若当前input为空，则alert提醒 
if(!this.value || this.value.trim() == "") {
    var label = this.previousElementSibling;
    mui.alert(label.innerText + "不允许为空");
    check = false;
    return false;
}
}); //校验通过，继续执行业务逻辑 
if(check){
    mui.alert('验证通过!')
}
```

* 注：始终为button按钮添加`type`属性，若button按钮没有type属性，浏览器默认按照`type="submit"`逻辑处理， 这样若将没有type的button放在form表单中，点击按钮就会执行form表单提交，页面就会刷新，用户体验极差。















