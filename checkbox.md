# 单选框\/复选框

radio用于单选的情况

#### DOM结构

```js
<div class="mui-input-row mui-radio">
	<label>radio</label>
	<input name="radio1" type="radio">
</div>
```

默认radio在右侧显示，若希望在左侧显示，只需增加`.mui-left`类即可，如下：

```js
<div class="mui-input-row mui-radio mui-left">
	<label>radio</label>
	<input name="radio1" type="radio">
</div> 
```

若要禁用radio，只需在radio上增加disabled属性即可；

mui基于列表控件，提供了列表式单选实现；在列表根节点上增加`.mui-table-view-radio`类即可，若要默认选中某项，只需要在对应`li`节点上增加`.mui-selected`类即可，dom结构如下：

```js
<ul class="mui-table-view mui-table-view-radio">
	<li class="mui-table-view-cell">
		<a class="mui-navigate-right">Item 1</a>
	</li>
	<li class="mui-table-view-cell mui-selected">
		<a class="mui-navigate-right">Item 2</a>
	</li>
	<li class="mui-table-view-cell">
		<a class="mui-navigate-right">Item 3</a>
	</li>
</ul>
```

列表式单选在切换选中项时会触发selected事件，在事件参数（`e.detail.el`）中可以获得当前选中的dom节点，如下代码打印当前选中项的innerHTML：

```js
var list = document.querySelector('.mui-table-view.mui-table-view-radio');
list.addEventListener('selected',function(e){
	console.log("当前选中的为："+e.detail.el.innerText);
});
```

