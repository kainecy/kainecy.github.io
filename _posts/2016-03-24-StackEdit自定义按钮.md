---
layout: post
title: StackEdit自定义按钮
---

###1. 添加按钮UI
bodyEditor.html 中

```
<ul class="nav left-buttons">
	<li class="wmd-button-group4 btn-group">
		<a class="btn btn-success button-open-award" title="插入精品题"><i class="icon-award"></i></a>
	</li>
</ul>
```

###2. 给按钮添加颜色
base.less中

```
.icon-award {
	color: #ee1d24 !important;
}
```

###3. 给按钮添加点击事件





