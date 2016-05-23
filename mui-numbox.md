# mui-numbox

```
4741
.mui-numbox
{
    position: relative;

    display: inline-block;
    overflow: hidden;

    width: 120px;
    height: 35px;
    padding: 0 40px 0 40px;

    vertical-align: top;
    vertical-align: middle;

    border: solid 1px #bbb;
    border-radius: 3px;
    background-color: #efeff4;
}
.mui-numbox [class*=numbox-btn], .mui-numbox [class*=btn-numbox]
{
    font-size: 18px;
    font-weight: normal;
    line-height: 100%;

    position: absolute;
    top: 0;

    overflow: hidden;

    width: 40px;
    height: 100%;
    padding: 0;

    color: #555;
    border: none;
    border-radius: 0;
    background-color: #f9f9f9;
}
.mui-numbox [class*=numbox-btn]:active, .mui-numbox [class*=btn-numbox]:active
{
    background-color: #ccc;
}
.mui-numbox [class*=numbox-btn][disabled], .mui-numbox [class*=btn-numbox][disabled]
{
    color: #c0c0c0;
}
.mui-numbox .mui-numbox-btn-plus, .mui-numbox .mui-btn-numbox-plus
{
    right: 0;

    border-top-right-radius: 3px;
    border-bottom-right-radius: 3px;
}
.mui-numbox .mui-numbox-btn-minus, .mui-numbox .mui-btn-numbox-minus
{
    left: 0;

    border-top-left-radius: 3px;
    border-bottom-left-radius: 3px;
}
.mui-numbox .mui-numbox-input, .mui-numbox .mui-input-numbox
{
    display: inline-block;
    overflow: hidden;

    width: 100% !important;
    height: 100%;
    margin: 0;
    padding: 0 3px !important;

    text-align: center;
    text-overflow: ellipsis;
    word-break: normal;

    border: none !important;
    border-right: solid 1px #ccc !important;
    border-left: solid 1px #ccc !important;
    border-radius: 0 !important;
}

.mui-input-row .mui-numbox
{
    float: right;

    margin: 2px 8px;
}

```
