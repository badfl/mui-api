# mui-checkbox
复选框
```
2086
.mui-table-view-cell.mui-radio input[type=radio], .mui-table-view-cell.mui-checkbox input[type=checkbox]
{
    top: 8px;
}
.mui-table-view-cell.mui-radio.mui-left, .mui-table-view-cell.mui-checkbox.mui-left
{
    padding-left: 58px;
}
2966

.mui-radio, .mui-checkbox
{
    position: relative;
}
.mui-radio label, .mui-checkbox label
{
    display: inline-block;
    float: none;

    width: 100%;
    padding-right: 58px;
}

.mui-radio.mui-left input[type='radio'], .mui-checkbox.mui-left input[type='checkbox']
{
    left: 20px;
}

.mui-radio.mui-left label, .mui-checkbox.mui-left label
{
    padding-right: 15px;
    padding-left: 58px;
}

.mui-radio input[type='radio'], .mui-checkbox input[type='checkbox']
{
    position: absolute;
    top: 4px;
    right: 20px;

    display: inline-block;

    width: 28px;
    height: 26px;

    border: 0;
    outline: 0 !important;
    background-color: transparent;

    -webkit-appearance: none;
}
.mui-radio input[type='radio'][disabled]:before, .mui-checkbox input[type='checkbox'][disabled]:before
{
    opacity: .3;
}
.mui-radio input[type='radio']:before, .mui-checkbox input[type='checkbox']:before
{
    font-family: Muiicons;
    font-size: 28px;
    font-weight: normal;
    line-height: 1;

    text-decoration: none;

    color: #aaa;
    border-radius: 0;
    background: none;

    -webkit-font-smoothing: antialiased;
}
.mui-radio input[type='radio']:checked:before, .mui-checkbox input[type='checkbox']:checked:before
{
    color: #007aff;
}

.mui-radio.mui-disabled label, .mui-radio label.mui-disabled, .mui-checkbox.mui-disabled label, .mui-checkbox label.mui-disabled
{
    opacity: .4;
}
3046
.mui-checkbox input[type='checkbox']:before
{
    content: '\e411';
}

.mui-checkbox input[type='checkbox']:checked:before
{
    content: '\e442';
}
```