# mui-switch-handle
开关上的滑块


---


### Mui.css （*v3.0.0*）部分源码：
```
4440
.mui-switch .mui-switch-handle
{
    position: absolute;
    z-index: 1;
    top: -1px;
    left: -1px;

    width: 28px;
    height: 28px;

    -webkit-transition: .2s ease-in-out;
            transition: .2s ease-in-out;
    -webkit-transition-property: -webkit-transform, width,left;
            transition-property:         transform, width,left;

    border-radius: 16px;
    background-color: #fff;
    background-clip: padding-box;
    -webkit-box-shadow: 0 2px 5px rgba(0, 0, 0, .4);
            box-shadow: 0 2px 5px rgba(0, 0, 0, .4);
}
4479
.mui-switch.mui-dragging .mui-switch-handle
{
    width: 38px;
}
.mui-switch.mui-dragging.mui-active .mui-switch-handle
{
    left: -11px;

    width: 38px;
}
.mui-switch.mui-active
{
    border-color: #4cd964;
    background-color: #4cd964;
}
.mui-switch.mui-active .mui-switch-handle
{
    -webkit-transform: translate(43px, 0);
            transform: translate(43px, 0);
}
4521
.mui-switch-mini.mui-active .mui-switch-handle
{
    -webkit-transform: translate(16px, 0);
            transform: translate(16px, 0);
}
```