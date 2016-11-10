# mui-slider-group



### Mui.css （_v3.0.0_）部分源码：

```
804
.mui-plus-pullrefresh .mui-fullscreen .mui-scroll-wrapper .mui-scroll-wrapper, .mui-plus-pullrefresh .mui-fullscreen .mui-slider-group .mui-scroll-wrapper
{
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;

    overflow: hidden;

    width: 100%;
}
.mui-plus-pullrefresh .mui-fullscreen .mui-scroll-wrapper .mui-scroll, .mui-plus-pullrefresh .mui-fullscreen .mui-slider-group .mui-scroll
{
    position: absolute;

    width: 100%;
}
.mui-plus-pullrefresh .mui-scroll-wrapper, .mui-plus-pullrefresh .mui-slider-group
{
    position: static;
    top: auto;
    bottom: auto;
    left: auto;

    overflow: auto;

    width: auto;
}
.mui-plus-pullrefresh .mui-slider-group
{
    overflow: visible;
}

4274

.mui-slider .mui-segmented-control.mui-segmented-control-inverted ~ .mui-slider-group .mui-slider-item
{
    border-top: 1px solid #c8c7cc;
    border-bottom: 1px solid #c8c7cc;
}
.mui-slider .mui-slider-group
{
    font-size: 0;

    position: relative;

    -webkit-transition: all 0s linear;
            transition: all 0s linear;
    white-space: nowrap;
}
.mui-slider .mui-slider-group .mui-slider-item
{
    font-size: 14px;

    position: relative;

    display: inline-block;

    width: 100%;
    height: 100%;

    vertical-align: top;
    white-space: normal;
}
.mui-slider .mui-slider-group .mui-slider-item > a:not(.mui-control-item)
{
    line-height: 0;

    position: relative;

    display: block;
}
.mui-slider .mui-slider-group .mui-slider-item img
{
    width: 100%;
}
.mui-slider .mui-slider-group .mui-slider-item .mui-table-view:before, .mui-slider .mui-slider-group .mui-slider-item .mui-table-view:after
{
    height: 0;
}
.mui-slider .mui-slider-group.mui-slider-loop
{
    -webkit-transform: translate(-100%, 0px);
            transform: translate(-100%, 0px);
}

5303
.mui-fullscreen.mui-slider .mui-slider-group
{
    height: 100%;
}
.mui-fullscreen .mui-segmented-control ~ .mui-slider-group
{
    position: absolute;
    top: 40px;
    bottom: 0;

    width: 100%;
    height: auto;
}
5336
.mui-bar-tab ~ .mui-content .mui-slider.mui-fullscreen .mui-segmented-control ~ .mui-slider-group
{
    bottom: 50px;
}
```

