# Requests

>Author: Sylvie233
>
>Date: 23/1/31

[TOC]

## 基础介绍

### xpath

```
// : 任意子节点
/ : 子节点
./: 当前接地
../: 父节点
following-sibling:: : 兄弟节点
	[xxx]: 子标签
    [@xxx]: 属性
	[1]: 第一个子节点
	[last()]: 最后一个子节点
	[position()]: 指定位置
	contains(): 包含判断
	text(): 文本内容
```







## API

### bs4

```
bs4:
	BeautifulSoup:
		a:
			attrs:
			has_attr():
		p:
			children:
		title:
			text:
		find():
		find_all():
		get_text():
		prettify():
		select():
	element:
		Tag:
```



### lxml

```
lxml:
	etree:
		HTML:
			xpath():
```



### requests

```
requests:
	Session:
		get():
	get():
		():
			auth:
			cookies:
			headers:
			params:
			proxies:
			timeout:
		reason:
		status_code:
		text:
		iter_content():
		json():
		raise_for_status():
	post():
		():
			data:
```





























