# mui-search

默认搜索框
例子：
```
<div class="mui-input-row mui-search">
    <input type="search" placeholder="请输入搜索内容" class="mui-input-clear"/>
  </div>
    ```

---


### Mui.css （*v3.0.0*）部分源码：
```
2957
.mui-input-row.mui-search .mui-icon-clear
{
    top: 7px;
}
.mui-input-row.mui-search .mui-icon-speech
{
    top: 5px;
}

3174
.mui-search
{
    position: relative;
}
.mui-search input[type='search']
{
    padding-left: 30px;
}
.mui-search .mui-placeholder
{
    font-size: 16px;
    line-height: 34px;

    position: absolute;
    z-index: 1;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;

    display: inline-block;

    height: 34px;

    text-align: center;

    color: #999;
    border: 0;
    border-radius: 6px;
    background: none;
}
.mui-search .mui-placeholder .mui-icon
{
    font-size: 20px;

    color: #333;
}
.mui-search:before
{
    font-family: Muiicons;
    font-size: 20px;
    font-weight: normal;

    position: absolute;
    top: 50%;
    right: 50%;

    display: none;

    margin-top: -18px;
    margin-right: 31px;

    content: '\e466';
}
.mui-search.mui-active:before
{
    font-size: 20px;

    right: auto;
    left: 5px;

    display: block;

    margin-right: 0;
}
.mui-search.mui-active input[type='search']
{
    text-align: left;
}
.mui-search.mui-active .mui-placeholder
{
    display: none;
}
```