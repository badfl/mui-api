# mui-disabled
将单选框复选框文字变成灰色  不可选中状态

---


### Mui.css （*v3.0.0*）部分源码：
```
1223
input[type='button']:disabled, input[type='button'].mui-disabled,
input[type='submit']:disabled,
input[type='submit'].mui-disabled,
input[type='reset']:disabled,
input[type='reset'].mui-disabled,
button:disabled,
button.mui-disabled,
.mui-btn:disabled,
.mui-btn.mui-disabled
{
    opacity: .6;
}
3031
.mui-radio.mui-disabled label, .mui-radio label.mui-disabled, .mui-checkbox.mui-disabled label, .mui-checkbox label.mui-disabled
{
    opacity: .4;
}
4125
.mui-pagination > li.mui-disabled > span,
.mui-pagination > li.mui-disabled > span:active,
.mui-pagination > li.mui-disabled > a,
.mui-pagination > li.mui-disabled > a:active
{
    opacity: .6;
    color: #777;
    border: 1px solid #ddd;
    background-color: #fff;
}
4205
.mui-pager .mui-disabled > a,
.mui-pager .mui-disabled > a:active,
.mui-pager .mui-disabled > span,
.mui-pager .mui-disabled > span:active
{
    opacity: .6;
    color: #777;
    border: 1px solid #ddd;
    background-color: #fff;
}
4436
.mui-switch.mui-disabled
{
    opacity: .3;
}

```