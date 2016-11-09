# 按钮

mui默认按钮为灰色，另外还提供了蓝色（blue）、绿色(green)、黄色(yellow)、红色(red)、紫色(purple)五种色系的按钮，五种色系对应五种场景，分别为primary、success、warning、danger、royal；使用.mui-btn类即可生成一个默认按钮，继续添加.mui-btn-颜色值或.mui-btn-场景可生成对应色系的按钮，例如：通过.mui-btn-blue或.mui-btn-primary均可生成蓝色按钮；

普通按钮
在button节点上增加.mui-btn类，即可生成默认按钮；若需要其他颜色的按钮，则继续增加对应class即可，比如.mui-btn-blue即可变成蓝色按钮

```
<button type="button" class="mui-btn">默认</button>
<button type="button" class="mui-btn mui-btn-primary">蓝色</button>
<button type="button" class="mui-btn mui-btn-success">绿色</button>
<button type="button" class="mui-btn mui-btn-warning">黄色</button>
<button type="button" class="mui-btn mui-btn-danger">红色</button>
<button type="button" class="mui-btn mui-btn-royal">紫色</button> 
```
若希望无底色、有边框的按钮，仅需增加.mui-btn-outlined类即可，代码如下：

```
<button type="button" class="mui-btn mui-btn-outlined">默认</button>
<button type="button" class="mui-btn mui-btn-primary mui-btn-outlined">蓝色</button>
<button type="button" class="mui-btn mui-btn-success mui-btn-outlined">绿色</button>
<button type="button" class="mui-btn mui-btn-warning mui-btn-outlined">黄色</button>
<button type="button" class="mui-btn mui-btn-danger mui-btn-outlined">红色</button>
<button type="button" class="mui-btn mui-btn-royal mui-btn-outlined">紫色</button> 
```

