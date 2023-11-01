# Tornado基础

> Author: Sylvie233
> Date: 23/10.30
> Point: Python Web（Tornado）项目——微博APP开发的设计与实现_Python Web项目：P16


## 基础介绍

python的web框架




## 核心内容

```
tornado:
	ioloop:
		IOLoop:
			current():
				run_sync():
				start():
	web:
		Application:
			handlers:
				[("/xxx", xxx)]
			settings:
				debug:
				static_path:
				static_url_prefix:
			---
			listen():
		RequestHandler:
			get():
			post():
			set_cookie():
			set_default_headers():
			---
			application:
			request:
				arguments:
				body:
				body_arguments:
				cookies:
				files:
				headers:
				host:
				host_name:
			finish():
			get_body_argument():
			set_header():

wtforms:
	fields:
		core:
			StringField:
				validators:
		simple:
			HiddenField:
	validators:
		DataRequired:
			message:
		Length:
			max:
			min:
		
wtforms_tornado:
	Form: 输入数据模型
		---
		errors:
		validate(): 参数校验

peewee:
	Model: 数据库实体模型
		Meta:
			database:
			table_name:
		CharField:
			max_length:
			null:
			primary_key:
			verbose_name:
		DataTimeField:
			default:
			---
			desc():
		IntegerField:
			verbose_name:
		---
		create_table():
		---
		select():
			order_by():
		update():
			where():

peewee_async:
	Manager:
		--- 
		create():
		execute():
		get():
	MySQLDatabase:
		database:
		host:
		port:
		user:
		password:
		---
		
```



### 应用

#### 配置




### 控制器

```

```

#### 参数校验



#### 返回值约定


#### 会话

##### Token

JWT实现





#### 拦截器

装饰器实现



#### 文件上传








### 持久层

#### Model
##### DTO

##### Entity






#### ORM
peewee数据库连接工具，ORM


##### MySQL

数据库表设计





##### 联表查询
 




#### Redis

状态记录



### 模板引擎




### 工具类

#### 邮件发送

zmail包，发送邮件

#### 验证码



#### 短信发送









