# mui-table-view


---

列表是常用的UI控件，mui封装的列表组件比较简单，只需要在ul节点上添加.mui-table-view类、在li节点上添加.mui-table-view-cell类即可，
**如下为示例代码：**
```
<ul class="mui-table-view">
	<li class="mui-table-view-cell">Item 1</li>
	<li class="mui-table-view-cell">Item 2</li>
	<li class="mui-table-view-cell">Item 3</li>
</ul>
```
<ul class="mui-table-view">
	<li class="mui-table-view-cell">Item 1</li>
	<li class="mui-table-view-cell">Item 2</li>
	<li class="mui-table-view-cell">Item 3</li>
</ul>
**折叠面板：**
.mui.content下使用.mui-table-view第一个子项距离上外边距15px
```
<div class="mui-content">
			<ul class="mui-table-view">
				<li class="mui-table-view-cell mui-collapse">
					<a class="mui-navigate-right" href="#">Item 1</a>
					<div class="mui-collapse-content">
						第1个面板中的内容
					</div>
				</li>
			</ul>
		</div>
```
可以在折叠面板中放置任何内容；折叠面板默认收缩，若希望某个面板默认展开，只需要在包含.mui-collapse类的li节点上，增加.mui-active类即可；mui官网中的方法说明，使用的就是折叠面板控件。

---


### Mui.css （*v3.0.0*）部分源码：


```
.mui-table-view
{
    position: relative;

    margin-top: 0;
    margin-bottom: 0;
    padding-left: 0;

    list-style: none;

    background-color: #fff;
}
.mui-table-view:after
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
.mui-table-view:before
{
    position: absolute;
    top: 0;
    right: 0;
    left: 0;

    height: 1px;

    content: '';
    -webkit-transform: scaleY(.5);
            transform: scaleY(.5);

    background-color: #c8c7cc;
}
.mui-table-view:before
{
    top: -1px;
}

```