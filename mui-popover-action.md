# mui-popover-action


---


### Mui.css （*v3.0.0*）部分源码：
```
3484
.mui-popover.mui-popover-action
{
    bottom: 0;

    width: 100%;

    -webkit-transition: -webkit-transform .3s, opacity .3s;
            transition:         transform .3s, opacity .3s;
    -webkit-transform: translate3d(0, 100%, 0);
            transform: translate3d(0, 100%, 0);

    border-radius: 0;
    background: none;
    -webkit-box-shadow: none;
            box-shadow: none;
}
.mui-popover.mui-popover-action .mui-popover-arrow
{
    display: none;
}
.mui-popover.mui-popover-action.mui-popover-bottom
{
    position: fixed;
}
.mui-popover.mui-popover-action.mui-active
{
    -webkit-transform: translate3d(0, 0, 0);
            transform: translate3d(0, 0, 0);
}
.mui-popover.mui-popover-action .mui-table-view
{
    margin: 8px;

    text-align: center;

    color: #007aff;
    border-radius: 4px;
}
.mui-popover.mui-popover-action .mui-table-view .mui-table-view-cell:after
{
    position: absolute;
    right: 0;
    bottom: 0;
    left: 0;

    height: 1px;

    content: '';
    -webkit-transform: scaleY(.5);
            transform: scaleY(.5);

    background-color: #c8c7cc;
}
.mui-popover.mui-popover-action .mui-table-view small
{
    font-weight: 400;
    line-height: 1.3;

    display: block;
}
```