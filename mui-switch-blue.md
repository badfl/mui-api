# mui-switch-blue

蓝色开关控件

mui默认还提供了蓝色开关控件，只需在`.mui-switch`节点上增加`.mui-switch-blue`类即可，如下：

```
<!-- 蓝色开关关闭状态 -->
<div class="mui-switch mui-switch-blue">
  <div class="mui-switch-handle"></div>
</div>
<!-- 蓝色开关打开状态 -->
<div class="mui-switch mui-switch-blue mui-active">
  <div class="mui-switch-handle"></div>
</div>
```

### Mui.css （_v3.0.0_）部分源码：

```
4527
.mui-switch-blue.mui-active
{
    border: 2px solid #007aff;
    background-color: #007aff;
}
```

