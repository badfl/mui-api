# 开关

mui提供了开关控件，点击滑动两种手势都可以对开关控件进行操作 

默认开关控件,带on\/off文字提示，打开时为绿色背景，基本class类为`.mui-switch`、`.mui-switch-handle`，DOM结构如下：

```js
<div class="mui-switch">
  <div class="mui-switch-handle"></div>
</div>
```

若希望开关默认为打开状态，只需要在`.mui-switch`节点上增加`.mui-active`类即可，如下：

```js
<!-- 开关打开状态，多了一个.mui-active类 -->
<div class="mui-switch mui-active">
  <div class="mui-switch-handle"></div>
</div>
```

若希望隐藏on\/off文字提示，变成简洁模式，需要在`.mui-switch`节点上增加`.mui-switch-mini`类，如下：

```js
<!-- 简洁模式开关关闭状态 -->
<div class="mui-switch mui-switch-mini">
  <div class="mui-switch-handle"></div>
</div>
<!-- 简洁模式开关打开状态 -->
<div class="mui-switch mui-switch-mini mui-active">
  <div class="mui-switch-handle"></div>
</div>
```

mui默认还提供了蓝色开关控件，只需在`.mui-switch`节点上增加`.mui-switch-blue`类即可，如下：

```js
<!-- 蓝色开关关闭状态 -->
<div class="mui-switch mui-switch-blue">
  <div class="mui-switch-handle"></div>
</div>
<!-- 蓝色开关打开状态 -->
<div class="mui-switch mui-switch-blue mui-active">
  <div class="mui-switch-handle"></div>
</div>
```

蓝色开关上增加`.mui-switch-mini`即可变成无文字的简洁模式

### **方法**

若要获得当前开关状态，可通过判断当前开关控件是否包含`.mui-active`类来实现，若包含，则为打开状态，否则即为关闭状态；如下为代码示例：

```js
var isActive = document.getElementById("mySwitch").classList.contains("mui-active");
if(isActive){
  console.log("打开状态");
}else{
  console.log("关闭状态");  
}
```

若使用js打开、关闭开关控件，可使用switch插件的`toggle()`方法，如下为示例代码：

```js
mui("#mySwitch").switch().toggle();
```

### **事件**

开关控件在打开\/关闭两种状态之间进行切换时，会触发toggle事件,通过事件的detail.isActive属性可以判断当前开关状态。可通过监听toggle事件，可以在开关切换时执行特定业务逻辑。如下为使用示例：

```js
document.getElementById("mySwitch").addEventListener("toggle",function(event){
  if(event.detail.isActive){
    console.log("你启动了开关");
  }else{
    console.log("你关闭了开关");  
  }
})
```

