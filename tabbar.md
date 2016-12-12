# 选项卡
## 底部选项卡-DIV模式
何谓div模式的选项卡？实就是通过DIV模拟一个独立页面，通过DIV的显示、隐藏模拟不同页面的切换，典型的SPA模式；
这种模式适合简单业务系统，因为每个选项卡内容要写在一个DIV中，
若逻辑复杂，会导致当前页面DOM结构繁杂，造成webview响应缓慢，甚至崩溃；
因此若系统较复杂，需要下拉刷新等操作，推荐使用webview模式的选项卡；
[source code](https://jsfiddle.net/badfl/1rvjgat6/)



## 底部选项卡-Webview模式
何谓webview模式？其实就是每个选项卡内容都是一个独立的webview，彼此之间互相独立、互不影响；
对于较为复杂的业务系统，推荐使用该模式。
基于webview模式的选项卡，支持原生加速的下拉刷新，切换选项卡等；

HTML结构
```
<nav class="mui-bar mui-bar-tab">
			<a id="defaultTab" class="mui-tab-item mui-active" href="tab-webview-subpage-about.html">
				<span class="mui-icon mui-icon-home"></span>
				<span class="mui-tab-label">首页</span>
			</a>
			<a class="mui-tab-item" href="tab-webview-subpage-chat.html">
				<span class="mui-icon mui-icon-email"><span class="mui-badge">9</span></span>
				<span class="mui-tab-label">消息</span>
			</a>
			<a class="mui-tab-item" href="tab-webview-subpage-contact.html">
				<span class="mui-icon mui-icon-contact"></span>
				<span class="mui-tab-label">通讯录</span>
			</a>
			<a class="mui-tab-item" href="tab-webview-subpage-setting.html">
				<span class="mui-icon mui-icon-gear"></span>
				<span class="mui-tab-label">设置</span>
			</a>
</nav>
```

```js
 //mui初始化
			mui.init();
			var subpages = ['tab-webview-subpage-about.html', 'tab-webview-subpage-chat.html', 'tab-webview-subpage-contact.html', 'tab-webview-subpage-setting.html'];
			var subpage_style = {
				top: '45px',
				bottom: '51px'
			};
			
			var aniShow = {};
			
			 //创建子页面，首个选项卡页面显示，其它均隐藏；
			mui.plusReady(function() {
				var self = plus.webview.currentWebview();
				for (var i = 0; i < 4; i++) {
					var temp = {};
					var sub = plus.webview.create(subpages[i], subpages[i], subpage_style);
					if (i > 0) {
						sub.hide();
					}else{
						temp[subpages[i]] = "true";
						mui.extend(aniShow,temp);
					}
					self.append(sub);
				}
			});
			 //当前激活选项
			var activeTab = subpages[0];
			var title = document.getElementById("title");
			 //选项卡点击事件
			mui('.mui-bar-tab').on('tap', 'a', function(e) {
				var targetTab = this.getAttribute('href');
				if (targetTab == activeTab) {
					return;
				}
				//更换标题
				title.innerHTML = this.querySelector('.mui-tab-label').innerHTML;
				//显示目标选项卡
				//若为iOS平台或非首次显示，则直接显示
				if(mui.os.ios||aniShow[targetTab]){
					plus.webview.show(targetTab);
				}else{
					//否则，使用fade-in动画，且保存变量
					var temp = {};
					temp[targetTab] = "true";
					mui.extend(aniShow,temp);
					plus.webview.show(targetTab,"fade-in",300);
				}
				//隐藏当前;
				plus.webview.hide(activeTab);
				//更改当前活跃的选项卡
				activeTab = targetTab;
			});
			 //自定义事件，模拟点击“首页选项卡”
			document.addEventListener('gohome', function() {
				var defaultTab = document.getElementById("defaultTab");
				//模拟首页点击
				mui.trigger(defaultTab, 'tap');
				//切换选项卡高亮
				var current = document.querySelector(".mui-bar-tab>.mui-tab-item.mui-active");
				if (defaultTab !== current) {
					current.classList.remove('mui-active');
					defaultTab.classList.add('mui-active');
				}
			});
```


## 底部选项卡-二级菜单（div）
点击底部菜单，会展开显示对应的二级菜单
[source code](https://jsfiddle.net/badfl/b5a05o1L/)


## 顶部选项卡-div模式
[source code](https://jsfiddle.net/badfl/x1g39tmc/)

变成文字模式，只需要加上.mui-segmented-control-inverted类即可
```
<div class="mui-segmented-control mui-segmented-control-inverted ">
       <a class="mui-control-item mui-active" href="#item1">待办</a>  
       <a class="mui-control-item" href="#item2">已办</a>
       <a class="mui-control-item" href="#item3">完成</a>
</div>
```
改变颜色，增加.mui-segmented-control-negative,.mui-segmented-control-positive,.mui-segmented-control-primary类即可

```
<div class="mui-segmented-control mui-segmented-control-inverted mui-segmented-control-primary ">
       <a class="mui-control-item mui-active" href="#item1">待办</a>  
       <a class="mui-control-item" href="#item2">已办</a>
       <a class="mui-control-item" href="#item3">完成</a>
</div>
```

## 顶部选项卡-可左右拖动(div)
[source code](https://jsfiddle.net/badfl/7863j52n/)

## 左侧选项卡-div模式
## 左侧选项卡-div模式-滚动监听

