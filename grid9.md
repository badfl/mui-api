# 九宫格
MUI 提供了非常简单实用的12列响应式栅格系统。使用时只需在外围容器上添加.mui-row，在列上添加 .mui-col-[sm|xs]-[1-12]，即可
[source code](https://jsfiddle.net/badfl/dnpL4pt5/)
实例:
左侧:通过定义.mui-col-sm-6类在大屏(≥400px)设备上会展现为并排的两列,而.mui-col-xs-12在小屏(＜400px)设备上会覆盖之前定义的类展现为水平排列

<div class="mui-content">
    <div class="mui-row">
        <div class="mui-col-sm-6 mui-col-xs-12">
            <li class="mui-table-view-cell">
                <a class="mui-navigate-right">
                    Item 1    
                </a>
            </li>
        </div>
        <div class="mui-col-sm-6 mui-col-xs-12">
            <li class="mui-table-view-cell">
                <a class="mui-navigate-right">
                    Item 1
                </a>
            </li>
        </div>
    </div>
</div>
实例:多余的列将会另起一行排列
如果在一个.mui-row内包含的列（column）大于12个,包含多余列（column）的元素将作为一个整体单元被另起一行排列。

如果不足12个列将不会撑满整个.mui-row容器


<div class="mui-content">
    <div class="mui-row">
        <div class="mui-col-sm-8">
            <li class="mui-table-view-cell">
                <a class="mui-navigate-right">
                    Item 1    
                </a>
            </li>
        </div>
        <div class="mui-col-sm-6">
            <li class="mui-table-view-cell">
                <a class="mui-navigate-right">
                    Item 1
                </a>
            </li>
        </div>
    </div>
</div>

实例:通过为列设置padding 属性，从而创建列与列之间的间隔
两列之间白色区域为左侧列的padding


<div class="mui-content">
    <div class="mui-row">
        <div class="mui-col-sm-6" style="padding-right: 20px;">
            <li class="mui-table-view-cell">
                <a class="mui-navigate-right">
                    Item 1    
                </a>
            </li>
        </div>
        <div class="mui-col-sm-6">
            <li class="mui-table-view-cell">
                <a class="mui-navigate-right">
                    Item 1
                </a>
            </li>
        </div>
    </div>
</div>


九宫格实例：
`
<ul class="mui-table-view mui-grid-view mui-grid-9">
 <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3">
 <a href="#">
 <span class="mui-icon mui-icon-home"></span>
 <div class="mui-media-body">Home</div>
 </a>
 </li>
 <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3"><a href="#">
 <span class="mui-icon mui-icon-email"><span class="mui-badge">5</span></span>
 <div class="mui-media-body">Email</div></a></li>
 <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3"><a href="#">
 <span class="mui-icon mui-icon-chatbubble"></span>
 <div class="mui-media-body">Chat</div></a></li>
 <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3"><a href="#">
 <span class="mui-icon mui-icon-location"></span>
 <div class="mui-media-body">location</div></a></li>
 <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3"><a href="#">
 <span class="mui-icon mui-icon-search"></span>
 <div class="mui-media-body">Search</div></a></li>
 <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3"><a href="#">
 <span class="mui-icon mui-icon-phone"></span>
 <div class="mui-media-body">Phone</div></a></li>
 <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3"><a href="#">
 <span class="mui-icon mui-icon-gear"></span>
 <div class="mui-media-body">Setting</div></a></li>
 <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3"><a href="#">
 <span class="mui-icon mui-icon-info"></span>
 <div class="mui-media-body">about</div></a></li>
 <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3"><a href="#">
 <span class="mui-icon mui-icon-more"></span>
 <div class="mui-media-body">more</div></a></li>
 </ul>


`
