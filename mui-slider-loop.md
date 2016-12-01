# mui-slider-loop

在mui-slider-group节点增加mui-slder-loop样式，实现循环轮播，在子节点第一项与最后增加带mui-slider-item-duplicate与轮播第一项与最后一项相同的mui-slider-item节点

```js
 <p>
循环轮播
 </p>
  <div id="" class="mui-slider">
    <div class="mui-slider-group  mui-slider-loop">
    <!-- 额外增加的一个节点(循环轮播：第一个节点是最后一张轮播) -->
     <div class="mui-slider-item  mui-slider-item-duplicate">
        <div style="background:#ffff00;height:200px;line-height:200px;text-align:center;">
        轮播内容4
        </div>
      </div>
    <!--第一个内容区容器-->
      <div class="mui-slider-item">
        <div style="background:#ff00ff;height:200px;line-height:200px;text-align:center;">
        轮播内容1
        </div>
      </div>
      <!--第二个内容区容器-->
      <div class="mui-slider-item">
        <div style="background:#ffff00;height:200px;line-height:200px;text-align:center;">
        轮播内容2
        </div>
      </div>
      <!-- 额外增加的一个节点(循环轮播：最后一个节点是第一张轮播) -->
      <div class="mui-slider-item mui-slider-item-duplicate">
        <div style="background:#ff00ff;height:200px;line-height:200px;text-align:center;">
        轮播内容1
        </div>
      </div>
    </div>

  </div>
```






