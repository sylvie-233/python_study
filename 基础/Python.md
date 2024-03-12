# Python基础

>Author: Sylvie233
>
>Date: 2022/11/30
>
>Point:

## 基础介绍

### python

```
python:
	-m: 执行模块内命令
	--version:
```



### pip

```
pip:
	config:
	freeze:
	install:
		-i: 指定镜像源
		-r:
		--upgrade:
	list:	
```



### virtualenv

```
virtualenv:
	--help:
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

预定义变量

```
预定义变量：
	__name__:
```



### 数据类型

```
TypeHint:
	Any:
	Callable:
		Callable[[argType], returnType]:
	dict:
		dict[xxx, xxx];
		get():
		values():
	int:
	list:
	List:
		list[xxx]:
		append():
		index():
		remove():
	Literal:
	NewType:
	None;
	NoReturn:
	Optional:
		Optional[xxx]:
	Sequence:
	str:
		format():
	tuple:
		tuple[xxx]:
		
	Union:
		Union[xxx, xxx];
		|:
	“xxx”:
```



`mypy`类型检查

`typing`内置类型库







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
```
python:
	argparse:
	asyncio:
		Event:
			set():
			wait():
		create_task():
		gather():
		get_event_loop():
		run():
		sleep():
	builtin:
		dir():
		enumerate():
		eval():
		input():
		int():
		len():
		list():
		print():
		repr(): 类似__str__
		reversed():
		set():
		sorted():
		str():
		sum():
		vars(): 对象转字典
	calendar:
		Calendar:
			firstweekday
		HtmlCalendar:
		TextCalendar:
		calendar():
		isleap():
		month():
	cgi:
	cgitb:
	collections:
		defaultdict:
		Count: dict（value为key的个数）
	concurrent:
		fetures:
			ThreadPoolExecutor: 
				submit():
	
	datetime:
		date:
			strftime(): 格式化日期字符串
		datetime:
			fromtimestamp():
		date():
		time():
	difflib:
		get_close_matches():
	functools:
		filter():
		lru_cache(): 缓存函数
		reduce():
		sorted():
	http:
		server:
			HTTPServer:
				
	importlib:
		import_module(): 动态导入模块（返回模块对象）
	io:
		TextIOWrapper:
			buffer():
			close():
			closed():
			readline():
			readlines():
			seek():
			write():
			writelines():
	json:
		loads():
	logging:
	math:
	multiprocessing:
		Pool:
			map():
		Process:
			
	os:
		environ: 环境变量
		implementation:
			name:
		path:
			abspath():
			basename():
			dirname():
			exists():
			getatime():
			getmtime():
			getsize():
			isdir():
			isfile():
			join():
			realpath():
		stat_result:
			st_atime:
			st_ctime:
			st_dev:
			st_mode:
			st_mtime:
			st_size:
		version_info: 版本信息
		remove():
		rename():
	pathlib:
		Path:
	pickle:
		Pickler:
		dump():
		dumps():
		load():
		loads():
	pkgutil:
		
	re:
		Match:
			group():
			groups():
		Pattern:
			findall():
			fullmatch():
			match():
				pos: 指定开始位置
			search():
			split(): 匹配拆分字符串
			sub(): 匹配替换
		compile(): 
			pattern:
			flags:
		findall():
	shutil:
		copy():
		copyfile():
	socket:
		error:
		socket:
			accept():
			bind():
			close():
			connect():
			fineno():
			listen():
			recv():
			recvfrom():
			send():
			sendto():
			setblocking():
			setsockopt():
	socketserver:
		BaseServer:
			serve_forever():
		TCPServer:
			server_address:
			socket:
			close_request():
			fileno():
			get_request():
			server_activate():
			server_bind():
			server_close():
	sqlite3:
		Connection:
			close():
			commit():
		Cursor:
			rowcount:
			close():
			execute():
			executemany():
			fetchall():
			fetchone():
		Error:
		connect():
	subprocess:
		run(): 运行子进程
	sys:
		argv:
		implementation:
		meta_path:
		modules: 已经存在的模块
		orig_argv:
		path:
		stderr:
		stdin:
		stdout:
			write():
		thread_info:
		version_info:
		addaudithook():
		exc_info():
		getsizeof():
	threading:
		Event：
			set():
		Lock:
			acquire():
			release():
		RLock: 可重入锁
		Thread:
			start(): 启动线程
		current_thread():
	time:
		struct_time:
			tm_year:
			tm_mon:
			tm_mday:
		ctime():
		localtime():
		sleep():
		strftime(): 格式化字符串时间
		strptime(): 格式化结构体时间
		time():
	tkinter:
	typing:
		bool:
		bytes:
			decode():
		callable:
		float:
		int:
		range:
		str:
			encode():
			format():
		Any:
		Dict:
			items()
		Exception:
			
		List:
			count():
			sort():
		Optional:
		Sequence:
		Tuple:
		Type:
		TypeVar: 类型不确定
		Union:
	urllib:
		error:
			
		parse:
			quote():
			urlencode():
		rebotparser:
			
		request:
			urlopen():
			urlretrieve():
		response:
			getcode():
			getheaders():
			geturl():
			read():
			readline():
			readlines():
		Request:
			data:
			headers:
			url:
	warnings:
		warn():
	wsgiref: wsgi服务的简单实现
		simple_server:
			WSGIServer:
				application:
				get_app():
				serve_forever():
				server_bind():
				set_app():
				setup_environ():
			make_server():
			
			
