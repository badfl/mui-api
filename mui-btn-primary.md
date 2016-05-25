# mui-btn-primary/mui-btn-blue



>## 定义背景颜色、边框与字体颜色，颜色值请看下面源码，想改变颜色值可重写相应样式或重新定义样式。









---


### Mui.css （*v3.0.0*）部分源码：
```
1236
input[type='submit'],
.mui-btn-primary, .mui-btn-blue
{
    color: #fff;
    border: 1px solid #007aff;
    background-color: #007aff;
}
input[type='submit']:enabled:active, input[type='submit'].mui-active:enabled,
.mui-btn-primary:enabled:active,
.mui-btn-primary.mui-active:enabled, .mui-btn-blue:enabled:active, .mui-btn-blue.mui-active:enabled
{
    color: #fff;
    border: 1px solid #0062cc;
    background-color: #0062cc;
}

```