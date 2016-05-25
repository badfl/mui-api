# mui-input-password

例子：
```
<div class="mui-input-row mui-password">
	<input type="password" class="mui-input-password" />
</div>

```
---


### Mui.css （*v3.0.0*）部分源码：
```

2919
.mui-input-row .mui-input-clear ~ .mui-icon-clear, .mui-input-row .mui-input-speech ~ .mui-icon-speech, .mui-input-row .mui-input-password ~ .mui-icon-eye
{
    font-size: 20px;

    position: absolute;
    z-index: 1;
    top: 10px;
    right: 0;

    width: 38px;
    height: 38px;

    text-align: center;

    color: #999;
}
.mui-input-row .mui-input-clear ~ .mui-icon-clear.mui-active, .mui-input-row .mui-input-speech ~ .mui-icon-speech.mui-active, .mui-input-row .mui-input-password ~ .mui-icon-eye.mui-active
{
    color: #007aff;
}
```

