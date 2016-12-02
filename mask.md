# 遮罩蒙版

在popover、侧滑菜单等界面，经常会用到蒙版遮罩；比如popover弹出后，除popover控件外的其它区域都会遮罩一层蒙版，用户点击蒙版不会触发蒙版下方的逻辑，而会关闭popover同时关闭蒙版；再比如侧滑菜单界面，菜单划出后，除侧滑菜单之外的其它区域都会遮罩一层蒙版，用户点击蒙版会关闭侧滑菜单同时关闭蒙版。

遮罩蒙版常用的操作包括：创建、显示、关闭，如下代码：


```js
var mask = mui.createMask(callback);//callback为用户点击蒙版时自动执行的回调；
mask.show();//显示遮罩
mask.close();//关闭遮罩
```

注意：关闭遮罩仅会关闭，不会销毁；关闭之后可以再次调用mask.show();打开遮罩；

mui默认的蒙版遮罩使用.mui-backdrop类定义（如下代码），若需自定义遮罩效果，只需覆盖定义.mui-backdrop即可；


```css
.mui-backdrop {
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: 998;
    background-color: rgba(0,0,0,.3);
}
```


