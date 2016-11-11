# 列表\/折叠面板

[source code](https://jsfiddle.net/badfl/h4j4fhzy/)

普通列表

列表是常用的UI控件，mui封装的列表组件比较简单，只需要在ul节点上添加.mui-table-view类、在li节点上添加.mui-table-view-cell类即可，如下为示例代码

```
<ul class="mui-table-view">
    <li class="mui-table-view-cell">Item 1</li>
    <li class="mui-table-view-cell">Item 2</li>
    <li class="mui-table-view-cell">Item 3</li>
</ul>
```

自定义列表高亮颜色
点击列表，对应列表项显示灰色高亮，若想自定义高亮颜色，只需要重写.mui-table-view-cell.mui-active即可，如下：

```
/*点击变蓝色高亮*/
.mui-table-view-cell .mui-active{
    background-color: #0062CC;
}
```

右侧添加导航箭头
若右侧需要增加导航箭头，变成导航链接，则只需在li节点下增加a子节点，并为该a节点增加.mui-navigate-right类即可，如下：

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

右侧添加数字角标等控件
mui支持将数字角标、按钮、开关等控件放在列表中；mui默认将数字角标放在列表右侧显示，代码如下：

```
<ul class="mui-table-view">
    <li class="mui-table-view-cell">Item 1 
        <span class="mui-badge mui-badge-primary">11</span>
    </li>
    <li class="mui-table-view-cell">Item 2 
        <span class="mui-badge mui-badge-success">22</span>
    </li>
    <li class="mui-table-view-cell">Item 3 
        <span class="mui-badge">33</span>
    </li>
</ul>
```

media list（图文列表）
图文列表继承自列表组件，主要添加了.mui-media、.mui-media-object、.mui-media-body、.mui-pull-left\/right几个类，如下为示例代码
[source code](https://jsfiddle.net/badfl/t4htb4re/)

```
<ul class="mui-table-view">
    <li class="mui-table-view-cell mui-media">
        <a href="javascript:;">
            <img class="mui-media-object mui-pull-left" src="../images/shuijiao.jpg">
            <div class="mui-media-body">
                幸福
                <p class='mui-ellipsis'>能和心爱的人一起睡觉，是件幸福的事情；可是，打呼噜怎么办？</p>
            </div>
        </a>
    </li>
    <li class="mui-table-view-cell mui-media">
        <a href="javascript:;">
            <img class="mui-media-object mui-pull-left" src="../images/muwu.jpg">
            <div class="mui-media-body">
                木屋
                <p class='mui-ellipsis'>想要这样一间小木屋，夏天挫冰吃瓜，冬天围炉取暖.</p>
            </div>
        </a>
    </li>
    <li class="mui-table-view-cell mui-media">
        <a href="javascript:;">
            <img class="mui-media-object mui-pull-left" src="../images/cbd.jpg">
            <div class="mui-media-body">
                CBD
                <p class='mui-ellipsis'>烤炉模式的城，到黄昏，如同打翻的调色盘一般.</p>
            </div>
        </a>
    </li>
</ul>
```

折叠面板从二级列表中演化而来，dom结构和二级列表类似
[source code](https://jsfiddle.net/badfl/k4mfLnsx/)
```
<ul class="mui-table-view"> 
        <li class="mui-table-view-cell mui-collapse">
            <a class="mui-navigate-right" href="#">面板1</a>
            <div class="mui-collapse-content">
                <p>面板1子内容</p>
            </div>
        </li>
    </ul>
```

可以在折叠面板中放置任何内容；折叠面板默认收缩，若希望某个面板默认展开，只需要在包含.mui-collapse类的li节点上，增加.mui-active类即可；mui官网中的方法说明，使用的就是折叠面板控件。

