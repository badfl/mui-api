# 轮播组件

轮播组件是mui提供的一个核心组件，在该核心组件基础上，衍生出了图片轮播、可拖动式图文表格、可拖动式选项卡、左右滑动9宫格等组件，这些组件有较多共同点。首先，Dom构造基本相同，如下：

```js
<div class="mui-slider">
  <div class="mui-slider-group">
    <!--第一个内容区容器-->
    <div class="mui-slider-item">
      <!-- 具体内容 -->
    </div>
    <!--第二个内容区-->
    <div class="mui-slider-item">
      <!-- 具体内容 -->
    </div>
  </div>
</div>
```
[source code](https://jsfiddle.net/badfl/49up0q4y/)


当拖动切换显示内容时，会触发slide事件，通过该事件的detail.slideNumber参数可以获得当前显示项的索引（第一项索引为0，第二项为1，以此类推），利用该事件，可在显示内容切换时，动态处理一些业务逻辑。

如下为一个可拖动式选项卡示例，为提高页面加载速度，页面加载时，仅显示第一个选项卡的内容，第二、第三选项卡内容为空。

当切换到第二、第三个选项卡时，再动态获取相应内容进行显示：

```js
var item2Show = false,item3Show = false;//子选项卡是否显示标志
document.querySelector('.mui-slider').addEventListener('slide', function(event) {
  if (event.detail.slideNumber === 1&&!item2Show) {
    //切换到第二个选项卡
    //根据具体业务，动态获得第二个选项卡内容；
    var content = ....
    //显示内容
    document.getElementById("item2").innerHTML = content;
    //改变标志位，下次直接显示
    item2Show = true;
  } else if (event.detail.slideNumber === 2&&!item3Show) {
    //切换到第三个选项卡
    //根据具体业务，动态获得第三个选项卡内容；
    var content = ....
    //显示内容
    document.getElementById("item3").innerHTML = content;
    //改变标志位，下次直接显示
    item3Show = true;
  }
});
```

图片轮播、可拖动式图文表格等均可按照同样方式监听内容变化，比如我们可以在图片轮播界面显示当前正在看的是第几张图片：

```js
document.querySelector('.mui-slider').addEventListener('slide', function(event) {
  //注意slideNumber是从0开始的；
  document.getElementById("info").innerText = "你正在看第"+(event.detail.slideNumber+1)+"张图片";
});
```



