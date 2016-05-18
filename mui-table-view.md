# .mui-table-view

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