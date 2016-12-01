# 进度条

[source code](https://jsfiddle.net/badfl/wrxfem2x/)

**有准确值的进度条**

有准确值的进度条会显示当前进度正处于整体进度的占比位置，用户可以更直观的预期完成时间；
使用进度条控件，需要一个进度条控件容器，mui会自动识别该容器下是否有进度条控件，若没有，则自动创建。
进度条控件DOM结构：


```
<div id="demo1" class="mui-progressbar">
	<span></span>
</div>
```

**初始化:**

	mui(container).progressbar({progress:20}).show();
**例如:**

	mui("#demo1").progressbar({progress:20}).show();

progressbar初始化逻辑：

检查当前容器(container控件)自身是否包含.mui-progressbar类：

当前容器包含.mui-progressbar类，则以当前容器为目标控件，直接显示进度；
否则，检查当前容器的直接孩子节点是否包含.mui-progressbar类，若存在，则以遍历到的第一个含有.mui-progressbar类的孩子节点为目标控件，显示进度；
若当前容器的直接孩子节点，均不含.mui-progressbar类,则自动创建进度条控件；

**更改显示进度条:**

	mui(container).progressbar().setProgress(50);
**关闭进度条:**

	mui(container).progressbar().hide();
**备注：**关闭进度条一般用于动态创建（DOM中预先未定义）的进度条，调用hide方法后，会直接删掉对应的DOM节点；若已提前创建好DOM节点的进度条，调用hide方法无效；

**无限循环进度条:**

若无法准确提供当前进度，可以提供无限循环进度条（无限循环进度条类似于waiting等待框,参考[HTML5+规范]

无限循环进度条和准确值的进度条的用法基本相同，有如下差异：

进度条控件DOM结构（多了.mui-progressbar-infinite）：


```
<div id="demo1" class="mui-progressbar mui-progressbar-infinite">
	<span></span>
</div>
```

**初始化**

	mui("#demo1").progressbar().show();
注意：无限循环进度条不显示具体进度，因此初始化时，不能传入progress参数；mui框架也是根据progressbar构造方法中是否包含progress参数来区分当前进度条为有准确值的进度条还是无限循环进度条；

同样因为不显示具体进度的原因，无限循环进度条调用setProgress()方法无效。

**关闭进度条**

	mui("#demo1").progressbar().hide();

**页面顶部进度条**

页面顶部进度条类似浏览器进度条，固定显示在页面顶部（标题导航控件下方）； 因此，若当前页面使用父子双webview模式，子页面没有标题导航组件，则需通过自定义css的方式，重定义顶部进度条的位置，示例代码如下：

```js
body>.mui-progressbar{
	top:0
}
```

使用页面顶部进度条时，无需编写DOM结构，使用如下代码即可自动创建（顶部无限循环进度条同理）：

```js
mui('body').progressbar({
	progress: 20
}).show();
```

**自定义进度条颜色：**

```js
  <div id="demo5">
    <p class="mui-progressbar infinite-success mui-progressbar-infinite"><span></span></p>
    <p id="changeColor" class="mui-progressbar mui-progressbar-warning"><span></span></p>

  </div>
```
增加CSS样式或者重写官方css样式
```css
//自定义进度条颜色
.mui-progressbar-warning span {
  background-color: #f0ad4e;
}
//自定义无限进度条颜色
.infinite-success:before {
  background-color: #4cd964 !important;
}
```



