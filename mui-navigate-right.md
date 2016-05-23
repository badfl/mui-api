# mui-navigate-right
在折叠面板（mui-collapse）中右侧添加下拉箭头，点击后变成上拉箭头
在列表（mui-table-view-cell）中，右侧添加右箭头

下箭头例子：
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
右箭头例子：
```
<ul class="mui-table-view">
	<li class="mui-table-view-cell">
		<a class="mui-navigate-right">Item 1</a>
	</li>
	<li class="mui-table-view-cell">
		<a class="mui-navigate-right">Item 2</a>
	</li>
	<li class="mui-table-view-cell">
		<a class="mui-navigate-right">Item 3</a>
	</li>
</ul>
```



mui.css中源码（Mui v3.0.0）
```

2419行
.mui-table-view-cell.mui-collapse > .mui-navigate-right:after, .mui-table-view-cell.mui-collapse > .mui-push-right:after
{
    content: '\e581';
}
2431行
.mui-table-view-cell.mui-collapse.mui-active > .mui-navigate-right:after, .mui-table-view-cell.mui-collapse.mui-active > .mui-push-right:after
{
    content: '\e580';
}
4567行
.mui-navigate-right:after,
.mui-push-left:after,
.mui-push-right:after
{
    font-family: Muiicons;
    font-size: inherit;
    line-height: 1;

    position: absolute;
    top: 50%;

    display: inline-block;

    -webkit-transform: translateY(-50%);
            transform: translateY(-50%);
    text-decoration: none;

    color: #bbb;

    -webkit-font-smoothing: antialiased;
}
/*4596行*/
.mui-navigate-right:after,
.mui-push-right:after
{
    right: 15px;

    content: '\e583';
}

```
