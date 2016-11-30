# 数字输入框

[source code](https://jsfiddle.net/badfl/8ez9n79e/)
mui提供了数字输入框控件，可直接输入数字，也可以点击“+”、“-”按钮变换当前数值；默认numbox控件dom结构比较简单，如下：

```js
<div class="mui-numbox">
  <!-- "-"按钮，点击可减小当前数值 -->
  <button class="mui-btn mui-numbox-btn-minus" type="button">-</button>
  <input class="mui-numbox-input" type="number" />
  <!-- "+"按钮，点击可增大当前数值 -->
  <button class="mui-btn mui-numbox-btn-plus" type="button">+</button>
</div>
```

### **numbox自定义参数**

**data-numbox-min**
输入框允许使用的最小值，默认无限制
**data-numbox-max**
输入框允许使用的最大值，默认无限制
**data-numbox-step**
每次点击“+”、“-”按钮变化的步长，默认步长为1

mui提供了数字输入框控件，可直接输入数字，也可以点击“+”、“-”按钮变换当前数值；默认numbox控件dom结构比较简单，如下

示例：设置取值范围为0~100，每次变化步长为10，则代码如下

```
<div class="mui-numbox" data-numbox-step='10' data-numbox-min='0' data-numbox-max='100'>
  <button class="mui-btn mui-numbox-btn-minus" type="button">-</button>
  <input class="mui-numbox-input" type="number" />
  <button class="mui-btn mui-numbox-btn-plus" type="button">+</button>
</div>
```

