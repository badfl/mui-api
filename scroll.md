# 区域滚动
[source code](https://jsfiddle.net/badfl/9o3ecor4/)

在App开发中，div区域滚动的需求是普遍存在的，但系统默认实现又有如下问题：

Android平台4.0以下不支持div滚动
Android平台4.0以上支持div滚动，但不显示滚动条
弹出层的div滚动在iOS平台存在事件透传的问题
因此，mui额外提供了区域滚动组件，使用时需要遵循如下DOM结构


```
<div class="mui-scroll-wrapper">
	<div class="mui-scroll">
		<!--这里放置真实显示的DOM内容-->
	</div>
</div>
```

区域滚动组件默认为absolute定位，全屏显示；在实际使用过程中，需要手动设置滚动区域的位置（top和height）

若使用区域滚动组件，需手动初始化scroll控件

***常用配置项:**

### scroll.options

```
options = {
 scrollY: true, //是否竖向滚动
 scrollX: false, //是否横向滚动
 startX: 0, //初始化时滚动至x
 startY: 0, //初始化时滚动至y
 indicators: true, //是否显示滚动条
 deceleration:0.0006 //阻尼系数,系数越小滑动越灵敏
 bounce: true, //是否启用回弹
}
```

示例：初始化scroll控件：


```
mui('.mui-scroll-wrapper').scroll({
	deceleration: 0.0005 //flick 减速系数，系数越大，滚动速度越慢，滚动距离越小，默认值0.0006
});
```

mui中iOS平台的下拉刷新（Android平台的下拉刷新使用的是双webview+原生滚动方案）、popover、可拖动式选项卡均使用了scroll组件。 为方便大家使用，mui还额外为scroll插件封装了部分方法。

滚动到特定位置
### scrollTo( xpos , ypos [, duration] )

```
xpos
Type: Integer
要在窗口文档显示区左上角显示的文档的 x 坐标
ypos
Type: Integer
要在窗口文档显示区左上角显示的文档的 y 坐标
duration
Type: Integer
滚动时间周期，单位是毫秒
```


示例：快速回滚到该区域顶部，代码如下：


```
mui('.mui-scroll-wrapper').scroll().scrollTo(0,0,100);//100毫秒滚动到顶
```

**滚动到底部位置**
滚动到顶部的代码比较容易实现,坐标值设为0、0即可；但滚动到底部，需要计算该区域的实际高度，因此mui封装了scrollToBottom方法。

### scrollToBottom(duration)

```
duration
Type: Integer
滚动时间周期，单位是毫秒
```

### 横向滚动
横向滚动只需在scroll组件基础上添加mui-slider-indicatorcode mui-segmented-control mui-segmented-control-inverted这三个class即可.(给子元素添加mui-control-item可加大文字间距增强体验
[source code](https://jsfiddle.net/badfl/tLns7dpx/)
如:)


```
<div class="mui-scroll-wrapper mui-slider-indicator mui-segmented-control mui-segmented-control-inverted">
    <div class="mui-scroll">
        <a class="mui-control-item mui-active">
            推荐
        </a>
        <a class="mui-control-item">
            热点
        </a>
        <a class="mui-control-item">
            北京
        </a>
        <a class="mui-control-item">
            社会
        </a>
        <a class="mui-control-item">
            娱乐
        </a>
        <a class="mui-control-item">
            科技
        </a>
    </div>
</div>
```
