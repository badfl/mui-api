# mui-progressbar

```
3895
/* === Progress Bar === */
.mui-progressbar
{
    position: relative;

    display: block;
    overflow: hidden;

    width: 100%;
    height: 2px;

    -webkit-transform-origin: center top;
            transform-origin: center top;
    vertical-align: middle;

    border-radius: 2px;
    background: #b6b6b6;

    -webkit-transform-style: preserve-3d;
            transform-style: preserve-3d;
}
.mui-progressbar span
{
    position: absolute;
    top: 0;
    left: 0;

    width: 100%;
    height: 100%;

    -webkit-transition: 150ms;
            transition: 150ms;
    -webkit-transform: translate3d(-100%, 0, 0);
            transform: translate3d(-100%, 0, 0);

    background: #007aff;
}

```