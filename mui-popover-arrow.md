# mui-popover-arrow
弹出菜单定位箭头
```
3444
.mui-popover .mui-popover-arrow
{
    position: absolute;
    z-index: 1000;
    top: -25px;
    left: 0;

    overflow: hidden;

    width: 26px;
    height: 26px;
}
.mui-popover .mui-popover-arrow:after
{
    position: absolute;
    top: 19px;
    left: 0;

    width: 26px;
    height: 26px;

    content: ' ';
    -webkit-transform: rotate(45deg);
            transform: rotate(45deg);

    border-radius: 3px;
    background: #f7f7f7;
}
.mui-popover .mui-popover-arrow.mui-bottom
{
    top: 100%;
    left: -26px;

    margin-top: -1px;
}
.mui-popover .mui-popover-arrow.mui-bottom:after
{
    top: -19px;
    left: 0;
}
3500
.mui-popover.mui-popover-action .mui-popover-arrow
{
    display: none;
}

```
