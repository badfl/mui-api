# 数字角标


数字角标一般和其它控件（列表、9宫格、选项卡等）配合使用，用于进行数量提示。 角标的核心类是`.mui-badge`，默认为实心灰色背景；同时，mui还内置了蓝色（blue）、绿色\(green\)、黄色\(yellow\)、红色\(red\)、紫色\(purple\)五种色系的数字角标
[source code](https://jsfiddle.net/badfl/ynr3z2wn/)
```js
<span class="mui-badge">1</span>
<span class="mui-badge mui-badge-primary">12</span>
<span class="mui-badge mui-badge-success">123</span>
<span class="mui-badge mui-badge-warning">3</span>
<span class="mui-badge mui-badge-danger">45</span>
<span class="mui-badge mui-badge-purple">456</span>
```

若无需底色，则增加`.mui-badge-inverted`类即可，如下

```
<span class="mui-badge mui-badge-inverted">1</span>
<span class="mui-badge mui-badge-primary mui-badge-inverted">2</span>
<span class="mui-badge mui-badge-success mui-badge-inverted">3</span>
<span class="mui-badge mui-badge-warning mui-badge-inverted">4</span>
<span class="mui-badge mui-badge-danger mui-badge-inverted">5</span>
<span class="mui-badge mui-badge-royal mui-badge-inverted">6</span>
```

