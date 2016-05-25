# mui-collapse-content
折叠面板需要展开的内容
例子：
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
---


### Mui.css （*v3.0.0*）部分源码：
```
2427
.mui-table-view-cell.mui-collapse.mui-active .mui-table-view, .mui-table-view-cell.mui-collapse.mui-active .mui-collapse-content
{
    display: block;
}
2440
.mui-table-view-cell.mui-collapse .mui-collapse-content
{
    position: relative;

    display: none;
    overflow: hidden;

    margin: 11px -15px -11px;
    padding: 8px 15px;

    -webkit-transition: height .35s ease;
         -o-transition: height .35s ease;
            transition: height .35s ease;

    background: white;
}
2456
.mui-table-view-cell.mui-collapse .mui-collapse-content > .mui-input-group, .mui-table-view-cell.mui-collapse .mui-collapse-content > .mui-slider
{
    width: auto;
    height: auto;
    margin: -8px -15px;
}
.mui-table-view-cell.mui-collapse .mui-collapse-content > .mui-slider
{
    margin: -8px -16px;
}
```