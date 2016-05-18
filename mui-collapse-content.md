# mui-collapse-content
折叠面板需要展开的内容
```
2427
.mui-table-view-cell.mui-collapse.mui-active .mui-table-view, .mui-table-view-cell.mui-collapse.mui-active .mui-collapse-content
{
    display: block;
}
2440
.mui-table-view-cell.mui-collapse .mui-collapse-content
{
    position: relative;

    display: none;
    overflow: hidden;

    margin: 11px -15px -11px;
    padding: 8px 15px;

    -webkit-transition: height .35s ease;
         -o-transition: height .35s ease;
            transition: height .35s ease;

    background: white;
}
2456
.mui-table-view-cell.mui-collapse .mui-collapse-content > .mui-input-group, .mui-table-view-cell.mui-collapse .mui-collapse-content > .mui-slider
{
    width: auto;
    height: auto;
    margin: -8px -15px;
}
.mui-table-view-cell.mui-collapse .mui-collapse-content > .mui-slider
{
    margin: -8px -16px;
}
```