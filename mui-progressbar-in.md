# mui-progressbar-in

动态设置进度条动画


```
V3.4
4150
.mui-progressbar-in
{
    -webkit-animation: mui-progressbar-in 300ms forwards;
            animation: mui-progressbar-in 300ms forwards;
}
4162
@-webkit-keyframes mui-progressbar-in
{
    from
    {
        -webkit-transform: scaleY(0);

        opacity: 0;
    }

    to
    {
        -webkit-transform: scaleY(1);

        opacity: 1;
    }
}
@keyframes mui-progressbar-in
{
    from
    {
        transform: scaleY(0);

        opacity: 0;
    }

    to
    {
        transform: scaleY(1);

        opacity: 1;
    }
}
@-webkit-keyframes mui-progressbar-out
{
    from
    {
        -webkit-transform: scaleY(1);

        opacity: 1;
    }

    to
    {
        -webkit-transform: scaleY(0);

        opacity: 0;
    }
}
@keyframes mui-progressbar-out
{
    from
    {
        transform: scaleY(1);

        opacity: 1;
    }

    to
    {
        transform: scaleY(0);

        opacity: 0;
    }
}
```