```


### argparse

```

```



### array

```
array:
	append():
	remove():
```



### asyncio

```
asyncio:
	@coroutine:
	create_task():
	ensure_future():
	get_event_loop():
		run_in_executor():
        run_until_complete():
    get_running_loop():
    	create_future():
    		set_result():
    run(): 事件循环执行协程对象
    set_event_loop_policy():
	sleep():
	wait():
```



### base64

```
base64:
	b64encode():
		decode():
	standard_b64encode():
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
		mode:
		encoding:
		
	print():
	property():
	range():
	repr():
	reversed():
	round():
```



### collections

```
collections:
	OrderedDict:
```





### concurrent

#### futures

```
concurrent.futures:
	Future:
	process:
		ProcessPoolExecutor:
	thread:
        ThreadPoolExecutor:
            ():
                max:
            shutdown():
            submit():
```





### csv

```

```



### ctypes

```
ctypes:
	cdll:
		LoadLibrary:
```





### datetime

```
datetime:
	now():
```



### errno

```

```



### gc

```

```



### hashlib

```
hashlib:
	new():
		hexdigest():
	sha1():
		digest():
```



### http

```

```



### io

```
io:
	BytesIO:
        ---
        getvalue():
```





### json

```
json:
	dumps():
```



### logging

```
logging:
	INFO:
	FileHandler:
		---
		addFilter():
		setFormatter():
	Filter:
	Formatter():
	Logger:
		---
		addFilter():
		addHandler():
		critical():
		debug():
		error():
		info():
		setLevel():
		warning():
	getLogger():
```



Loggers



Handlers



Filters



Formatters

```
:
	%(levelno)s:
	%(levelname)s:
	%(pathname)s:
	%(filename)s:
	%(funcName)s:
	%(lineno)s:
	%(asctime)s:
	%(thread)s:
	%(threadname)s:
	%(process)s:
	%(message)s:
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
	environ: 环境变量
	mkdir():
```



#### path

```
os.path:
	dirname():
	exists():
	join():
```







### pickle

```
pickle:
	loads():
```



### queue

```
queue:
	Empty:
	Queue:
		get():
		get_nowait():
		join():
		put():
		qsize():
		task_down():
```



### random

```
random:
	choices():
	randint():
```



### re

```
re:
	findall():
```



### select

```
select:
	EPOLLHUP:
	EPOLLIN:
	EPOLLOUT:
	epoll():
		modify():
		poll():
		registre():
		unregister():
	select():
```



### signal

```
signal:
	signal():
```



### socket

```
socket:
	AF_INET:
	SOCK_STREAM:
	create_connection():
	socket():
		accept():
		bind():
		close():
		connect():
		fileno():
		listen():
		recv():
		send():
		setblocking():
		setsockopt(): 设置属性




```



### sqlite3

```

```



### string

```
string:
	encode():
	endswith():
	format():
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
threading:
	Lock:
		acquire():
		release():
	Thread:
		():
            target:
            args:
        setDaemon():
        start():
```



### time

```
time:
	sleep():
	strftime():
	time():
```



### tkinter

```
tkinter:
	Button:
		command:
		show:
		---
	Entry:
		textvariable:
		---
	Frame:
		---
		destroy():
		focus_force():
		forget():
		grid():
		pack():
	Label:
		text:
		width:
		---
		grid():
			row:
			column:
	Menu:
		---
		add_command():
			label
	StringVar:
		---
		get():
		set():
	Tk:
		---
		geometry():
		mainloop():
		quit():
		title():
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
urllib:
	parse:
		urlencode():
		urlparse():
			fragment:
			netloc:
			path:
			query:
			geturl():
	request:
		HTTPBasicAuthHandler:
			add_password():
		ProxyBasicAuthHandler:
		ProxyHandler:
		Request:
			add_header():
		build_opener():
			open():
		install_opener():
		urlopen():
			headers:
				get_all():
				keys():
			reason:
			status:
			read():
```



### uuid

```
uuid:
	uuid4():
		hex
```



### venv

```

```





### xml

```

```



### xmlrpc

```
xmlrpc:
	client:
		ServerProxy:
			
	server:
		SimpleXMLRPCServer:
			register_function():
			register_instance():
			serve_forever():
```



### zlib

```

```















