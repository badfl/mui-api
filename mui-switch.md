# mui-switch

定义开关背景与文字（on\/off）

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

重新定义背景文字与颜色：

```
.mui-switch:before{
            color: #8A6DE9;
            content: '关';
        }
        .mui-switch.mui-active:before{
            color: #FFFF00;
            content: '开';
        }
```

---

### Mui.css （_v3.0.0_）部分源码：

```
4415
.mui-switch
{
    position: relative;

    display: block;

    width: 74px;
    height: 30px;

    -webkit-transition-timing-function: ease-in-out;
            transition-timing-function: ease-in-out;
    -webkit-transition-duration: .2s;
            transition-duration: .2s;
    -webkit-transition-property: background-color, border;
            transition-property: background-color, border;

    border: 2px solid #ddd;
    border-radius: 20px;
    background-color: #fff;
    background-clip: padding-box;
}
.mui-switch.mui-disabled
{
    opacity: .3;
}
4461
.mui-switch:before
{
    font-size: 13px;

    position: absolute;
    top: 3px;
    right: 11px;

    content: 'Off';
    text-transform: uppercase;

    color: #999;
}
4489
.mui-switch.mui-active
{
    border-color: #4cd964;
    background-color: #4cd964;
}
4499
.mui-switch.mui-active:before
{
    right: auto;
    left: 15px;

    content: 'On';

    color: #fff;
}
```

