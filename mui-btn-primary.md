# mui-btn-primary/mui-btn-blue



>## 定义背景颜色、边框与字体颜色，颜色值请看下面源码，想改变颜色值可重写相应样式或重新定义样式。



<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
    <title></title>
    <script src="../js/mui.min.js"></script>
    <link href="../css/mui.min.css" rel="stylesheet"/>
    <script type="text/javascript" charset="UTF-8">
      	mui.init();
    </script>
    <style>
    	
    	.mui-input-range .mui-tooltip
{
    font-size: 30px;
    line-height: 50px;

    top: -50px;

    width: 50px;
    height: 50px;

    color: #007AFF;

}
    </style>
</head>
<body>
<div class="mui-content">
    <div class="mui-content-padded">
    	<div class="mui-input-row mui-input-range" style="margin-top: 50px;">
    		<label>滑块默认样式：</label>
    		<input type="range" min="0" max="100"/>
    	</div>
    </div>
</div>
	
</body>
</html>





---


### Mui.css （*v3.0.0*）部分源码：
```
1236
input[type='submit'],
.mui-btn-primary, .mui-btn-blue
{
    color: #fff;
    border: 1px solid #007aff;
    background-color: #007aff;
}
input[type='submit']:enabled:active, input[type='submit'].mui-active:enabled,
.mui-btn-primary:enabled:active,
.mui-btn-primary.mui-active:enabled, .mui-btn-blue:enabled:active, .mui-btn-blue.mui-active:enabled
{
    color: #fff;
    border: 1px solid #0062cc;
    background-color: #0062cc;
}

```