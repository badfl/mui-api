# mui-left
使单选框与复选框在左侧显示

---


### Mui.css （*v3.0.0*）部分源码：
```
2090
.mui-table-view-cell.mui-radio.mui-left, .mui-table-view-cell.mui-checkbox.mui-left
{
    padding-left: 58px;
}
2979
.mui-radio.mui-left input[type='radio'], .mui-checkbox.mui-left input[type='checkbox']
{
    left: 20px;
}

.mui-radio.mui-left label, .mui-checkbox.mui-left label
{
    padding-right: 15px;
    padding-left: 58px;
}

4552
.mui-content.mui-sliding.mui-left
{
    z-index: 1;

    -webkit-transform: translate3d(-100%, 0, 0);
            transform: translate3d(-100%, 0, 0);
}
```