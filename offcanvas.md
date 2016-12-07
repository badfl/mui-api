# 侧滑菜单
mui提供了两种侧滑导航实现：webview模式和div模式，两种模式各有优劣，适用于不同的场景。

### webview模式
主页面和菜单内容在不同的webview中，两个页面根据内容需求分别组织DOM结构，mui对其DOM结构无特殊要求，故其有如下优点：

菜单内容是单独的webview，故可被多个页面复用；
菜单内容在单独的webview中，菜单区域的滚动不影响主界面，故可使用原生滚动，滚动更为流畅；
另一方面，webview模式也有其缺点：

不支持拖动手势（跟手拖动）；
主页面、菜单不同webview实现，因此若需交互（如：点击菜单触发主页面内容变化），需使用自定义事件实现跨webview通讯；

### div模式
主页面和菜单内容在同一个webview下，嵌套在特定结构的div中，通过div的移动动画模拟菜单移动；故该模式有如下优点：

支持拖动手势（跟手拖动）；
主页面、菜单在一个页面中，可通过JS轻松实现两者交互（如：点击菜单触发主页面内容变化），没有跨webview通讯的烦恼；
另一方面，div模式也有其缺点：

不支持菜单内容在多页面的复用，需每个页面都生成对应的菜单节点；
主界面和菜单内容的滚动互不影响，因此会使用div区域滚动，在低端Android手机且滚动内容较多时，可能会稍显卡顿；
div模式支持不同的动画效果，每种动画效果需遵从不同的DOM构造；下面我们以右滑菜单为例（左滑菜单仅需将菜单父节点上的mui-off-canvas-left换成mui-off-canvas-right即可），说明每种动画对应的DOM结构。

**动画1：主界面移动、菜单不动**

```
<!-- 侧滑导航根容器 -->
<div class="mui-off-canvas-wrap mui-draggable">
  <!-- 菜单容器 -->
  <aside class="mui-off-canvas-left">
    <div class="mui-scroll-wrapper">
      <div class="mui-scroll">
        <!-- 菜单具体展示内容 -->
        ...
      </div>
    </div>
  </aside>
  <!-- 主页面容器 -->
  <div class="mui-inner-wrap">
    <!-- 主页面标题 -->
    <header class="mui-bar mui-bar-nav">
      <a class="mui-icon mui-action-menu mui-icon-bars mui-pull-left"></a>
      <h1 class="mui-title">标题</h1>
    </header>
    <div class="mui-content mui-scroll-wrapper">
      <div class="mui-scroll">
        <!-- 主界面具体展示内容 -->
        ...
      </div>
    </div>  
  </div>
</div>
```

**动画2：缩放式侧滑（类手机QQ）**
该种动画要求的DOM结构和动画1的DOM结构基本相同，唯一差别就是需在侧滑导航根容器class上增加一个mui-scalable类

**动画3：主界面不动、菜单移动**
该种动画要求的DOM结构和动画1的DOM结构基本相同，唯一差别就是需在侧滑导航根容器class上增加一个mui-slide-in类

**动画4：主界面、菜单同时移动**
该种动画要求的DOM结构较特殊，需将菜单容器放在主页面容器之下


```
<!-- 侧滑导航根容器 -->
<div class="mui-off-canvas-wrap mui-draggable">
  <!-- 主页面容器 -->
  <div class="mui-inner-wrap">
     <!-- 菜单容器 -->
    <aside class="mui-off-canvas-left">
      <div class="mui-scroll-wrapper">
        <div class="mui-scroll">
          <!-- 菜单具体展示内容 -->
          ...
        </div>
      </div>
    </aside>
    <!-- 主页面标题 -->
    <header class="mui-bar mui-bar-nav">
      <a class="mui-icon mui-action-menu mui-icon-bars mui-pull-left"></a>
      <h1 class="mui-title">标题</h1>
    </header>
    <!-- 主页面内容容器 -->
    <div class="mui-content mui-scroll-wrapper">
      <div class="mui-scroll">
        <!-- 主界面具体展示内容 -->
        ...
      </div>
    </div>  
  </div>
</div>
```

JS API
mui支持多种方式操作div模式的侧滑菜单：

1、在界面上拖动操作（drag）；
2、点击含有mui-action-menu类的控件；
3、Android手机按menu键；
4、通过JS API触发，
如下：
可以有两种调用方式

```js
mui('.mui-off-canvas-wrap').offCanvas('show');
```

或

```js
mui('.mui-off-canvas-wrap').offCanvas().show();
```

以下方法皆支持上述两种调用方式

```
方法名	作用
show()	显示
close()	隐藏
toggle()	切换事件监听
```

你可以通过一下方式监听侧滑菜单显示隐藏


```
事件名	作用
shown	显示
hidden	隐藏
```


```js
document.querySelector('.mui-off-canvas-wrap').addEventListener('shown',function (event) {
    //...
})
```

也可以通过isShown()方法判断是否为显示状态


```js
mui('.mui-off-canvas-wrap').offCanvas().isShown();
```

isShown() 方法也可以传递 direction(方向) 参数( 非必选!! )进而可以判断左右侧滑


```js
mui('.mui-off-canvas-wrap').offCanvas().isShown('left');//true
```


