# mui-switch-mini

隐藏开关on\/off文字提示，变成简洁模式

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

---

### Mui.css （_v3.0.0_）部分源码：

```
4513
.mui-switch-mini
{
    width: 47px;
}
.mui-switch-mini:before
{
    display: none;
}
.mui-switch-mini.mui-active .mui-switch-handle
{
    -webkit-transform: translate(16px, 0);
            transform: translate(16px, 0);
}

```

