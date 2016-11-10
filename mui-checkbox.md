# mui-checkbox

复选框

checkbox常用于多选的情况，比如批量删除、添加群聊等；

#### DOM结构

```
<div class="mui-input-row mui-checkbox">
  <label>checkbox示例</label>
  <input name="checkbox1" value="Item 1" type="checkbox" checked>
</div>
```

默认checkbox在右侧显示，若希望在左侧显示，只需增加`.mui-left`类即可，如下：

```
<div class="mui-input-row mui-checkbox mui-left">
  <label>checkbox左侧显示示例</label>
  <input name="checkbox1" value="Item 1" type="checkbox">
</div>
```

若要禁用checkbox，只需在checkbox上增加disabled属性即可；

---

### Mui.css （_v3.0.0_）部分源码：

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

