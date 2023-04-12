# Flask基础

> Author: Sylvie233
>
> Date: 23/1/29
>
> Point: P76

[TOC]

## 基础介绍

Flask

jinja2模板引擎、Werkzeug WSGI工具集、









### flask-blueprint

路由分组



### flask-bootstarp

集成jinja2模板

```
{% extends "bootstrap/base.html" %}
	block插槽:
		html_attribs:
		html:
			head:
                title:
                metas:
                styles:
			

```



### flask-caching



### flask-debugtoolbar



### flask-mail



### flask-migrate



### flask-restful

```
from flask_restful import Api, Resource


```





### flask-script

#### manage.py

```
manage.py:
	db: 集成migrate插件
		downgrade:
		init:
		migrate:
		upgrate:
	runserver:
		-d:
		-h:
		-p:
		-R:
		-r:
		--threaded:
    shell:
```



### flask-session

session持久化到redis中

默认31天



### flask-sqlalchemy

ORM框架







### uwsgi.ini

```ini
[uwsgi]
master = true
processes = 1
threads = 2

# 虚拟环境目录
home = /xxx
# 指定项目目录
chdir = /www/wwwroot/xxx
wsgi-file = %(chdir)/app.py
callable = app
# http = x.x.x.x:x
socket = x.x.x.x:x


logto = /xxx
chmod-socket = 660
vacuum = true
max-request = 1000

# uwsgi的运行状态
stats = %(chdir)/uwsti.status
pidfile = %(chdir)/uwsgi.pid
```



### gunicorn

```
gunicorn:
	-b: 监听地址
	-c: .py配置文件
	-D: 后台运行
	-h:
	-v:
	-w: 进程数
	--access-logfile:
	--error-logfile:
	xxx: 文件
		xxx: 对象
	
```









## 核心内容

### 配置

```
config:
	DEBUG:
	MAIL_DEFAULT_SENDER:
	MAIL_PASSWORD:
	MAIL_PORT:
	MAIL_SERVER:
	MAIL_USERNAME:
	SECRET_KEY: 密钥
	SESSION_KEY_PREFIX:
	SESSIOIN_REDIS:
	SESSION_TYPE: redis|memcached|sqlclchemy|
	SESSION_USE_SIGNER: True
	SQLALCHEMY_DATABASE_URI:
	SQLALCHEMY_POOL_SIZE: 连接池
	TESTING:
```





### 路由

converter







### 模板

jinja2

```
{ var }

{% block xxx %}
	{{ super() }}
{% endblock %}

{% extends "xxx" %}

{% for it in list %}
	{
		loop:
			first:
			index:
			index0:
			last:
			revindex:
	}
{% else %}
{% endfor %}

{% from "xxx" import 宏 %}

{% if xxx %}
{% endif %}

{% include "xxx" %}

{% marco func(arg) %}
{% endmarco %}

过滤器:
	capitalize:
	default:
	first:
	format:
	last:
	length:
	lower:
	reverse:
	safe:
	sort:
    striptags:
	sum:
	title:
	trim:
	upper:
```





### 模型



### hook函数

中间件实现、装饰器





### Restful













## API

### flask

```
flask:
	Blueprint:
		name:
		template_folder:
		url_prefix:
		@after_app_request():
		@before_request():
		@errorhandler():
		@route():
			methods: []
	Flask:
        config:
        	from_object():
        		SESSION_TYPE: "redis"|
        static_folder:
        @after_request():
        @before_request():
        @errorhandler():
		@route():
		@teardown_request():
		register_blueprint():
		run():
			debug: 调试模式
			host:
			port:
	current_app:
	g:
	request:
		args:
		cookies:
		data:
		files:
		form:
		headers:
		host:
		method:
		remote_addr:
		url:
	session:
	sessions:
		SecureCookieSession: 序列化后存储在浏览器中
	abort():
	flash():
	make_response():
	redirect():
	render_template():
	url_for():
	wrappers:
		Response:
			headers:
			delete_cookie():
			set_cookie():
			
```



### flask_bootstrap

```
flask_bootstrap:
	Bootstrap:
```



### flask_caching

```
flask_caching:
	Cache:
		config:
			CACHE_TYPE: simple|redis|filesystem|
		@cached():
			timeout:
		get():
		init_app():
		set():
```



### flask_debugtoolbar

```
flask_debugtoolbar:
	DebugToolbarExtension:
```



### flask_mail

```
flask_mail:
	 Mail:
         init_app():
         send():
     Message:
     	body:
     	html:
     	recipients:
     	subject:
```



### flask_migrate

```
flask_migrate:
	Migrate:
		init_app():
	MigrateCommand:
```



### flask_restful

```
flask_restful:
	Api:
		():
			prefix:
		add_resource():
			endpoint:
		init_app():
	Resource:
		delete():
		get():
		patch():
		post():
		put():
	fields: 序列化字段定义
		DateTime:
		Float:
		Integer:
		List: 
		Nested: 级联字段
		Raw: 自定义字段类型
			format():
			output():
		String:
			attribute:
			default:
		Url:
			absolute:
	reqparse: 请求参数校验
		RequestParser:
			add_argument():
				action:
					append:
				dest:
				help:
				location:
					args:
					cookies:
					form:
				required:
				type:
			copy(): 继承
			parse_args():
				strict:
            remove_argument():
    @marshal_with(): 对象字段序列化
    	envelope:
    abort():
    	http_status_code:
    marshal(): 手动序列化
```



### flask_script

```
flask_script:
	Manager:
		app:
		add_command():
		run():
```



### flask_session

```
flask_session:
	Session:
		init_app():
```



### flask_sqlalchemy

```
flask_sqlalchemy:
	SQLAlchemy:
		Boolean:
		Column:
			autoincrement:
			default:
			nullable:
			primary_key:
			unique:
		DateTime:
		ForeignKey: 外键设置Column
		Integer:
		Model:
			__abstract__: 抽象模型（供继承用）
			__tablename__: 表名
			query:
				all():
				filter():
					BaseQuery:
				filter_by(): 直接写字段名
				first():
				get():
				get_or_404():
				limit():
				offset():
				order_by():
					-xxx:
				paginate():
					page:
					items():
					iter_pages():
			xxx: 自定义属性Column（用于定义查询条件：魔术方法）
				__eq__():
				__lt__():
				contains():
				---sqlalchemy中的逻辑运算
				and_():
				not_():
				or_():
		String:
		Table: 定义表
		session:
			add():
			add_all():
			delete():
			commit():
		backref():
			lazy:
		create_all(): 创建数据库 
		drop_all(): 删除数据库
		init_app():
		relationship(): 定义一对多关联字段
			backref: 给外键表定义的反向引用自身的字段
			lazy: 懒加载
			secondary: 多对多关联时使用的中间表模型
```



### werkzeug

```
werkzeug:
	exceptions:
	security:
		check_password_hash():
		generate_password_hash():
```















