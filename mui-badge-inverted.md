# mui-badge-inverted

设置数字角标背景透明

```
<span class="mui-badge mui-badge-inverted">1</span>
<span class="mui-badge mui-badge-primary mui-badge-inverted">2</span>
<span class="mui-badge mui-badge-success mui-badge-inverted">3</span>
<span class="mui-badge mui-badge-warning mui-badge-inverted">4</span>
<span class="mui-badge mui-badge-danger mui-badge-inverted">5</span>
<span class="mui-badge mui-badge-royal mui-badge-inverted">6</span>
```

---

### Mui.css （_v3.0.0_）部分源码：

```

1381
.mui-btn .mui-badge-inverted,
.mui-btn:enabled:active .mui-badge-inverted
{
    background-color: transparent;
}

.mui-btn-primary:enabled:active .mui-badge-inverted,
.mui-btn-positive:enabled:active .mui-badge-inverted,
.mui-btn-negative:enabled:active .mui-badge-inverted
{
    color: #fff;
}
1774
.mui-badge.mui-badge-inverted
{
    padding: 0 5px 0 0;

    color: #929292;
    background-color: transparent;
}

1787
.mui-badge-primary.mui-badge-inverted, .mui-badge-blue.mui-badge-inverted
{
    color: #007aff;
    background-color: transparent;
}
```

