# mui-card
形成圆角带边框白色背景区域
```

.mui-card
{
    overflow: hidden;

    margin: 0 15px;

    border: 1px solid #ddd;
    border-radius: 6px;
    background-color: white;
    background-clip: padding-box;
}

.mui-content > .mui-card:first-child
{
    margin-top: 15px;
}
```