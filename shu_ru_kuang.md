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



