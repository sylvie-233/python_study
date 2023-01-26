# Python基础

>Author: Sylvie233
>
>Date: 2022/11/30

[TOC]

## 基础介绍

### python

```
python:
	
```





## 常用工具

### Anaconda

一个Python的包管理工具，内置多个包

可代替pip工作

```
conda:
	--version:
	-V:
	
	activate: 激活虚拟环境（默认base）
	clean: 清除包缓存
	config:
	create: 创建虚拟环境
		--clone: 复制旧环境
		--name/-n: 指定环境名称
		python: 指定python解释器版本（包对应版本）
	deactivate: 退出虚拟环境
	env:
		list: 列出所有环境
		export: 导出当前的包信息
		create: 创建环境
			-f: 指定包信息文件
	info:
		--env/-e: 查看虚拟环境
	init:
	install:
		-i: 指定下载源
	list: 列出当前环境下安装的包
		--name: 
	package:
	remove: 移除指定环境
		--name: 指定名称
		--all: 删除环境下所有包
	uninstall: 同remove
	run:
	search:
	update: 更新包
	upgrade: 更新
		--all: 更新所有工具包
		
	
activate: 激活指定环境
deactivate: 取消激活指定环境
```



Anaconda Prompt

DOS窗口



Anaconda Navigator

GUI窗口



环境默认安装包：

```
package:
	certifi:
	pip:
	python:
	setuptools:
	vc:
	vs2015_runtime:
	wheel:
	wincertstore:
```





### jupyter notebook

```
jupyter:
	
```







## 核心内容

### 字符串

### 类和对象

魔术方法：

```
魔术方法：
	__bool__(self):
	__bytes__(self):
	__call__():
	__contains__(self, item):
	__del__():
	__delattr__(self, name):
	__delete__(self, instance):
	__delitem__(self, key):
	__dir__(self):
	__enter__(self):
	__exit__(self, exc_type, exc_value, traceback):
	__format__(self, format_spec):
	__get__(self, instance, owner):
	__getattr__(self, name):
	__getattribute__(self, name):
	__getitem__(self, key):
	__hash__(self):
	__init__():
	__iter__(self);
	__len__(self):
	__new__():
	__repr__():
	__reversed__(self):
	__set__(self, instance, value):
	__setattr__(self, name, value):
	__setitem__(self, key, value):
	__str__():
```









## 常用API

### argparse

```

```



### array

```

```



### asyncio

```

```



### base64

```

```



### builtins（内置函数）

```
builtins:
	abs():
	any():
	ascii():
	bin():
	bool():
	bytearray():
	bytes():
	chr():
	classmethod():
	delattr():
	dict():
	dir():
	eval():
	exec():
	filter():
	float():
	format():
	getattr():
	globals():
	hasattr():
	hash():
	hex():
	id():
	input():
	int():
	isinstance():
	issubclass():
	iter():
	len():
	list():
	locals():
	map():
	max():
	min():
	next():
	object():
	open():
	print():
	property():
	range():
	repr():
	reversed():
	round():
```



### csv

```

```



### datetime

```

```



### errno

```

```



### gc

```

```



### http

```

```



### io

```

```





### json

```

```



### logging

```

```





### math

```

```



### numbers

```

```



### os

```
os:
	
```



#### path

```
os.path:
	
```







### pickle

```

```



### queue

```

```



### random

```

```



### re

```

```



### socket

```
socket:
	socket():
		accept():
		bind():
		close():
		connect():
		listen():
		recv():
		send():
		




```



### sqlite3

```

```



### sys

```
sys:
	argv:
	exit():
```



### tempfile

```

```



### test

```

```



### threading

```

```



### time

```

```



### typing



### unittest

```
unittest:
	TestCase:
		assertEqual():
		setUp():
		setUpClass():
		tearDown():
		tearDownClass():
	TestLoader():
        discover():
		loadTestsFromTestCase():
	TestSuite:
		addTest():
		addTests():
	TextTestRunner:
		run():
	defaultTestLoader():
	main():
```





### urllib

```

```



### uuid

```

```



### venv

```

```





### xml

```

```



### zlib

```

```















