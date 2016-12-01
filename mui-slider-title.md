# mui-slider-title
增加轮播图标题


```
<p>
    加下标题循环轮播
  </p>
  <div id="" class="mui-slider">
    <div class="mui-slider-group  mui-slider-loop">
      <!-- 额外增加的一个节点(循环轮播：第一个节点是最后一张轮播) -->
      <div class="mui-slider-item  mui-slider-item-duplicate">
        <div style="background:#ffff00;height:200px;line-height:200px;text-align:center;">
          轮播内容4
        </div>
        <p class="mui-slider-title">标题2</p>
      </div>
      <!--第一个内容区容器-->
      <div class="mui-slider-item">
        <div style="background:#ff00ff;height:200px;line-height:200px;text-align:center;">
          轮播内容1
        </div>
        <p class="mui-slider-title">badfl.com</p>
      </div>
      <!--第二个内容区容器-->
      <div class="mui-slider-item">
        <div style="background:#ffff00;height:200px;line-height:200px;text-align:center;">
          轮播内容2
        </div>
        <p class="mui-slider-title">标题2</p>
      </div>
      <!-- 额外增加的一个节点(循环轮播：最后一个节点是第一张轮播) -->
      <div class="mui-slider-item mui-slider-item-duplicate">
        <div style="background:#ff00ff;height:200px;line-height:200px;text-align:center;">
          轮播内容1
        </div>
        <p class="mui-slider-title">badfl.com</p>
      </div>
    </div>
    <div class="mui-slider-indicator">
      <div class="mui-indicator mui-active"></div>
      <div class="mui-indicator"></div>
    </div>
  </div>
```
