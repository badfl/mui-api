# 卡片视图

卡片视图常用于展现一段完整独立的信息，比如一篇文章的预览图、作者信息、点赞数量等
使用mui-card类即可生成一个卡片容器，卡片视图主要有页眉、内容区、页脚三部分组成，结构如下：
```
<div class="mui-card">
	<!--页眉，放置标题-->
	<div class="mui-card-header">页眉</div>
	<!--内容区-->
	<div class="mui-card-content">内容区</div>
	<!--页脚，放置补充信息或支持的操作-->
	<div class="mui-card-footer">页脚</div>
</div>
```
卡片页眉及内容区，均支持放置图片； 页眉放置图片的话，需要在.mui-card-header节点上增加.mui-card-media类，然后设置一张图片做背景图即可，代码如下：

```<div class="mui-card-header mui-card-media" style="height:40vw;background-image:url(../images/cbd.jpg)"></div>```
若希望在页眉放置更丰富的信息，比如头像、主标题、副标题，则需使用.mui-media-body类，示例代码如下：

```<div class="mui-card-header mui-card-media">
	<img src="../images/logo.png" />
	<div class="mui-media-body">
		小M
		<p>发表于 2016-06-30 15:30</p>
	</div>
</div>```