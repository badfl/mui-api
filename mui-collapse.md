# mui-collapse

```
2346
.mui-table-view.mui-unfold .mui-table-view-cell.mui-collapse .mui-table-view
{
    display: block;
}
.mui-table-view.mui-unfold .mui-table-view-cell.mui-collapse .mui-table-view:before, .mui-table-view.mui-unfold .mui-table-view-cell.mui-collapse .mui-table-view:after
{
    height: 0 !important;
}
.mui-table-view.mui-unfold .mui-table-view-cell.mui-media-icon.mui-collapse .mui-media-body:after
{
    position: absolute;
    right: 0;
    bottom: 0;
    left: 70px;

    height: 1px;

    content: '';
    -webkit-transform: scaleY(.5);
            transform: scaleY(.5);

    background-color: #c8c7cc;
}
2411

.mui-table-view-cell.mui-collapse .mui-table-view:before, .mui-table-view-cell.mui-collapse .mui-table-view:after
{
    height: 0;
}
.mui-table-view-cell.mui-collapse .mui-table-view .mui-table-view-cell:last-child:after
{
    height: 0;
}
.mui-table-view-cell.mui-collapse > .mui-navigate-right:after, .mui-table-view-cell.mui-collapse > .mui-push-right:after
{
    content: '\e581';
}
.mui-table-view-cell.mui-collapse.mui-active
{
    margin-top: -1px;
}
.mui-table-view-cell.mui-collapse.mui-active .mui-table-view, .mui-table-view-cell.mui-collapse.mui-active .mui-collapse-content
{
    display: block;
}
.mui-table-view-cell.mui-collapse.mui-active > .mui-navigate-right:after, .mui-table-view-cell.mui-collapse.mui-active > .mui-push-right:after
{
    content: '\e580';
}
.mui-table-view-cell.mui-collapse.mui-active .mui-table-view-cell > a:not(.mui-btn).mui-active
{
    margin-left: -31px;
    padding-left: 47px;
}
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
.mui-table-view-cell.mui-collapse .mui-table-view
{
    display: none;

    margin-top: 11px;
    margin-right: -15px;
    margin-bottom: -11px;
    margin-left: -15px;

    border: 0;
}
.mui-table-view-cell.mui-collapse .mui-table-view.mui-table-view-chevron
{
    margin-right: -65px;
}
.mui-table-view-cell.mui-collapse .mui-table-view .mui-table-view-cell
{
    padding-left: 31px;

    background-position: 31px 100%;
}
.mui-table-view-cell.mui-collapse .mui-table-view .mui-table-view-cell:after
{
    position: absolute;
    right: 0;
    bottom: 0;
    left: 30px;

    height: 1px;

    content: '';
    -webkit-transform: scaleY(.5);
            transform: scaleY(.5);

    background-color: #c8c7cc;
}
```