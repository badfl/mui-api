# mui-input-password

密码框：给input元素添加`.mui-input-password`类即可使用 

例子：

```js
<div class="mui-input-row mui-password">
    <input type="password" class="mui-input-password" />
</div>

```

---

### Mui.css （_v3.0.0_）部分源码：

```css

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

