# mui-badge

---



### Mui.css （_v3.0.0_）部分源码：

```
1372
.mui-btn .mui-badge
{
    font-size: 14px;

    margin: -2px -4px -2px 4px;

    background-color: rgba(0, 0, 0, .15);
}

1394
.mui-btn-block .mui-badge
{
    position: absolute;
    right: 0;

    margin-right: 10px;
}
1761
.mui-badge
{
    font-size: 12px;
    line-height: 1;

    display: inline-block;

    padding: 3px 6px;

    color: #333;
    border-radius: 100px;
    background-color: rgba(0, 0, 0, .15);
}
.mui-badge.mui-badge-inverted
{
    padding: 0 5px 0 0;

    color: #929292;
    background-color: transparent;
}
1837
.mui-icon .mui-badge
{
    font-size: 10px;
    line-height: 1.4;

    position: absolute;
    top: -2px;
    left: 100%;

    margin-left: -10px;
    padding: 1px 5px;

    color: white;
    background: red;
}
2370

.mui-table-view-cell > .mui-btn,
.mui-table-view-cell > .mui-badge,
.mui-table-view-cell > .mui-switch,
.mui-table-view-cell > a > .mui-btn,
.mui-table-view-cell > a > .mui-badge,
.mui-table-view-cell > a > .mui-switch
{
    position: absolute;
    top: 50%;
    right: 15px;

    -webkit-transform: translateY(-50%);
            transform: translateY(-50%);
}
.mui-table-view-cell .mui-navigate-right > .mui-btn,
.mui-table-view-cell .mui-navigate-right > .mui-badge,
.mui-table-view-cell .mui-navigate-right > .mui-switch,
.mui-table-view-cell .mui-push-left > .mui-btn,
.mui-table-view-cell .mui-push-left > .mui-badge,
.mui-table-view-cell .mui-push-left > .mui-switch,
.mui-table-view-cell .mui-push-right > .mui-btn,
.mui-table-view-cell .mui-push-right > .mui-badge,
.mui-table-view-cell .mui-push-right > .mui-switch,
.mui-table-view-cell > a .mui-navigate-right > .mui-btn,
.mui-table-view-cell > a .mui-navigate-right > .mui-badge,
.mui-table-view-cell > a .mui-navigate-right > .mui-switch,
.mui-table-view-cell > a .mui-push-left > .mui-btn,
.mui-table-view-cell > a .mui-push-left > .mui-badge,
.mui-table-view-cell > a .mui-push-left > .mui-switch,
.mui-table-view-cell > a .mui-push-right > .mui-btn,
.mui-table-view-cell > a .mui-push-right > .mui-badge,
.mui-table-view-cell > a .mui-push-right > .mui-switch
{
    right: 35px;
}
```

